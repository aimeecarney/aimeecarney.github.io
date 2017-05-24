---
layout: post
title:  My first CLI App
date:   2017-05-23 22:02:22 -0400
---


You guys. I did it.
 
I built a command line interface as my final project for the Object Oriented Ruby section in the Learn curriculum. Let me start by saying the CLI Data Gem Project wasn’t an easy feat. First it took some time for me to actually get the courage and start writing code from scratch, something I had never done before. And secondly, I ran into multiple problems with scraping which altered exactly what I wanted my initial application to do, so getting a continuous work flow going also took some time.
 
It was fairly easy for me to think of an idea for my project. My entire life I have always been trying to invent something (I wholly believe that I thought of the pay to park mobile app before it came out, but that’s a story for another time). I think of everyday interactions and what I would want to use. While starting this project I was in the process of looking for nearby weekend getaways for my fiancé and I to go visit during Memorial Day weekend; the caveat: the place had to allow us to bring our furry child-- I’m sure you can see where this is going. I decided to create an application to scrape sites for pet friendly hotels and lodging, in other words my “Pawlidays Inn” app (I’m a huge supporter of puns and dad jokes).
 
After watching the CLI Data Gem walkthrough about a dozen times, I figured it would be best to start by creating the skeleton of my code based on the walk through and other examples given as resources. I wrote down Avi’s steps from the walkthrough on how to build a CLI Gem:
 
1. Plan your gem, imagine your interface
2. Start with the project structure - google
3. Start with the entry point - the file run
4. Force that to build the CLI interface
5. Stub out the interface
6. Start making things real
7. Discover objects
8. Program
 
As I started to write my code I found this list to be a good reference to keep looking back at. It’s intimidating beginning on a blank slate, but looking at it by steps helps you not only keep organized, but gives you a sense of direction.
 
I knew I wanted three different classes so I could better organize my code, so I started with the following: a CLI Class, a Scraper Class and a Listing Class.
 
From there I created my environment so all my files and gems could be aware and access each other. 
 
Once the skeleton was in place I started to look at what websites I wanted to scrape, I initially wanted to scrape multiple sites such as AirBnb, Hotels.com, Bring Fido etc. However, since I wasn’t scraping a plain URL I ran into trouble with altering the URL to output the user’s input and the different filters selected to view pet friendly options. After much research and experimenting, I found a site with a simple URL I could easily manipulate depending on the user’s input.
 
From there it was a lot of binding.pry to test scrapings and to get exactly the right output. Then I had to make sure my objects and methods not only worked, but worked together. I surprised myself at how *"easy"* I was able to write the code from there (easy being a generous word, as it was a ton of trial and error and looking at other CLI gems). I continued to make edits and create more methods to simplify and organize my code better. This was the first time throughout this whole process where I actually felt like a developer, and let me tell you, it felt pretty damn good.  
 
After two weeks of huffing and puffing, it was finally working, I actually MADE something, something that I came up with in my head and something that I am extremely proud of. I know that it’s just a CLI gem and I’ve only just started, and I hope in a couple weeks, months, years, I will look back at this and laugh at how simple this assignment was. But for now I will pour myself a nice glass of whisky and bask in the feeling of completing my first application.  It is starting to look like my aspirations of inventing something isn’t too far out anymore. 
 
*Cue happy dance*

![Imgur](http://i.imgur.com/yCCN527.jpg)

