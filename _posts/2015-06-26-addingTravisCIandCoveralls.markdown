---
layout: post
title:  "Quickly adding Coveralls.io and TravisCI to your Rails project"
date:   2015-06-26 19:18:16
categories: rails, CI, technicalDebt, environment, ruby, process
---

*What you're going to need:*

[A Github account](https://github.com/){:target="_blank"}

A project on that Github account (In this example we are using a Rails project)

[A TravisCI account](https://travis-ci.org/){:target="_blank"}

[A Coveralls account](https://coveralls.io/){:target="_blank"}



*Setting up TravisCI:*

The first thing you will need to do is sign up for a TravisCI account which you can find right [here](https://travis-ci.org){:target="_blank"} now sign in using your Github account.

Once you're signed into your account you can select the add button next to "My Repositories" where you will be taken to a page where all of your public repositories are shown. From here you will want to do the following:

Choose your project and set the repository switch to on

Add the .travis.yml file to your project directory and commit this to your repository (This tells travis what to build)

Trigger your first build with a git push and watch your build fail (In depth and .travis.yml setup Documentation can be found [here](http://docs.travis-ci.com/user/getting-started/){:target="_blank"})



*Setting up Coveralls:*

Next you will need to sign up for a Coveralls account which you can find right [here](https://coveralls.io){:target="_blank"} from here simply sign in using your Github.

Once you're logged into your account you will want to select the "Add Repos" button in the top right corner

From here you should see a list of your Github repos that are associated with the account that you used to sign up. Select a project and turn the off button to on, navigate into that project and follow the SET UP COVERALLS guide:

Add the coveralls gem to your Gemfile:

	gem 'coveralls', require: false

In your spec_helper.rb or test_helper.rb or what have you, add the following:

	require 'coveralls'
	Coveralls.wear!

	#Your code here.

And that's that! Coverage for your next Travis build should appear in coveralls!

Coveralls Documentation can be found [here](https://coveralls.zendesk.com/hc/en-us){:target="_blank"}

Your next step should be setting up tests and addressing the coverage reports that Coveralls reports on.













