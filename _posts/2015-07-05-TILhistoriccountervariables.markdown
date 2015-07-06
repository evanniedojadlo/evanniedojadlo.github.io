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

UPDATE:
My friend Trevor sent me a link [here](http://stackoverflow.com/questions/4137785/why-are-variables-i-and-j-used-for-counters) {:target="_blank"} as this has been brought up a lot in the past. It looks like the reasoning ultimately came from mathematics, specifically the summation notation (i for the first index, j for the second, etc.) and this was used in FORTRAN which became a habit carried over to other languages.

[This](http://www.pluralsight.com/courses/csharp-from-scratch){:target="_blank"} Pluralsight course needs to update the additional reasoning behind using those counter variables :) 