---
layout: post
title:  "Jekyll Liquid Exception Error - Resolved"
date:   2014-07-21 19:18:16
categories: jekyll
---

When I attempt to run the Jekyll local server I am returning the error:
  
  Liquid Exception: Included file '_includes/JB/setup' not found in _posts/2014-07-21-test-post-with-rake.md/#excerpt

 My guess is that this is due to my attempt at generating a post via the rake command. I will be going over it today in class and reporting on the fix.

 UPDATE:

 This error is regarding templating and once I deleted the body of the rake generated post containing a template script to a non-existant path I was able to run the server without issue.