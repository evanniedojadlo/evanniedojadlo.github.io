---
layout: post
title:  "The beginning of a simple acceptance test"
date:   2014-09-17 19:18:16
categories: rspec, ruby, qa, testing
---

I ran across a simple copy verification test case today that was dying to be automated, the following is what I whipped up:

Filename: menu_copy_verification.rb

describe 'Login' do

  before(:each) do
    @driver = Selenium::WebDriver.for :firefox
  end

  after(:each) do
    @driver.quit
  end

  it 'succeeded' do
    @driver.get 'http://staging server url/'
    @driver.find_element(id: 'loginEmailInput').send_keys('myemail@domain.com')
    @driver.find_element(id: 'loginPasswordInput').send_keys('PasswordHere')
    @driver.find_element(id: 'loginBtn').submit
  end

end

The first step logs in as the user. Once the user is logged in the test assertion identifies updated copy within a drop-down menu which will either pass or fail. 

Updates to follow.

