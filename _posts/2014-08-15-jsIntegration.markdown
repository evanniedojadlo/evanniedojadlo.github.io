---
layout: post
title:  "Blueimp Bootstrap Image Gallery + Rails, Gallery integration"
date:   2014-08-15 19:18:00
categories: projects, rails, bootstrap
---

Now that I have all of my gallery assets in the appropriate folders I went ahead and updated the asset pipeline with 'require .' to import all of the files.

Now onto the tricky part (considering I haven't implemented this before in rails) is to take my images that are served from postgres via erb and apply the blueimp gallery js plugin to each of the images on page load.

Updates to follow.