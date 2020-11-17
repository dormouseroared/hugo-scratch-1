---
title:  "0731 | Hugo front matter"
date:  "2020-11-11T09:14:00"
author:  "nigel"
authorTwitter:  "fred" #do not include @
cover:  "screenshot-hugo-theme-terminal.png"
tags:  ["hugo", "front matter", "shortcode"]
description:  "second.md repurposed to provide a place to document hugo front matter as a result of re-reading the terminal theme documentation and wondering how to update the theme and what has changed."
showFullContent:  false
testparam:  "a non-standard parameter added to the front matter referenced below as a shortcode"
---
[Hugo Terminal Theme](https://themes.gohugo.io/hugo-theme-terminal/)

```
terminal

A simple, retro theme for Hugo.

    Author: panr
    Minimum Hugo Version: 0.74
    Updated: 2020-11-01
    License: MIT
    Tags: blog clean customizable dark highlighting minimal monotone multilingual personal responsive simple technical retro
```
---
# title
# date
Either yyyy-mm-dd or yy-mm-ddThh-mm-ss can be used. Others may be available. A trailing Z causes the page not to be generated. 

**Any error in date will mean the page is not generated with no warning at all.** 

At the moment, posts are displayed in reverse date time order, so these might have to be invented until, say, **title** can be used.

## an article about the date time format and why it is used

[Hugo date time format](https://www.jvt.me/posts/2019/03/24/datetime-hugo/)

[Hugo doc on date](https://gohugohq.com/howto/hugo-dateformat/)

# author
# authorTwitter
No sign of this in the post
# cover
names of pictures in the static folder can be used here
# tags
displayed and active links can be clicked
# keywords
Keywords are not appearing anywhere.
# description
# showFullContent
# draft
No draft parameter in the default front matter. It may be available but need to re-read the terminal theme documentation.
# shortcode testparam

[hugo shortcodes are available in addition to those from the terminal theme](https://gohugo.io/content-management/shortcodes/#param)

## Here is the testparam parameter for this document's front matter

{{< param testparam >}}

## Documentation from the hugo shortcode page

```
param

Gets a value from the current Page's params set in front matter, with a fall back to the site param value. 

**It will log an ERROR if the param with the given key could not be found in either.**

{{< param testparam >}}

Since testparam is a param defined in front matter of this page with the value Hugo Rocks!, the above will print:

Hugo Rocks!

To access *deeply nested params*, use “dot syntax”, e.g:

\{\{< param "my.nested.param" >\}\}

```

# how and where are hugo errors logged?

# Hugo support forum

[Hugo Support Forum](https://discourse.gohugo.io/)
