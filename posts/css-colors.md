---
title: 'CSS Colors'
date: '2018-12-29'
---

### CSS Colors

In CSS, color is represented in a number of different ways and it is just up  to the developer to choose what is more useful to code.

The first way is with **keywords** that represent colors that are predefined in the program. They are about 140ish keywords colors.

```CSS
h1 {
  color: grey;
}
```

The second way is with **RGB** or **RGBA** values of have numbers represents the red, green, blue or alpha in a color. Alpha is the opacity of a color. The Alpha values are only ranging from 0 to 1. The RGB and the RGBA needs numbers in the parameters and are between 0 through 255. You can also pass in percentages and decimals for intensity as well.

```CSS
h1 {
  color: rgb(80, 80, 80);
}

h2 {
  color: rgba(90, 255, 20, 0.2);
}

h3 {
  color: rgba(10%, 255, 0.2, 0);
}

```

Another way to represent color is **Hexadecimal** numbers that are 6 numbers that the first 2 represent the red and the second 2 is the green and the last 2 is the blue. The parameters are numbers ranging from 00 to ff, and the ff with other selected letters represent colors. This method like the RGB values can be decimals and percentages for intensities. 

```CSS
h1 {
  color: #00ff02;
}
```

The last method is **HSL** or **HSLA** which represent Hue, Saturation, Lightness and Alpha. This is very similar to RGB of how it takes in numbers and can be in percentages or decimals for intensities. The Alpha like the RGBA values ranges from 0 to 1.  

```CSS
h1 {
  color: hsl(120, 120, 120);
}

h2 {
  color: hsla(120, 200, 12, 0.2);
}

h3 {
  color: hsla(30%, 2.1, 12, 0.3);
}
```

>Here is a reference for [colors](https://www.w3schools.com/colors/colors_names.asp)