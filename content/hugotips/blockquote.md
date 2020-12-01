---
title: "Blockquote"
date: 2020-12-01T10:50:33Z
tags: [blockquote, CSS]
draft: false
rating: 1
---
In hugo-scratch-1, using the markdown for blockquote, which is:

 `> followed by space at the start of a line`

 there was no formatting of any kind. 

 ## what html is hugo generating

 Understanding what HTML is generated is the starting point, so a simple `View Page Source` shows that BLOCKQUOTE start and end tags are being generated. So either the default CSS or the generated CSS is not set up for BLOCKQUOTE. 
 
 ## Update CSS for blockquote

 Found some CSS, and adjusted it to indent the left hand side with a bar down the left hand side for now, and will look for other alternatives.

 The CSS is in `/layouts/partials/styles.html`

 And here is the current BLOCKQUOTE:

 > Here is a blockquote!  