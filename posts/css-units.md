---
title: 'CSS Unit of Measurements'
date: '2018-11-11'
---


When styling you might want to change the size of some elements and this is achieved by two ways, one is **Relative** Measurements and the other is **Absolute** Measurements. 

**Relative** Units of measurements are based off of the DOM or Document Object Model or how the elements are relative to the view screen or relative to other elements.

```CSS
h1 {
  font-size: 40em; /* em is relative to font size of the selector element so 40em is 40 times the originals h1 font size. */
}

h1 {
  font-size: 40rem; /* rem is is relative to font size of the root element whatever root element of the selector element is. */
}

img {
  background-size: 80vh; /* vh or view height is the number of percentage of the height of the viewport or what the user can see on the screen. */
}

img {
  background-size: 80vw; /* vw or view width is the number of percentage of the width of the viewport or what the user can see on the screen. */
}

.nav-background {
  background-size: 40vmin; /* This is the viewport's minimum dimensions. */
}

.nav-background {
  background-size: 40vmax; /* This is the viewport's maximum dimensions. */
}

.nav-background {
  background-size: 40%; /* This is the viewport's percentage. */
}

/* The next two are rarely used */

span {
  font-size: 5ch; /* This is relative to the width of the zero character "0". */
}

span {
  font-size: 5ex; /* This is relative to the x height of the current element. */
}
```

**Absolute** units of measures are a set size for elements. Most of the measurements are based off of the inch measurement.

```CSS
h1 {
  font-size: 40cm; /* cm is centimeters. There are 2.54 centimeters in a inch. */
}

h1 {
  font-size: 40mm; /* mm is millimeters, there are 10 millimeters in one centimeter.  */
}

h1 {
  font-size: 36in; /* in is inches. */
}

h1 {
  font-size: 40px; /* px is pixels which is standardize in the tech industry. There are 96 pixels in a inch. */
}

h1 {
  font-size: 40pt; /* pt is points. There are 72 points in a inch. */
}

h1 {
  font-size: 40pc; /* pc is picas. One picas is 12 points. */
}

```