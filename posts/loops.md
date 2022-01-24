---
title: 'Loops'
date: '2020-06-20'
readTime: '9'
---

Another important concept that we often use in programming are **Loops**. 

> Run logic until a condition is met.

It is similar to a condition where it uses conditions to run the logic but it works differently since it runs the logic and continues to run the logic, until a condition is met. 

Loops are very good for iteration in a collection of objects, going through each element one by one. It is also good for running the same logic multiple times. Lastly another most common use case is for using in counting. Here is a example of what the structure of the loop looks like:

```js
x = 0

while (x < 5) {
	print “Hello”
	x++
}
```

We will start breaking this down in a sec but first we need to talk about what not to do with a loop. 

When we build the conditions, similar to conditionals, we would have to have the statements be contingent where it can be true or false, or else we would hit something called a **Infinite Loop** or not be able to run the loop at all.

> A loop that continues to run forever, or when the power runs out, or when the memory is full. 

Please **Do Not** do the loop below, because it is an example of an infinite loop.

```js
while (true) {
	print “Hello”
}
```

Because the condition is always met then it will print Hello til the end of time. The most important thing about infinite loops is to know how to stop or get out of them. It would vary depending on the programming language, so be sure to reference the program and language documentation, for example if it is in the terminal then the ctrl c would stop the loop. 

The other important item of infinite loops is to prevent them from happening by doing a **Base case** and a **Induction Step**. The base case is a starting point where it is able to progress through the loop. The statement should never be tautological meaning always true, because that is what causes the infinite loop and should always be contingent where it can be true and false. Lastly, you need an Induction Step, where it is a ways to get to the condition eventually, to get out of the loop when the condition is met. We will point out each of these items when we go through some examples. 

Here are the most common loops, they all work pretty much interchangable but the logic of how they work is slightly different. Depending on the languages, it might be called something different or the syntax is different, so be sure to refer to the official documentation of the technology you are using.
- for 
- for in
- for of
- while
- do while

We also have keywords of 
- break
- continue

We will also be talking about iterators, which may be confused to be a loop but it is not a loop and would iterate through a given set. It also does not repeat the logic however many times but go through items one at a time. 
- map
- filter
- for each 
- each with index

###### for
```js
let colors = [ “red”, “blue”, “green” ]
	
for ( let i = 0; i <= colors.length; i++) {
  print colors[i] 
}
```

The for loop would be a common loop that would also act as a iterator as well. The base case is the array of string of colors and that is our starting point. Our condition is while i is less than the length of the colors array. So it will continue to run the logic of printing out each color of the array. The induction step is the i++ which increases i by one so eventually i would be greater than the length of the array. 

- So when it runs, first i is 0 so since 0 is less than the length of 3 then it would print the color, so red, because we are calling the array by the index of the array, then it would do i++ to go to the next step. 
- Now i is 1, and 1 is less than 3, so it will print out blue and then increase i by one again. 
- Next i is 2, so then runs the logic to print out green then increase i by one again.
- Now i is 3 and 3 is now greater than or equal to the length of 3 so it would break out of the loop. 
- If we were to continue on then we would get a index out of bounds error, of it going beyond the length of the array. 

The next few loops will run the same logic but different loops, and you can use them interchangably. 

###### for in 
```js
let colors = [ “red”, “blue”, “green” ]

for ( let color in colors) {
  print color
}
```

Here we just reference each value by a variable name and we can call it what ever makes sense. 

###### for of
```js
let colors = [ “red”, “blue”, “green” ]

for ( let color of colors) {
  print color
}
```

###### while
```js
let colors = [ “red”, “blue”, “green” ]
	
let i = 0

while ( i <= colors.length ){
  print colors[i]
  i++
}
```

while would run the condition first and check it and then run the logic.

###### do while
```js
let colors = [ “red”, “blue”, “green” ]

let i = 0

do {
  print colors[i]
} while ( i <= colors.length )
```

Do while would run the logic first then the condition to check if it is met, so a bit backwards from a while.

Next would be iterators which is really good for going through arrays and hashes.

###### map
```js
let colors = [ “red”, “blue”, “green” ]

colors.map( color =>  {
  print color
}
```

###### for each
```js
let colors = [ “red”, “blue”, “green” ]

colors.forEach( color =>  {
  print color
}
```

###### each with index
```js
let colors = [ “red”, “blue”, “green” ]

colors.each_with_index( |color, index | {
  print index
  print color
}
```

This will give you the value and the index of the value, or if it is a hash then it would give you the key and value. 

###### filter
```js
let colors = [ “red”, “blue”, “green” ]

colors.filter( color => color.length > 3)
```

Filter would filter out what the condition is, so it would reverse of the other iterators.

Lastly, we are going to talk about the keywords that would give use more flexiblity of being in or out of the loop.

###### break
```js
let colors = [ “red”, “blue”, “green” ]

colors.map( color => {
  if (color === “blue”) { break }
  print color
}
```

Break will get out of the loop when it hits the keyword. In this case if the color is blue then it would break out of the loop and would not continue to run.

###### continue
```js
let colors = [ “red”, “blue”, “green” ]

colors.map( color => {
  if (color === “blue”) { continue }
  print color
}
```

Continue will run the next line of execution and would continue to run the logic or the next logic.

Loops are a very important concept to grasp and plays a key role for when we are programming. We just need to avoid infinite loops by having a contingent statement, with a base case and a induction step. Then we can utilize it in a variety of ways of counting, iterating, running repeated logic and much more!

