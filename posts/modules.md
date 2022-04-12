---
title: 'Modules'
date: '2020-07-18'
readTime: '3'
---

Modules are a very useful tool to keep your code D.R.Y

> Do not Repeat Yourself

and will keep your code not W.E.T

> Write Every Time

Essentially a module are:

> Libraries, holds methods to be reused. 

They can't really make objects and are only useful to store reuseable code that we can pass around in our program. In some languages they may be called something else or have differnt syntax. Just be sure to reference the official documentation of the language you are working in.

```ruby
module Math
  def sum(num1, num2)
    num1 + num2
  end

  def cube(num)
    num * num * num
  end
end

class HW
	include Math
	def sol1
		return sum(cube(3), 7)
	end
end
```

In the ruby language, we are able to create modules with the module key word and be able to put methods into the module. Then when we want to use them, we just need to include the module and then we can use any methods that are in the module. Now with this, we can use it in other places of our programs, and even in other files without having to rewrite the same logic over and over again. If there is some needed changes, then we would change it in the module and it will reflect that change in all the places we are using it. 

Modules are a useful tool to keep our code D.R.Y by putting all the reusable code in one place, and be able to reference the code as much as we want. 