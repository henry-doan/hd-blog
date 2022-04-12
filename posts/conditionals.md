---
title: 'Conditionals'
date: '2020-06-14'
readTime: '8'
---

One of the main logics that we use for programing are **Conditionals**:

> Run logic when a condition is met. 

With the condition, the condition has to be satified for the logic to be met. and is not tautological and not contradiction but a contingent conditions. You can read more about conditions [here](https://hd-blog-drab.vercel.app/posts/comparators). We should also have the most specific condition at the top so it can be ran first if the condition is met.

Here are the most common types of conditionals:
- If else 
- Case / Switch
- Ternary 
- Unless
- Begin / Rescue / Else

There are also some key words that will run extra logic or diverge the logic somewhere else. 
- Next 
- Break 
- Continue 

The conditionals change of how we write them depending on different languages but the structure and how it works will all be the same. So be sure to reference the official documentation of the language you are working in. 

All the conditonals all work the same but we can use different conditionals to achieve the same results. It really doesn't matter which one you want to use, just use the one that makes sense to you. Here are some examples in Javascripts.

```js
if ( num % 3 === 0 ) {
	print “Fizz”
} else if ( num % 5 === 0 ) {
	print “Buzz”
} else if ( num % 3 === 0 && num % 5 === 0 ) {
	print “Fizz Buzz”
} else {
	print “error”
}
```

This is the most common conditional which is a **If Else**. With this one, you don't need all the elements of the if and elses. What I mean is that you can have just a if 

```js
if ( num % 3 === 0 ) {
	print “Fizz”
} 
```

or andif with an else if
```js
if ( num % 3 === 0 ) {
	print “Fizz”
} else if ( num % 5 === 0 ) {
	print “Buzz”
}
```

or an if else 

```js
if ( num % 3 === 0 ) {
	print “Fizz”
} else {
	print “error”
}
```

You just can't have a else or an else if by it else, it would have to start with an if. How an if else works, is that it would go from top to bottom, of if the condition is met then it would run the logic of the code block. If it is not then it would move on to the next condition, then the next, until the condition is met. If all else then run the else of the statement. The else doesn't need a condition and would run when all the conditions above have not been met then it acts as a default. 

With this conditional this is FizzBuzz, Where if a number is divisible by 3 then print Fizz, if the number is divisible by 5 then print out Buzz, if it is divisible of 3 and 5 then print out Fizz Buzz. So For each condition we have one to check if the number is divisible by 3. Then else if divisible by 5 and then else if divisible by 3 and 5. Finally the Else is given and error because it is not meeting the conditions above. Once the condition is met, then it would run the logic and then it would get out of the conditional and not run any more logic. 

This conditional works but there is a case where it would not work. So if number is 9 then it would print out Fizz, if it is 10 then it would print out Buzz. 11 Will give you an error, so so far the inputs matches with what is expected so far with FizzBuzz. But when number is 15, we would expect it to print out FizzBuzz but it would hit the first condition of if divisible by 3, which 15 is then it prints out Fizz and then it stops. How to fix this is to put the most specific condition at the top, so that way, for the cases where it is more specific will trigger first then the basic ones.

```js
if ( num % 3 === 0 && num % 5 === 0 ) {
	print “Fizz Buzz”
} else if ( num % 3 === 0 ) {
	print “Fizz”
} else if ( num % 5 === 0 ) {
	print “Buzz”
} else {
	print “error”
}
```

Now if nubmer is 15, then it would print out the desire result. 

The next one is a **Case / Switch** conditional, and it would similiar with a if else, so it would run each condition one by one. In the ruby langauge it is case when, but in js it is switch case, so reference the documentation for the right syntax.

```ruby
case ( num )
when ( num % 3 === 0 && num % 5 === 0 )
	print “Fizz Buzz”
when ( num % 3 === 0 )
	print “Fizz”
when ( num % 5 === 0 )
	print “Buzz”
default 
	print “error”
```

Sometimes, depending on the language, the switch statement will continue to run each condition, even though the condition have been met. That is where the key work break would be of use. Break would break you out of the conditional.

```ruby
case ( num )
when ( num % 3 === 0 && num % 5 === 0 )
	print “Fizz Buzz”
	break
when ( num % 3 === 0 )
	print “Fizz”
	break
when ( num % 5 === 0 )
	print “Buzz”
	break
default 
	print “error”
```

Next and continue would go to the next line of execution if you choose so to use it.

Lastly, we are going to cover **Ternary** which is a one liner for a if else statement.

So this if else:

```js
if (name === “bob”) {
	print “hello!”
} else {
  print “you’re not bob”
}
```

would become:

```js
name === “bob” ? print “hello!” : print “you’re not bob”
```

It looks very cryptic at first but here is how it works:

> Condition ? If : Else

So the condition is on the left, followed by a question mark. After the question mark is what would happen if the condition is met. Then followed by a colon, of what happens when the condition is not met or the else. 

I would recommend to tranform simple if elses into ternaries so you can get the hang of how they work. 