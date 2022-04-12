---
title: 'Importance of Spacing and Indentations'
date: '2020-08-08'
readTime: '8'
---

First off, this isn't a post about spaces vs. indentation or else it would spark a wild debate but it is the importance of using both spaces and indentation, especially when you are writing code.

When we talk about coding **conventation** we are referring to 

> Coding best practices.

Items you should do, and recommended to do when you are coding. Using spaces and indentation is for me, arguably one of the most important, is to use proper spacing and indentation. 

Yes, there are some coding languages where you don't need it or it doesn't matter and there are other coding languages where you do need them. Such as in Python, spaces and indentation mean a new code block while in html you can it any ways and it will still work. Regardless of the langauge, you should still utilize them for the reasons I am about to list. 

Let's look at this example here:

```html
<html><head></head><body><div><h1>Hello</h1><p>World!</p></div></body></html>
```

In HTML, this would still compile and won't throw any errors and would work. But it is missing spacing and indentation. One of the reasons of why we should use them is to have better open source code. Meaning that we should have the readability of the code be more clear. If this was any longer, than we would have to scroll side to side and would be harder to read if it was any longer. If you are working with a group or even later down the line you come back to this project, it is hard to go through code that is all in one line or have poor spacing and indentation.

The other reason is for organization. 

This:
```html
<html><head></head><body><div><h1>Hello</h1><p>World!</p></div></body></html>
```

vs.

```html
<html>
  <head></head>
  <body>
    <div>
      <h1>Hello</h1>
      <p>World!</p>
    </div>
  </body>
</html>
```

You can now see the different parts of the code and how there are items inside of or part of other items. It visually shows that too with the same indentation and spaces all are part of the same group and more indentation is something embedded in the element. Even though the computer will read it either way, it is much more better for us to see which parts go where. The good rule of thumb is to have the same spacing and identation for all elements, and the embed them in once there is another layer or and element is in another element and continue if needed.

The next reason is for error handling. If I had this:

```html
<html><head></head><body><div><h1>Hello</h1><pWorld!</p></div></body></html>
```

My error would probably say your error is somewhere on line 1. Well... so is the rest of the code. So it is harder to track down.  

```html
<html><head></head>
          <body>
    <         div>
          <h1>Hello</h1><pWorld!</p> </div>
                   </body>
</              html>
```

Even with this example of poor use of spacing and indentation, it is also hard to track down since it is harder to pinpoint where the error could be. 

But with the right amount of spaces and identation, the error message would throw you in the exact line of where it is erroring or around that area is where the error is. 


```html
<html>
  <head></head>
  <body>
    <div>
      <h1>Hello</h1>
      <pWorld!</p>
    </div>
  </body>
</html>
```

In this case the error is around line 6. So because of spaces and indentations, you can check code blocks to see if any sections look off. Like if there was a pattern you always do with spaces and indentations, and an error occur, then it might be at the place where the pattern doesn't match or start to veer off. Here, we are missing a > at line 6 and it is easier to find and add that in.

Lastly, there are some cases where spaces do matter and having them means something else in program. Such as:

```
npm install reactbootstrap
```

vs.

```
npm install react bootstrap
```

For this example, in the npm install command, a space mean another package, and no space mean that it will loock for that package with that name. So for these cases, you would have to dig in to the languages, and programs documentation and research when to not and do use spaces and indentations. 

Next, are some common conventions to have with spaces and indentation. 
- Have 2-4 tab indentation
- Indent embedded elements
- Utilize spaces for better readability
- Consistent on the space and indentation pattern you use.
- Line break on every element 

**Have 2-4 tab indentation** This is a standard practice of setting the tab size to be 2 or 4 spaces so for everytime you use tab, then it will be the same size.

**Indent embedded elements** This will further enhance readability and organization of your code for you and your team to read.  

**Utilize spaces for better readability** This is mostly for readability and to have things not as bunched up on a line of code. For example: 

```js
({name:'bob',age: 43})
```

vs.

```js
({ name: 'bob', age: 43 })
```

**Consistent on the space and indentation pattern you use** When you use spaces and indentation, you should be consistent with them and always use them and use them in the same pattern as the rest of the code. A bad example would be:

```html
<html>
        <head></head>
  <body>
    <div>
                  <h1>Hello</h1> <p>World!</p>
        </div>
        </body>
  </html>
```

This is kinda hard to see where things start and where things end and it also have the readability of the code go more down hill.

Lastly,

**Line break on every element** This help group elelments together and keep them organized. 

Spacing and Indentation play a huge role in writing code in more ways than one. It keeps our code organized, readable, helps us reduce errors in following pattern of how we space and indent. Make sure to always follow the convention of the coding language you are working in and follow those, but for the most part you would use them on a daily basis. 