---
layout: post
title:  "Blueimp Bootstrap Image Gallery + Rails"
date:   2014-08-11 19:18:00
categories: projects, rails, bootstrap
---

I revived an older rails project that I was working on and found that my bootstrap image gallery was now returning some errors in the console.

[Error Screenshot]({{http://www.evanniedojadlo.github.io}}/img/error_screenshot1.png)

Instead of digging through the errors I just decided to delete any of the old assets and actually integrate them into the assets pipeline.

Update 8/10:

I deleted all of the existing assets from within /stylesheets and /javascripts and deleted all of the 'requires' from application.js and styles.

Reloaded the project and noticed some errors returned with the chrome inspector console so I loaded application.html.erb and deleted any of the references to blueimp. Reloaded the project and it looks like we are working with a clean slate.

I noticed that the large images are not showing within the page layout. No errors are being returned so this could be an environment issue considering I cloned the project from my remote repo. I am going to attempt a rake db:migrate and rake db:seed to resolve.

The rake db:migrate was successful but the rake db:seed returned "rake aborted! Connection refused - connect(2)" so it looks like a permission error with the database. I am going to try this on the original machine that I created the project on to confirm tomorrow evening.

Update 8/11:

I ended up narrowing down the error to the "tire" gem. I commented out the gem and noted that the error output in the terminal was halved so I cleaned up my model containing related code which ended up resolving the error.