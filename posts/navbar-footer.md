---
title: 'Navbars and Footers'
date: '2018-10-21'
readTime: '2'
---

When you look at some web sites, what is one of the things they have in common? 

The site navigation of the navbar and often times the site footer. We will first get into the navbar. The navbar is: 

> A place to display links to navigate to other parts of the site and to show the branding of the site. 

With how the web site works with navigation, there are different url patterns to take you to different parts of the application, but the end user doesn't know what the urls are and how to get to the other places. There for the navbar is where we can put all the links to go to the other places and navigate them correctly. Another thing is to show the branding on the site to show the logs and name of the company. 
Here is a basic code of the navbar. 

```html
<nav>
  <ul>
    <li><a href="index.html">Home</a></li>
    <li><a href="about.html">About</a></li>
    <li><a href="blog.html">Blog</a></li>
    <li><a href="contact.html">Contact</a></li>
  </ul>
</nav>
```

The nav is optional but you would usually use the ul an unordered list to create a nav bar the rest is in the styles. 

```css
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

li a {
  display: block;
  width: 60px;
}
```

These are just basic styles, you can find better examples depending on what look you want for the site. Also you can use styled libraries to make styling the navbar and footer a lot easier. 

With the footer, it is very similar to the navbar but the navbar goes on the top or side of the site but the footer goes in the bottom it is usually for:

> More navigation, who created the site, any copyright/trademark info, when it was last updated, sources of info, etc.

```html
<footer>
  <p>Created by: Your Name Here</p>
  <p>Contact information: <a href="mailto:you@gmail.com">
  you@gmail.com</a>.</p>
</footer>
```

With the navbar and footer, these are items you want in every page for some site navigation, and for branding and other related info of the site and the company. The bare bones of it is straight forward of a list of elements. As for the styles would change depending on the look and feel of what is wanted to be achieved and can be helped with some styled libraries. What will your navbar and footer look like and have?  