---
title: "Relative Link"
date: 2020-12-04T17:31:28Z
tags: [draft, shortcode, "Jeremy Likness", "relative link"]
draft: false
rating: 3
---
{{< star3 >}}
[Create Article Preview in Hugo](https://blog.jeremylikness.com/blog/create-article-preview-in-hugo/)
## From Jeremy's article
> After building this functionality I realized I could create a short code to do a similar thing with relative page links. I created a short code named relativelink.html, in which the .Site.GetPage allows me to fetch a page based on its URL. I then extract the title, image, and description to create my preview. The thumbnail generation produces a slightly wider image and constrains the height as well.
## Front matter used
* *title* is the only standard item
* *image* is not a standard item
* *description* is not a standard item
```go
{{$page := .Site.GetPage (.Get 0)}}
<div class="container alert alert-secondary">
    <div><a href="{{$page.RelPermalink}}" alt="{{$page.Title}}">
        <strong>{{ $page.Title }}</strong>
    </a></div>
    <div class="float-left m-2">
    {{ if $page.Params.image }}
        {{ $original := print "images/" (path.Base $page.Params.image) }}
        {{ $originalImg := $page.Resources.GetMatch $original }}
        {{ if $originalImg }}
            {{ $thumbnailImg := $originalImg.Fit "200x100" }}
            {{ printf `<img src="%s" alt="%s">` 
                $thumbnailImg.RelPermalink $page.Title | safeHTML }}
        {{end}}
    {{end}}
    </div>
    <p><small>{{$page.Description}}</small></p>
    <div class="clearfix"></div>
</div>
```
## Using relativelink (the double curly brackets have been removed)
```go
<relativelink "/hugotips/help.md" >
```
{{< relativelink "/hugotips/help.md" >}}
```go
<relativelink "/hugotips/featured-image.md" >
```
{{< relativelink "/hugotips/featured-image.md" >}}
```go
<relativelink "/testbundle/page-resources" >
```
{{< relativelink "/testbundle/page-resources" >}}
```go
<relativelink "/blog/0720-hugo.md" >
```
{{< relativelink "/blog/0720-hugo.md" >}}

## The article's front matter
```html
---
title: "Create an Article Preview in Hugo"
author: "Jeremy Likness"
date: 2019-07-12T11:08:28-07:00
years: "2019"
lastmod: 2019-07-12T11:08:28-07:00

draft: false
comments: true
toc: false

series: "From Medium to Hugo"
subtitle: "Generate thumbnails on the fly and pull page metadata for a proper preview."

description: "Generate a thumbnail for your Hugo posts on the fly, then create a custom short code that uses thumbnails and page data like title and description to embed a post preview to interlink documents."

tags:
 - Hugo
 - Static website 
 - Go

image: "/blog/create-article-preview-in-hugo/images/durabledungeonpreview.jpg" 
images:
 - "/blog/create-article-preview-in-hugo/images/durabledungeonpreview.jpg" 
---
```