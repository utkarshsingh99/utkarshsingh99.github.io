Okay, it's Vacation Time!
Now, I've already deleted the html file posts and converted them into md files. A heads up to [Kartikay Kumar](https://github.com/Kartikay26) for telling me this, saved a lot of time.
I've got quite a lot of things in mind that I've got to do.
So let me just list out the things I want to be doing today.
> 1. Format the first post properly
> 2. Choose a theme for a blog. Architect is too novice. :/
> 3. Research about GSoC organisations.
> 4. Competitive Coding. At least 2 problems of Easy from Codechef.

Okay, now let's take a moment to pray that I may finish all of these tasks today.

So let's begin.
The use of '>' shifts the text into a seperate division. I want to put all of the commands into such divisions.
Yeah, that's working!
Now there's another problem I want rectified. I want to change the Description below my Name on the Home Page.
Although I did change it in the site/about/index.html file, it's still not showing. I think I'll have to have a look at the YAML Front Matter in the repository.
Tough job!

Now I know when I change the description, I changed it in the meta name="description" tag. So I think I need to find something that says something.description,
most probably site.description or site.about.description.  
Well, I'm lazy as hell and I'm just gonna Google how to do this instead of studying the code.
Okay, so I just have to change the config.yml file.
Seems easy enough.
Now there seems to be a problem. My changes aren't reflecting in the main website.
Let me first delete all the unwanted files in my folder.
Hmm, this is an interesting problem, or to be honest, a very very Bad one. The content is not getting updated on the site.
So I tried looking at the site in the offline view. Turns out, my ruby installation is faulty.
Bundler is not working.
I tried a lot of stuff, googled a lot. Now I'm turning back to primitive ways. I'm uninstalling and reinstalling the ruby environment on my PC.
Still bundler doesn't work.
But I just checked my mail from Github. It says that there's a page build error in line 12 of my config.yml.
I corrected certain errors. The home page works fine, but the data of my posts is still not getting updated.

Phew, I reverted all the description changes in all the index.html and made the correct change in config.yml.
