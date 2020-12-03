---
title: "0756 Another Hugo Site From Scratch"
date: 2020-12-03T14:44:33Z
tags: [hugo, themeless, "leaf bundle", "branch bundle", "page bundle"]
draft: false
rating: 4
---
{{< star4 >}}
Looking for tutorials on building hugo sites from scratch, and in particular anything that helps to understand the vagaries of leaf bundle, branch bundle and page bundle.

This youtube video is actually about [setting up a theme](https://www.youtube.com/watch?v=wcMqrb3v2SM) but the idea is to have a working hugo site with some leaf and branch bundles as a working system to examine. The github [here](https://github.com/ericmurphyxyz/hugo-starter-theme) contains a starting point from which a site **HUGO-BUNDLE-1** without a theme has been constructed.

> One benefit of using a page bundle instead of a normal page is that you can put files associated with the post (such as images) in the same folder as the post itself instead of in the STATIC folder.

## Leaf bundle

* a collection of content for single pages
* would like to extend this site to include images from the static folder and also from the folder with the leaf bundle
* the key file is **index.md**

## Branch bundle
* for list pages e.g. section, home, taxonomy
* the key file is **_index.md**

## Things to do
* Look for a lightweight theme with good use of bundles etc to have a closer look at by deconstructing.
* Not sure how the 404.html found in this activity is actually used