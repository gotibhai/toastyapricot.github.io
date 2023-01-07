---
layout: post
title:  Skiller - Job Skills Aggregator
date:   2023-01-07 16:18:00 +0100
categories: projects
---

### The Idea: 
Imagine different stacks used by different companies - Find this information from their job advertisements.
Use the ChatGPT API to which can help you go from raw HTML of job page -> list of skills (aka stack).
Now you have a mapping from Company -> Position -> Skillset

1. Top k skills most required across all jobs
2. Try to get a correlation score between skillset and different companies
3. Given your current company - I can give you top 10 companies which have similar skills

#### How do we get the list of all positions? 

**Option 1: Straight to the point approach**
* Start with job boards and scrape them
    * [Angel Jobs](https://angel.co/jobs)
    * [Crunchbase API](https://data.crunchbase.com/docs/crunchbase-basic-using-api)
    * [Google Jobs](https://www.google.com/search?q=software+engineer+jobs&rlz=1C5GCEM_enNL1020NL1020&oq=linkedin+jobs+api&aqs=chrome..69i57j0i22i30l9.4094j0j1&sourceid=chrome&ie=UTF-8&ibp=htl;jobs&sa=X&ved=2ahUKEwjerayn7bX8AhX2xwIHHUH2DgwQutcGKAF6BAgYEBU&sxsrf=AJOqlzXM9p1sCidpfktSYWy_WRWwNmN1_A:1673108082338#fpstate=tldetail&htivrt=jobs&htidocid=GSDUoJaFRpEAAAAAAAAAAA%3D%3D)
    * indeed.com
    * ycombinator.com
    * Too many of them ><


**Option 2: Bottom Up approach**
* Get the list of top 2000 companies and top 200 startups
* Go on their jobs page -- Hard to search 
* Filter Software Engineering jobs and then scrape them


This seems like much more of a one time scripting analysis than a product --- Finding a reliable source of all constant streaming jobs is hard // 

**Ramblings:**

1. Why are jobs not centralized? 
2. Why is it so hard to scour the internet for all possible jobs?
3. Why such a gap between the potential employee and the company?

I still think that this could be valid project whereby given's one current company you can recommend to them potential jobs with a similar stack.
Maybe a future blogpost on reimagining job boards - but for now, closing this chapter.
















