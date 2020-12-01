---
title: "hugo-scratch-1 Mermaid diagram"
date: 2020-12-01T15:31:38Z
tags: [mermaidjs, hugo]
draft: false
rating: 5
mermaid: true
---
{{< star5 >}}

First go at trying to represent the relationship between the "elements" of this web site.

## HUGO converts the INPUTS into OUTPUTS

Hugo generation uses the "elements" to convert the content into the web site (HTML, CSS).

## DIAGRAM

Difficult to draw, but `HOME`, `LIST`, `SINGLE` and `TERMS` are the starting point, the templates. 

These templates in turn cause the `baseof` template to be used, and `partials` to be included.  

In addition, external libraries including `bootstrap`, `feather icons` and `mermaidjs` are shown.

So, for layouts/`HOME`.html page generation, all the following are included:
 * layouts/_default/`baseof`.html
    * layouts/partials/`head`.html
        * `bootstrap`
        * `favicon`
        * layouts/partials/`style`.html
    * layouts/partials/`nav`.html
    * layouts/`home`.html
    * layouts/partials/`script`.html
        * `feather icons`
{{<mermaid>}}
graph LR;
  H(baseof)-->I[head-partial];
  H-->J[nav-partial];
  H-->L[[main]];
  H-->K[script-partial];
  I-->M([bootstrap]);
  I-->N[favicon];
  I-->O[style-partial];
  L-.->P{{HOME}};
  L-.->Q{{SINGLE}};
  L-.->R{{LIST}};
  L-.->S{{TERMS}};
  R-->T[date-and-tags];
  Q-->V[date-and-tags];
  Q-->W([mermaid]);
  K-->U([feather icons]);
{{</mermaid>}}