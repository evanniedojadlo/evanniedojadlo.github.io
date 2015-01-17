---
layout: post
title:  "ODOT - Refactoring woes"
date:   2015-01-16 19:18:16
categories: rails, ruby, refactoring
---

I am currently running through the Rails Treehouse tutorial to brush up on RSpec and noticed the following code written in one of the models:

	validates :title, presence: true
	validates :title, length: { minimum: 3 }
	validates :description, presence: true
	validates :description, length: { minimum: 5 }

Even with my minimal rails knowledge I realized that this could be refactored into the following:

	validates :title, presence: true, length: { minimum: 3 }
	validates :description, presence: true, length: { minimum: 5 }

My question is why Treehouse wouldn't automatically introduce cleaning up the quality of code similar to the way that Code School hurls the student into strict exercises from the beginning.