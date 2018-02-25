---
layout: post
title:  "Codechef on 25th Feb"
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

```
char s[1000],j[1000];
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
```
Next Problem! [GCD2](https://www.codechef.com/problems/GCD2)  
This one is a constraints problem. Here's the problem statement.   
     There will be a smaller integer in the range of 0 to 400000, and there will be a bigger integer
     in the range of 0 to 10^250. I have to find out the GCD of these numbers.

The algo for GCD is also given:
```
int gcd(int a, int b)
{
	if (b==0)
		return a;
	else
		return gcd(b,a%b);
}
```
Now obviously I can't take the bigger integer input in an int datatype since I'm working in C.  
So I'll take the input in a character array, then extract the last digits of the array into an integer.  
This integer will just be one digit more than the smaller integer.  
Now, when extracted, the bigger int is a, and smaller one is b.   
Putting this into the recursive function will give the answer.  
The good thing about this is the first number will always be smaller, so I don't have to worry about which number to put in the character array.  
Now instead of keeping the number just one digit bigger than the smaller one, how about I keep it six digit fixed?  
I won't have to count the digits of the smaller one which will require anothe loop.  
So the code has been written. Now there was an interesting glitch I encountered; don't really know if it should be called one though.  
To convert longer numbers into shorter ones, this was the loop I initially used.  
```
for(int i=strlen(s)-1;i>=strlen(s)-7;i--)
{
  a=a+pow(10,j)*((int)s[i]-48);
  j++;
//  printf("%d\n",((int)s[i])-48);
}
```

So in this one, whenever I wrote a digit smaller than string length 7, it would automatically skip the loop.  
My guess is that it adds the strlen to the value if it goes negative.  
So I replaced it with this code.  
```
if(strlen(s)<9)
  num=0;
else
  num=strlen(s)-7;
for(int i=strlen(s)-1;i>=num;i--)
{
  a=a+pow(10,j)*((int)s[i]-48);
  j++;
//  printf("%d\n",((int)s[i])-48);
}
```

Although this gives the correct answer for sample test cases, when I submitted the solution, it shows WA.  
I hope my logic is correct. If I have to ultimately divide the bigger number by the smaller number and take its modulus, then shouldn't  
it be okay if I take the bigger number only slightly bigger than the smaller number by just using its last digits?  
Wait! What if I take "100000000000000"? The last 7 digits are 0. Thus, any number would show itself as the GCD even if it might not be!  
Yeah, so this method cannot be taken for all solutions. So I looked up Euclidean Algo for large numbers, and what they do is  
take modulo of the bigger number, all the while keeping bigger number in a character array and extracting it into another integer.  
Runtime Error! I think it could be because of division by 0, that is, if the smaller number is 0.  

```
if(b==0)
{
  printf("0\n");
  break;
}
```

So I added this code, and I'm back to wrong answer. :/  
Now there could be that the testcases don't follow the rule of smaller number first and bigger number second. That's unlikely though.  
Codechef doesn't make such mistakes, its not SPOJ! :P  
Woahh! There, GCD of 0 and a number is the number itself!
And there's another mistake that I did. In the b==0 condition, **continue** will be used instead of **break**.  
Now I must admit that the former mistake was revealed to me after I looked at the code of one of the accepted solutions.  
Finally, Correct Answer! This was a great problem, although I wish I hadn;t looked at the accepted code solutions.
