---
title: 'Fonts and Typography'
date: '2018-12-29'
---


For styling fonts there are limitation depending on web browsers and versioning  of the browsers. The browser does have some default fonts you can work with. To use the default fonts you can just have them in a string and in them the font name and it does not matter if it is capitalize or not.

```CSS
h1 {
  font-family: 'Times';
}
```

You can also chain fonts one after the other to cover if the browser supports it or not. If the browser does support it will use the font if it does not than it will go to the next one that is supported.

```CSS
p {
  font-family: 'Times', 'Arial', 'Serif';
}
```

If you are using a external font, you would have to import them by CDN or either downloading it. Depending on where you got the font, you would have to follow their documentation.

For example for google fonts.

```HTML 
  <link href="https://fonts.googleapis.com/css?family=Pacifico" rel="stylesheet">
```

or in the CSS
```CSS
  @import url('https://fonts.googleapis.com/css?family=Pacifico');
```

Then to put it to use in your CSS:
```CSS
p {
  font-family: 'Pacifico', cursive;
}
```