---
layout: post
title: Android Basics
date: 2018-03-08 00:30:00 -0600
---

So [AppTeam](https://github.com/appteam-nith) took some extrs efforts in teaching me Android Studio yesterday,  
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
