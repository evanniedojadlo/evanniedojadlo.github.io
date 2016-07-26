---
layout: post
title:  "TIL 7/10 Using wildcards for quickly moving multiple files"
date:   2016-07-26 19:18:16
categories: UNIX, Shell
---

I needed a quick way to move all of the .sh files in one directory to a new directory so I found the following solution which uses wildcards:

	mv *.sh /specifydirectory

You can also specify any other files within the directory that you want to move by adding the wildcard to each of the file extensions that you want to move:

	mv *.sh *.md *.rb  /specifydirectory 