---
title: First Post 
date: 2024-05-15 21:29:00 -7000
categories: [ frustration, complication ]
tags: [agro, fun ]
layout: post
---

# Time  

There just isn't enough time. Between work, crypto, and intelectual exploration I just can't find the time. I'm working around the clock. 

Ahh fuck it. Who cares right? 

Anyway I've spent a ton of time working on terraform. It's a very cool tool but I'm struggling to see the usefulness for one person. 

I've tried time and time again to use workflows to manage the day to day but at the end of the day, since it's just me it just doesn't make sense. 

I'm not going to give up with this though. 

What I'm strugging with now is coming up with a structure that will work with Github Actions. 

The problem is that the best practices suggest the following structure: 

account_1
    |_ zone_a 
          |_ dns 
          |_ page rules 


As for the structure this is great however GH Actions doesn't support this natively. Or perhaps I should say more correctly the GH Actions YAML that Hasicorp created doesn't support this. 

## Here is the dilema: 

- If this is structured zone by zone you only need to run terrafrom on the zone that changed by the push request. 
- GH Actions needs to know which directory changed and then perform the correct terraform command based on the workflow 
- There are several extension that claim they can do this. However I think this is too complicated. 

## The Alternative 

- It seems that GH Action script wants everything in one folder
- This would mean having a repo for every zone! Eek! 
- Now that I think about it ; it would be cool to have a "defaults" zone and that would terraform the 
  defaults for all of the zones 
- Then I could have the more specific rules down the tree. It still just means I'll have yet another repo if I plan to use GH Actions. 

## For Now 

I'm not going to sweat this for now. I'd rather have a nice folder structure. Plus it's just me there is no reason to create branches and go through a CI/CD pipeline 
by myself. 

## Jekyll 

This has been fun! I labelled this my First Post because it basically is. I'll leave the original grafitti post up because "why not". One thing that is especially cool is that 
there is no spell check :). I'm sure I could install something for VIM but fuck it. 

I'm really liking use source control again. I've always been into keeping things in a way that is organized and can easily be compared against other versions. Git is many steps 
above SCCS and also RCS :). 

Peace!
