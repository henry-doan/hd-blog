---
title: 'Objects'
date: '2020-08-10'
readTime: '4'
---

Often times when you are programming, you often here the term **Object** pop up here and there. What it is:

> Person, place or thing by context. 

When we are programming, we would have to create these objects in programming to represent actual objects in the real world. There is also a coding paradigm of **Object Oriented Programming** or **OOP** for short and it is where we: 

> Treating everything as an object and run logic based on the object.

We can represent actual objects many ways such as classes, hashes, and with other datatypes. Objects can also be items in the program language it self. 

We will go through some examples of how to represent objects in programming, first off we will start with a **Hash**.

```js
Person = {
	name: ‘Bob’,
	email: ‘bob@email.com’,
	phone: ‘123-123-1233’,
}

Car = {
	runs: true,
	seats: 5,
	color: ‘blue’
}
```

Hashes are key value pairs, where the attributes of the objects are the keys and the values of each of them are going to each of the feilds accordingly. This is really good for creating blueprints of objects and resuse them to create more of the same objects but with different values. 

Classes are blueprints of objects and encapsulates everything having to do with the class to preform any logic. 

```ruby
class Animal 
  attr_accessor :name, :age, :color
  
	def eat
		‘Nom nom’ 
	end
end

class Account 
  attr_accessor :number, :active, :balance
  
	def deposit(num)
		balance += num
	end
end
```

Lastly, when we are using the term object, it refers to items in the programming languages themselves, such as:

- Methods / Functions
- Variables
- Conditionals
- The Window
- Browser
- Elements on a page
 
and others depending on what discourse and technology you are working on. 

Even though the term object changes it's meaning, it could be hard to understand what it could mean. But based off of the context, it would be a huge indicator of what it is and how we can work with it.