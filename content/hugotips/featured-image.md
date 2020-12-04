---
title: "Featured Image"
date: 2020-12-04T12:31:28Z
tags: ["featured image", summary, absURL, "Hugo Forum"]
draft: false
summary: "Work through an interesting item on the Hugo forum about Featured Image to see what can be understood and applied if possible. This is also the first use of summary in front matter to override the default of first n characters in the post, and should be seen in the single template at the bottom of the page. The template single.html has been left updated with the ability to display the featured_image. Not sure how this relates to page bundles yet, but it will be useful for existing posts. And, still confused about relative links for images."
featured_image: "img/test.png"
image: "/img/test.png"
description: "How to set up and use a featured image from the static folder at the top of the page."
rating: 5
---
{{< star5 >}}
Searching for anything about the use of image and images in front matter with lists of images in the bundle, and found this. It isn't relevant to the original search, but it is worth working through.

[Hugo forum &bull; FEATURED IMAGE](https://discourse.gohugo.io/t/post-featured-image/864)

> I would like to have a section on one page which displays post featured images (maybe specified in the front matter or the first image used in the post) together with a summary of that post. If this could be done to automatically pick up the most recent post in any given category, that would be marvellous. Can it be done?

## Initial understanding
* new section (folder) in content to find any posts in blog with a featured image
* OR, is it a chunk of code at the bottom of single
* OR, a part of the home page
* has this got anything to do with bundles? Think not.

> For anyone else who finds this and wants to know how I did it: in the .md file, you need to include this in the front matter:
```html
+++
featured_image = “images/pic01.jpg”
+++
```
Then at the point you want to include it in the page, you add into the template
```html
<a href="#" class="image featured">
    {{if isset .Params "featured_image" }}
        <img src="{{ index .Params "featured_image" }}"></a>
    {{ end }}
```
> In this case it’s a matter of taste (and space…), but I tend to use this construction for these conditionals (your code works fine, but “with” has less surprises in some cases, and it’s more compact):
```html
{{ with .Params.featured_image }}
    <img src="{{ . }}">
{{ end }}
```
## Testing
* Insert {{ .Params.featured_image }} into the single.html template. This results in the display of the placeholder text if the parameter is present in front matter, or nothing at all if it isn't.
* Add the 3 lines into the single.html template. Where the parameter is set, an attempt to display an image can be seen.
* Now to put an image address in the static folder into the placeholder text.
* Could not work out the relative address of the image, so added a pipe to absURL, and that will do for now.
* The featured image is now displayed on the single.html template page.
* This isn't quite what the original question seemed to ask for, but the result is very useful!
## Next steps
[Hugo Forum &bull; Featured images and bundles](https://discourse.gohugo.io/t/displaying-featured-images/10520)