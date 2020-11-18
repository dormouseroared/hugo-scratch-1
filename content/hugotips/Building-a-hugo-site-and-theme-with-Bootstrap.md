---
title: "Building a Hugo Site and Theme With Bootstrap"
date: 2020-11-18T09:50:09Z
tags: ["bootstrap", "photos"]
draft: false
---
## How is Bootstrap used with Hugo?
Bootstrap is in use with hugo-scratch-1 but there aren't many explicit uses of the classes. So it is time to explore this in more detail by taking notes whilst reading this first search result:
* [Building a Hugo Site and Theme With Bootstrap](https://willschenk.com/articles/2018/building-a-hugo-site/)

## Result

* In the photos, this didn't look right:
 * Now if you go to http://localhost:1313 you should see the normal list of pages that is generated with the default list template. Let’s now create a list template for our new photos type in themes/mytheme/layouts/posts/list.html
 * Now if you go to http://localhost:1313 you should see the normal list of pages that is generated with the default list template. Let’s now create a list template for our new photos type in themes/mytheme/layouts/**photos**/list.html
* Apart from that the instructions were carried out as far as the last sections which involved another update to the header, and various other small changes, which can be returned to.
* See | green | websites | hugo-bootstrap | for the code, which has been tested with hugo server.

## Follow up
[Adding Netlify CMS to Hugo](https://willschenk.com/articles/2018/adding_a_cms_to_hugo/)