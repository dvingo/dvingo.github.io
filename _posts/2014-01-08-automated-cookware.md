---
layout: post
title: "Automated Cookware"
date: 2014-01-08 16:51:39 -0500
---
I like to cook very minimal meals and found myself eating the same things over and over: rice, beans, pasta, steamed vegetables. Pretty basic, but also healthy. Anyway, as a natural side effect of being a programmer, I thought abstractly about how all these things are prepared and realized they're roughly all the same:

* Measure dry ingredients
* Measure water

<br>
Then either:

* Boil the water
* Add ingredients

<br>
or

* Rinse ingredients in water
* Add ingredients and water together and then boil

<br>
Pretty much the same thing over and over again. Why not automate it?

The overall idea is to control the boiling with a hot plate on a timer via an arduino or raspberry pi
and dispense the ingredients via a predetermined number of rotations of one of these:
<br>
<img src="http://www.yankodesign.com/images/design_news/2009/10/27/smartspace.jpg" height="234" width="235" alt="food dispenser">

You'd also need a pump to control the water, and a couple of motors with multiple containers to rinse the ingredients and to mix them if needed.

You could then hookup a web server to it and control it remotely, for example, starting it when you leave work
 and have the ingredients of a meal waiting for you when you get home!

It would definitely be a lot of effort, but I imagine some industrial individuals could make a self contained
appliance that works for any water-plus-ingredients food.
