---
title: 'Hashes'
date: '2020-05-30'
readTime: '7'
---

Hashes might be called something else in other programming languages or even be combined with other datatypes, but the datatype I am referring to is 

> An object of key value pairs.

For the content below it will be referring to a hash in web development, specifically in Ruby and Javascript since that is where i have the most knowledege, it would be similiar in other languages but I would double check with the official documentation of the given language you are working in. 

What makes this a really good data type is that there is a **Key** which is a reference to a column in the hash and you can call it to be what makes sense, and the **Value** of what the object would be. This is a really good datatype to represent objects and often times are used interchangeably.

For ruby, you can create a new hash by using the Hash class or with the most common way of the symbols of the curly brackets. 

```ruby
Hash.new
{}
```

Then you can define your key value pairs in the hash and each key value pair is separated by a comma. In Ruby there are three syntax to do this but the top is the most common one.

```ruby
{ first: 'John', last: 'Doe', age: 34 }
{ 'first' => 'John', 'last' => 'Doe', 'age' => 34 }
{ 1 => 'John', 2 => 'Doe', 3 => 34 }
```

As you can see the value on the right side can be any datatype but on the left for the key it would a word or value to represent what the value on the right it. Yes, we could call it anyting but it is better to be descriptive when naming keys. This really helps us represent objects where the attributes of the object is going to be the keys and the values of the keys will be on the value side. 

To grab values from each of these ways, we first need to assign them to variables so we can reference them then we can pull out the values from the keys, like the following:

```ruby
hash = { first: 'John', last: 'Doe', age: 34 }
hash2 = { 'first' => 'John', 'last' => 'Doe', 'age' => 34 }
hash3 = { 1 => 'John', 2 => 'Doe', 3 => 34 }

hash[:first]
hash2['first']
hash3[1] 
#or 
hash3['1']
```

This will grab the first name of "John" from each style of hash. 

We are going to use the first way which is the most common way, so if we want to get the values, we would get them by the keys.

```ruby
hash = { first: 'John', last: 'Doe', age: 34 }

hash[:first]
hash[:last]
hash[:age]
```

This will return "John" for the first name, "Doe" for the last name and 34 for the age. 

You can also run logic on the values as well with the reference. For example, let's say I want to add 1 to the age since it's their birthday. Since referencing the key gives you the value, you can then run logic on the value.

```ruby
hash = { first: 'John', last: 'Doe', age: 34 }

hash[:age] = hash[:age] + 1
```

What we are doing here is setting the age to be what it was before, which is 34, then add 1 to it so now the age is 35. You can do this for any value by referencing the key. 

For this next trick, let's say I want to run some logic on all key and values in my hash, such as displaying all key value pairs in a hash. And Yes you could do that manually like so:

```ruby
hash = { first: 'John', last: 'Doe', age: 34 }

'first' + hash[:first]
'last' + hash[:last]
'age' + hash[:age]
```

And this would work with using some string concatenation and calling each key to the value I still get the desired results. But what would you do when you have 10 or 50 or 100 more key value pairs? Would you type out each 10 or 50 or 100 key value you pairs? No! that would take forever and such a tedious task to do it that many times. Also what happens when you don't know the keys or how many numbers of them? Then the above code wouldn't work. 

So the solution to this is to create something called a **Iterator** which can go through each key value pair in the hash, without having to know the keys or how many there are. 

```ruby
hash = { first: 'John', last: 'Doe', age: 34 }

hash.each do |key, value|
  print key + " " + value
end
```

With this example, this is one way we can iterate through the hash. How it works is that it goes through each key and value from left to right, one at a time. and the key references each key that it goes to, and the value is what each of those values are so this will print out:

```
  first  John
  last  Doe
  age  34
```

This is a better way for us to run any logic with all the key values pairs in a hash. 

Hashes are a very powerful and descriptive datatype that is really good to represent objects. We can grab the values by referencing the keys and iterate through each key value pairs to do any logic. 

```ruby
  person = { first: 'John', last: 'Doe', age: 34 }
  car = { make: 'Toyota', model: 'Prius', year: 1999 }
  user = { username: 'Foobar', email: 'foobar@email.com' password: '******'}
```

Now you have another datatype in your toolbelt to use to represent data. We will see what other datatypes are there!