---
layout: post
title: Android Basics
date: 2018-03-08 00:30:00 -0600
---

So [AppTeam](https://github.com/appteam-nith) took some extra efforts in teaching me Android Studio yesterday,  
and a special thanks to [Sahil Sir](https://github.com/RamolaWeb) for that.
So here are some notes that I took down at the time of teaching, ofcourse I didn't write a lot of stuff and practiced it instead.  
Yet,

**manifest**
Declares empty point
Declares name of app, icon of app, permission of app  

>android: layout_width="match_parent"
android: layout_height="match_parent"  

This takes all the space available in the parent.

><TextView
android: layout_width="wrap_content"
android: layout_height="wrap_content"/>

Takes only that much space as much as its content.  
Use of TextView: To create uneditable code.  

><TextView
android: id="@+id/firstView"
android: layout_margin="10dp"
android: layout_marginRight="30dp"
android: text="Utkarsh"
andorid:textColor="#FF0000"
android:gravity="center"
android: layout_width="wrap_content"
android: layout_height="wrap_content">

EditText - TO Create editable text
><EditText
android: hint="Please Type Your Name"
android: layout_width:"match_parent"
android:id="@+id/userInput"
android: layout_margin="10dp"/>

We can also create editable text by adding
> android: text:"Check"

Under MainActivity.java
Change
>SetContentView(R.layout.activity_second);

"activity_second" is the name of the xml in the layout section.

Okay, this was it. This was probably nothing and completely unorganized, but I'll see if I can change it later on.  
Now, to start making my own dream apps, I must get fluent in this app and language.  
And for that, I need to make some basic apps rather than going for my own ones.  
So I saw a Quotes-maker app on the internet as a basic app. Let me see if I can link my Random Quote Generator project with this.  

Let's begin!  
Opened the JS Side Project of Random Quotes
Now, the first thing I need in my app is a new background image. I'm too stylish to keep the plain white background.  
Here's the net solution:

1. You can go to Drawable and choose the Show in Explorer. Click now and Drawable opens. We can go to Drawable folder. The folder is empty and you can select any one image. Cut to paste on Drawable folder and automatic is enabled in the image.
2. Now, under the Linear/Relative Layout tab, add:
>android:background="@drawable/darkness"

So this gives us a complete background.
Now, there's this nav bar which doesn't suit the background.  
Okay, so I just went to the values folder, and changed up the color.xml. Just a few trial and errors, and I was done.  
One problem which I faced was that while making changes to the color.xml file, I couldn't see the changes realtime as I could for the layout xml file I was coding in.  

Anyway, then I decided to give it a textual animation at the beginning. But my app wasn't exactly what I wanted. The intro text wasn't on top of the image but below it!  
What's the point of a background image then?
So I changed my LinearLayout to RelativeLayout. It worked so easily!  
Although in this struggle I did find the equivalent to 'z-index' in Android Studio for LinearLayout, that is:
>android:layout_weight="0.8"

Although this didn't work for what I really wanted, I might need it some day.  
Then what I did was just adding a button, made colour changes to it through
> android:background="@color/colorPrimary"

Since too many colours also spoil the mood, I just gave it the colour of a nav bar and changed the font color to white.  
One big problem I had was figuring out how to center-align all the contents and which I should be highlighting  

*android:layout_centerHorizontal="true"*

And if we want it to be perfectly aligned from everywhere,
>android:layout_CenterInParent="true"

So this was just the .xml changes done. Now, as a last task, let me just finally animate the text.  
Well, I think it'll require me to build an xml file, and then implement it in the Main_Activity.java.  
Done! I implemented the fade in effect on the startup screen.  
So here are the steps:  
1. Create a resource directory under res folder. Under that, create your xml file containing your animation.  
2. I created the fade in effect, so my code was basically this:
```
<alpha
        android:duration="1000"
        android:fromAlpha="0.0"
        android:interpolator="@android:anim/accelerate_interpolator"
        android:toAlpha="1.0" />
```
Obvoiusly there are many more available on the internet and we don't need to write our own codes for them, but a systematic understanding about them is important.  
From  [JournalDev](https://www.journaldev.com/9481/android-animation-example), these are the notes:
```
android:interpolator : It is the rate of change in animation. We can define our own interpolators using the time as the constraint. In the above xml code an inbuilt interpolator is assigned
android:duration : Duration of the animation in which the animation should complete. It is 300ms here. This is generally the ideal duration to show the transition on the screen.

The start and end of the animation are set using:

android:fromTRANSFORMATION
android:toTRANSFORMATION

TRANSFORMATION : is the transformation that we want to specify. In our case we start with an x and y scale of 0 and end with an x and y scale of 1
android:fillAfter : property specifies whether the view should be visible or hidden at the end of the animation. We’ve set it visible in the above code. If it sets to false, the element changes to its previous state after the animation
android:startOffset : It is the waiting time before an animation starts. This property is mainly used to perform multiple animations in a sequential manner
android:repeatMode : This is useful when you want the animation to be repeat
android:repeatCount : This defines number of repetitions on animation. If we set this value to infinite then animation will repeat infinite times
```
3. Now implementing this in the Main_activity.java.
```
TextView text =(TextView)findViewById(R.id.intro);
        Animation animation;
        animation = AnimationUtils.loadAnimation(getApplicationContext(),R.anim.fade_in);
        text.startAnimation(animation);
```

Although I have added the animation, the presentation still doesn't look good. One reason is because even after I center the text, it's still left-aligned.  
I need to put "Welcome to", "Quote a" and "Quote" on seperate lines. And I could add two animations at once which include fade_in and slide_down effects.  
I have added animations now, however, I need the 3 TextViews to fade in one after the other. Anyway, I couldn't figure it out so I have put up an issue on my repo for that.  

Okay, so I have designed the startup screen completely. Time to move on to the real content. There's a lot of Java coming up right now!  

Hurray! I have completed the first version of my app Completely!
Yup, I did the Java code, created the new xml layout, and currently I can't believe I made a complete app by myself!
With this joy, I list out the things that I aim on doing ahead on this app.  
1. Animate the text that comes after every "Next Quote" button press.
2. Make the quotes and authors array accessible to the user.
3. Allow the user to delete and modify the quotes.

So on this happy note, I bid goodbye to my first Android Post.
