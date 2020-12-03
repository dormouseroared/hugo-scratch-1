---
title: "Simple Shortcode To add raw html"
date: 2020-11-24T16:10:17Z
tags: ["shortcode", "raw html", "feather icons", "rating"]
rating: 4
draft: false
---
[Simple Shortcode To add raw html](https://anaulin.org/blog/hugo-raw-html-shortcode/)

{{< rawhtml >}}
  <p class="speshal-fancy-custom">
    This is <strong>raw HTML</strong>, inside Markdown.
  </p>
  <p>And here is a feather icon!!! <i data-feather="home"></i></p>
  <p>And the Rating, which could be set up as separate hard coded short codes, so star-1, star-2, etc. There must be a way to input the number of stars as a variable.</p>
  <p>
  <i style="fill: red;" data-feather="star"></i>
  <i style="fill: red;" data-feather="star"></i>
  <i style="fill: red;" data-feather="star"></i>
  <i style="fill: red;" data-feather="star"></i>
  <i style="fill: none;" data-feather="star"></i>
  </p>
{{< /rawhtml >}}

## Other links to follow up

* [Structured book data in Hugo posts](https://anaulin.org/blog/structured-book-data-in-hugo-posts/)
* [Adding web mentions](https://anaulin.org/blog/adding-webmentions/)
* [Adding syndication URLs](https://anaulin.org/blog/adding-syndication-urls/)