---
title: "0745 GitCourse on Youtube (LearnWebCode)"
date: 2020-11-22T17:36:30Z
tags: ["LearnWebCode", "git", "shortcode", "git checkout", "revert"]
draft: false
---
## LearnWebCode's short 4 part Youtube about git
This is the Hugo shortcode for a youtube video. Don't think a playlist can be used, so here are all the videos in the series. More details may be available in the Udemy course called Git a web developer etc.

{{< youtube 9GKpbI1siow >}}
{{< youtube n-p1RUmdl9M >}}
{{< youtube UFEby2zo-9E >}}
{{< youtube ol_UCWox9kc >}}



## Revert to last commit point

This worked very well. Tried it out by making a commit to the local repository, then making a change, then issuing this command, and straight back to the commit point. More to find out about other uses of git.

```bash
git checkout -- .
```