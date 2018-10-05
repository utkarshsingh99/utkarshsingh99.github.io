---
layout: post
title: Competitive Coding in JavaScript
date: 2018-07-20 14:30:00 -0600
---
## Competitive Coding in JavaScript

All over the internet people have debated on this issue, and yet the knowledge about this seems so lost around.  
This is my first post on Medium, and I was compelled to choose this topic. If you have read some stuff about this before,
I suppose everything you read was on the negative. That’s true, however I just believe that everyone has the right to try
and then form an opinion instead of just reading something and stopping. If you want to just learn How to program in JS for CP,
you can skip over the next section and move to the subsequent one.

There is no need to stop anyone from going into CP with JS. My first search on this landed me on Quora where coders were all against JS for the following reasons:

### JavaScript is Slow

JS is slow as compared to C, C++ and Java, which are known as the best languages for CP. Even the “brilliant” and “popular” language Python doesn’t seem to make the cut. There are many codes which get accepted as the correct solution in C/C++ for CP questions, but the same algorithm used to code in Python fails citing [TLE]Time Limit Exceeded as the error. (This has actually happened with one of my friends who knew both C++ and Python). For beginners of CP, if you want to familiarize yourself with all the possible errors and basics of CP, here’s a link:

[Hackerearth](www.hackerearth.com)

So there is a high chance that in certain complicated questions, your best algorithm still won’t work in the allotted time while using JS.

### JavaScript is not a language used in major Competitions

Yes, the main competitions of CP namely, ACM ICPC host only C++ and Java as their main programming language. So if you’re looking to go to such highly reputed competitions, there’s not a chance you’ll be able to fight the war there when your prized language weapon would be banned!

Having summarised everything on the internet, let’s move on to the next step. What happens when you ignore all of this and actually start coding in JavaScript? Not much of a damage, I must say. In every CP hosting site, there is the option to choose your language before submitting your solution. Almost every site has the option to choose JavaScript. For JavaScript there are two options for you to choose from:

    JavaScript Node
    JavaScript Rhino

I bet the majority of the JS developers would have experienced a slight mental delight when they would have read “JS Node”. And it sure was the case for me too. Don’t worry though, even if you don’t know anything about Node or Rhino, you still can code in them. Here’s a quick introduction about them:

NodeJS: is an open-source, cross-platform JavaScript run-time environment that executes JavaScript code outside the browser.

RhinoJS: is a JavaScript engine written fully in Java and managed by the Mozilla Foundation as open source software.

Now here’s my story of starting CP in JS. I obviously knew JS and NodeJS, but wasn’t quite sure of taking input in JS. I knew that in the servers of CP sites, they have an input test cases file which they feed to every program code submitted; but without using any modules or form elements, I didn’t know how to do that. And I think that is the only problem any JS developer faces while starting CP. In fact, this is the only reason I wrote this blog!

There are 2 possibilities: One, if you choose JS Node as your coding language submission. In that case here is what you’re going to do:

    Syntax for JavaScript Node
```
process.stdin.resume();
process.stdin.setEncoding(“utf-8”);
var stdin_input = “”;

process.stdin.on(“data”, function (input) {
 stdin_input += input; // Reading input from STDIN
});

process.stdin.on(“end”, function () {
 main(stdin_input);
});
```

This code right here, is how you’re going to take input. At the end, you might find this line: main(stdin_input);

That will be your function running for the submission. So what you need to do after this is:

function main(input) {
// your code here
}

Remember, the input variable is one test case input for you. Every input will be taken in as a seperate String. You will have to convert these inputs to numbers or whatever you want using parseInt() and other such functions.

That’s it. You just don’t have to bother about anything else here. Just input the “process” lines above in your CP code and you’re good to go. Of course, you’ll have to provide your own logic for it to work too! :-P

For the output, here is the “simple” line:

process.stdout.write("Hi, " + input + ".\n");

2. Syntax for JavaScript Rhino

This was one language selection for me which was only 50% similar at the first glance since Rhino was only some animal for me at that time. However, when I found out the input procedure in this one, this came up as a love child between JavaScript and Java. Here’s the input code:

```
importPackage(java.io);
importPackage(java.lang);
importPackage(java.math);
importPackage(java.util);

var sc = new Scanner(System['in']);     // Reading input from STDIN

var my_name = sc.nextLine();

Yup, when you run your program, as you might have probably guessed, you’ll use my_name as the argument since that is the acual input.

function main(my_name){
//your code here
}
```

Don’t forget to run your function or use IIFE in your code since this code doesn’t explicitly declare the main function to run. You could use any of the function name for any sub-language choice by the way.

Here, the output is exactly same as Java:

> System.out.println("Some output");

Yes, it might look that this is quite different from the usual JavaScript that you’ve been practicing, but after writing these starting lines of code, what you’ll be really doing is only your own code and nothing else. All in all, I feel that if your main language is JavaScript and you’re doing CP for fun and improving your logic building, you should go for it!

Hope this article helped you. If you have any suggestions or anything to say to me, here’s a list of ways to reach me out:

Twitter: @listenMrUtkarsh

LinkedIn: Utkarsh Singh

Github: utkarshsingh99
