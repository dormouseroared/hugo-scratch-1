---
title: "Using Bootstrap in Markdown"
date: 2020-12-06T13:17:18Z
tags: [bootstrap, markdown]
draft: false
rating: 4
summary: "Try some bootstrap in this markdown e.g. grid layout using container, row and col, and a go at putting a border round each cell."
---
{{< star4 >}}

## Bootstrap Grid with borders
<div class="container">
    <div class="row text-uppercase text-light bg-dark">
        <div class="col border border-primary">
            <p>first</p>
        </div>
        <div class="col border border-primary">
            <p>second</p>
        </div>
        <div class="col border border-primary">
            <p>third</p>
        </div>
        <div class="col border border-primary">
            <p>fourth</p>
        </div>
    </div>
    <div class="row">
        <div class="col border border-primary">
            <p>five</p>
        </div>
        <div class="col border border-primary">
            <p>six</p>
        </div>
        <div class="col border border-primary">
            <p>seven</p>
        </div>
        <div class="col border border-primary">
            <p>eight</p>
        </div>
    </div>

</div>