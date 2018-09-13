---
layout: post
title: Mad Libs Game
date: 2018-07-20 14:30:00 -0600
---

### Don't call it a comeback!

A big break was taken from blogging, yet I am still upbeat about my coding since I was busy in learning Nodejs from Udemy.  
It's an obviously great course and I recommend everyone to it. Here's the [link to it](https://www.udemy.com/the-complete-nodejs-developer-course-2/learn/v4/overview).  

### Ideation

So I was playing around with Google Assistant and I came across this game of Mad Libs. Basically, all you have to do is keep naming a few words, whether it asks you for a noun, adjective, or adverb; and it promptly just gives you a paragraph that constitutes your words. I think it's the beautiful fault in the ability of the AI to understand some of the nouns and adjectives that makes this so funny at the end when you read the paragraph which includes names of your friends and stuff around you which makes just enough sense to give you the gist of the final para and just not enough to make you laugh. If you didn't understand the previous line, I think you should really try the game in your Assistant first.

### Making the Mad Libs game

Hmm, now making it. It's simple. Keep a lot of paragraphs in a database, or a string array. Pick one para from it. Now ask the user for the words. Replace an adverb from the para with the adverb given by the user and do this with all the other parts of sentences. That's it! Now there's only one thing that I need and I found it in the first try.

#### [WordPOS](https://www.npmjs.com/package/wordpos)
```
wordpos is a set of fast part-of-speech (POS) utilities for Node.js using fast lookup in the WordNet database.
```

### Basic Front end

First let's design a basic HTML page that gives us a page to input our cases.
I ran the code after building a basic HTML page for word input only, but this error was thrown:
>Reference Error: require is not defined

Of course I can't just use Node functions in the browser. The only way is to build up a server.
Now, since I will be constantly giving data to server every time I hit the submit button in my HTML page, I will have to include a socket like connection.
