---
layout: post
title:  "Spellcheck for Markdown"
date:   2015-01-17 19:18:16
categories: markdown, blogging, spelling
---

If you're using Jekyll to blog or just using Markdown files for blogging and want to ensure that you're not making spelling errors you can do the following:

Within the Sublime Text editor, open your markdown file -> Select Preferences -> Settings - More -> Syntax Specific - User -> (This should open a file called Markdown.sublime-settings where you need to add the following)

	{
	"spell_check": true
	}

You should now see any potential corrections in your file.