---
title: 'The Box Model'
date: '2018-11-11'
readTime: '4'
---

All HTML tags generate content to a web page and all of the content on the page is wrapped within a box. This is called the **Box Model** and inside of this box, we are able to add positioning, styles, spacing and borders on HTML elements.

**Content**
The inner most section of the box model is the **content** where it consist of the HTML tags and what they contain. With the content you can manipulate the width and height of the content with using units of measurement.

```CSS
h1 {
  width: 40px;
  height: 100px;
}
```

**Padding**
One level outside of the content is **padding**. With padding you can change the spacing around the content.

```CSS
h1 {
  padding: 10px;
}
```
For padding, if you set one value, all of the sides will be the value that is inputted. For the example above, the h1 element will have 10px on the top, right, bottom, left sides.

If you set the value of padding to have two measurement then the first number will be the padding of the top and bottom sides and the second number will be for the left and right padding as follows:

```CSS
h1 {
  padding: 10px 30px;
}
```

This h1 element has the padding of 10px for the top and bottom and 30px for the left and right padding.

Having four values for padding gives spacing for all the sides and specifies the padding of top, right, bottom, and left.

```CSS
p {
  padding: 10px 30px 60px 15px;
}
```

The above element has the padding of 10px for the top, 30px for the right, 60px for the bottom, and 15px for the left side.

Finally, the padding can be declared on multiple lines instead of a single line where you can specify padding on certain sides.

```CSS
h3 {
  padding-top: 20px;
  padding-right: 10px;
  padding-bottom: 30px;
  padding-left: 15px;
}
```

**Border**
One layer outside of padding is **border** and in this level of the box model, not only can we manipulate the size and position, but also we can manipulate the styles.

The border specifies the edge of the padding and we can have it look a certain way.

For example, to add a border to an element, you do the following:

```CSS
img {
  border: 3px solid green;
}
```

The example above uses just the border property and takes in three arguments, the first being the size of the border, second is the type of border, and the last is the color of the border.

In the example, the image tag has a border 3px thick, with a solid type of border style, and lastly is colored green.

The declaration of the first argument takes in a unit of measurement for the border size. The last argument takes in any color using the color css conventions.

The second argument assigns a style to the border and can be one of these options:

- none
- hidden
- solid
- dashed
- dotted
- double
- groove
- inset
- outset
- ridge