---
title: 'Inheritance'
date: '2020-09-07'
readTime: '4'
---

Another coding term that gets used is **Inheritance**

> A object extended all of its logic and data to another object

Typically with Inheritance we are talking about 

> A parent to child relationship 

With this relationship, everything the parent has, the child also has access to. Often times the data flow is one way, meaning the child can grab info from the parent but the parent can't grab info from the child. The child can also modify the parent's data and logic but in it's own context. 

This is really good for extending logic from one place to another and keep our code D.R.Y and not duplicate already existing items. 

Inheritance would look different in different programming languages and you should refer to the offical documentation for the language. For the Ruby language, it is depicted as a > of what the parent on the right and the child on the left. 

```ruby
class Parent
	.
	.
	.
end

class Child > Parent
	.
	.
	.
end
```

Here is a example of inheritance where there are multiple levels of inheritance of Bird and Fish is inheriting Animal and Parrot is inheriting Bird.

```ruby
class Animals
	.
	.
	.
end

class Bird > Animals
	.
	.
	.
end

class Fish > Animals
	.
	.
	.
end

class Parrot > Bird
	.
	.
	.
end
```

This also makes sense in polymorphism of where a fish and a bird is also a animal and a parrot is also a bird. Anything the parent class can do the child class can do as well. 

Often times when we start to branch out into multiple level of inheritance, it will start to get hard of keeping track of the relationships. So the best way to visualize the inheritance is to do a tree diagram. Where the root element is the highest level and the starting point, and the will branch out when there are children. When two childs have the same parent, then they are sibling elements 

![tree](https://res.cloudinary.com/doan/image/upload/v1642475030/datatree_bmqkwq.png)

```ruby
class Animals 
	def breathe
    print ‘Inhale exhale’
	end

	def speak
		print ‘talk’
	end
end

class Bird > Animals
	def speak
		print ‘Chirp’
	end
end

@my_bird = Bird.new
@my_bird.breathe                           
@my_bird.speak                               
```

```
result:
Inhale Exhale
Chirp
```

With the child, we can use the methods and data from the parent, and in other lanaguages we can also use 

```ruby
super()
```

which would grab what is inherited. 

Inheritance is really good to abstract logic into other objects and still have the objects do what it needs to. 

```ruby

class User 
	attr_accessor :email
	:password

	def change_pass(new_pass)
		@pass = new_pass
	end
end

class Employee > User
  attr_accessor :id, :start
  
	def clock_in
		@checked_in << Date.now
	end
end

@hd = Employee.new()
@hd.clock_in
@hd.started
@hd.email
@hd.change_pass(‘******’)
```

With this live example, we are inheriting a user class with email and password. The employee inherits from the user and also has those same fields along with id and when they start. Then the employee can do what the user can do and what the employee can do. This will help make other roles that can steam off of the user and have that base functionality while adding in addition of what the object needs in their own class. 

To wrap up, inheritance defines the relationship between objects and also share data and logic between them as well. Often times when we are using inheritance, it is a parent and child relationship, where everything the parent has, the child also has access to as well and is a powerful tool in programming.