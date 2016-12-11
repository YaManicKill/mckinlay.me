---
layout: post
title: PubSubHubbub with superfeedr
date: 2010-12-13 18:35:48.000000000 +00:00
collection: posts
category: Tech
---

[![](http://www.10people.co.uk/wp-content/uploads/2010/12/Pubsubhubbub.png "Pubsubhubbub")](http://www.10people.co.uk/wp-content/uploads/2010/12/Pubsubhubbub.png)There are 3 types of people. Those who understand “PubSubHubbub”, those who haven’t got around to looking into it (but have heard the name) and those who see that name for the first time and go “That looks like my cat just walked over the keyboard…

If you are not the 1st type of person, trust me, you will want to be soon enough.

I will very quickly go over what [PubSubHubbub](http://code.google.com/p/pubsubhubbub/) is, but the main point of this is to talk about [superfeedr](http://superfeedr.com "SuperFeedr") (I will get to that in a minute).

Firstly, PubSubHubbub:

If you know what RSS/atom are, this will be nice and simple to understand. RSS/atom are what we call “feeds” which is a stream of information that constantly updates with new information, generally from a blog, or a social networking site or really anything with dynamic information. This allows feed readers or applications to check it to see if there is new information on it, and display it to you, or do something else with it. This was fantastic when it came out, and still is great, but it has 1 problem. That problem is the application needs to check the RSS feed every so often to see if anything has changed. This is a problem for both the application, and the server, as it is unnecessary load on both of them.

Into this void steps PubSubHubbub. It is a protocol which takes RSS, and makes it near instant. With it, you have 3 things, Publishers, Subscribers and Hubs. Publishers are the blog, or the social network etc (the RSS feed), Subscribers are the application that reads it, and Hubs are the middle man.

What happens is the publisher has a line in the RSS or atom feed, which is a url to a “Hub”. This tells any Sub to go to that Hub to get the information. The Sub then subscribes to the Hub, and waits. The Pub gets new information in it (a new blog post for example) and pings the Hub to say “I have more info”, then the Hub grabs the info, and sends it off to the Sub, or many Subs. The Subs then have the new info, and do whatever they want with it.

This is my simple understanding of PubSubHubbub, so it may be a bit off, but it works ![:-P](http://www.10people.co.uk/wp-includes/images/smilies/icon_razz.gif)

However, in this process, you need a Hub. This is the part that does all the work (the Pub only needs to have 1 extra line in the feed, and ping the Hub everytime it has new content). So, it is the part that is most resource intensive, and hardest to set up. This is where superfeedr steps in. It is a service that creates a Hub for you to use. Then, you just point all your feeds to that Hub, ping it whenever they update, and thats all good, and PuSH enabled application pointing to your feed can automatically get the almost-instant updates to your site.

To set up your [superfeedr](http://superfeedr.com) hub, just go to the site, click “Are you a publisher” and then register on the right hand side. There is very little information you need to give: username and password (obviously), subdomain for your hub (subdomain.superfeedr.com) and the name and url of your site or application. After this, you get thrown to a page that tells you how to get your site to start pinging the hub. If you run a CMS, like this site, then there are plugins for them, and you just set the Hub to “http://subdomain.superfeedr.com” and you are set to go. If you are making your own app, however, then it is almost as easy. There is a line to add to your RSS/atom, and then you have to ping the hub whenever you want to tell it there is new stuff. There is a really easy to use [PHP library](http://code.google.com/p/pubsubhubbub/source/browse/trunk/publisher_clients/php) for this (which is what I’m using for fourdenty, once I release the new version).

That is you sorted…you have PubSubHubbub’ed your site.

There are many advantages to using a hosted hub, rather than building your own. It is the most server-intensive part, is just another burden on yourself, and is quite tricky to set up well. Superfeedr themselves actually give you 25000 free notifications (although it is still too early to see how quickly those are used up) and then very reasonable pricing on notifications after this. They give you your own personal hub, rather than just a communal hub, hopefully meaning that if someone runs a stupid amount of stuff through theirs, it doesn’t affect your own feeds, and their customer service is great.

I have asked [@superfeedr](http://twitter.com/superfeedr "SuperFeedr on Twitter") on twitter several questions, and I get a clear, succinct answer from them within minutes sometimes, but always within a few hours. They also seem to be humans behind the twitter feed, and that is always great, because you get better answers, rather than stock answers from someone who clearly knows nothing about what they are doing. The answers I am getting sound like they are coming from the developers.

So, in conclusion…PubSubHubbub is fantastic – use it for everything you are every going to do in the future, Superfeedr are great – use them as your hub, and my joke at the beginning of the blog post was terrible. You know it makes sense ![;-)](http://www.10people.co.uk/wp-includes/images/smilies/icon_wink.gif)

Also, this is the first post I am releasing that is going out to my [social](http://identi.ca/yamanickill) [networking](http://twitter.com/yamanickill) sites via pubsubhubbub and[ brdcst.it](http://brdcst.it/), so this is quite exciting to check it works ![:-P](http://www.10people.co.uk/wp-includes/images/smilies/icon_razz.gif)
