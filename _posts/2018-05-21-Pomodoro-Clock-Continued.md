---
layout: post
title: #100DaysOfCode Day 6
date: 2018-05-21 21:20 -0600
---

#### Day 6 of #100DaysOfCode Challenge

Not much to put on log today except just the logic behind core code of Pomodoro Clock.

Before this, though, I remembered something. 

> What is a carousel - Bootstrap

```
Carousel

A slideshow component for cycling through elements—images or slides of text—like a carousel.
```

Hmm, pretty interesting. I'd heard of this component but obvioously this is quite new to me.
Code Usage Example:

```
<div id="carouselExampleSlidesOnly" class="carousel slide" data-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img class="d-block w-100" src="..." alt="First slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="..." alt="Second slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="..." alt="Third slide">
    </div>
  </div>
</div>
```

Anyway, coming back to this screwed up Pomodoro,  
What do I really want to do:  

Let's just start with a simple timer stopwatch. Forget the circular progress bar, forget the reverse countdown. That'll all come.  
First, just the simple timer stopwatch.  
And without p5.js.

#### AFK at 9:30 pm

### 11:15 pm - Solution 1 - Using many setTimeOuts();

Okay, so I saw one of the stopwatch basic codes; the trick is to use setTimeout function, and call the function in it where we want to change the display.  
And in the called function, again call that function which houses the setTimeout function. Kind of like a recursion.

### 11:55 pm - Core Code done

Phew! Finally, did it. I think I need to improve my knowledge of setTimeout, setInterval functions.

What a stupid misunderstanding.   
**setTimeout** - Calls a function after a given amount of time.
**setInterval** - Calls a function at certain intervals. 

Wow, so I could rather have my code using setInterval. That would simplfy the function calls atleast.

Yup, working.

### 12:30 am - User Stories fulfilled

All I need to do now is design the page. 

First up, a background-image. Got one from unsplash. 
Next is writing about the pomodoro technique in short at the top-right of the web page.

### 1:20 am - Design midway

The design won't be that great for this anyway, I'm tired of this project. Just want to make it decent looking now, too tired!

## AFK at 1: 20 am 
