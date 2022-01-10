---
title: 'Polymorphism'
date: '2020-09-07'
readTime: '2'
---

Polymorphism is another object oriented programing term that seems more complex than it really is. But if you break up the work, **Poly** means many and **morphism** can change to many forms. So in case of programming the definition is:

> Objects can take on many forms.

And that definition makes sense since object represent real items in the real world and they also take on many forms. 

For example, if you think of a Parrot, a parrot is also a Bird and a Bird is also a Animal. So therefore a parrot is a bird and a animal. 

This also applies for programming objects such as the user object can be a employee, and a manager and a intern. This will help reduce redundancy of the objects of each of them having a employee id, but with polymorphism it is already trickled to all of the objects. 

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

In this ruby program, we have a user class with email and password and a method to change the password. We also have another class of employee that inherits from user and has and id and start attribute as well as a clock in method. This means the employee is also a user can has everything employee has like clock in and started, but also have email, password and the change password method due to polymorphism of employee is employee and also a user.

Polymorphism is good with sharing logic across objects and is a key role in inheritance and encapsulation while also reducing redundancy of logic and data. With this under your tool belt, you can create very powerful objects to use in any program.