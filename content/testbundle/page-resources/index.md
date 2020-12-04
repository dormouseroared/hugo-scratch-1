---
title: "Page Resources"
date: 2020-12-03T19:00:00Z
tags: ["page resources", "Regis Philibert", "page bundle"]
description: "Images in the folder can be displayed as Page Resources"
image: "/hugo-scratch-1/testbundle/page-resources/derek-oyen-Pp-zoKs3pXQ-unsplash.jpg"
---
## At last, we can display an image from this page bundle!
* The routine to list out the relative links of any page bundle images has now been added to the single.html template using [this code](https://gohugo.io/content-management/image-processing/#the-image-page-resource) .
![](/hugo-scratch-1/testbundle/page-resources/derek-oyen-Pp-zoKs3pXQ-unsplash.jpg)
* [Regis Philibert &bull; Hugo Page Resources and how to use them](https://regisphilibert.com/blog/2018/01/hugo-page-resources-and-how-to-use-them/)
* to start with, front matter only contains manually added `title` and `date`
* some random images have now been placed in the first folder, and displayed using new Resources template code in single.html that should work for all pages
* also added testbundle to the menu, and it can be changed later
* image details
    * 3511x1975 0.7 MB
    * 4599x2587 1.9 MB
    * 3376x1899 0.6 MB
    * 4069x2289 1.3 MB
* `description` and `image` have been added to the front matter to enable the relativelink shortcode to be used, but at the moment the image is not being displayed.
> Is there a hugo new command to generate new content (including Front Matter) in Page Resource format, including an Archetype, or does everything have to be added manually?

## using the newly created imgptoc shortcode
[hugo documentation](https://gohugo.io/content-management/image-processing/#image-processing-examples)
{{< imgproc "derek-oyen-Pp-zoKs3pXQ-unsplash.jpg" Resize "300x" />}}