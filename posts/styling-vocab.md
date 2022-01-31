---
title: 'Styling Vocab'
date: '2020-01-08'
readTime: '3'
---

In CSS there are some terms we would go over and that would be in what we are doing with CSS so we are going to break those down here. 

When we want to style, we need to know what we are going to style and that is where **Selectors** comes in. 

> CSS selectors are used to "find" (or select) HTML elements based on their element name, id, class, attribute, and more.

Here’s an example of multiple selectors:
```css
p, div, .button {
  background-color: purple
}
```

The selectors is the p, div and .button in this example. 

But Selectors can be HTMl elements that make up the HTML stucture. 

IDs, that you can put in the HTML element to let you set apart different elements from one another and be more specific of what you want to style.

In the HTML:
```html
<h1>Hello</h1>
<h1 id="title">World</h1>
```

In HTML you would put id as a property in the HTML element and then you can name it whatever that makes sense. 

In the CSS you would need to use a # to reference the id. 

```css
#name-of-id {
  color: blue
}
```

Another way you can select elements that would set apart from another element is Class.

In the html it would be a class property of what ever makes sense.
```html
<button class="primary">Send</button>
<button>Cancel</button>
```

To select an element by class is to use the . infront of the class name.
```css
.primary {
  background: aliceblue;
}
```

Now that we have ways to select the elements with Selectors, we will go into the syntax of CSS. 

It would start off with the selector or selectors and separate by commas if there are multiple. Then it is a pair of curly braces, then it would be what CSS property you want to style followed by a colon. Then the value of the property followed by a semicolon then you can do more properties. 

Here is a list of CSS [properties](https://www.w3schools.com/cssref/)

```css
h1 {
  color: blue;
  font-size: 12px;
}
```

These are just some basic styling and CSS vocab, there are a lot more you can do with them and how we can style and animate.