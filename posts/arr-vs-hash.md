---
title: 'Arrays vs. Hashes'
date: '2020-06-02'
readTime: '4'
---

Today we are going to look two datatypes that are often confused and to see the best use cases for both. Some languages may call these data types something else or even combine them but for this we will refer to arrays as:

> A Collection of Objects.

and a hash 

> Object of Key Value Pairs.

Technically we can use either datatypes for any use case, but there are where some cases where we can use the one that makes the most sense.

For object storage.

```js
[“apple”, “pear”, “berry”]

{ fruit1: “apple”, fruit2: “pear”, fruit3: “berry” }
```

Arrays are better for item storage because it is the most straight forward way to store the item by just putting them in a array. With a hash, you can have it be storage but then each value would need a key so it would not be as efficient as an array.

For defining objects.

```js
[ ‘John’, ‘Doe’, 34 ]

{ first: ‘John’, last: ‘Doe’, age: 34 }
```

The array does store the values but we don't know what each value is. Where as in a hash, each value is paired off with a key. With a descriptive key name, we can know what the value we are storing and can refer to them by the key to pull out the right fields. With arrays if we switch the order than the values will change, but when we switch the key value pairs in the hash, we can still pull out the key we want.

Storing one value

```js
[“#fff”]
	
{ color:  “#fff” }
```

Either case would work but for a single value that we are storing, it is a bit of a overkill to use a array or a hash. A better way to store this value is with a variable and then reference the variable when we need to use it.

```
color = "#fff"
```

We may often times needs to combine the datatypes together to make a complex collection of items.

```js
users = [
	{ email: ‘bob’,  pass: ‘123’ },
  { email: ‘jill’, pass: ‘123’ },
  { email: jack, pass: ‘123’  },
	...
] 
```

With arrays of hashes, they really work with having a collection of objects. When we want to get the data out, we can treat it as a array first then as a hash to get the value it is that we want.

```js
stuff = {
  states: [ ‘az’, ‘ol’, ‘rv’, ‘fl’],
  colors: [ ‘red’, ‘green’, ‘blue’ ]
}
```

With hashes of arrays, they are really good at having define options of multiple varieties. We can have multiple arrays with it's own keys to define what it is that the array is storing. 

To wrap up, arrays are good at storing items while creating and storing objects are better off with hashes. With a single item, a array and a hash would not be the best and would use a variable instead. Lastly, you can using a combination of embedded arrays of hashes or hashes of arrays to have a collection of objects.