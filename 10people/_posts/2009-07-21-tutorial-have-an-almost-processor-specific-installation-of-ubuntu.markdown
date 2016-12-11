---
layout: post
title: 'Tutorial: Have an almost processor specific installation of Ubuntu - 100th
  post'
date: 2009-07-21 21:56:24.000000000 +01:00
collection: posts
category: Tech
---

Have you ever wanted the power that you gain from compiling everything from source? But do you run Ubuntu rather than something such as Gentoo? Do you not like compiling, and would like an easy way to compile your installation? Then look no further than apt-build

![compiling](http://imgs.xkcd.com/comics/compiling.png "Compiling")

**Note: this guide is specific to Ubuntu.It should work on most other deb based systems, and may work on other systems using a different packaging system, but some things may be different.**

**  
**

**Also note that this will increase the total install space of your operating system quite a bit, as source takes up much more space than binaries. My install is about 8 Gig now.**

Now, the installation of apt-build is a wee bit more difficult than just “sudo apt-get install apt-build”. Although that will install apt-build, you will have to do a few other things as well.

Ok, so first of all, install using “sudo apt-get install apt-build”. During the installation, it will ask you to choose the strength of compiling that you use. Basically, you can choose how specific it compiles. If you have a very low-power processor and don’t want to wait for hours, use light or medium. If you have a bog-standard processor, use medium, and if you have a really nice processor (or you don’t mind how long it takes) then use strong.

Then it will ask you to choose your processor. It is important to note that there are very few processors that are listed here just now, so if yours isn’t listed, don’t worry. Choose one that is very similar to your processor, and we will make it more specific later on. For example, I am running an AMD phenom, but it doesn’t currently have that in the list. So I chose Opteron.

If your installer doesn’t ask you what you want to use, then throw this command at it “sudo dpkg-reconfigure apt-build”.

Ok, good, now you have installed it. Next, you will want to edit the file “/etc/apt/apt-build.conf” (For example type “gksu gedit /etc/apt/apt-build.conf” for a gui text editor, or “sudo nano /etc/apt/apt-build.conf” for a console text editor). Your file should look something like this

> build-dir = /var/cache/apt-build/build  
>  repository-dir = /var/cache/apt-build/repository  
>  Olevel = -O3  
>  mtune = -mtune=opteron  
>  options = ” ”  
>  make_options = ” “

The main option you will want to edit is the ‘make_options = ” “‘ line. This should look like ‘make_options = ” -j5″‘ replacing ‘5’ with the number of cores +1. For example, for single core it would be “-j2″ and for dual core, would be “-j3″ etc…

Ok…lovely. Now you are nearly ready to start compiling. If you were to issue a “sudo apt-build world” command at this point, you would get this.

> —–Rebuilding the world!——
>
> —-Building package list—–
>
> Please read README.Debian first.

This is because apt-build doesn’t have your package list. So, what you will need to do is issue these commands:

> sudo -i
>
> apt-build update  
>  dpkg –get-selections | awk ‘{if ($2 == “install”) print $1}’> /etc/apt/apt-build.list  
>  apt-build upgrade –force-yes –yes

**NOTE: I have had a note that sometimes the third command won’t copy properly. So, if you get an error, type it in rather than copying it. I’m not sure why this is, but just a warning. Note also that “–get-selections” doesnt come up correctly on my blog for some reason. It should have 2 “-” before get.  
**

These will update your repositories, pass the list of packages to apt-build and then make sure your system is up to date. NOW you are ready to start compiling. The 2 main commands you will want are

> sudo apt-build world           #This will reinstall your whole system, compiling everything from  source
>
> sudo apt-get install ***       #This will download the source for package *** and compile it

Now, please note that if you do a “sudo apt-build world” this WILL take a while, especially on such a bulky distro as Ubuntu. Also, compiling takes up more disk space than just installing the binaries. So, if you have a 10GB disk for everything…don’t do this. But then…we all have hundreds of gig now, don’t we. So its not a problem.

So, go out and have fun compiling. Btw, kudos to [Torikun1](http://rusher.webhop.org/wordpress/) for telling me about this on #linuxoutlaws on irc.freenode.net.

p.p.s This is my 100th post. Celebrate and be happy! I only just realised this, half an hour after posting it.
