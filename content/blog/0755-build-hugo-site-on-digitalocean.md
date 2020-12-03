---
title: "0755 Build Themeless Hugo Site"
date: 2020-12-01T20:13:09Z
tags: [hugo, themeless]
draft: false
rating: 4
---
{{< star4 >}}
> This is another Hugo site built from scratch without a theme, using a different setup approach. The intent is to summarise, then carry out the instructions and refine these notes.
* [DigitalOcean &bull; Hugo &bull; new site](https://www.digitalocean.com/community/tutorials/how-to-build-and-deploy-a-hugo-site-to-digitalocean-app-platform)

> In this tutorial, you’ll use Hugo to build a small static website and deploy the site to DigitalOcean’s App Platform by using GitHub. Then you’ll make changes to your site and see those changes deployed automatically.
## Hugo Versions
Hugo comes in two versions: the regular version and the extended version. Download the extended version so you have support for asset management and support for CSS preprocessing.

## Hugo setup on Windows

On Windows, create the directory C:\Hugo, unzip the file you’ve downloaded, and place it in C:\hugo. Then add that folder to your PATH environment variable. To do this, use Windows Search and type “environment”. Select Edit Environment Variables for My Account. On the screen that appears, press the Environment Variables button, locate PATH in the System Variables section, and press the Edit button. Add c:\hugo\bin in the text area and press OK to save the settings. Press OK on the rest of the dialogs to close them.
## Hugo folders
* `archetypes` are your content templates. You can use the hugo command to create new Markdown pages, and it’ll use the files in the archetypes directory as the template for those pages.
* `config.toml` is the configuration file for the site, where you specify the site’s domain, title, and the theme you want to use.
* `content` is the directory that holds your site’s content.
* `data` is where you can store JSON files you can use when generating your site.
* `layouts` is where you place the HTML files that define your site’s look and feel, or override the templates from a theme.
* `resources` is where Hugo places files it generates, like optimized images.
* `static` holds static assets, like files, stylesheets, scripts, or other assets that you don’t need Hugo to manage for you.
* `themes` contains themes you create or download.
## Templates
The site will have a home page and a section called “Sharks”. 

To display the content, Hugo needs:

* A template for the `home page`.
* A template that shows a `list of pages`, such as a page that lists all the sharks, or all of the tags or categories on the site.
* A template for a `page of content`, like a page about a single shark.
## Home page
Create the file layouts/index.html

* The {{ .Site.Title }} lines grab the title from the config.toml file. 
* The {{ .Title }} line and {{ .Content }} line grab the title and content from the document associated with the home page, which you’ll create next.

```html
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title><^>{{ .Site.Title }}</title>
    <link rel="stylesheet" href="/style.css">
  </head>
  <body>

    <header>
      <h1>{{ .Site.Title }}</h1>
    </header>

    <main>
      <h2>{{ .Title }}</h2>
      {{ .Content }}
    </main>

    <footer>
      <small>Made with love and Hugo</small>
    </footer>
  </body>
</html>
```
## archetype
By default, Hugo creates all new pages in draft mode. Open the file archetypes/default.md in your editor and modify it so that draft is false. This way all new pages you create won’t be in draft mode.
```
---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: false
---
```
## home page
Now use Hugo to generate a content file for your home page. 

From the terminal, in the directory of your project, type this command:

`hugo new _index.md`

This generates the file content/index.md:

`/Users/your_username/sharkopedia/content/_index.md created`

The underscore in the filename tells Hugo that this is the content page for either a listing page or the home page, as opposed to a regular piece of content.

Open the content/_index.md file in your editor and add some text and change the title:
```
---
title: "Welcome"
date: 2020-10-07T14:07:35-05:00
draft: false
---
This is a site all about sharks! Select a shark from the list to learn more:
```
## single template
Next you’ll need a template for single pieces of content, and for this project, you can duplicate the home page, although you’ll have to place it in a specific directory.

Create the directory layouts/_default:

`mkdir layouts/_default`

Then create the file layouts/_default/single.html and copy the contents of your layouts/index.html file into the new file. You can do this from the command line with this command:

`cp layouts/index.html layouts/_default/single.html`

## content
Next, you’ll create a sharks content section of the site. To do so, you’ll use the hugo command to create new Markdown files in the content directory under a sharks subdirectory. Execute this command to create a content page for Hammerhead sharks:

`hugo new sharks/hammerhead.md`

Note that you don’t specify the content directory when using the hugo new command.
## default list template
Create the file layouts/_default/list.html and open it in your editor. Inside the file, place the same content as your other templates:
```html
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title><^>{{ .Site.Title }}</title>
    <link rel="stylesheet" href="/style.css">
  </head>
  <body>

    <header>
      <h1>{{ .Site.Title }}</h1>
    </header>

    <main>
      <h2>{{ .Title }}</h2>
      {{ .Content }}
    </main>

    <footer>
      <small>Made with love and Hugo</small>
    </footer>
  </body>
</html>
```
Inside the <main> tag, after the title and content, place the following code which generates a bulleted list of pages to display:
```html
<main>
  <h2>{{ .Title }}</h2>
  {{ .Content }}

  <ul>
  {{ range .Pages }}
    <li><a href="{{ .RelPermalink }}">{{ .Title }}</a></li>
  {{ end }}
  </ul>
</main>
```
The range function iterates over all of the pages for the section of the site. The actual value of .Pages is determined when Hugo generates your site. This list template you created will be used as the default template for any lists, including tag pages, category pages, and your “sharks” section. 

You can make more specific templates for your sections, but this gives you a default layout that works everywhere.
## add more content
Finally, create some more pages so there’s more content to display:

`hugo new sharks/mako.md`

`hugo new sharks/whale.md`

## add the list of sharks to the home page

Open the file layouts/index.html in your editor and add the following code to iterate over all the pages of your site that are sharks and display them:

```html
    <main>
      <h2>{{ .Title }}</h2>
      {{ .Content }}

      <ul>
      {{ range (where site.RegularPages "Type" "in" "sharks") }}
        <li><a href="{{ .RelPermalink }}">{{ .Title }}</a></li>
      {{ end }}
      </ul>
    </main>
```
This version uses (where site.RegularPages "Type" "in" "sharks") to find only the content pages for sharks. 

Unlike your default list template, your home page needs more direction about what kind of content to display.