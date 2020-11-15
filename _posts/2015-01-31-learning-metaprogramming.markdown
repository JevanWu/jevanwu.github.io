---
layout: post
title: "Learning metaprogramming"
date:   2015-01-31 22:07:20
categories: Ruby
---

#### 1. Dynamic Patch
  the `send` method could be used to call methods

  ```
  obj.send(:my_method, params)
  ```

#### 2. Dynamic Method
  the `define_method` method could be used to create instance method

  ```
  class Foo do
    define_method(name) do
      info = @data_source.send "get_#{name}_info", @id price = @data_source.send "get_#{name}_price", @id result = "#{name.capitalize}: #{info} ($#{price})" return "* #{result}" if price >= 100
      result
    end
  end
  ```

  the `instance_method` could be used to call an instance method

  ```
  f = Foo.new
  f.instance_method(:method_name)
  ```

#### 3. Remove Method
  the `undef_method` method could be used to remove method, it would remove both receiver's methods and inherited methods

  ```
  undef_method method_name
  ```

  the `remove_method` method is similar, but it leaves the inherited methods

  ```
  remove_method method_name
  ```


