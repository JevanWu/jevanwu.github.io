---
layout: post
title: "Ruby: Clean your code!"
date:   2014-05-05
categories: [programming, ruby]
---

## Minimize the number of "nested if statement"
  "nested if statement" is normally considered as the code smell. We should try to minimize the number of "nested if statement", though we cannot avoid using it completely.

### if the 'if statement' is embraced by a loop and without 'else', use 'next' instead
 original code:

 ```ruby
 foo.each do |f|
   if bar
     if baz
       ...
     else
       ...
     end
   end
 end
 ```

 It looks not quike clean, isn't it?

 cleaned code:

 ```ruby
 foo.each do |f|
   next if bar
   if baz
     ...
   else
     ...
   end
 end
 ```
 It looks much better to me.

### use variable to eliminate the 'if statement'
 original code:

 ```ruby
 if bar
   name = "Jevan"
   age = 24
 else
   name = "John"
   age = 24
 end
 ```

 cleaned code:

 ```ruby
 user_name = bar ? "Jevan" : "John"
 name = user_name
 age = 24
 ```

