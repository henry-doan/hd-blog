---
title: 'JQuery'
date: '2018-12-19'
readTime: '45'
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

#### Subscription Application:
Let's say we have an application where a user can sign up for some subscription.  The price can change depending on if they pay monthly or yearly.  Let's set up our index.html to reflect this:

index.html
```html
<html>
 <body>
   <h1 id="title">Super Cool Service</h1>
   <h2 id="price">$10.00 /mo</h2>

   <p>Choose a plan</p>

   <select id="plan">
     <option value="monthly">Monthly</option>
     <option value="quarterly">Quarterly</option>
     <option value="yearly">Yearly</option>
   </select>

   <script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
   <script src="main.js"></script>
 </body>
</html>
```

Next let's create an event listener.  This will listen on a DOM element for a users actions and perform some JavaScript when that happens.

main.js
```js
$(document).ready( function() {
 $('#plan').on('change', function() {
   var priceText;

   switch(this.value) {
     case 'monthly':
       priceText = '$10.00 /mo';
       break;
     case 'quarterly':
       priceText = '$9.00 /mo';
       break;
     case 'yearly':
       priceText = '$7.00 /mo';
       break;
   }

   $('#price').text(priceText)
 });
});
```

We are listening for an element with an id of plan to change.  When this happens an event is triggered.

In this case `this` refers to the element that fired the event (The select).  We are switching on the value of the select which will be the value of the option that was selected.  Finally update the price header with the appropriate text.

Next we will create a cart section so a user can add the item to their cart.

First we will update our HTML to give us 2 sections.  Pricing on the left and the cart on the right:

index.html
```html
<html>
 <head>
   <link rel="stylesheet" href="styles.css" />
 </head>

 <body>
   <div id="wrapper">
     <div id="options">
       <h1 id="title">Super Cool Service</h1>
       <h2 id="price">$10.00 /mo</h2>
       <p>Choose a plan</p>
       <select id="plan">
         <option value="monthly">Monthly</option>
         <option value="quarterly">Quarterly</option>
         <option value="yearly">Yearly</option>
       </select>
     </div>
     <div id="cart">
       <h1>Cart</h1>
       <hr/>
       <ul id="in_cart">
       </ul>
     </div>
   </div>

   <script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
   <script src="main.js"></script>
 </body>
</html>
```

styles.css
```css
#wrapper {
 width: 100%;
 overflow: hidden
}

#options {
 width: 50%;
 float: left;
 border-right: solid 1px black;
}

#cart {
 margin-left: 51%;
}
```

Next we will add an Add to card button.
index.html
```html
...
</select>
<button id="add">Add To Cart</button>
...
```

Now let's create a click handler to "Add To Cart"
main.js
```js
...
$('#add').on('click', function() {
  var plan = $('#plan')
  var installment = plan.val();
  var price = $('#price').text();
  var inCart = $('#in_cart');
  inCart.append('<li>' + installment + ' - ' + price + '</li>')
});
```

Next let's create a running total:
index.html
```html
...
<div id="cart">
 <h1>Cart</h1>
 <hr />
 <ul id="in_cart">
 </ul>
 <h2 id="total">$0</h2>
</div>
...
```

Next we need to keep a running total.  If monthly we add the price * 1, if it's quarterly we add the price * 4, and if yearly price * 12.  We could have an easier time accessing the price if we added a data attribute to each li.
main.js
```js
...
$('#add').on('click', function() {
 var plan = $('#plan')
 var installment = plan.val();
 var price = $('#price').text();
 var inCart = $('#in_cart');
 var numeric = price.replace(/[[A-Za-z$\/\s]/g, '')
 var data = 'data-price="' + numeric + '" data-plan="' + installment + '"'
 inCart.append('<li class="entry"' + data + '>' + installment + ' - ' + price + '</li>')
});
```

Next let's add a function to update the total
main.js
```js
$(document).ready( function() {
 function updateTotal() {
   var total = 0;

   $('.entry').each( function(index, entry) {
     var data = $(entry).data();
     var price = parseFloat(data.price)
     var installment = data.plan
     switch(installment) {
       case 'monthly':
         total += price;
         break;
       case 'quarterly':
         total += price * 4;
         break;
       case 'yearly':
         total += price * 12;
         break;
     }
   })

   $('#total').text('$' + total);
}

.....
$('#add').on('click', function() {
   .....
   updateTotal();
})
```

Next let's create a way to remove an item from the cart
Add this to the <li> created in $('#add')
main.js
```js
'<button class="remove">X</button></li>'
```

Let's add an event listener for this button:
main.js
```js
...
$('.remove').on('click', function() {
 alert('Button clicked');
});
```

Notice that clicking these buttons doesn't work.  This is because the button was created dynamically after the listener was created so there is no listener attached.  To get around this we can attach the listener to the document instead of the button.
Replace $('.close') with:
```js
$(document).on('click', '.remove', function() {
```

Next we can remove the item from the cart
```js
$(document).on('click', '.remove', function() {
 ...
 updateTotal();
});
```

Next let's create a way for the user to empty the cart:
index.html
```html
....
<div id="cart">
 <h1>Cart</h1>
 <hr />
 <button id="empty">Clear Cart</button>
 <ul id="in_cart">

....
```

main.js
```js
function updateTotal() {
 var total = 0;
 var entries = $('.entry')

 if (entries.length)
   $('#empty').show();
 else
   $('#empty').hide();

 entries.each( function(index, entry) {

....

$('#empty').on('click', function() {
 $('#in_cart').empty();
 updateTotal();
});
```

Next let's add some css so the button doesn't show up when the page is first loaded:
styles.css
```css
#empty {
  display: none;
}
```


#### Animations
Let's make it so the user can show / hide the cart.
index.html
```html
<button id="add">Add To Cart</button>
<button id="display_cart">Hide Cart</button>
```

jQuery Selectors
main.js
```js
$('#display_cart').on('click', function() {
 var cart = $('#cart');
 var button = $(this);
 if (button.text() === 'Hide Cart')
   button.text('Show Cart')
 else
   button.text('Hide Cart');

 cart.slideToggle();
});
```

We can also pass options to the animation
```js
//animate slowly
cart.slideToggle('slow');

//animate quickly
cart.slideToggle('slow');

//animate over time
cart.slideToggle(3000);  // 3 seconds or 3000 milliseconds
```

We can also do any animations with the .animate method:
Let's make a checkout status element
index.html
```html
 <h2 id="total">$0</h2>
 <div id="complete"></div>
<button id="purchase">Purchase</button>
</div>
```

main.js
```js
$('#purchase').on('click', function() {
$('#complete')
  .html('<h2>PURCHASE COMPLETE<h2>')
  .css({
    'background-color': '#bca',
    'width': '25%',
    'border': '1px solid green',
    'text-align': 'center'
  })
  .animate({
    width: "70%",
    opacity: 0.4,
    marginLeft: "0.6in",
    fontSize: "3em",
    borderWidth: "10px"
  }, 1500 );
});
```