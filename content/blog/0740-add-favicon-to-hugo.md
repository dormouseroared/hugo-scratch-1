---
title: "0740 Add Favicon to Hugo"
date: 2020-11-22T18:27:54Z
tags: [favicon]
draft: false
---
## sample heading
[Add favicon to Hugo based website](https://www.kiroule.com/article/add-favicon-to-hugo-based-website/)

* Favicon is a 16 x 16 pixel image.
* It goes in the static folder.
* [favicon.io](https://favicon.io) was used to make a DM logo from text.
* This didn't work for ages but the answer seemed to be to make an absolute reference as per hugo-scratch-1

```
    {{/* The favicon works as a relative link for the index.html at root    */}}
    {{/*  but not for any other link on the menu or any content at a lower level  */}}
    {{/*  that's why the absURL is used  */}}
    {{/*  <link rel="shortcut icon" href="favicon.ico" type="image/x-icon">  */}}

    {{ $fav := "favicon.ico" | absURL }}
    <link rel="shortcut icon" href="{{ $fav }}" type="image/x-icon">


```
* There is more to do with other parts of the html for favicons for all the other possibilities.