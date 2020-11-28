---
title: "mermaidjs"
date: 2020-11-27T22:19:32Z
tags: ["shortcode", "mermaidjs", "theme", "drawing", "diagram", "netlify"]
rating: 4
draft: false
mermaid: true
---
{{< star4 >}}
# Some links to mermaidjs

The topic is interesting because it will be useful to create the various diagrams. Initially, some links can be collected here, and mermaidjs explored. 

[mermaid js](https://mermaid-js.github.io/mermaid/#/)

## Netlify Learn Theme &bull; mermaidjs shortcode

Looking for information about being able to make a diagram in Hugo using shortcodes, found this [Learn Theme](https://learn.netlify.app/en/) which has a [Github repository](https://github.com/matcornic/hugo-theme-learn) with shortcodes, including [mermaid](https://learn.netlify.app/en/shortcodes/mermaid/).

There would be a link to the javascript, and a shortcode to set up, but here is an example of the shortcode being used to make a diagram. This has now been enabled, using the mermaid shortcode in the next heading section. It should still work. It does. Now we have the live rendering and the picture.

```
{{< mermaid align="left">}}
graph LR;
    A[Hard edge] -->|Link text| B(Round edge)
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
{{< /mermaid >}}
```
![mermaid picture](../../img/mermaidjs.png)

## Trying out a mermaid shortcode

[mermaid js hugo shortcode](https://codewithhugo.com/mermaid-js-hugo-shortcode/)

* add layouts/shortcodes/mermaid.html
* add mermaid js package load (a specific version at the moment) to the bottom of /layouts/_default/single.html
* set mermaid: true in the front matter for this markdown
* here is some mermaid definition using the shortcode (it works!)

{{<mermaid>}}
graph TD;
  A-->B;
  A-->C;
  B-->D;
  C-->D;
{{</mermaid>}}

## More links to follow up

Hugo is the name of the person running this website, but there are a few links to the static site generator.

* [Code With Hugo &bull; Using Hugo](https://codewithhugo.com/switching-the-lights-on-hugo-vs-hugo-config-files/)
* [Disaster at Github &bull; Migrate To Netlify](https://codewithhugo.com/a-tiny-case-study-about-migrating-to-netlify-when-disaster-strikes-at-github-featuring-cloudflare/)
* [Add Search To A Hugo Site](https://codewithhugo.com/hugo-lunrjs-search-index/)