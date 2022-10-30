--- 
title: React CheatSheet
description: The most important and useful methods of React are given here.
created: 2022-10-30
---

## Table of Contents

- [React CheatSheet for Developers](#react-cheatsheet-for-developers)
  - [Create React App](#create-react-app)
  - [React Components](#react-components)
  - [React Props](#react-props)
  - [React Children Props](#react-children-props)
  - [React Conditionals](#react-conditionals)
  - [React Context](#react-context)
  - [React useEffect Hooks](#react-useeffect-hooks)

# React CheatSheet for Developers

## Create React App

> Create React App is a comfortable environment for learning React, and is the best way to start building a new single-page application in React.

```
npx create-react-app my-app
cd my-app
npm start
```

**[🔼Back to Top](#table-of-contents)**

## React Components

```js
function App() {
  return <div>Hello Developers</div>;
}

export default App;
```

**[🔼Back to Top](#table-of-contents)**

## React Props

```js
function App() {
  return <User name="Developer" />
}

function User(props) {
  return <h1>Hello, {props.name}</h1>; // Hello, Developer!
}
```

**[🔼Back to Top](#table-of-contents)**

## React Children Props

```js
function App() {
  return (
   <User>
     <h1>Hello, Developer!</h1>
   </User>
  );
}

function User({ children }) {
  return children;
}
```

**[🔼Back to Top](#table-of-contents)**

## React Conditionals

```js
function App() {
  const isAuthUser = useAuth();

  if (isAuthUser) {
    // if our user is authenticated, let them use the app
    return <AuthApp />;
  }

  // if user is not authenticated, show a different screen
  return <UnAuthApp />;
}
```

**[🔼Back to Top](#table-of-contents)**

## React Context

> React context allows us to pass data to our component tree without using props.

```js
function App() {
  return (
    <Body name="Developer" />
  );
}

function Body({ name }) {
  return (
    <Greeting name={name} />
  );
}

function Greeting({ name }) {
  return <h1>Welcome, {name}</h1>;
}
```

**[🔼Back to Top](#table-of-contents)**

## React useEffect Hooks

```js
import { useEffect } from 'react';

function MyComponent() {
   useEffect(() => {
     // perform side effect here
   }, []);
}
```

**[🔼Back to Top](#table-of-contents)**

