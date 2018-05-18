---
layout: post
title: #100DaysOfCode Day 2 continued
date: 2018-05-17 11:41 -0600
---

### Log w/o timings

Added hover animations for search results.
Found a font that resemebles that of Jarvis.

Added my clock side project at the side of the page, just as an enhancer.

Made the background transparent. 
In the draw() function,
replace
>background(0);

with 
>clear();

**In setup function, there should be another line added to fit the canvas into the divison we want it to be.**
>var canvas=createCanvas(100,100);
canvas.parent('idOfDiv');

Formatted the Input Field to fit in across the clock and not below it.