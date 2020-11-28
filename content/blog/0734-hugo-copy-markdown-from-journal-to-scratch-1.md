---
title:  "0734 | Copy markdown files from hugo-journal to hugo-scratch-1"
date:  "2020-11-13T17:00:00"
author:  "Nigel"
authorTwitter:  "" #do not include @
cover:  ""
tags:  ["Hugo", "hugo-journal", "hugo-scratch-1"]
description:  "not used"
showFullContent:  false
---
The Journal Theme looks good, but there is more opportunity to learn about Hugo by evolving hugo-scratch-1 and seeing how easy it is to copy markdown entries between setups. The Journal Theme is like all the themes seen so far, at an advanced level that makes understanding it an impossible challenge at the moment.  But it is useful to have it there as a reference as the understanding increases.
For example, the front matter parameter *cover* results in an image being displayed at the top of the post. There will be other similar fragments that might be understood and extracted for use.

* Changed the leading journal number in the Title from 3 to 4 digits becuase this is being used as the reverse sort key as we don't have dat and time stamps available for every post.
* ByPublishDate Reverse has been changed to ByTitle.Reverse in layouts/_default/list.html
* Changed front matter delimeters to be consistent, so three plus signs changed to 3 minus signs etc and this is part of toml to yaml or the other way round.
* use hugo server -D to ensure that any draft items are included
* Any other parameters can be left and may be worth looking at for understanding as per the earlier point.
