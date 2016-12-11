---
layout: post
title: 'Tutorial: Migrating from Apache to Lighttpd, Saving 200M of ram'
date: 2010-05-19 17:14:40.000000000 +01:00
collection: posts
category: Tech
---

Ok, so, after just 2 hours of playing around with my server, I upgraded it from Ubuntu 8.04 to 10.04 (w00t for LTS) and migrated it away from apache to lighttpd. “Whats wrong with Apache?” I hear you ask. Well, my VPS is running on 512MB of ram, and with apache running, it was literally using over 256Mb of ram, and that caused the server to crash 3 times in the last 2 weeks. This, obviously, isn’t a good thing, so I decided to try lighttpd and it turns out that my server now has almost 240Mb of ram free. So, that is a saving of over 200Mb of ram. Fantastic.

“How can I move over to lighttpd?” I now hear you cry. Well, it was actually quite simple, and I plan to show you how I moved my WordPress install over to it.

****NOTE** This  was written for Ubuntu 10.04, but should work in any other version of ubuntu, and should work for most other distros if you just use your respective package manager, and different places where the files are saved possibly**

- Well, lets go, first of all, make sure you are totally up to date with all your packages (sudo apt-get update && sudo apt-get upgrade).

- Install lighttpd

In Ubuntu this would be “sudo apt-get install lighttpd” – this will install lighttpd, created a default conf file and start lighttpd (however, if you currently have apache running, it will fail to start because apache is already binded to port 80).

- Edit lighttpd.conf

In ubuntu, you can find this at “/etc/lighttpd/lighttpd.conf”. If you have apache running on port 80 just now then find the line “server.port = 80″ and change it to something else (such as 81). You can keep it like this until you have all your configuration working, and access it at http://www.domain.com:81 to see if it works.

You can edit the root for your website on the line ‘server.document-root        = “/var/www”‘ – just change this to wherever your website is saved.

- Edit wordpress settings for permalinks

Lighttpd doesn’t work very well with wordpress’ permalinks because it goes for a 404 error. For this, you will have to do 2 things.

First, edit your 404.php file in your wordpress theme and add this to the top “`< ?php header("HTTP/1.1 404 Not Found"); ?>`“. This will make sure that proper 404 errors will still show up in search engines (which is kinda important).

Second, edit this line in your lighttpd.conf ‘#server.error-handler-404  = “/error-handler.php”‘ and turn that into ‘server.error-handler-404  = “/index.php”‘. If you have virtual hosts set up (and I’ll show you how to do that very soon) make sure you do that in the virtual host rather than the default one.

- And that is it…

You now have a working wordpress install on lighttpd. If it all seems to work, change the port back to 80, stop apache, and restart lighttpd (sudo /etc/init.d/lighttpd restart). There are obviously many more things you can get to do, such as virtual hosts (which I’m literally just about to tell you about), but you still can have a working install, so enjoy.

- Virtual hosts

This is one bit of lighttpd that I really love, it is so much easier than apache. Ok, so get to a nice empty bit of you lighttpd file, (make sure it is before the bit at the end of the file that says it must be at the end of the file. Things will break…) and copy this into it:

> $HTTP["host"] =~ “(^|\.)domain\.co.uk” {  
>  server.document-root = “/path/to/”  
>  server.errorlog = “/var/log/lighttpd/domain/error.log”  
>  accesslog.filename = “/var/log/lighttpd/domain/access.log”  
>  server.error-handler-404 = “/index.php”  
>  }

Make sure you replace “domain\.co.uk” with your domain (make sure you leave the slash there though) and replace “/path/to/” to wherever your files are. Then restart lighttpd, and you are all sorted. Nice and easy. If you are using an ip address, or a subdomain instead, you don’t need the whole bit before the domain, and you can just have “sub.domain.com” or “192.168.2.1”.

I hope this tutorial has helped anyone free up some RAM on their webserver. If you have any suggestions for this tutorial, or any questions about something that has gone wrong, then please leave a comment ![:-)](http://www.10people.co.uk/wp-includes/images/smilies/icon_smile.gif) I’ll include any corrections to my work (and credit you). Have fun with your lighttpd.
