---
title: "Arduino Based FM-Radio"
excerpt_separator: "<!--more-->"
categories:
  - Projects
tags:
  - radio

header:
  image: /assets/images/schematic.png
  teaser: /assets/images/schematic.png
---

{% include video id="gF0skXeZqDc" provider="youtube" %}

## What is this Project?

In Novemeber of 2020, I was tasked by my ex-Engineering teacher, Bruce Mazer, to develop some kind of electrical device using arduino and the [Arduino IDE](https://www.arduino.cc). Students came up with their own ideas. My friend Shayan actually designed a solar powered iPhone charger. While there were other students who had more basic ideas, I really wanted to build something that had purpose. During the development of my radio, most of my classmates were completely fed up and irrated by the static that would blare out of my speakers. Below you can find the parts list. 

## Parts List

* Arduino UNO
* 2x 10K Variable Resistors
* TEA5767 FM Radio Module
* Standard Breadboard
* USB Cable
* 3.5mm Headphone Cable Extension
* LM386 Sound Amplifier
* 2x 3W Speakers
* Alligator Wires
* General Wires
* Light Emitting Diode
* LCD Display for Arduino
* PIR Sensor
* 100uF Capacitor
* Antenna

## Unexpected Features

During development, I implemented features that I intially did not plan on. Namely, the IR sensor and remote controls was not my initial design. I first relied on a dial/variable resistor based resistor to change radio stations. The drawback of these devices was apparent, they were way too imprecise. Even the smallest turn in the dial would change the station so much so that it was hard to really stabilize at a radio station. To combat this, I implemented an IR sensor and remote control based channel switching. Not only did this solution look more elegant and professional, it was actually not that big of a hassle to implement after searching through some documentation. I also looked on Amazon for a cheap wireless transmitter that I could connect to my iPhone. Any sounds and music I played from my phone would then be transmitted through a certain frequency I set it to transmit at. I could then tune my radio to that station and listen to music broadcasted from my phone just as I would as if it were a bluetooth compatible device.

## Static Issues and Future Improvements

One of the biggest issues I had to deal with in this project was static. Initially, I believed the static was caused by poor antennas and lack of ability of the TEA5767 module to pick up signals. However, I was able to hook the radio up to an external soundsystem. This resulted in crispy clear sound quality and I was able to capture literally every channel in the spectrum. After doing some investigative work and research, I concluded that the LM386 Sound Amplifier was the culprit to blame. I would definitely **NOT recommend someone to use that module. There are other versions of this device that work far better than the one I received.

## 2 Years Later

I really love this project and I found myself coming back to it every few months just to admire its beauty. Unfortunately, the breadboard recently decided to collapse on itself and all its connections have come out the backside. This is was happens when you implement temporary prototyping solutions such as breadboard into a finished product. If I have time in the future, I'll fire this up again and rebuild it using a new amplifier and actual materials and soldering equipment.

## Want to Take a Peek/Learn More?

Visit the [FM-Radio Github Repository](https://github.com/faizaanqureshi/FM-Radio) for the code and schematic diagram.

