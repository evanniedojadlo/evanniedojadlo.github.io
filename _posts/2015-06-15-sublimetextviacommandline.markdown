---
layout: post
title:  "Utilizing Sublime Text via the command line in OS X"
date:   2015-06-15 19:18:16
categories: shell, zsh, sublimetext, environment
---

Despite this question having been covered a number of times I figured that I would make a note for myself in the instance that I have to set this up again within a new environment. I also wanted to combine the multiple sources into one post that I found scattered throughout the interwebs.

To begin, the shell path for a user is a set of locations within the filing system in which the user can utilize certain applications, commands, and programs without any need to specify the full path to that program or command.

This means that if you’re using Sublime Text and want to open files within the command line you can utilize something explicit like this:

	sublime

First, you will want to ensure that Sublime Text currently resides within the Applications directory. The next step is to hop into shell and enter the following:

	echo $HOME

This should return the home directory location which we will want to navigate into. Once you’re within the home directory you will want to enter the following:

	ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/sublime

The ln command makes links between files and the -s flag makes symbolic links instead of hard links. More information on the difference between symbolic and hard links can be found within this [post](http://unix.stackexchange.com/questions/9575/what-is-the-difference-between-symbolic-and-hard-links)

That's it. From here you can test your new command by entering sublime within the shell and you should see the application load.

Sources:

[Olivier Lacan](http://olivierlacan.com/posts/launch-sublime-text-3-from-the-command-line/){:target="_blank"}

[Explain Shell](http://explainshell.com/){:target="_blank"}

[Sublime OS X Command Line](http://www.sublimetext.com/docs/3/osx_command_line.html){:target="_blank"}






