---
title: "0735 | Publish Hugo Website on Github"
date: 2020-11-14T23:56:16Z
tags: ["green", "git", "github", "hugo", "publish", "GeekLaunch", "youtube"]
draft: false
---
### GeekLaunch has a Youtube Hugo playlist (7 videos)
[Youtube | GeekLaunch | How to make a website and put it online 2017 Tutorial (Hugo, Linux)](https://www.youtube.com/watch?v=3wkR8GyDODs&list=PLwnSaD6BDfXIWCBwbZNTl7pc-mbon8LSi)

[Github](https://github.com)

### youtube shortcode

{{< youtube 3wkR8GyDODs >}}

### Web: Sign into github account

### Web: Create new repository and copy the address for the git remote add origin

### Terminal: navigate to green websites/hugo-harrycresswell
This is where some Hugo testing is in progress.

### Terminal: git commands
```
git init
git remote add origin https://github.com/dormouseroared/hugo-dm1.git
git status
git add --all
git commit -m "Initial commit"
git push -u origin master
```

Note that the response to push might be to enter these commands:
```
git config --global user.email "github email"
git config --global user.name "github name"

```

### Web: refresh github page to see updated repository
### Web: click Settings on right hand end of commands, scroll down to Github Pages

* Choose Branch=master, then see that the only folder that can be used to publish from is called Docs
* Update config.toml with publishDir = "docs"
* Repeat git terminal command block above
* Update baseURL in config.toml to be the github address
* Repeat git terminal command block above
* [Github Hugo Website](https://dormouseroared.github.io/hugo-dm1)

### Other points

> No real content published because every post or content has draft=True. Need to see how to > publish to make that draft=False without having to go through every document.
> This is a test site which has no HTML header stuff at all.

