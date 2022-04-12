---
title: 'D.R.Y vs. W.E.T'
date: '2020-07-18'
readTime: '2'
---

When we are writing code, we want our code to be efficient as possible. Meaning, when we write our code we want to be **D.R.Y**:

> Do not Repeat Yourself

versus **W.E.T** code:

> Write Every Time

When we are writing W.E.T code, we need write the same logic over and over again or even copy and paste it over and over again. This does work but we are reinventing the wheel every time and would not make our code as clean as it can be. 

But when we are writing D.R.Y code, we are only writing the logic once and then referencing it multiple times when we need to use this. We can do this multiple of ways, of creating methods, modules and other coding techniques to keep our code D.R.Y. 

Here is an example of W.E.T code:

```ruby
def start
  print ‘Welcome Choose 1 or 2 to start’
  opt1
end

def opt1
	print ‘Welcome Choose 1 or 2 to start’
	user_input = gets.to_i
end
```

Here we are being W.E.T with our code of printing the same menu over and over again. Also if we need to change the line, we would need to change all the places that it is repeating. 

To help make our code D.R.Y we are going to use modules in the ruby language to have our menu be it's own method and use it any place we need to.

```ruby
module Msg
  def menu
    print ‘Welcome Choose 1 or 2 to start
  end
end

  include Msg
	def start
    menu()
    opt1
  end

  def opt1
    menu()
    user_input = gets.to_i
  end
```

Now we are more D.R.Y with our code and if there are any changes we only need to change the one place. We can also use this menu in other places and in other files without having to rewrite the logic. 

When we are writing our code, we want to write in a way where it can be as efficient as possible, to keep our code D.R.Y. Where we Do not repeat yourself. If you can I would think of ways to already do this when you are coding or you can go back and refactor your code to be D.R.Y. As Long as we are writing code in a efficient way, it will make our job as a developer easier.