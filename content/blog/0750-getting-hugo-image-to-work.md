---
title: "0750 Getting Hugo Image to Work"
date: 2020-11-28T11:43:31Z
tags: ["image", "picture", "SVG", mermaidjs, figure, markdown, shortcode]
draft: false
rating: 5
---
{{< star5 >}}
![image markdown ](../img/test.png)

## The problem

Trying to follow the documentation and [forum](https://discourse.gohugo.io/t/confused-with-where-to-put-static-image/9822/2) on how to get an image to display did not seem to work, because there is an assumption about how the generated website is laid out. The original objective was to find a few shortcodes as well as vanilla markdown to see if a responsive image could be displayed with captions, etc.

The image test.png (2408 x 968) in static was used as input to a number of shortcodes etc, but to no avail, because the structure of the generated website was not taken into account.

Eventually, the penny dropped when the generated website was looked at, and the relationships between the HTML and the image location understood.

So, currently, image references in the blog and in hugotips are different, and if the markdown were moved to a different website with a different structure, some editing would be needed to correct any differences.

## Initial Mermaid drawing &bull; hugotips

This diagram shows the **two up, across and one down** relationship between markdown in hugotips and the image in the img folder in static.

![image markdown ](../img/mermaid-diagram-20201128114003.svg)

## Follow on Mermaid &bull; blog

The blog folder structure is different to hugotips, which means that JPEG, PNG and SVG are **one up, across and one down** as indicated by this *SVG* made with [Mermaid Live Editor](https://mermaid-js.github.io/mermaid-live-editor) which allows diagrams to be made and downloaded in a variety of formats.

This diagram has the corrected folder name within hugotips. The reason for the different structure is something to do with one of the configuration parameters.

Also, at some point, when this approach is understood, there is an alternative method, involving *bundling* which allows pictures to be placed directly in the relevant blog folder, and hence references are more straightforward. 

In the interim, care is needed to look at the generated HTML structure to see how the generated website is laid out.

Here is the SVG using vanilla markdown:

![image markdown ](../img/mermaid-diagram-20201128120917.svg)

## Using the built in figure shortcode

{{< figure src="../img/mermaid-diagram-20201128120917.svg" title="title: mermaid drawing of generated website folders" caption="caption: figure shortcode has other options!" >}}

## Mermaid diagram definition

```
graph TD
    A[Root] --> B(img)
    B -->F(test.png)
    A --> C[hugotips]
    C -->D[shortcode-for-figure]
    D -->E(index.html) 
    A -->G[0750-getting-hugo-image-to-work]  
    G -->H(index.html)
```
## imgfig shortcode

No luck with this one even though the right reference given. Have to come back to this. Fortunately other methods are working.

[imgfig](https://yktoo.solutions/blog/2019/10/08-hugo-toolbox-image-figure-shortcode-imgfig/)

## html in markdown

Tried this article about [html in markdown](https://stackoverflow.com/questions/14675913/changing-image-size-in-markdown) but no image apears here.

<img src="../img/test.png" width="200" height="200" />

## more on Hugo shortcodes

[summary and examples](http://lab-emergent360.com/workshops/example/hugo_shortcodes/)

## Responsive images in Hugo

[Laura Kalbag &bull; Processing Responsive Images in Hugo](https://laurakalbag.com/processing-responsive-images-with-hugo/)