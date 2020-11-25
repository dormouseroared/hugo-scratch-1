---
title: "Shortcode highlight"
date: 2020-11-24T15:49:25Z
tags: ["shortcode", "highlight"]
draft: false
---
[shortcodes](https://gohugo.io/content-management/shortcodes/#highlight)

[shortcode tweet](https://gohugo.io/content-management/shortcodes/#tweet)

[shortcode vimeo](https://gohugo.io/content-management/shortcodes/#vimeo)

[shortcode youtube](https://gohugo.io/content-management/shortcodes/#youtube)




See the markdown for how this works. Basically wrap the target text in the pair of highlight tags.

{{< highlight html >}}
<section id="main">
  <div>
   <h1 id="title">{{ .Title }}</h1>
    {{ range .Pages }}
        {{ .Render "summary"}}
    {{ end }}
  </div>
</section>
{{< /highlight >}}
