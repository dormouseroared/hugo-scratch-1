---
title: "How to resize images in Hugo"
date: 2020-12-04T00:00:00Z
tags: ["draft", "image optimisation"]
---
[Vegard Skjefstad &bull; How to resize images with Hugo](https://www.vegard.net/hugo-resize-images/)

# Initial setup limits images to 640 px width
Create this file: `layouts/render-image.html`
```html
{{ $image := (.Page.Resources.GetMatch .Destination).Resize "640x" }}
<img src="{{ $image.RelPermalink | safeURL }}" />
```

Carried out. 

The optimisation only works on **bundles**. 

Looked at Page Info then media for the images, and there were hopeful messages about reduced size, so need to disable the change and inspect before and after.

