---
title: 'Instance vs. Class Methods'
date: '2020-08-10'
readTime: '4'
---

When we are working with classes

> Blueprints of objects.

We would have different logic or methods / functions in the classes 

> Group of code that performs a specific task.

But when used in classes, there are two different types of methods. We have **Instance Methods**

> Performs a specific task on a instance of a class.

and **Class Methods**

> Performs a specific task on the class as a whole.

With **Instance Methods** they look like regular methods in classes but the content of what it returns or the logic will change based off of different instances of the class.

```ruby
class Car
	.
	.
	.
	def car_trip(num)
		mileage += num
	end
	
	def print_color
		print @color
	end
end

@bobs_car = Car.new(‘blue’, 34002, 3)
@bobs_car.car_trip(23)
@bobs_car.print_color()
```

To use the method, we have to create a new instances and then call the method by the name and pass in some parameters if there are some parameters needed. The return value is based off of the instance. So here for bobs_car the color will print blue and the car trip will add to be 34025. These values will change based on different cars and that is why it is called **Instance Method**

For **Class Method**, the logic will apply for the whole class it self and for all instances. So the logic or the result will not change when we use them. For the ruby language, there is a key work self for the name of the method to distinguish it to be a class method. 

```ruby
class Car
	.
	.
	.
	def self.honk
		“Beep Beep”
	end
end

@bobs_car = Car.new(‘blue’, 34002, 3)
@bobs_car.honk                                             -> error
Car.honk                                                           -> Beep Beep
```

When we use the **Class Method** if we try to use it like a instance method, we would get an error. To actually use it, we would need to call the class name then the method them to run the value. The result will always be the same because it applies to the class as a whole. 

In conclusion, when we are working with classes, we are able to use two kinds of methods. Instance Methods that would change the logic or the result based off of different instances of the class. For Class Methods, the logic and results do not change on instances and applies to the class as a whole. 
