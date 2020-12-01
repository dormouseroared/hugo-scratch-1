---
title: "Blockquote"
date: 2020-12-01T10:50:33Z
tags: [blockquote, CSS]
draft: false
rating: 5
---
{{< star5 >}}
## the problem
In hugo-scratch-1, using the markdown for blockquote, which is:

 `> followed by space at the start of a line`

 there was no formatting of any kind. 

 ## what html is hugo generating?

 Understanding what HTML is generated is the starting point, so a simple `View Page Source` shows that BLOCKQUOTE start and end tags are being generated. So either the default CSS or the generated CSS is not set up for BLOCKQUOTE. Not sure how to work out the default styling situation, so have a go at putting some styling in. Note that Visual Studio Code reports errors in the CSS which look as if they are because Hugo templating code is in the CSS which VSC does not understand.
 
 ## Update CSS for blockquote

 Searched, and there are many good examples, including [codepen](https://codepen.io/cliftwalker/pen/XJaEXY).
 Adjusted it for width and will look for other alternatives.

 The CSS is in `/layouts/partials/styles.html`

 And here is the latest BLOCKQUOTE, with the first version commented out:

 > Here is a blockquote!  