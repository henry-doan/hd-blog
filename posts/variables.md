---
title: 'Variables'
date: '2020-07-04'
readTime: '10'
---

Variables are a really important concept to understand in coding. We would use them often to:

> Store a reference to a object.

If we want to reuse the same object multiple times we can assign it to a variable so we can reference it for later. We can also assign or reassign variables to new values and reuse them as much as we can. 

Before we dive deeping in variables, we need to talk about **Scope**

> Where you have access to the variable.

Here are the different scopes we can work with. 
- Global
- File
- Class
- Instance
- Local / Code block

Scope is where we have access to the variable and with the different scopes we have difference accesses to the variables. This mean that we can use or not use the variable depending on what scope they have. So if it is global then we can use it machine wide. File scope is within the file. Class in within a class. Instance is a running instance of an object, so as long as we are using the instance then the variable is in scope. Finally local or code block is within a method or a opening and closing code block. Depending on the language you might have syntax to decide what scope it uses, or you might need to define the variable in what ever scope you are using.

Depending on the programming language it might be a different syntax to create and use variables so be sure to reference the documentation of the language you are working in. For the most part it follows this patter of 

```
Keyword name = object
```

If there is a keyword then it would go in the left. Then it would be the name of the variable. The = means assignment and not equality in this case so we are assigning this variable to a object. Here are some examples from different programming languages.
```
var name = ‘bob’

name = ‘bob’

@name = ‘bob’

String name = ‘bob’

```

With the value on the right, it can be any object that the programming language allows. We can also reassign the variable but referencing the name and the assigning it to a new value. This one does not need a keyword. Depending on the programming language it might be restricted to datatypes or it might not and you can change the datatype to whatever you want.

```js
var name = 'bob'
name = 'jill'
```

With naming variables, they are similar to 	[methods](https://hd-blog-drab.vercel.app/posts/method-functions) naming where it has to be: 
- Specific
- Follow the language best practice
- Uses the right scope 
- Don't use keywords

Please refer to the methods for more indepth naming conventions. Here are some bad examples of variable names.

```js
var x = [ ‘apple’, ‘orange’, ‘grape’ ]

class = [ ‘fall20’, ‘spring20’, ‘winter20’ ]

!@#$%^&**()*^%# = 4 
```

These are broad or they use keywords and symbols that would cause error or confusion. 

```js
var fruits = [ ‘apple’, ‘orange’, ‘grape’ ]

courses = [ ‘fall20’, ‘spring20’, ‘winter20’ ]

num = 4 
```

These are better examples because they are specific of what the variables are referencing and they do not use any keywords.

To use variables, you would need to define them with the right keyword and scope and then you can reference it but using the variable's name. But if you are not in the same scope and the variable then it will error out of not being the right scope or it doesn't know what you are referencing. 

```js
var fruits = [ ‘apple’, ‘orange’, ‘grape’ ]

fruits.map( f => print f )
```

You can also use variables in **String Interpolation** 

> Be able to use a value within a string.

The syntax may depend on the language
```
person = ‘sam’

“Hello #{person}!”         ->  ‘Hello Sam!’
`Hello ${person}!`        -> ‘Hello Sam!’
```

This will convert the variable as best as possible to a string datatype or error out. The would inject the string into the string you want to interpolate. So the above example will say hello same since it is converting the value of the person variable into a string and put it in the place we want it. This is really good for creating custom strings that would change based off of a variable. 

The next concept is similiar but different and that is **String Concatenation** 

> Combines strings and values into bigger strings 

String Concatenation utilizes the **+** between strings. Depending on the language, it might limit you of what datatype you can concatenate since it might limit you or wont covert to a string for. But will for sure work with the string datatypes.
```js
var person = ‘sam’

‘Hello’ + person          -> ‘HelloSam’
‘Hello’ + ‘ ‘ + person    -> ‘Hello Sam’
‘4’ + ‘4’                 -> ‘44’
```

So this would put together strings into bigger strings. It would take the string as a literal of what you put into the string so the string of Hello concatenated with person which is a sam string it would be helloSam with no spaces because we are squishing them both together into a bigger string. So if we want to have a space then we would need to concatenate the space where we want it. Also if the string has other datatypes in the string, it is still a string and would treat it like so. So that is why in the last line we have 44 since it is a string of 4 and 4 concatenated together.

With variables you are able to store objects as references to be used later. When we name them we would need to be specific, avoid key words and even define the scope of where we have access to the variable. When we use them, we can only use them in scope, and we can use them in string interpolation, string concatenation and storing values we need. We just reference the variable by the name and we can use the reference it is storing. Finally we can reassign variables to different values we want to now reference. 