---
layout: post
title:  "Presenting RoDI"
date:   2015-12-14 00:00:00
categories: [General]
---

RoDI is in its escence and Arduino-based board with a WiFi module, motors, sensors and a clever firmware on it.

![RoDI]({{ site.url }}/assets/rodi-v11.jpg)

Let's break it into its main parts

### Hardware

The brains of RoDI is an ATMEGA328p 8 bits microcontroller (the same used on the Arduino UNO), connected to an ESP8266 WiFi module from Espressif. The other components include

* Two 360 degrees micro servo motors
* Up to three Ultrasonic sensors (HC-SR04)
* Two infrarred sensors for line following (QRD1114)
* An user LED
* A WS2812b RGB smart led
* An Inertial Measurement Unit, including an accelerometer and a gyroscope (MPU6050)
* A light sensor (LDR)
* An integrated battery charger for a LiIon cell

All of these are designed into a custom PCB

![RoDI PCB]({{ site.url }}/assets/rodi_pcb.jpg)

### Firmware

Since the brains of RoDI is a custom Arduino, it can simply be programmed writing an Arduino sketch using the Arduino IDE. The default firmware we use is called [rodi-web](https://github.com/tchx84/rodi-web).

RoDI-web is a web-service interface for RoDI. It allows programmers to control RoDI by simply using HTTP requests, ie., from a web browser, a bash script, and basically any programming language.

### Software

Thanks to the implemented firmware, you can use almost any language to control RoDI (provided that you use the rodi-web firmware).

The default programming IDE for RoDI is [turlteblocksjs](https://turtle.sugarlabs.org/) developed by Walter Bender.

From the Turtle Blocks Javascript github page:

> Turtle Blocks Javascript is an activity with a Logo-inspired graphical "turtle" that draws colorful art based on snap-together visual programming elements. Its "low floor" provides an easy entry point for beginners. It also has "high ceiling" programming, graphics, mathematics, and Computer Science features which will challenge the more adventurous student.

We've developed a plugin for RoDI, which let us control RoDI using this great IDE.

![RoDI plugin blocks]({{ site.url }}/assets/turtleblocksjs_start_guide_8.png)

Other amazing people have already contributed with great libraries for controlling RoDI in Python, Smalltalk and even created an Android app for teleoperating RoDI.

