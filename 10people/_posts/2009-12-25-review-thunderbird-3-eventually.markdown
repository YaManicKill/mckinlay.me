---
layout: post
title: 'Review: Thunderbird 3...eventually'
date: 2009-12-25 18:27:27.000000000 +00:00
collection: posts
category: Tech
---

So, last week, after such a long time, thunderbird 3.0 was released. It is the first major release of thunderbird since, I believe, 2006. So, 3.0 is a very long awaited release.

Between 2 and 3, there were some political problems within mozilla, and eventually thunderbird split from mozilla, and mozilla messaging was created, which is now the entity that does thunderbird and a few other things. But, thats not what I’m here to talk about. I’m here to talk about thunderbird 3.0.

- Tabs[![](http://www.10people.co.uk/wp-content/uploads/2009/12/thunderbird-3.0.jpeg "thunderbird-3.0")](http://www.10people.co.uk/wp-content/uploads/2009/12/thunderbird-3.0.jpeg)

Ok, many people will talk about tabs being the biggest and most important change in thunderbird. And yeah, it is quite cool. It wasn’t what I origionally thought it would be, and I do believe they aren’t quite what I wanted them to be like.

It is something that you think should have been plugged into thunderbird years ago. And you would be correct. To be honest, tabs are something that really should be included in every single application. Your email client is absolutely no different. In my opinion there are still plenty of apps that do not have tabs that really really should. So, it is about time that your email client gets tabs.

Now you will notice that there are a bunch of tabs above my email list. Now this is great. If you right click on an email you can open it in a tab. Fantabydosie. Well, I would also like a way to open tabs in the email viewer bit. Where you normally view emails, have a number of them in tabs. That isn’t possible just now, but I would love it.

Also, notice that those 2 tabs I have up are not emails. They are “Bloglines” and “Google Wave”. Well, you can run any normal webpage in thunderbird. Go into thunderbird, go tools > error console, and then type this into the bar:

Components.classes['@mozilla.org/appshell/window-mediator;1'].getService(Components.interfaces.nsIWindowMediator). getMostRecentWindow(“mail:3pane”).document.getElementById(“tabmail”).openTab(“contentTab”, {contentPage: “https://wave.google.com/wave/?nouacheck”});

This will open Google wave in a tab. This is fantastic, because it means you can view your email and your google wave in the same thing, and still use a normal mail client. Absolutely amazing.

There is also an [addon](https://addons.mozilla.org/en-US/thunderbird/addon/55713) that makes it easier. But it is still in development. I tried using it and it works really well. What it really needs is an option to automatically open some tabs. Would make it perfect.

- Account adding[![](http://www.10people.co.uk/wp-content/uploads/2009/12/thunderbird-3.0-300x187.png "Thunderbird 3 Accounts")](http://www.10people.co.uk/wp-content/uploads/2009/12/thunderbird-3.0.png)

If you wanted to add an account in thunderbird 2, or in outlook, or some similar generic desktop email client, you would first of all have to find out what type of email server your email runs on, what protocol it uses to deliver your email, what the server urls are, what ports they use, then plug them all into your email client’s account settings along with your username and password and finally you can start checking your email. Well, not any longer. Well, not if you run Thunderbird 3.0.

When you run thunderbird 3 for the first time, you are met with this screen which asks you for your name (can be anything), your email address (pretty obvious, if you don’t know this then you shouldn’t have an email account), and your password (the same password you use to log into your webmail). Then, it scans your email address, possible mail servers and ports, and then tells you if it has worked. Then all you do is click “create account” and you are done. How much easie is that???

I tried this on a number of my email accounts. It worked great on my gmail, great on1 of my uni email accounts, but not so great on my domain. I’ve figured out that it doesn’t work well on google apps email addresses. The reason being that when you use google apps with imap/pop, the servers are “imap.gmail.com” and not “imap.domain.com”. This confuses the thunderbird account thing, and it ends up saying it can’t find any servers, and you have to do it manually. However, if you are clever enough to set up a google apps for your domain, you should be pretty tech savvy enough to edit your account manually.

Other than my domain google app, it seems very promising. I also didn’t get my other uni email account to work, but that could be because it doesn’t have imap or pop enabled. I haven’t found any information on it.

- New Search Function[![](http://www.10people.co.uk/wp-content/uploads/2009/12/thunderbird5-300x187.png "thunderbird5")](http://www.10people.co.uk/wp-content/uploads/2009/12/thunderbird5.png)

They have completely redesigned the search function. I’m not going to say much about it. When you search for something it opens up in a new tab, and shows stuff. There isn’t much to talk about, so here ya go, just have a screenshot.

I really love Thunderbird 3. It is fantastic. There are so many cool features and I can’t wait to see what else they are going to do for the next version. Normally I complain for a while about what they should have done, but I can’t think of many other things I want included in this. Enjoy it if you try it. I would highly recommend it.
