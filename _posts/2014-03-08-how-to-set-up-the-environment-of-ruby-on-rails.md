---
layout: post
title: "How to set up the environment of Ruby on Rails"
date:   2014-03-08 22:35:42
categories: [ruby, programming]
---

## Install RVM and Ruby
  RVM is used to manage different version of ruby. With RVM, you can switch between multiple different version of ruby.
  To install RVM, simply type the following command in the terminal

  ```
  $ \curl -sSL https://get.rvm.io | bash
  ```

  or, more convenient, you can just install the RVM with stable ruby by using

  ```
  $ \curl -sSL https://get.rvm.io | bash -s stable --ruby
  ```

  When you finish this step, you can type

  ```
  ruby -v
  ```

  to check if the ruby is available.

## Install Rails
  Rails is the popular web framework based on ruby.
  With Ruby installed, you can install all of Rails and its dependencies through RubyGems on the command line:

  ```
  gem install rails
  ```

  type

  ```
  rails -v
  ```

  to check if the rails is available.

  Here we go! Welcome to the world of Ruby on Rails
