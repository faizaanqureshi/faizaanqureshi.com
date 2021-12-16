---
title: "Astroworld - A Travis Scott Jukebox Desktop Application"
excerpt_separator: "<!--more-->"
categories:
  - Projects
tags:
  - Travis Scott
  - Astroworld
  - Music
  - Games
  - Application
  - Desktop
  - Java
  - Processing

header:
  image: /assets/images/astroworld.png
  teaser: /assets/images/astroworld.png
---

## What is Astroworld?

Astroworld is a project I developed in my junior year of high school as the culminating assignment in my Intro to Computer Science class. It's named after Travis Scott's album, Astroworld, and the application grabs many thematic and stylistic elements from his work. It was developed in a Java IDE called [Processing](https://processing.org), it primary focuses on making life easier in developing visuals and graphics for applications while keeping the same Object Oriented approach as Java. 

## Minigame Screen

This is an example of a minigame I implemented into the application. The first picture shows the main game title screen and the second shows a character selector. The game is oddly similar to some dinosaur game you may recall playing when ill fate causes you to suffer from the lack of Wifi. There's really not much to the code here. It mostly involved an object having to dodge other objects, and if the primary object (the player) made contact with one of the other objects (the cactus) then the game would be over. The score is based on how long the player can play the game. A players' top score is then stored in an application file and thus remembered from that point on.

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/astro1.png" alt="" class="full">

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/astro2.png" alt="" class="full">

## Music Catalogue

The music catalogue screen was the main meat and potatoes of my project. It was a collection of all of Travis Scott's albums and some unreleased tunes in one package. On the left, the user can see a leaderboard of their most played songs. The application saves these values into a text program file and remembers them, adding a play everytime the use plays a specific song and running a simple sorting algorithm to sort by the most played in the data set. Cool stuff. I also included a player scrubber at the bottom to make it easier to move along parts of the song without having to go into the main player every time.

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/astro3.png" alt="" class="full">

## Player Screen

After selecting an album/collection, the user is greeted with a music player to the right and a list of songs to the left. The .wav file wavelengths are displayed on the player for aesthetic effect and a music scrubbing bar is provided. The user can pause a song simply by pressing the space bar.

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/astro4.png" alt="" class="full">

Wherever you are in the application, a small box to your top right tells you what song is currently being played.

## Challenges/Learning Outcomes

Overall, this was definitely one of the most gruelling, satisfying, and rewarding projects I've worked on. It was my first introduction to algorithms and file saving with real world implementation. I would work on this for hours and hours during my winter break to the point where even my teacher told me there was no point developing the code base any further. But for a brief period in Winter 2020, this project became my obsession. To this day, it represents me as a person and a coder. From recursion to classes to file storage, this project forced me to implement thoughtful solutions to problems and gave me an introduction to the world of software development.

## Want to Try/Learn More?

Visit the [Astroworld Github Repository for Windows](https://github.com/faizaanqureshi/Astroworld) or [Astroworld Github Repository for macOS](https://github.com/faizaanqureshi/Astroworld-macOS-) to download the application yourself and get a better peek at the source code. Be wary! The application is about 1GB in size because of all the songs contained in the application files.