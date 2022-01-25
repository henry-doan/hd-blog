---
title: 'Procs & Lambdas'
date: '2020-07-18'
readTime: '4'
---

Procs and Lambdas are a less known concept and might be different in other tools and languages with other shortcuts to them. They:

> Wraps around a block of code to be use later. 

They really help keep our code D.R.Y and work a bit different than methods and modules. 

With **Procs** we typically pair them up with variables and it returns from content and the proc itself. Like methods, it will work when you call them but ti doesn't really care for arguments it takes. 

```ruby
name = Proc.new { |name| 
  puts  "#{name}!" 
}

name.call
name.() 
name[]
name.===
```

With the ruby language there is a Proc class you can use to create new procs and there are multiple ways you can call them. Like methods you can also return values as well as pass in arguments:

```ruby
def print_name
  name = Proc.new { |name| 
    return "#{name}!" 
  }
end

name.call(‘bob’)
```

With **Lambdas**, like procs, they also like to be paired up with variables and can be used like method of returning in the code block. But unlike procs, it does care about the amount of arguments passed in. 

```ruby
name = lambda { |name| 
  puts "#{name}!" 
}

name = -> { |name| 
  puts "#{name}!" 
}

name.call
name.() 
name[]
name.=== 
```

With lambdas in ruby, there are two ways to create them, one is with the lambda class and the other is the shorthand way. We call them the simliar way of how we call procs. When we return in a lambda it would look like so:

```ruby
def print_name
  name = lambda { |name| 
    return "#{name}!" 
  }
end

name.call
```

But when you are passing in arguments, it does matter how many arguments you pass because it should be the same as how many it takes in or else you would get an error. 

```ruby
def print_name
  name = lambda(name, age) { |name| 
    return "#{name}!" 
  }
end

name.call(‘bob’, 2)
 
name.call(‘bob’)
  # ArgumentError (wrong number of arguments (given 0, expected 1))
```

With procs and lambdas, you may use or encounter them sometime during your development career, now you know how to use them and the differences between them to put them in your program.
