---
title: 'Transitioning from React Router V4 or V5 to the new V6'
date: '2022-01-01'
readTime: '15'
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

The route is now rendering a jsx element rather than rendering a component. This will help us to use whatever it is that we are rendering, whether it is a component or jsx without having to change the syntax and this would handle both cases in the brackets. With the new version, we no longer need to put the *exact* because now internally it does that automatically for all the paths. There are other ways to have the path be matching such as the */** which will match the best route starting with what is to the left of it to make it more dynamic.

---

The next part are *Link* and *NavLink* where there are not a lot of changes to them but there are some extra features we can use. For example for a NavLink, if I want to see if the link is active or not, V6 has a way in the class name for us to see if the data is active or inactive.

###### Navbar.js
```js
...

import { Routes, Route } from 'react-router-dom';

const Navbar = () => (
  <>
    <NavLinks className={(navData) => navData.isActive}>
      Home
    </NavLinks>
  </>
)

export default Navbar;
```

With the class name it runs a function of the data that is coming from the nav link and see if the route as well as the link is a active link and will return a boolean value. This way you can base your styles on the value to have it style differently whether or not it is active.

---

The next item of business is the way we redirect to other pages. We would often use this when we want to redirect to another page base on a router, or base on a action like form submission, api calls etc. to take the user somewhere after. This syntax was previously the *Redirect* but now it has changed to the *Navigate*. It will still work the same but we can add more functionality to the element now.


###### app.js
```js
...

import { Routes, Route, Navigate } from 'react-router-dom';
import Home from '../components/pgs/Home';
import About from '../components/pgs/About';

const App = () => (
  <>
    <Routes>
      <Route path='/' element={<Home />} />
      <Route path='/home' element={<Navigate replace to='/' />} />
      <Route path='/about' element={<About />} />
    </Routes>
  </>
)

export default App;
```

You might notice a new prop of replace. With out the replace prop it would simply push to the new page but then you might get an issue of using the back button. The *replace* replaces the current route to the new route and would add the route to the stack and then the back button would work like normal.

A similar way to do this is the do it functionally with the new hook provided. This is really good if we want to pass the function to navigate somewhere after an action.

###### form.js
```js
import { useNavigate } from 'react-router-dom';

const Form = () => {
  ...
  const navigate = useNavigate();

  const handleSubmit = (e) => {
    ...
    navigate('/thank-you')
  }

  return (
    <>
      <form onSubmit={handleSubmit}>
      ...
      </form>
    </>
  )
}

export default Form;
```

You can also pass in a option to replace the current route with the new route so it can be in the stack.

```js
navigate('/thank-you', { replace: true })
```

This will allow us to navigate using the functions. We can also go back and forward of routes in the state as well with:

```js

// go back one route
navigate(-1)
// go back two route
navigate(-2)
// go forward one route
navigate(1)
// etc.
```

---

With embedded routes, we have the ability to define them where we are defining the other routes and we are embedding them in side of the route we want. Such as:

###### app.js
```js
...

...
import Contact from '../components/pgs/Contact';

const App = () => (
  <>
    <Routes>
      ...
      <Route path='/about' element={<About />}>
        <Route path='/contact' element={<Contact />}/>
      </Route>
    </Routes>
  </>
)

export default App;
```

Up above, we are having an opening and closing route, and then what we want to embed is inside of the opening and closing route and would give us access to the contact component with the url of*/about/contact*. This way is a lot more better with embedded routes because we have all of our routes in one place and separation of concerns. The only caveat is that for this way we need to defined where we are rendering the embedded content, so we have to do the following in the parent route: 

###### About.js
```js
import { Outlet } from 'react-router-dom';

const About = () => (
  <>
    <h1>This is about me!</h1>
    <p>I am learning react router</p>
    <Outlet />
  </>
)

export default About;
```

The *Outlet* is where the nested content will be inserted.

--- 

While passing data through the routes, you would have to defined them slightly different and to access them with a hook.

###### Profile.js
```js
import { useNavigate } from 'react-router-dom';

const Profile = () => {
  const navigate = useNavigate();

  return (
    <>
      <button onClick={() => navigate('/about', { state: {name: "bob", age: 33, email: 'bob@email.com'} })}>
    </>
  )
}

export default Profile;
```

###### About.js
```js
import { Outlet, useLocation } from 'react-router-dom';

const About = () => {
  let location = useLocation();
  const { name, age, email } = location.state;
  return (
    <>
      <h1>About Page { name }</h1>
      <p>{age}</p>
      <p>{email}</p>
      <Outlet />
    </>
  )
}

export default About;
```

With the *useLocation* hook you are able to grab the data from state and then use them accordingly. The only thing is that with this way it will convert things to strings, so it is really good for read only items and not functionality.

---

To specify all other routes that doesn't have a path defined, it would have to be the very bottom of the routes and is the following:

###### App.js
```js
import { Routes, Route } from 'react-router-dom';
import Home from '../components/pgs/Home';
import About from '../components/pgs/About';
import NoMatch from '../components/pgs/NoMatch';

const App = () => (
  <>
    <Routes>
      <Route path='/' element={<Home />} />
      <Route path='/about' element={<About />} />
      <Route path='/*' element={<NoMatch />} />
    </Routes>
  </>
)

export default App;
```

---

Syntax wise there are little changes but the techonology it self changed a whole lot for the better. In conclusion, change is inevitable, especially in the tech industry where more advances happens on the daily. The main thing for us to do be continual learners to adapt to the changes so we don't be left behind and still relevant in today's world.