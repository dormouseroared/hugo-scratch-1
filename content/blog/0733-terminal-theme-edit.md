---
title:  "0733 | Hugo Terminal theme edit"
date:  "2020-11-13T17:00:00"
author:  "Nigel"
authorTwitter:  "" #do not include @
cover:  ""
tags:  ["Hugo", "Terminal Theme", "edit"]
description:  "Worth a shot. Manual update of theme to see if pages can be displayed in reverse order by title rather than date"
showFullContent:  false
---
# code change

themes > terminal > layouts > _default > index.html

line 17 

added .ByTitle.Reverse

ran hugo to update.

No errors.

Now adding some extra posts without dates eg 733 and 622.

It didn't work, so back to date invention.

#Experiment?

> It may be worth an experiment! Using the no theme setup, move the posts into there. At least with the simplified approach things can be tried out.

> Given that a refresh is needed which wasn't done, it may be worth repeating the exercise...