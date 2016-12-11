---
layout: post
title: Adding my thoughts to the package installation discussion
date: 2009-07-19 23:00:01.000000000 +01:00
collection: posts
category: Tech
---

<div class="wp-caption alignright" id="attachment_305" style="width: 310px">[![Installing programs in linux](http://alimckinlay.110mb.com/wp-content/uploads/2009/07/Screenshot-300x187.png "Package installations")](http://alimckinlay.110mb.com/wp-content/uploads/2009/07/Screenshot.png)Installing programs in linux

</div>I mulled over for a long while about whether or not to publicise my feelings about Package Installation. The reason I did this, is I normally don’t just blog about something that everyone is blogging about. (There are a few ones that I do, but only when I am excited about something, or really really wanna say something.) So, I came to the decision that I would, I’m  still not quite sure why.

Ok, so it seems to me that this discussion has been underground for a long long time, and was just grave robbed when [this was posted](http://www.freesoftwaremagazine.com/columns/2009_software_installation_linux_broken_and_path_fixing_it) to the FSM website. And now, suddenly everyone is talking about it.

For those of you who are 1. too lazy to read the post, or 2. not able to read the post, I will tell you about the basics of the discussion.

Basically, [Tony Mobily](http://www.freesoftwaremagazine.com/user/2) wrote this article complaining about how he thinks that software installation is broken in linux, and how we should have a unified system between all the distros, and it should be simpler, with a way to install programs similar to Mac, where you can just copy 1 file between computers, and you have installed it.

Now, obviously he talks about it in a lot more detail than that, but that is the basics of it, go over the jump to see what I think.

Just very quickly – here are his ideas of what is wrong with package management and installation

> - Users need to have root access in order to install a piece of software; no per-user installation is allowed
> - It’s very tricky to install several versions of the same piece of software. Just think of the poor graphic designer who needs to install several versions of Opera and Firefox;
> - Users are stuck with the piece of software installed system-wide;
> - The software needs to be downloaded from the official repositories. Well, it doesn’t *need* to, but an average user wants to stay well away from unofficial repositories for technical reasons;
> - In some cases (especially when the user adds repositories or installs packages directly), the dependency-checking mechanism often *fails* and users end up with *circular dependencies*. They are nasty;
> - A piece of software is bound to a specific distribution, and — what’s worse — to a specific version of that distribution too. It’s not trivial to install Openoffice 3.1 on Ubuntu 8.10. You can argue that you can install the bunch of .deb packages from OpenOffice’s web site. Tell that to your grandmother or your average inexperienced computer user.
> - It’s not trivial to “give” a program to a friend. To the end user, giving a program to a friend should be as simple as dragging an icon onto a memory stick; instead, files are scattered all over the system.

I agree with him on some parts, but disagree on a lot of it. Basically, I don’t think I like the idea of all distros using the same package management system. One of the main things about Linux is choice. I can choose to use a specific WM, a specific web browser, a specific text editor, etc etc. But if this happens, I will have no choice what package management system I use. And what happens if they don’t choose apt? Which I prefer so much more than yum. But then, on the other side, there are plenty of people who swear by yum.

If you then say “Ok, well, how about we do the idea of having a stock set of dependencies, and libraries, and any other libraries used will be distributed with the app itself.” I don’t think this solves any of the problems. They problem is that when packaging a linux app, you need a .deb, .rpm, and then ones for specific distros. I suppose, if you have a stock set of dependencies for all linux distros, then how do we deal with older distros?

Does Ubuntu 7.04, Ubuntu 9.10, Fedora 9 and Fedora 11 all have the same dependencies? How on earth do the distribution developers keep that up to date? At any one time, does Ubuntu not have something like 4 or 5 versions it is keeping up to date at one time? And they have to make sure that all of these repos have the exact same dependencies? If yes…ok, but I don’t see how they can do that AND improve at the same time. However…if no, then the whole plan of stock dependencies and libraries falls down. Otherwise, have fun running your new software on your old operating system.

I agree with his idea that they should be installed in 1 directory. /bin, I would think. But that specific directory isn’t for me to say. And I think this should be publicised. It took me ages to find where applications were installed.

However…I do think that needing root should stay. Give me an example where you would need to have a program installed without having admin? If you do not have admin, then the admin will not want you to install programs. If you NEED a program…then the admin will install it.

As for several versions of a program. 1st of all…that kills dependencies and libraries. Euch, I don’t want to deal with that. 2nd, who on earth needs 2 versions of a program? A visual designer needing 2 versions of opera??? How?? Nah, I cannot think of any reason you would need 2 versions of 1 program.

I have talked about most of what he says, and all of the other ideas he has for fixing this, confuses things more than they are confusion at the time. If you think that it is confusing just now, I think all of his “Changes” to do with linking directories and libraries and stuff makes it so much more confusion.

I agree that we need to simplify it partially, and that they should be installed in 1 directory. But I don’t have any answers. I just don’t agree with the rest of what he says. These are just my thoughts…and I don’t know who agrees with me, but for once, I will shove my thoughts on a popular topic into the blogosphere to annoy people.
