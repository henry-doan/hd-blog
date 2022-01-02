---
title: 'Transitioning from React Router V4 or V5 to the new V6'
date: '2022-01-01'
---

You probably heard of the term 

>"If it ain't broke, don't fix it". 

That holds true to developers, and the more seasoned they are, the more they tend to only use what they are comfortable with and has been working for them. 

React Router has been used in many ReactJS applications to help with routing and navigation between components to have the ability to go to pages in web development. Recently, their patterns have changed and the old way is causing errors inside new projects and would need to do the new way for it to work like intended. Granted, if you have old projects that are lower than version 6 or want to use a older version, than it will still work like normal, just updating the package or using the newer package would follow these changes.

For more details and their documentation, you can find that here [https://reactrouter.com/docs/en/v6](https://reactrouter.com/docs/en/v6). I am just going to outline the main changes below.

if you want to implement the new version you would have to install it in your project using your prefered package manager. We will be using yarn but you can also run the command in npm as well.

To install the new version in your a ReactJS project you would run a in the terminal:

```console
yarn add react-router-dom@6
```

or with npm:

```console
npm install react-router-dom@6
```

This will install the version 6 of React Router Dom but if you exclude the *@6* it would grab the latest and greatest version but in this case we are focusing on version 6.

The begining step of initializing the browser router has not changed, so that step remains the same.

###### index.js
```js
...

import { BrowserRouter } from 'react-router-dom'

...

  <BrowserRouter>
    <App />
  </BrowserRouter>

...
```
 
The next change of defining the routes does change however and we would replace the *switch* to the *routes*

###### app.js
```js
...

import { Routes, Route } from 'react-router-dom';

const App = () => (
  <>
    // before <Switch>
    <Routes>
      <Route ... />
      <Route ... />
      <Route ... />
    </Routes>
  </>
)

export default App;
```

This would work exactly like before but now the terms are different and this term makes more sense since we are having routes and not switching between them per say. 

The way that we defined our routes has also changed. The key word *route* is still there but the content has been switch to a new syntax. So to define a route, you would do the following: 

###### app.js
```js
...

import { Routes, Route } from 'react-router-dom';
import Home from '../components/pgs/Home';
import About from '../components/pgs/About';

const App = () => (
  <>
    <Routes>
      // previously <Route path='/' exact component={<Home />} />
      <Route path='/' element={<Home />} />
      <Route path='/about' element={<About />} />
    </Routes>
  </>
)

export default App;
```

Where as Home and About are other component for the different pages.



In conclusion, change is inevitable, especially in the tech industry where more advances happens on the daily. The main thing for us to do be continual learners to adapt to the changes so we don't be left behind and still relevant in today's world.

