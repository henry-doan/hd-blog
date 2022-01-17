---
title: 'Comparators'
date: '2020-06-13'
readTime: '4'
---

When you are working with making coding statements, loops or conditionals, you are going to encounter some comparators. Which: 

> Compares two items or create conditions and results in returning a boolean value.

Here are the different types of comparators:
- ==
- ===
- !=
- !==
- !
- <
- &gt;
- <=
- &gt;=
- &&
- ||

And these are the common ones you would see across languages but some languages may or may not have these or they are different within the language, so refer to the official coding language documentation for the right reference. 

Something that isn't a comparator is:

- = 

This is a comparator in some languages where it does mean equals, but in most other languages this means assignment and reassignment of variables. So even though in math this is equals, in programming this means assignment, and we have something else for equality. 

###### ==
 
> Equality in value

```
5 == “5”              true
5 == “h”              false
```

###### !=
 
> Inequality in value
> Not equal

```
5 != “a”                true
5 != “5”                false
```

###### ===
 
> Equality in value and type

```
5 === “5”            false
5 === 5               true
```

###### !==
 
> Inequality in value and type

```
5 !== “a”                true
5 !== “5”                true
```

###### <
 
> Less than

```
4 < 10                   true
3 < 2                    false
4 < 4                    false
```

###### <=
 
> Less than or equal to

```
4 <= 4                   true
7 <= 2                   false
```

###### &gt;
 
> Greater than

```
1 > 0.2                  true
2 > 22                   false
2 > 2                    false
```

###### &gt;=
 
> Greater than or equal to

```
2 >= 2                   true
8 >= 6                   true
```

###### &&
 
> And
> Both sides needs to be true to be true otherwise false.

```
5 > 2 && “X” !== 3             true
5 < 2 && “X” !== 3             false

userNum >= 0 &&  userNum <= 10
```

###### | |
 
> Or
> At least one side needs to be true to be true

```
5 > 2 || “X” !== 3            true
5 < 2 || “X” !== “X”          false

userName === “Bob”  || userNum <= 10
```

![how comparators works](https://res.cloudinary.com/doan/image/upload/v1642381537/How_comparators_works_osb05t.png)

When we are comparing items, the items we are comparing should be specific, meaning that we should be clear of what it is we are comparing. When we are creating statements, we should not be **Tautological** and not be **Contradiction** but **Contingent**.

###### Tautological 
Is creating statements that are:

> Always returns true in every way.

```
true  === true
5 != 6
```

The reason why we shouldn't be tautological, is that if it is always true then the statement will always be true so our logic is always right and will always run. 

###### Contradiction 
The opposite of tautological is creating statements that are:

> Always returns false in every way.

```
true  === false
5 === 6
```

The reason why we shouldn't be contradiction, is that if it is always false then the statement will always be false so our logic is never right and will never run. 

So we need a common ground between the two, which is:

###### Contingent
 
> Can return true and false

```
Person[:name] === “Bob”
```

This is what we build statements off of and can run logic based off of the different results. We aren't always having anything always true or always false, it can be true or false. This also helps with avoiding infinite loops and dead code. 

There are a lot of comparators we can use, and some of them work the same way as in math, others works slightly different. Comparators are there to help you create very powerful statements to use in conditionals and loops. When we right them in a contingent way, we can assume to be able to have some branched off logic. 