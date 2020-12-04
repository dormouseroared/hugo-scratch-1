---
title: "Shortcode Github"
date: 2020-12-04T21:55:56Z
tags: [shortcode, github]
draft: false
rating: 1
---
The shortcode used in this [blog](https://blog.jeremylikness.com/blog/create-article-preview-in-hugo/) about Hugo uses font awesome to provide the github icon. 

Let's see if we can use a feather icon for `github`. For the moment, we'll add it after the fontawesome icon, so we could get both!

The second parameter is a comment that is added to the end of the link.

Shortcodes can be used to insert HTML etc into the content.

{{<github "feathericons/feather#feather" "for the icons such as github">}}

{{<github "JeremyLikness/DurableDungeon">}}

<figcaption>what happens with figcaption</figcaption>