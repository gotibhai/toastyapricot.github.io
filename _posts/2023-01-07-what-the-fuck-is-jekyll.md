---
layout: post
title:  "What the fuck is Jekyll?"
date:   2023-01-07 13:45:00 +0100
categories: technology
---


This seems like an appropriate start to the blog -- To try and understand **what the fuck is Jekyll**.

Couple years ago, [Vibhanshu](https://www.linkedin.com/in/vbmach/) guided me on starting a blog - "Spin up a jekyll site and host it using the native integration with Github Pages" - It just works. 

Since I couldn't justify the $25 plan on Ghost - I decided to give this a shot. It took me ~2 hours to getup and running na dhave this first blog out with fairly low effort - Yes, It's not my dream blog but hey; action > thought

So how does this thing work anyway? What the fuck is jekyll? 

--> a free and open source static site generator
--> Jekyll generates all the content at once, instead of waiting for people to visit your website's pages.
--> available through [RubyGems](https://guides.rubygems.org/rubygems-basics/)
    * Basically packed Ruby Code - can be understood as plugins 

Jekyll Pages define a segment on top called the front matter something like this:

{% highlight yaml %}
---
layout: post
title:  "What the fuck is Jekyll?"
date:   2023-01-07 13:45:00 +0100
categories: technology
---
{% endhighlight %}

[Liquid](https://shopify.github.io/liquid/basics/introduction/) Adds some more excitment to Markdown essentially

### How is this parsed? 
Explained in more detail [here](https://jekyllrb.com/tutorials/orderofinterpretation/)

1. Jekyll will populate all site variables (site / page / post) (What does this mean exactly?)   
2. Jekyll will analyse all pages with front matter and process any liquid formatting in these pages.   
    - This is where the code gets parsed from highlight 
    blocks    
    - This is where '{ { site.time } }' will get converted.   
3. Markdown gets processed.
4. Jekyll pushes content to the layouts specified by the front matter.
5. Jekyll writes the generated content into files in the directory structure in _site. Hides the folders which are prefixed with `_` in the output.


### Collections are cooool - they say
1. Collections help with including structured data in your website—by splitting the data from its presentation, they make the task easier and less error-prone. You can reference the data using liquid and Jekyll will serve it in the `_site` folder.

{% highlight liquid %}

{ % for friend in site.friends % }
--> Do something cool with your friend's data here
{ % endfor % }

{% endhighlight %}

### Some More Learnings --

* A static site generator (SSG) lets you build a fully static website using template files or components. SSG generates HTML pages during a build process from a given content source. In most cases, static site generators accept markdown-formatted text files, although some (such as Gatsby) extend support for other sources. Main benefits include: Security, Scale and Performance

![SSG workflow]( {{ site.baseurl | append: "/assets/ssg.png" }} )








