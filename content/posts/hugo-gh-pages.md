---
title: "Hugo on GitHub Pages"
date: 2022-12-03T22:00:00+01:00
categories: 
    - Meta
---

## A new beginning

So I decided to unearth my old blog which was started around 2014 on GitHub pages with Jekyll. This time I wanted to try [hugo](https://gohugo.io/) and import old content here. 
After looking though the 2 articles I wrote back in the day, I decided to leave them be. They were about playing around with Django-CMS and a [contribution](https://github.com/ccampbell/chromelogger-python/pull/7) to cromelogger-python. 

## Using hugo

Hugo is a modern static site generator, much like Jekyll. Go instead of Ruby, maybe a bit more flexible, but not directly supported by GitHub. Some say, hugo is a bit trickier to learn, but blazing fast. I just wanted to try it out :smile: 

The setup and start to a basic site with a custom template was easy, maybe 20 to 30 minutes. I don't know if I run into some roadblocks if I want to change some major stuff, but it'll suffice for now. No big issues yet, I basically just followed the tutorial.

## Deploying

The [documentation](https://gohugo.io/hosting-and-deployment/hosting-on-github/) also has a nice section about deploying the site to GitHub pages, which I have done. To use it on your own CI/CD solution, it all boils down to running the script to generate the site and copy/upload the output directory to the desired destination.

## Custom domain and Cloudflare

GitHub pages supports serving personal and project pages using an own domain. I use Cloudflare's DNS to point the domain to GitHub pages. I also could do this on the registrars site, but with an own DNS I feel more flexible, I plan to update some things and possibly need some subdomains pointing all over the place. Just as I wrap up this article, I found out that there is also a possibility to host such a site directly on [Cloudflare](https://developers.cloudflare.com/pages/framework-guides/deploy-a-hugo-site/).

## Conclusion

All this said (which is nothing interesting at all...), this is basically an article to test the installation and the DevOps pipeline :blush:. Ignore this and enjoy other posts and this image of some llamas I took some years ago in a zoo.

![Three llamas facing away from the viewer, with white, reddish and dark brown fur, from left to right. ](img/llamas.jpg "Some llamas, picture taken 2015 in Cologne zoo.")
