---
layout: post
title: Side Project on NGO Site
date: 2018-020-27 00:45:00 -0600
---

Just recently, I was having a talk with one of my classmates about one of the top coder on the Codeforces site, a Russian-origin CP hub.  
He said that the top coder once said that his strength, was Graph algorithms. And guess how many problems did he solve in relation to  
only the specific Graph algorithms?  
4,000!!  
Yes, Four Freaking Thousand CP problems only related to Graphs!!!  
This teaches me a very important lesson. Instead of running behind newer algos and trying to take in all of them as soon as possible,  
I should master those which I already know. For the first time I'm realising that Coding is just like the Martial Arts. We've heard about  
these in movies and stories, about practising one technique or skill in at most perfection. This is what I'm gonna do.
The first CP topic that I'm truly gonna MASTER, is **Linked Lists.**  

I have learnt and understood Linked List, practised it once, but not applied it in CP. So that's what I'll be doing today.  
Well, later though. Right now, I'm high on inspiration after watching 'The Social Network', and will be doing the side project  
which hasn't been perfectly named, but let's call it **NGO Site** for now.

Okay, So here's the idea.
>There should be an online encyclopedia of all NGOs, grouped by their original locations, informing the reader what  
they really do, and what kind of donations they accept: Money, Clothes, etc.
In addition to just donate, the viewer can also inform the NGO about any work that s/he think can be done by the NGO.  
For example, an NGO serving free education to poor children could be made aware by a person who has seen some wrecked kid recently w/o education.  

The [repository](https://github.com/parasg1999/HTML-NGO-Project) is already created in [Paras Gupta's profile](https://github.com/parasg1999).  
I have already forked it, checked if he wasn't working on it, and with the road clear, I'm good to go.  
When we last discussed, I was assigned the job of designing filters for searching.  
Now when the user clicks on `Donate Now` button on the home page, s/he either knows what to donate and are looking for the organisation that would accept it,
or know which organisation to donate to, and then from their profile, donate whatever they want to donate.  

So the filter should have 2 categories:
1. Kind of donation       -       Dropdown
2. NGO                    -       Text input box

I'll obviously have a list of NGOs. A loop would be run across all elements. Now, what I think I should do is,  
I should create objects within an array. Each object will contain *Name of NGO*, *Kind of Donation*, *Year of Establishment*, and *Location*.  
I'm thinking one step ahead here, that is for presenting the profile page of every organisation. If I save the data in this format, it'll be easier to
get data from it and paste it onto the profile template.  

I can't remember much of this object within array thing, so let me just revise about this.  
Okay, what I need, can be done simply by a 2D-array. However, I still think the info could be more presentable to coders if objects will be used.  
So I could create a prototype of an object, and then access it for every array element. Well, even that would be similar to the 2D array thing, but  
the code would be understandable and tidier.  

I again googled Creating Object Prototypes JS. Seems like I've forgotten quite a lot about JS. Okay, not to worry about anything. I remember quite a lot of stuff.
So I didn't get the answer to the question I was looking at, that is, I'll have to put some value as the default value of the object datatypes.  
Let's begin by first constructing the array.  

Okay, so I did construct the array, added the loop to find the donation thing. Now, the important thing is, how will I display the info about the selected NGOs.  
I have just begin by writing the JS code, and haven't started the HTML page design. But the real question is, how will I make the list appear.  
Now I must point out that I don't want a simple basic list, no. I want rectangular, post card kind of results. on each post card, the Name of the NGO, and all the other info
shall be displayed.  

I'll come back to this problem later on. For now, I'm gonna sleep and hope I get to enroute Mumbai.
