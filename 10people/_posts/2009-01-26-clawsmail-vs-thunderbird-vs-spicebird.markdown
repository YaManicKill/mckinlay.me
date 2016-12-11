---
layout: post
title: ClawsMail vs Thunderbird vs Spicebird
date: 2009-01-26 21:57:00.000000000 +00:00
collection: posts
category: Tech
---

<div>I have been getting increasingly annoyed with Thunderbird, as it hasn’t had a lot of work done on it, and Thunderbird 3.0 is looking like it is going to take ages to come round. Once it comes out I’ll try it. So…I found this cool program called Spicebird. However…it didn’t quite cut it.I recently moved to Crunchbang Linux, and realised there was a very cool program that is installed by default. It is called Claws Mail. So I decided to try it.

There are many good things about it, and there are a few rubbishy things about it. Thing is, it seems like a program that wasn’t designed for ease of use. It is very powerful, very configurable, but very hard and confusing.

For example…I wanted to view html emails. I thought this would be simple. But it wasn’t.

 1. sudo apt-get install claws-mail-html2-viewer  
 2. Go to Configuration > Plugins  
 3. Click on Load and go to /usr/lib/claws-mail/plugins and choose gtkhtml2_viewer.so  
 4. Configuration > Preferences > Message View > Text Options  
 5. Untick “Render html messages as text” and tick the 2 below it.  
 6. Configuration > Preferences > Plugins > GtkHtml2Viewer  
 7. Tick “Load remote images in mail” If you want it to.

So yeah…7 steps to view html messages in Claws mail.

So maybe it’s not the easiest. But it certanarily is the most configurable I’ve used in a long time. If you’ve not used it, then I would say use it. NOW.

</div>
