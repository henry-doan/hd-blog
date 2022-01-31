---
title: 'JQuery'
date: '2018-12-19'
readTime: '20'
---

When we are working in programming languages we often times would use **Libraries**

> Predefined code that we can use in our projects.

Some languages may call it something else like packages, gems, etc. so it would be referenced on the language documentation. But there are also built in libraries that are included in the programming language or tool that you are using. There are also external packages you can use with CDN or with library managers.

One library we are going to go over is **JQuery**. It is a JavaScript library that allows to do some JavaScript shortcuts. So it would do the same logic like JavaScript but with less code with other syntax. This will allow you in web developement to manipulate the [DOM](https://hd-blog-henry-doan.vercel.app/posts/dom) and allow you to change the structure, layout, and styles of your web page as well as run logic more efficiently. Here are a few examples of what JQuery can do:
- HTML / DOM manipulation
- CSS manipulation
- HTML event methods
- Effects and animations
- AJAX / Sending requests over a network
- Finding elements on a page
- Changing HTML content
- Listening for user interaction
- Animate content

For the next part, we are going to go over some examples of how to use JQuery and the syntax of what we can do with it.

The next part would go over some HTML, Command Line, CSS, and JS. Be sure to know the basics or review them before moving forward.

Let's create the project files:
```
mkdir jquery_project
```
```
cd jquery_project
```
```
touch index.html main.js
```

index.html
```html
<html>
 <body>
   <h1>Hello World</h1>
   <p>My first JQuery App</p>
 </body>
</html>
```

The next part is to add JQuery into the projects and there are 2 ways to do this. 
1. CDN or Content Delivery Network
  - You can grab the latest version [here](https://releases.jquery.com/)
  - I would recommend slim minified or minified and that would give you the code you need for embedding for the HTML.
2. Download and add.
  - You can download JQuery [here](https://jquery.com/download/)
  - I would recommend the latest stable version and that is compressed so it save space. Be sure to save it in the project folder

We will be using the CDN method since it is the most popular but be sure to change the version to the latest one. 

index.html
```html
<html>
 <body>
   <h1>Hello World</h1>
   <p>My first jQuery App</p>

   <script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
   <script src="main.js"></script>
 </body>
</html>
```

Note that we have included JQuery before our JavaScript file. This is important because jQuery must be loaded before we can use it in our own files. We also have it towards the bottom of the HTML file because we want to load all the content first then do the JS to change it. 

Next we will be in our JavaScript file. The first thing we want to do is assure that all of our HTML is loaded before any of our JavaScript code runs.
NOTE: JQuery methods begin with $

main.js
```js
$(document).ready( function() {
 //Our code will go here
});
```

#### Syntax
Basic syntax:
```js
$(selector).action()
```
- A $ sign to define / access jQuery
- A (selector) to 'query (or find)' HTML elements
- A jQuery action() to be performed on the element(s)

main.js
```js
$(document).ready( function() {
 var header = $('h1')
 console.log(header)
})
```

When the page loads let's find our h1 and log it to the console

Now lets open the HTML file
terminal:
```
open index.html
```

Open up chrome dev tools and look at the console tab.  There is the element!

Now let's print the text of our H1 do the console.

main.js
```js
$(document).ready( function() {
 var header = $('h1').text()
 console.log(header)
})
```
Next let's change the text

main.js
```js
$(document).ready( function() {
 $('h1').text('This is the new text')
})
```

What if we had multiple h1's on the page?
index.html
```html
<h1>Hello World</h1>
<p>My first jQuery App</p>
<h1>I don't want this text to change</h1>
```

Refresh your browser and see what happens...

jQuery accesses elements as an array so we have some options for only changing the elements we intended to target.

The first  way would be accessing only the first element that matches h1
main.js
```js
$(document).ready( function() {
 $('h1:first').text('This is the new text')
})
```
A better approach would be to give the element a unique identifier
index.html
```html
<h1 id="title">Hello World</h1>
```

main.js
```js
$(document).ready( function() {
 $('#title').text('This is the new text')
})
```
NOTE classes are found with a . and id's are found with a #

You can find elements by class id or tag.
Examples:
```js
$('p').hide() 
```
  - hides all <p> elements
```js
$('#test').hide()
```
  - hides the element with an id of test
```js
$('.red-label').hide()
```
  - hides all elements with the class of red-label


## Bringing It All Together
