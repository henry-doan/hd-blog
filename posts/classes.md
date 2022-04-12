---
title: 'Classes'
date: '2020-08-10'
readTime: '3'
---

Classes play an important role in object oriented programming because classes are one of the ways to define an object and act as a 

> Blueprint of the object.

When we are creating objects, we could create each class for the object, such as for Bob, Sue, John etc. That works, but there are a lot of repeated code and data and it is not efficient as it can be. Because if we have 100 people, then we would have 100 different classes with simliar logic and data, and that would drag down efficiency. A better thing to do is to create a blueprint of an object, and create different instances of the object. How this would work if we create everything a person has like a first name, last name, age, email etc. then we can fill in those values for each person while using the same class or blueprint. So the code is the same for each person but the different instances will have different values. 

To create classes will change depending on the language, so be sure to reference the offical documentation of the given language. 

For the Ruby language, you can use the class keyword and will look like this:

```ruby
class Car
	attr_accessor: :color, :mileage, :seats

	def initialize(color, mileage, seats)
		If (mileage % 5000 === 0 || mileage % 5000 === 5000)				print ‘time for oil change’
		end
		@color = color
		@miliage = mileage
		@seats = seats
	end
	
	def car_trip(num)
		mileage += num
	end
end
```

For the Ruby classes, it is make up of attributes of what the object has, the access of to read or write the attributes. The initialize, which is a method that would run when the class runs, this is good for beginning steps of of the class. Lastly it would have other logic and methods to do in the object. 

This class we have a blueprint of a car of the car having color, mileage, and seats and other relevant information for the car. In the initialize method for when we create a new car, we are setting the attributes to variables and run some logic to see if they need a oil change. Then we have a method to add a car trip to the update the mileage. 

To use the class, we need to do something called **Instantiation** of creating a new instance of the object. 

```ruby
class Car
	.
	.
	.
end

@dads_car = Car.new(“red”, 20000, 4)
@moms_car = Car.new(“pink”, 15000, 4)
@bros_car = Car.new(“green”, 50000, 2)
```

In Ruby, to create a new object it would be with .new() method by using the blueprint. This way, by using the same code in the class, we can create new instances of the objects and the only thing that would change, would be the values of the new objects. So in this case we have different values for different cars. 

This is scoped of where we are using the instances. Meaning if I am still using dads_car then the color will always be red. But if I switch to another instances of moms_car, then the color is pink, so it is based off of which car we are refering to. 

In conclusion, classes are blueprint of objects and are useful in creating different instances of an objects. Classes play a key role in inheritance, polymorphism and with encapsulation. When we need to create multiple objects, we can use classes to do it in a efficient way.