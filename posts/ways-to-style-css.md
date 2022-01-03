---
title: 'Ways to style, with CSS'
date: '2017-11-28'
---

## CSS
CSS or Cascading Style Sheet is allows us to style our HTML elements using rules. CSS can style the sizing, typography, colors and positioning content on the page. Depending on the style, it is good to note that not all styles are supported on all browsers.

### Ways to Style
There are three ways to style a web page, in line styling, style tag, and another file styling. 

**In line styling** is styling inside the element itself.

```HTML
<h1 style="color: red; font-size: 24px"></h1>
```

**Style tag** styling is using the style tags and putting styles in between the style tags.

```HTML
<style>
h1 {
  color: red;
  font-size: 24px;
}

.nav-bar {
  background-color: green;
  opacity: 0.3;
}

</style>
```

Last but not least is the most recommended and best practice is to have all the styles in a .css file

```CSS
/* in a style.css file */

h1 {
  color: red;
  font-size: 24px;
}

.nav-bar {
  background-color: green;
  opacity: 0.3;
}

```

### How to make a CSS file 
CSS files end in .css and like HTML files are case sensitive and it will tell web browsers that it is an CSS file and it is the **styles** of the web page. Before the .css is the name of the page, and for best practice for the main styles the name is main.css or style.css. 

Here are some examples below:

```
main.css
contact.css
about.css
style.css
```

To create an CSS file similarly to HTML there are two best ways. The first is if you right click on where you want the file to be there might be an option under new to have a new file and name it something ending in .css. The other way is what developers do to create one, is opening up the terminal and the change directory to where you want the file to be and then run this command:

```shell
touch style.css
```

### How to connect a style sheet to the HTML document

In the HTML file or document, in order to have the element have the styles you would have to connect it. You don't need to connect the styles if you are doing in line styling or with the style tags because it is in the document itself. For another file styles, you would have to add this line in the head of the document that says what the file is, the relationship it has and where the file is in retrospect of where you are. For example if your style.css is in the same folder then in the href you would put "style.css". If it is in side of a folder or directory, it is "foldername/style.css". If is it out side then it is "../style.css".

```HTML
<head>
  <title>My Website</title>

  <!-- this is how you link the stylesheet to a HTML file inside of your HTML file -->
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
```

### Syntax
The **Syntax** for the CSS language is a very different than the HTML **Syntax** and it has two parts a **Selector** and a **Declaration**. **Selectors** are used to select elements that you want to manipulate.**Declarations** is how you want to manipulate the element and is encased in { } brackets. Declarations have a **Property** and a **Value** to manipulate the element and ends each manipulation with a semicolon ; .

```CSS

p {
  color: red;
}

/* 
  - p is the selector
  - everything in the { } is the declaration
  - color is a property
  - color is a property
  - ; ends the line of the what you want to declare

  You can have multiple declarations such as below.
 */

h1 {
  padding: 10px;
  color: green;
  font-size: 32px;
}

```

Here is a resource of all the properties you can use on an element:

>Link to the [CSS Properties](https://www.w3schools.com/cssref/)

### Selectors
In CSS, Selectors really depend on what you want to change. 

```CSS
h1 {

}

#id_Name {

}

.class_name {

}
```

You can select certain HTML elements by their class, id or by the element itself. Also be aware that if you select a certain selector in the CSS, all of the elements that the selector will share all the styles. For example, if you have a selector of h1 that means all of the h1 on the page will have the style specified in the CSS. Sometimes you might not want all the h1 ones to have the styles that are why using classes and ids are recommended in for selectors in CSS.

In CSS you can also chain selectors together to span the same styles across from elements. You can do this by adding commas after each element selector.

```CSS
h1, p, b {
  color: green;
}
```

If you have embedded elements in the HTML such as:

```HTML
<div class="box">
  <div id="little_box">
    <p>Doll</p>
  </div>
  <div id="big_box">
    <p>Toy</p>
  </div>
</div>
```

To just style the p tag with the doll you can put a id or class on it or you can list the embedded parent selectors of where the p tag is. you can do this by listing each of the parent element selector and having a space after each listing.

```CSS
.box #little_box p {
  color: blue;
}
```

### CSS Comment
This is an example of a CSS comment:

```CSS
/* This is a CSS comment */
```

Like HTMl comment and every comment everything in the comment will not run or show up in the browser. The same purposes as a HTML comments. You can also do single line comments or multi-line comments as well.

This is an example of a single line CSS comment:

```CSS
/* This is a single line CSS comment */
```

This is an example of a multi-line CSS comment:

```CSS
/* 
  This is a 
  multi-line CSS 
  comment. 
*/
```