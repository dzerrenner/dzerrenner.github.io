---
layout: post
title: Learning Django-CMS
---

Recently i looked around a bit for some new things to learn. I stumbled over [Django-CMS](https://www.django-cms.org/en/), as the name says - a CMS built upon Django. They updated to version 3.0 recently, many new features and a great frontend-editing feature, which integrates the admin page for editing pages in the frontend in a quite ingenious way.

So i gave it a try. Installation is quite easy, they have a nice bootstrap script that installs a working environment. A bit harder is understanding, how the system works altogether. All pages are composed out of content parts, i.e. a text block, an image, links, etc. These parts are called plugins. 

The CMS can be extended via addons. An addon may provide a new plugin. To learn about it, i wanted to develop a simple addon. The [docs](http://docs.django-cms.org/en/latest/index.html) provide quite a good help to incorporate the Poll app from the Django tutorial into the CMS, so i decided to do something simple too. I came up with a simple issue manager, with an overview and single issues as plugins.

First i tried to copy and adapt the text block plugin, but this proved to be more complex than i expected, because of some special porperties of the text plugin. But i didn't knew that. So i tried to get help from the IRC channel, and got some great help. You can read what i've learned in the [IRC log](https://github.com/dzerrenner/django_cms_tickets/blob/master/irc_log.txt) i've put in the repository. Thanks again, [Martin](https://github.com/mkoistinen)!

The addon is working, but far from production ready. There are no tests, and you can not assign issues to anyone. But it's good enough as a prove of concept. You can look at the repository here.  

To come to a conclusion: The CMS is quite a player, highly extensible and relatively easy to understand, once you get into the design principles. 