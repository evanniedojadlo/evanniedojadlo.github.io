---
layout: post
title:  "TIL: Historic counter variables"
date:   2015-07-05 19:18:16
categories: C#, VisualStudio, FORTRAN, Loops
---

Over the past week I have been picking up C# so that I can better contribute to our front-end automation efforts. Luckily a lot of the Selenium Webdriver syntax is transferable from what I learned and have used with Ruby.

So, today I was going over "program flow" in C# with For Loops and had learned that the reasoning behind using the variable i was historical and that ijkl were the only legal counter variables allowed within FORTRAN (FORmula TRANslator) all of those years ago.

	for (int i = 5, i < 10; age++)

Pretty cool.