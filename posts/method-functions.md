---
title: 'Methods / Functions'
date: '2020-07-15'
readTime: '6'
---

When we are coding, technically we could write all the code all in the file and then it would run top to bottom. But usually we don't program like that but we would break up our code into small manageable chunks called **Methods / Functions**

> Group of code that performs a specific task.

This is a better way to code so we can break up our code and encapsulate them together with a common function and return a value. So you can bundle together code all in one method. So then when we write it this way it can run by order of execution instead of the whole file top to bottom. If you are doing multiple things in one method, you might need to break it up into smaller methods. Also when there is an error then it would point you in the right direction of what method it is happening in and better for error handling. 

You are probably wondering what's the differences between functions and methods? well... there are none and the terms can be used interchangably and mean the same thing. Depending on programming languages however, they would use one term over the other. Such as in Ruby it is called methods, and in Javascript it is called functions, so it really also depends on the language of what term you are using.

This also leads into the term of **Scope**

> Where we have access to a variable or parameter. 

There are different kinds of scopes
- Global
- File
- Class
- Instance 
- Local / Code Blocks

With the methods, if we have variables and parameters that are defined in the methods, then the scope is to be only used in that method and you can't use it in other places because it will be out of scope.

There are also two kinds of methods, one that passes parameters / arguments and one that doesn't.

```js
function sum() {
	return 4 + 1
}

sum()

function sum(num1, num2) {
	return num1 + num2
}

sum(4, 1)
```

To use a function, it really depends on the programming language so be sure to reference the official documentation of the language you are working in. 

For JavaScript, there is a function key word to create functions, and then it is followed by name of the function and some syntax. Then in the function we can run code and whatever we want to return we can do so with the return keyword. If we have parameters / arguments, we would pass them within the parathesis and we can reference them by what ever makes sense and use those terms to represent the different arguments passed in. To use the function we would call it by it's name and the syntax. If it has some arguments then we need to pass in the right amount of arguments and order does matter so the first argument is the first value passed in and the second argument is the second value passed in and so on.

So in this function it is a sum function and would return 5 when we call it by it's name. 

With the second function, we need to pass in two arguments, num1 and num2. So when we call the function, we would need to pass in values for num1 and num2. So 4 is num1 and 1 is num2. So the return value when we call the function will be the sum of the two values.

Even though this example is a simple one, we can reuse the same logic over and over again but calling the method name and pass in different arguments. This really helps keep our code D.R.Y since we can use code in the methods multiple times without having to rewrite the same logic. 

Next we will be discussing about naming the function. We could technically name it what ever we want.

```js
function x() {
  ...
}
function function() {
  ...
}
```

But there are a few problems naming the functions these ways. The first function it is too broad and I really don't know what the function does. When we are programming, we are doing so in a open source community so other people may not understand what that means. Even if you aren't working with other people, when you come back to the code later, you may not even know what that function does. So we should have a specific function name describing what the function does or what it is for so it is easy to understand the function more. The second function will give you an error because it is using a reserve keyword. In programming langauges there are keywords that are reserved for naming because they do something or represent something in that language. It is impossible to learn them all and varies depending on programming languages so you can look up the reserve words based off of the language you are working in. Most common reserve words are:
- class
- type 
- string 
- integer
- date 
- etc.

If you do need to use a word like the reserve word try to be even more specific of what it is for. For example, instead of type, you can do user type. 

Functions also follow the programming language best practice such as the different casing of name. So you would follow the convention of the language you are working in. Here are the most common ones:
- camelCase
- snake_case
- PascalCase
- kebab-case


So when you are naming a function you should:
- Be specific
- Follow the programming language best practice
- Don't use keywords
- Name what the function is doing or is for

```js
function sum() {
  ...
}
function printCars() {
  ...
}
```

Whether we call them methods or functions it really matter depending on the programming language and the convention of what we are working with. But they are for grouping common code that performs a specific task. With it we can pass in parameters / arguments and have the scope within the function itself. It is better to name the function as specific of what the function does or what it is for, that way we can utilize it to built out our awesome programs!