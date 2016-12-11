---
layout: post
title: Open ID and why it is nowhere near as good as it should be.
date: 2009-07-24 19:17:06.000000000 +01:00
collection: posts
category: Tech
---

![21](http://10people.co.uk/wp-content/uploads/2009/07/21-300x115.jpg "21")When people hear about Open ID, they think “Wow…that sounds fantastic.”. And it does. 1 login for all your social networking sites. Sounds amazing. 1 password to remember. But, it really hasn’t worked the way that everyone has hope. Well, it hasn’t worked the way I would like it to. Lets take a look at an example. Lets take signing up to GetSatisfaction.com.

<span style="text-decoration: underline;">**Creating an OpenID**</span>

To sign up for open id, you can do that at http://myopenid.com . This is just 1 of many open id services. There are a bunch more at http://openiddirectory.com/ – if you are signed up to any of these, you either have an OpenID, or you can get one really easily. Go check the info on the site in question. Now, on this site, you can set up your aliases (the site will send these to the sites each time when you ask it to.)

Ok, now you are set up with an OpenID. Now you can sign up to sites using OpenID. Everything up to here is good. I can’t think of any improvements to that bit. It is after here that I’m not impressed.

[![MyOpenID](http://alimckinlay.110mb.com/wp-content/uploads/2009/07/MyOpenID-300x270.png "MyOpenID")](http://alimckinlay.110mb.com/wp-content/uploads/2009/07/MyOpenID.png)

<span style="text-decoration: underline;">**Signing into a site using OpenID**</span>

Go to http://getsatisfaction.com/session/new and if you have a MyOpenID, in the open id box type http://username.myopenid.com (replacing username with your username). This will take you to your my open id page, which will ask you to sign in (if you havent asked to be automatically signed in) and ask you which alias you want to use.

Once MyOpenID signs you in, it will take you back to GetSatisfaction, which will then ask you to fill out a username and password and your profile. If you set up an alias, your profile will be set up, however, you still have to fill in a username and password.

This brings me to a couple of problems that I have with OpenID. Don’t get me wrong, I love the idea. However…

- It does not get rid of usernames and passwords, they are still there. Why do we still have a username and password for each account as well as the OpenID. This does not make sense.
- OpenID is nowhere near widespread enough. Currently 2 of my sites use OpenID. GetSatisfaction, and identi.ca. That really isn’t many.
- OpenID for identi.ca doesn’t allow you to sign in on APIs, as far as I know. Either that, or people just aren’t implementing it.

There may be more problems with it, but this is just what I’m thinking. And the username and password problem is a huge one. Until sites allow you to sign in with OpenID ONLY, will the problem of lots of usernames and passwords go away. And more sites will have to do it as well. Theres no point in a unified ID on the internet if there are only few websites that use it.

What do people think?
