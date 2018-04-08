---
layout: post
title: Weather API JS Project
date: 2018-04-08 16:30 -0600
---

###4:30 pm
I got a mail from Quincy Larson this morning, and I read this [post](https://medium.freecodecamp.org/how-i-went-from-newbie-to-software-engineer-in-9-months-while-working-full-time-460bd8485847).   
Absolutely brilliant! Motivated me and reminded me of a good new direction. I am always influenced so much by my surroundings, I often lose my identity.
I should have continued the freecodecamp front end development course consistently and I might have had my Front-End Development certificate by now. But I went after libraries,  
then App Development, and so on. So I'll be in this course for the entire month, and hopefully I'll finish it before May.

Before that, I'm going to add my Clock project in p5.js to Codepen since I'll be deleting my repository on Github related to p5. I'm not going into it right now, it seems easy, and I think it can be learnt when
the need arises. I know the basics already.
###5:00 pm
Now moving on to the main project. I'll use freecodecamp's API which they have given in the challenge itself. It should be easy but I'll still make tht my first step: Testing the response.
I'll first ask the location of the user, that should be pretty easy since the browser automatically does that.

###5:30 pm
It's been 30 minutes and I'm still struggling with getting geolocation. It's weird, whenever I try to run a copied program, it runs delightfully, but when I write my own typed code, even if it's similar to the copied program, it just doesn't work.

###5:45 pm
Phew! It worked, finally! The only change after which it worked was I changed my h4 tag to p when I called it for innerHTML. No idea why. The freecodecamp site has it running with h4 tag but they have used jQuery for it. Now let's move on to using the API.

###6:15
After a lot of hardwork, I finally managed to run an API!!! I am so damn happy! I used the **getJSON** method to call data from an API.
```
$.getJSON("https://fcc-weather-api.glitch.me/api/current?lat="+lat+"&lon="+lon,api);
function api(json){
  a.innerHTML="Longitude: "+json.coord.lon;
}
```
Obviously the api function is just testing the API. The real data will be extracted later. Now I'll be taking a break unwillingly for my studies.

###12:30 am
And I'm back! So let's begin the designing. Now that I know how to run, get data from an API and display it on the page, let's start with shortlisting what all parameters should be there to display.  
So first the user stories need to be taken into account:
1. Weather for current location. **Done**
2. Different Background Image for Different weather. **Done**
3. Button to toggle between Farenheit and Celsius.

Okay, easy to achieve the basic stuff. First I need to get high definition images of different weather
conditions.
So if I choose to display images based on the "main" data, I need to first find out how many answers are there.
1. Clouds  **Done**
2. Haze   **Done**
3. Clear  **Done**
4. Fog    **Done**
5. Rain   **Done**
6. Drizzle **Done**

###12:50 am
Hmm, seems like these are the categories. So, I'll be looking for great wallpapers for these categories.
First I need a great site that gives them.
Let's try with wallcoo.net, favoured by the search result for HD wallpapers.

###1:15 am
All done! Some from this site and some from google. Now I need to display data on the screen.
I think I should just display the Place and the temperature. All the other interesting things with p5 that are coming to my mind right now should be let aside for some time.

Now I have once again forgotten the animation using JS.

###2:00 am
Revised the Random Quote animation, so I just have to add intervals. But first I need to display the data in a nice stylish format.

###2:15 am
I discovered an interesting coding mistake that I was doing.
```
var anim=setInterval(animation,100);
function animation(){
  var op=0;
  if(place.style.opacity==1){
    clearInterval(id);
  }else{
    op+=0.1;
    place.style.opacity=op;
    temp.style.opacity=op;
  }
}
```
This was my original code. Now, what was happening was that the text would appear only for half its entire opacity. The op variable is being declared at each call to the frame, and that's why it is never 1.
Thus the correct way to declare this function is:
```
var op=0;
function animation(){
  if(place.style.opacity==1){
    clearInterval(id);
  }else{
    op+=0.1;
    place.style.opacity=op;
    temp.style.opacity=op;
  }
}
```

###2:30 am
Wow! I'm actually learning a lot in this! I wanted to cascade the place and temperature animations, so I tried with newer variables, but the console showed a lot of bugs. Turns out, I was making too many independent functions. When calling out functions in setInterval, I need to declare those function lines within the parent function of the setInterval function.

Anyway, now I need to try changing the background of the page.

###2:45 am
The Background Image stuff has been done. Now I just need to add that Farenheit to Celsius toggle.

###3:00 am
So the toggle button has also been added. A basic functional User-Story fulfilling Weather Forecaster is ready and it's time to sleep! Today was really fun!
