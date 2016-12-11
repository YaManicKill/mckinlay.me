---
layout: post
title: Ubuntu 10.10 Maverick Meerkat Review
date: 2010-10-10 12:12:32.000000000 +01:00
collection: posts
category: Tech
---

[![](http://www.10people.co.uk/wp-content/uploads/2010/10/warty-final-ubuntu.jpg "warty-final-ubuntu")](http://www.10people.co.uk/wp-content/uploads/2010/10/warty-final-ubuntu.jpg)As many of you will know, version 10.10 of Ubuntu has just been released. It seems to have become a tradition for me to write a review of every Ubuntu release, and post it just after it has been released. So, this is where I try and quickly write it just incase I miss the deadline. Plus, I would like some sleep tonight ![:-)](http://www.10people.co.uk/wp-includes/images/smilies/icon_smile.gif) On with the review:

**Improved Installer**  
 The installer (also known as ubiquity) has had a major overhaul in this version. You are presented with very few options, and also the option to install non-free codecs. Both of these things are good and bad. Having very few options is a great thing for new people, but leaves many of the options that people like me may want to use out of the equation. Many of these options are available in advanced settings (such as advanced partitioning) however, there is 1 glaring omission. Where to install the bootloader. To most people, this really doesnt matter, but let me give you an example. You are installing it on a removable harddrive, so you can have an untouched OS on your internal drive, and you can just unplug to boot into the other. If it automatically installs the bootloader onto the external harddrive, when you take out the harddrive you can’t boot your other OS.

I am not complaining about the lack of options, just that I wish we have them in an advanced screen. That would be nice ![:-)](http://www.10people.co.uk/wp-includes/images/smilies/icon_smile.gif)

As for the non-free codecs, all in all, I think it is a good thing, as most people who would like that option have mp3s, use flash for things on the web, and would like graphics drivers that actually allow them to use their graphics cards in a meaningful way (wobbly windows, anyone?). There really is no disadvantage, imho. It clearly states that they are not open, and that they should only be used if they make your experience better. This is totally in line with how I view proprietary software. If it is better, I may use it. If there is open software that does the same as what I need it to, I’m so using that instead.

The installer also includes many more of the application “slides” I guess you could call them. The slides they show you as it is installing to let you know about some of the great applications you get with Ubuntu.

**Shotwell**

I’ll be honest with you…I hated f-spot. So it gives me great pleasure to finally let you know that Shotwell has replaced f-spot as the default photo manager. Shotwell has a much cleaner interface, has only a few basic editing tools (which are all most people actually need), really quick tag editing (for easily finding that photo that you can’t remember whenyou took it, but you know what is in it), facebook, flickr and picasa integration, and to top it all off, it doesn’t duplicate, delete or corrupt your photos (like f-spot did several times to my fiancee’s photos). It isn’t perfect, it could probably improve its effects and the slideshow has no configurability, but in all I think it is a great photo-manager and it can only get better.

**[![](http://www.10people.co.uk/wp-content/uploads/2010/10/Screenshot.png "Screenshot")](http://www.10people.co.uk/wp-content/uploads/2010/10/Screenshot.png)Software Centre**

When I saw the Software Centre first, I thought it was going to be very much like a lot of rubbish installers I’ve seen before (I’m looking at you Kpackagekit), and it didn’t really do anything great, infact I preferred to use Synaptic. However, it has grown into a really great product.

I don’t often say that Apple do things well, but one thing they did great was the App Store. I think that the Software Centre is as good as the App Store, and even better because it is open source ![:-)](http://www.10people.co.uk/wp-includes/images/smilies/icon_smile.gif)

The software Centre has great featured apps sections, support for ppas, a large description for apps and also screenshots of many of them. It hides all of the useless libraries that noone wants to see (and if you want to remove them 1 by one, use apt) and it makes it really easy to search through the apps and find what you want. The sections of apps really work well and I think this would be a great thing for people who are new to linux (or computers in general). People are getting used to “App Store” type things, and want to be able to install things without going to websites. This is something linux has done great for ages, and Ubuntu has just made it simple.

**[![](http://www.10people.co.uk/wp-content/uploads/2010/10/Ubuntu-Ubunity-Screenshot-3.png "Ubuntu-Ubunity-Screenshot-3")](http://www.10people.co.uk/wp-content/uploads/2010/10/Ubuntu-Ubunity-Screenshot-3.png)Unity**

Tried the new UNE with unity? No? Do it. It is very different. You can see the screenshot at the side. It turns a netbook into what it should be: a simple computer that browses the internet, with a few other apps that you can use at the side.

A netbook was never designed to have a normal desktop interface, and I’ve been wondering for ages what a good interface for a netbook would look like. I’ve tried things like jolicloud, meego, android and the origional UNR interface, and none of them did it for me. They all seemed not right for a netbook. This is a step in the right direction. It is getting closer  and closer to feeling right. It integrates the menus, window decorations and panel into 1 top panel, saving 2 blocks of precious vertical pixels. It also has a nice sidepane (this is what I’m going to call it) where it has a few default apps, and you can add or remove ones into it. If you press the ubuntu logo at the top left, it brings up a search pane which allows you to search for files and webpages really simply.

The whole thing is built on mutter, which allows cool 3d effects that are very gnome-shell esque. However, this  also makes it difficult to use with compiz. But then, you can’t eat all your cake can you.

I do have some contentions with it, for example it makes it difficult to run apps that aren’t in the sidepane (as “alt-f2″ doesn’t work there). It also breaks my key combination for gnome-do. Pressing alt allows you to choose one of the apps on the side pane with a number, however I like using alt-space for gnome-do, but you can’t change which key unity uses for this weird number-pressing ability. Why it was built in such a way to break key combinations, I have no idea. You can’t tell me that noone on the team uses gnome-do. Gnome-do is great.

**Other good things**

The useful notification controls added in Lucid (for audio, comminication etc) have gotten even better. Allowing you to control apps such as rhythmbox and gwibber. I hope, however that this is open in such a way that allows apps to harness this ability to put controls into it for their apps.

The new version of Ubuntu one allows streaming your Ubuntu One music to your android or iphone device. That’s useful, but I don’t buy any music in there…so I’ll have to wait for a while to use that.

**Bad things**

Still no decent video editor. Pitivi is terrible. It works rubbish, looks like it has been dragged through a hedge backwards, and is so not intuitive. I would like a decent video editor please. Openshot possibly?

No huge innovations in the default Desktop version. Everything seems to be incremental updates, which is normally fine, but the release after an LTS is meant to be the most experimental, the one with all the broken software in it that will be fixed by the next LTS, but canonical would never recommend this version. Everything seems kinda boring and stable, and just a wee bit better than the last version. Apart from Unity that is.

What is up with that default background??? Seriously? As I saw someone somewhere on the internet say: “It looks like Chuck Norris sneezed on my screen, and I can’t wipe it off.” It looks like they took the 10.04 background and threw an orange at it. Seriously…get some decent backgrounds.

**Conclusion**

All in all, I think Ubuntu 10.10 is probably the best version of Ubuntu yet (well, thats always good) and is a few more steps on the way towards being better. Thats what I would say if I was a boring tech blogger who always likes to say that something isn’t quite there yet, and likes to use cliches. Well, I’m not.

Ubuntu has improved a lot over the last few years, but it really feels like there is nothing groundbreakingly great in this version. Yeah, sure a few apps are great, and the new UNE interface is amazing, but for the normal person who uses the Desktop version there isn’t much to stick his teeth into. Maybe this is part of the proble of a 6-monthly release cycle? Or maybe it is Canonical thinking that they can’t innovate too much because NORMAL people are starting to use Ubuntu, so it has to always be totally stable.

I’m not sure what the problem is, but hopefully 11.04 will give me some great new features to stick my teeth into.
