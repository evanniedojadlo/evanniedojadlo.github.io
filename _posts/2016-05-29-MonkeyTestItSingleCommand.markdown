---
layout: post
title:  "Running multiple tests with one command using the Monkeytest.it API and cURL"
date:   2016-05-29 19:18:16
categories: Testing, QA, Automation, Shell, cURL, Cron
---

A few weeks ago I discovered the MonkeyTest.it service on ProductHunt and wanted a way to run a single command to test my current organizations production help site for any broken links. (This site is hosted using desk.com making traditional automation slightly more tricky) 

The problem is that MonkeyTest.it only supports a single URL per test (e.g. if you're in Slack you can run /monkeytest https://www.google.com ) this will test the specified page but not crawl the site as questioned within the ProductHunt comments [here](https://www.producthunt.com/tech/monkey-test-it){:target="_blank"}

Luckily you can use the following solution to run a single command in order to run a suite of MonkeyTests against your site:

Log into [MonkeyTest.It](https://monkeytest.it/){:target="_blank"} using your credentials

Navigate to the "API key for automation" section and copy the generated code containing your unique key. You will want to update the URL to a page that you want to test along with modifying the provided test parameters.

I personally wanted to test for broken links so my tests looked like the following:

	curl 'https://monkeytest.it/test?secret=YOURKEYGOESHERE&url=https://yourpageundertest1.com&on_click=false&page_weight=false&seo=false&broken_links=true&asset_count=false'

Go ahead and open an editor of your choice and create a file containing your tests:

	curl 'https://monkeytest.it/test?secret=YOURKEYGOESHERE&url=https://yourpageundertest1.com&on_click=false&page_weight=false&seo=false&broken_links=true&asset_count=false'

	curl 'https://monkeytest.it/test?secret=YOURKEYGOESHERE&url=https://yourpageundertest2.com&on_click=false&page_weight=false&seo=false&broken_links=true&asset_count=false'

	curl 'https://monkeytest.it/test?secret=YOURKEYGOESHERE&url=https://yourpageundertest3.com&on_click=false&page_weight=false&seo=false&broken_links=true&asset_count=false'

Now save this file using the .sh extension. Navigate to the file and run the following command which will turn it into an executable:

	chmod +x yourfilename.sh

Finally you can go ahead and run your file:

	./yourfilename.sh

You should see the cURL output within the terminal and if you log into your monkeytest.it account you will see the results of your tests.

Next steps:
Updating the tests to run in parallel
Updating cURL not to show any output within the terminal
Adding automation using Cron to run the command once a week at midnight