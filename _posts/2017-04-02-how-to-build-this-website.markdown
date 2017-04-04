---
layout: post
title:  "How to build this website"
author: yduan
date:   2017-04-02 00:00:00 -0500
categories: jekyll
tags: Jekyll Website
---
Here is what I did to build this my very first website. I used [Jekyll][jekyll], a static website generator, to build the website, and used [GitHub Pages][githubpage] to host this website. 

For building the website with Jekyll, I find this [video][youtube-howto] very useful. You can start with a theme you like from [Jekyll Themes][jekyll-themes]; my theme is [jekyllDecent][decent].

For publishing the website with GitHub Pages, I basically follow this [tutorial][githubhelp] and this [video][youtube-githubpage](I don't follow their suggestion modifying the head.html and my website just works fine).

Tips:
* Installing Jekyll: If you use a Mac like I do, it's likely that ``gem install jekyll`` does not work (you may check this [troubleshooting page][troubleshooting]). Try ``sudo gem install jekyll`` instead.

* Publishing the website: You need to go to **_ _config.yml_** and change ``url:`` and ``baseurl:`` to be the base hostname & protocol for your site. If you use the same theme as I do, modify **_robots.txt_** as well. Make sure your url is something like ``https://<yourusername>.github.io``, not ``http://...``, which may lead to a display error like _This page is trying to load scripts from unauthenticated sources_ (find the solution [here][httpserror]).

* To change the order of your pages shown in the navigation, go to ``_pages``, and add a ``weight: <#orderYouWant>`` parameter to the layout section of each page.

[jekyll]: https://jekyllrb.com/
[youtube-howto]: https://www.youtube.com/watch?v=HOg8jWZ3lt0
[githubpage]: https://pages.github.com/
[jekyll-themes]: http://jekyllthemes.org/
[decent]: https://github.com/jwillmer/jekyllDecent
[githubhelp]: https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/
[youtube-githubpage]: https://www.youtube.com/watch?v=x352fsLm3gE
[troubleshooting]: https://jekyllrb.com/docs/troubleshooting/
[httpserror]: https://github.com/gcushen/hugo-academic/issues/24