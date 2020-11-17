---
title: "Shortcode: codecaption"
date: 2020-11-15T22:21:37Z
tags: ["shortcode", "code"]
draft: false
---
## Source
[Github repository: Hugo Shortcodes](https://github.com/parsiya/Hugo-Shortcodes)

Searched for hugo shortcodes and found this Github repo. Copied the HTML without the comments into layouts/shortcodes/codecaption.html and then just wrap the code to be displayed in a code box as per the example.

* There are other shortcodes to copy over.

```
add the double curly brackets

< codecaption lang="html" title="Code caption shortcode" >
    code to be displayed in the box
< /codecaption >
```
## Purpose
Adds title to code blocks.
## Example of how to use this shortcode
{{< codecaption lang="html" title="Code caption shortcode" >}}
<figure class="code">
  <figcaption>
    <span>{{ .Get "title" }}</span>
  </figcaption>
  <div class="codewrapper">
    {{ highlight .Inner (.Get "lang") "linenos=true" }}
  </div>
</figure>
{{< /codecaption >}}

## Image of shortcode result

![example](/codecaption1.jpg)