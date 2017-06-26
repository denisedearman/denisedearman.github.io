---
layout: post
title:  "My CLI Gem - "Wiser Wine""
date:   2017-06-26 14:20:21 +0000
---


Yesterday I was able to complete my first final draft of my CLI gem project and published it to RubyGems!


To install my gem now all you have to do is run: gem install wiser-wine


# What my gem does
My gem scrapes Wikipedia and provides users with a list of wine grape varieties. The user can then select one of these grape types to find out the grape's color, common tasting descriptors, and notable wine regions (if availible).


# How I built it

I built my app using an outside-in approach; first I built the CLI and then I moved onto my objects. When thinking about commiting and building out my app I tried to take the tiniest steps possible, test, commit, and then move on. 

Ultimately I decided to use two classes: the CLI class and a grape varieties class. The two methods that I built to scrape data are included in the grape varieties class. If I decide to add more features or the scraping I might think about splitting this code out into a separate scraping class.

# Problems I ran into
Most of the problems that I came across were due to scraping. Originally I wanted my app to list wine regions and have the user learn more about these regions but I found out that the website that I had chosen had strict rules about using their information so I had to change my idea. Finding a well-formatted website that would be able to be scraped from was a little bit difficult. I looked through many wikipedia pages to try to find a good scraping page candidate.

Finally I settled on the wine tasting wikipedia page. This page included the list of grape varieties with links to their separate pages and tasting descriptors. These individual grape pages seemed to be somewhat consistently formatted, but some of them were much more filled in than others. Because of this I decided to use some of the most common details (the color and notable regions) and have my scraper only fill in information that was availible.

Ideally all information would be complete for each grape, but I decided that since each grape on my list at least had the tasting descriptions I was okay not having color and regions for each grape.

# Conclusion

I am very excited to have finished this project and have my very first gem published! In the future I would like to add testing and refactor my code for the gem. But for now....

![](https://media.giphy.com/media/YJ5OlVLZ2QNl6/giphy.gif)



