---
layout: post
title:  "Formatting Markdown Files"
date:   2018-02-23 23:00:00 -0600
categories: none
---
So I'm exploring the md file commands for better presentation in posts.  

I'm using [this link](https://confluence.atlassian.com/bitbucketserver/markdown-syntax-guide-776639995.html) as a reference for this post.
###Enter a New Line
To enter a new line
> a__
> b

where _ is a space.  
For a new paragraph, press enter twice.  
###Now the Headings
> Headings
># This is an H1
>## This is an H2
>###### This is an H6

>This is also an H1
>==================

>This is also an H2
>------------------

>####Testing Heading Size

>###Lists

Unordered list

*  Item 1
*  Item 2
*  Item 3
    *  Item 3a
    *  Item 3b
    *  Item 3c

Ordered list

1.  Step 1
2.  Step 2
3.  Step 3
    1.  Step 3.1
    2.  Step 3.2
    3.  Step 3.3

Code blocks

    Indent every line of the block by at least 4 spaces.

    This is a normal paragraph:

        This is a code block.
        With multiple lines.

    Alternatively, you can use 3 backtick quote marks before and after the block, like this:

    ```
    This is a code block
    ```

    To add syntax highlighting to a code block, add the name of the language immediately
    after the backticks:

    ```javascript
    var oldUnload = window.onbeforeunload;
    window.onbeforeunload = function() {
        saveCoverage();
        if (oldUnload) {
            return oldUnload.apply(this, arguments);
        }
    };
    ```

Okay, here's something new.
###Adding images to md files.  
> ![Alt text](/path/to/image.jpg)

###Adding Tables
```
>| Day     | Meal    | Price |
>| --------|---------|-------|
>| Monday  | pasta   | $6    |
>| Tuesday | chicken | $8    |
```

And the result is,

| Day     | Meal    | Price |
| --------|---------|-------|
| Monday  | pasta   | $6    |
| Tuesday | chicken | $8    |
