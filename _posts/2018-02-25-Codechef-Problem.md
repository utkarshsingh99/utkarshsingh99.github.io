---
layout: post
title:  "Codechef- 1 Jewels and Stones"
date:   2018-02-25 00:40:00 -0600
categories: none
---

This is the first time I'm practising CP simultaneously while blogging.  
Don't know why I'm nervous.  
So the first problem, [Jewels and Stones](https://www.codechef.com/problems/STONES).  
It's a short problem, one thing I'll need while starting blogging while coding.

    So basically the problem statement is that there are two strings.  
    J & S, and I have to find how many characters of S occur in J.
    Easy to start with. Let's begin  

Now, to find each character, I could either use two nested loops, as in simple brute force,  
Or convert the array into their integer ASCII and sort them, thus making a possibility for binary search.  
Since the constraints are only 100, I don't think I need to do the latter method. So let's just try brute force.  
Sample test cases passed.   
Although I do have a doubt in putting the datatype of the counting variable as only int, I think it should still be fine  
since the maximum the count can go is only uptill 100, since that's the string limit of S.

There we go, the result's out, it's a correct answer!  
Now I feel too embarassed to be putting such an easy question as the first one on my blog, Damn!  
It's fine though since the blog is like a diary only for me and not an application for a job.  
Here's my main C code.

>char s[1000],j[1000];  
int count=0;  
scanf("%s %s",j,s);  
for(int i=0;i<strlen(s);i++)  
{  
  for(int k=0;k<strlen(j);k++)  
  {  
    if(s[i]==j[k])  
    {  
      count++;  
      break;  
    }  
  }  
}  
printf("%d\n",count); 
