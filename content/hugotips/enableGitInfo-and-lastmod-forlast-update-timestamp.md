---
title: "EnableGitInfo and Lastmod For Last Updated Timestamp"
date: 2020-11-26T16:44:33Z
tags: ["git", "lastmod", "rating"]
draft: false
rating: 4
---
## Reading through the Hugo documentation

This first link wasn't the one originally read that resulted in changing hugo-scratch-1, [Git variable](https://gohugo.io/variables/git/), but it does have some useful information to be followed up.

* update the config file to make enableGitInfo true

```
enableGitInfo (false)
Enable .GitInfo object for each page (if the Hugo site is versioned by Git). 
This will then update the Lastmod parameter for each page using the 
last git commit date for that content file.
```

* use *lastmod* in layouts/_default/single.html to show the last updated timestamp for each bit of content.

[configuration](https://gohugo.io/getting-started/configuration/)

* Added rating as well, as it is available via Params. Not sure what happens if it is absent.

{{< star4 >}}
