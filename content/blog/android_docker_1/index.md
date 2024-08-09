---
title: "Docker on Android Part 1: Introduction"
date: 2023-12-27T12:18:04+05:30
draft: false
toc: true
---

This series of blogs serves as a walkthrough for building and running docker on
an Android device. I have done this on a [OnePlus 6](https://www.oneplus.in/6)
(codename _enchilada_), but the instructions for the most part remain the same
for any other Android device which is capable of running
[LineageOS](https://lineageos.org/) version 20 or higher.

## DISCLAIMER

- I am not responsible for bricked devices, dead SD cards, thermonuclear war, or
  you getting fired because the alarm app failed. 
- Please do some research if you have any concerns about the steps described in
  this blog series before performing them! 
- YOU are choosing to make these modifications, and if you point the finger at
  me for messing up your device, I will laugh at you.

## Why Docker on Android?

Android devices have a lot of wasted potential. These devices are quite powerful
with regards to processing power. Unfortunately, devices support Android updates
for only two years (unless you have a Google device), when in reality these
devices can run the latest version of Android without any issues. This is what
LineageOS tackles. But what if I told you that you can do a lot more with your
device than just run the latest version of [AOSP](https://source.android.com/)?

Yes, you heard that right! By unlocking the bootloader of your Android phone and
rooting the phone, you gain a lot of power over the way your phone works. **Be
careful, since with great power comes great responsibility! If you have not read
the disclaimer at the top of this blog, please do so.** In particular, I will
demonstrate how you can use docker to turn your Android phone into a Linux box
(not really, but almost!).

Read on to find out how!