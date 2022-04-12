---
title: 'Create React App React 18 Cannot Resolve Dependency'
date: '2022-04-12'
readTime: '2'
---

React 18 came with breaking new features of Concurrent rendering, Update batching, and new hooks! But for every time a new techonolgy come out, others would have to learn it and implement them in the projects and libraries. We will go through the features in another blog but for this one, we do have a small issue with the new React 18 version. 

As of yesterday of April 11, of 2022, when you run a: 

```js
npx create-react-app new_app
```

or 

```js
yarn create react-app new_app
```

or 

```js
npm init react-app new_app
```

You would get the same error.

![Cannot Resolve Dependency](https://res.cloudinary.com/doan/image/upload/v1649783376/hd-blog/Cannot-resolve-dependcy.png)

A cannot resolve dependency error. This would happen when you create a new create application with the create-react-app package. The package has not been updated yet with the new react version and have not implement the new features and got rid of the old one. The developers are working hard to fix the issue, for now we would have to do some band-aid fixes to get it to work again. 

Usually with these new changes, you don't want to go and change all your projects and new project to the new version since it is still being implemented and has bugs here and there. Currently the new version doesn't even work in all browser either. So for those cases you would need to downgrade your react and react-dom version to 17. 

package.json
```js
"dependencies": {
    ...
    "react": "17.0.2",
    "react-dom": "17.0.2",
    ...
  },
```

then run 
```js 
yarn 
```

or 

```js
npm install
```

Then all the react features would work like normal and we would have to wait until the new package supports and implements the new react version. 

Another alternative, is to run a  
```js 
yarn 
```

or 

```js
npm install
```

With the new version and then remove the webvitals if you don't use it.

before
index.js
```js
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';
import reportWebVitals from './reportWebVitals';

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById('root')
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();
```

after
index.js
```js
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById('root')
);
```

Then it would work like normal and you can slowly implement the new React 18 features since the react package is already loaded up.