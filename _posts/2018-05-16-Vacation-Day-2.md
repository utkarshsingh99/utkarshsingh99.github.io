---
layout: post
title: #100DaysOfCode Day 1
date: 2018-05-16 10:26 -0600
---

### - 10:30 am
Officially kickstarted #100DaysOfCode challenge. 

Installed Sublime Text owing to weird text output bugs in Atom.

Beginning Wikipedia Viewer project again.
Aim: Finish this project today.

References: Austin Tackaberry's direct wikipedia links used for **query** and **open search**

### - 8:30 pm
Referencing [Austin Tackaberry's project](https://www.freecodecamp.org/austintackaberry).
Main aim: To reverse engineer links used for search list MAINLY and also for wiki page of each topic.

Here is the wiki.js file
```
var searchData = {
  titles: [],
  snippet: []
};

function Callback() {
  var titleHTML = "<ol class='list'>";
  for (var i = 0; i < 10; i++) {
    titleHTML += "<li><a href='https://en.wikipedia.org/wiki/" + searchData.titles[i] + "'" + ">" + searchData.titles[i] + "</a>: " + searchData.snippet[i] + "</li>";
  }
  titleHTML += "</ol>"
  $("p").html(titleHTML);
}

$(document).ready(function () {
  $(".search").on("click", function() {
    $.ajax({
      dataType: "json",
      url: "https://en.wikipedia.org/w/api.php?action=query&format=json&list=search&srsearch=" + document.getElementById("search").value + "&callback=?",
      async: false,
      success: function(json) {
        for (var i = 0; i < 10; i++) {
          searchData.titles.push(json.query.search[i].title);
          searchData.snippet.push(json.query.search[i].snippet);
        };
        return Callback();
    }});

  });
});

```
So when the search button is pressed, the link that is acting is:
https://en.wikipedia.org/w/api.php?action=query&format=json&list=search&srsearch= + something + [&callback=?]().

https://en.wikipedia.org/w/api.php?action=query&format=json&list=search&srsearch=check&callback=?
Let's check this link's functionality.

The problem is that it's almost unreadable for me since the json format is not formatted properly.

I don't know why but the json document is not being parsed properly by both the browsers in spite of adding specific extensions.
I'll leave this problem and extract it just the way Austin has does: 

>json.query.search[index].(title/snippet) 

Basically this link returns 10 search results and I have to give out this data by looping the results.

The link for the Wiki page to open up is just what I imagined. 
https://en.wikipdia.org/wiki/something

So let's just sum up the work that I need to do:
1. Create HTML file and create a text input field in it. [Done Already]
2. Create JS file and do the following.
3. First make a search function that stores text input field into a variable string. Because I want to keep the search option always functional unlike the other projects which I saw.
4. Then in the function itself, using the getJSON function, call a function to display the text search results. 
5. Put in links in titles of the search results.
6. Design the rest of the page.

#### 9:00 pm - Break announced

### 11:00 pm - Resuming Code

Used the search list invoking link, however, search results aren't that accurate. 
Tried cracking the freeCodeCamp, but I just don't get it! It's too cubersome.

### 12:10 am - Core Code Done

The user stories are complete. Now I have up till 1:30 am to design the rest of the page and use p5.js. 
Let the creativity flow!

### 12:40 am - Designing Begins

First up, I want to enclose these search results in card-like divisions.

### 1:10 am - CardView Desgined

Now, I want a good colour combination. I'm thinking of JARVIS. Everything in blue.

>New Tip: To style list icons: use **list-style-type** in your classes.
Maybe a black background and blue font-color.

### 1:40 am - Animations Added

2 Tasks:
1. Formatting of Search Box and Icon
2. Display list horizontally to make it look more like JARVIS.

### 2:45 am - Both the tasks have been done

Now I need to make the search box go up when searched once.
Changed my mind, not vertically centering the input field.

### 2:50 am - Bug Alert

Input field does not accept another text after searching once. 
Going to put this as an issue. Can't find a proper answer to this. 

###3:00 am - Project Complete!

Finally the Wikipedia Viewer page is complete. Took a lot of hardword, disappointed due to no use of p5.js, but still quite on track for FreeCodeCamp certification.