---
layout: post
title:  "My Sinatra Project"
date:   2017-07-22 14:31:18 +0000
---


Today I am finishing up my sinatra portfolio project, the Road Race Database. What follows is a recount of my processs, goals, and lesson learned in creating this project.


# Goals

My main goal for this project (beyond hitting all the requirements) was to write tests for my project to cover as much of the code as possible. A secondary, but more of a bonus goal, was to review bootstrap and style my project a little.

# Process
**1. Brainstorming:**
The first step was to come up with my project idea. In the midst of marathon training (week 2 of 18) and being the run nerd that I am I decided that a race reviewing (or reporting) app would be a fun idea for my project. 

**2. Planning**
The next step was planning out my app. In planning I first tried to think about what features I would want to incorporate in the app. Then with these ideas in mind I started to design my models. I decided on having 3 models: Users, Reports, and Races. In my design Users have many Reports, Races have many Reports, and Reports belong to Users and Races. Reports have many Races through Reports and Races have many Users through Reports.


**3. Coding**
Throughout the coding process I repeated two steps:
1. Writing Tests: Since my goal was to learn more about test writing and get into the Test Driven Development mode for my own code, I constantly would write my tests **first** before writing any code that would pass my test. Usually I would write tests for one page or functionality. After writing the tests for a functionality I often found that I had a very clear understanding of what I needed to do to get the tests to pass.
2. Getting Tests to Pass: The really fun part! After writing my tests I would write the code to get those tests to pass. I tried to go down the line and knock down one failure at a time.


**4. Styling**
I am still in the midst of styling my app with Bootstrap. I am finding that a little bit of styling goes a long way and am excited to get it all polished up!

# One of Many Lessons Learned
TDD does take time, especially when you are new to writing tests (like I was!). However, that time spent writing tests is well worth it. Writing tests that only checked one functionality at a time before coding helped me to break down the to-do coding items. 

I feel exponentially more confident in my test writing skills after writing my tests for my project. I also feel more capable of understanding why pre-written specs are failing that I did in the past. Understanding tests more accurately may be a huge time saver in the future!


# Side Notes - Running Log

I am now finishing up my second full week of marathon training. We are almost 15 weeks out from the NYC Marathon. The past few weeks I have been feeling *fatigued* from building up my base miles. My training went up from 30 miles per week at the end of June up to 38 this week (where at some points I had more than 40 miles on my legs). 

Having gotten injured in the process of training for my first marathon, I have approached this training cycle with a slightly different approach. Along with running **all** the miles I have been adding in specific injury prevention warmups and movement exercise routines. I know that my core is one of my weaknesses as far as strength so I have been adding in core work daily for 10 minute intervals. Hopefully these methods and keeping in tune with my pain will help me to sustain my health.

