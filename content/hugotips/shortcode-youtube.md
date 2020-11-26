---
title: "Shortcode Youtube"
date: 2020-11-16T20:13:47Z
tags: ["shortcode", "youtube"]
draft: false
---
## example of using an existing shortcode

[Medium | The Agent | shortcodes in Hugo](https://medium.com/@the.agent/how-to-create-your-own-shortcodes-in-hugo-72b48454c47e)
[Hugo | built in short codes](https://gohugo.io/content-management/shortcodes/#use-hugos-built-in-shortcodes)

```
---
title: "Embed a Youtube video"
date: 2020-01-01T14:17:03-05:00
draft: false
---
```
{{< youtube w7Ft2ymGmfc >}}




## How to create a custom shortcode

So how do we create our own custom shortcode? 

It’s fairly easy. All we have to do is create a shortcodes folder under the layouts folder, and put the HTML file that we want the shortcode to insert in the folder. The name of the HTML file (without the .html extension) will be the name of the custom shortcode.






![example](/img in static folder.jpg)