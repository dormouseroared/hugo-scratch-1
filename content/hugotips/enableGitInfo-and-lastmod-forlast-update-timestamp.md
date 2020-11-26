---
title: "EnableGitInfo and Lastmod For Last Updated Timestamp"
date: 2020-11-26T16:44:33Z
tags: ["git", "lastmod", "rating"]
draft: false
rating: 4
---
## Reading through the Hugo documentation

This first link wasn't the one originally read that resulted in changing hugo-scratch-1, [Git variable](https://gohugo.io/variables/git/), but it does have some useful information to be followed up.

* update the config file to make enableGitInfo true (default is false)

```
enableGitInfo (false)
Enable .GitInfo object for each page (if the Hugo site is versioned by Git). 
This will then update the Lastmod parameter for each page using the 
last git commit date for that content file.
```

* use *lastmod* in layouts/_default/single.html to show the last updated timestamp for each bit of content.

[configuration](https://gohugo.io/getting-started/configuration/)

* Added *rating* as well, as it is available via Params. If rating is absent, there are no errors, and blank is displayed. 
* In addition, a first attempt at a shortcode for 4 stars (red feather icons), called star4.html, is being tried out, and it seems to work! It would be better to have this generated in the template but this will have to do for now.

{{< star4 >}}
