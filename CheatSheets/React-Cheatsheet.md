# 📚 React Cheat Sheet
This repository is a cheat sheet to React for daily use. It contain a lot of snippets from my own use / official documentation and i'll improve it soon !  
It's made for people like me who like to continue have a overview of some snippets.

## Table of Contents

1. **[React](#1---react)**
2. **[Redux](#2---redux)**

## 1 - React
### Use React
```javascript
// Import React and ReactDOM
import React from 'react'
import ReactDOM from 'react-dom'
```

```javascript
// Render JSX into a DOM element
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

```javascript
// Render Component into a DOM element
ReactDOM.render(
  <MyComponent />,
  document.getElementById('root')
);
```
**[⬆ Go to top](#table-of-contents)**

### JSX
```javascript
// JSX produce React Element
const item = <h1>My JSX Element</h1>;
```

```javascript
// Use curly braces to embed some Javascript
const item = <div>{getContent()}</div>;
```

```javascript
// Use camelCase for attribute name
const item = <div className="example"></div>;
```

```javascript
// Use curly braces to embed some Javascript
const item = <img src={image.url}></img>;
```

```javascript
// Self close if tag is empty
const item = <div />;
```
**[⬆ Go to top](#table-of-contents)**

### Components
```javascript
// Stateless Functional Component
function Heading(props) {
  return <h1>{props.title}</h1>;
}
```

```javascript
// Stateless Functional Component (with arrow function)
const Heading = (props) => {
  return <h1>{props.title}</h1>;
}
```

```javascript
// ES6 Class Component, can have states
class Heading extends React.Component {
  render() {
    return <h1>{this.props.title}</h1>;
  }
}
```

```javascript
// Always start component names with capital
<Heading />
```
**[⬆ Go to top](#table-of-contents)**

### Render
```javascript
// Return React Element
render() {
  return <div>Example of return<div />
}
```

```javascript
// Return Another Component
render() {
  return <MyComponent />
}
```

```javascript
// Return String
render() {
  return 'Return a string works!'
}
```

```javascript
// Return Numbers (rendered as text node)
render() {
  return 100
}
```

```javascript
// Return nothing
render() {
  return null
}
```
**[⬆ Go to top](#table-of-contents)**

### Component Lifecycle
```javascript
componentWillMount() {

}
```

```javascript
componentDidMount() {
  // Call after the component output has been rendered in the DOM
}
```

```javascript
componentWillReceiveProps() {

}
```

```javascript
shouldComponentUpdate() {

}
```

```javascript
componentWillUpdate() {

}
```

```javascript
componentDidUpdate() {

}
```

```javascript
componentWillUnmount() {

}
```

```javascript
componentDidCatch() {

}
```
**[⬆ Go to top](#table-of-contents)**

### Props (Properties)
Props are immutable.

```javascript
// Component with a single valid argument : props
function Heading(props) {
  return <h1>{props.title}</h1>;
}
```
**[⬆ Go to top](#table-of-contents)**

### State
State are locals and fully controlled by the component itself.

```javascript
// Update state with setState, except in constructor
this.setState({
  title: 'Updated title',
});
```

```javascript
// Set state with previous state
this.setState((prevState, props) => {
  return {count: prevState.count + 1};
});
```

```javascript
// Declare initial state in constructor
class Heading extends React.Component {
  constructor(props) {
    super(props);
    this.state = {title: 'My title'};
  }
}
```

```javascript
// Do not update state directly
this.state.title = 'Hello';
```

```javascript
// Lifting state up to share state between component
class Wrapper extends React.Component {
  constructor(props) {
    super(props);
    this.handleInputChange = this.handleInputChange.bind(this);
    this.state = {value: ''};
  }

  handleInputChange(value) {
    this.setState({value});
  }
  render() {
    const value = this.state.value;
    return (
        <Input value={value} onInputChange={this.handleInputChange} />
    );
  }
}

class Input extends React.Component {
  constructor(props) {
    super(props);
    this.handleChange = this.handleChange.bind(this);
  }

  handleChange(e) {
    this.props.onInputChange(e.target.value);
  }

  render() {
    const value = this.props.value;
    return <input value={value} onChange={this.handleChange} />;
  }
}
```
**[⬆ Go to top](#table-of-contents)**

### Handling Event
```javascript
// React Event are in camelCase
<button onClick={handleClick}>
  Action
</button>
```

```javascript
// Use preventDefault instead of return false
function handleClick(e) {
  e.preventDefault();
}

```

```javascript
// Bind this to use it in the callback
constructor(props) {
  super(props);
  this.handleClick = this.handleClick.bind(this);
}
```

```javascript
// Pass data to callback
<button onClick={(e) => this.deleteItem(id, e)}>Delete item</button>
<button onClick={this.deleteItem.bind(this, id)}>Delete item</button>
```
**[⬆ Go to top](#table-of-contents)**

### Conditional Rendering
```javascript
// Using if operator with props
function Heading(props) {
  const isHome = props.isHome;
  if (isHome) {
    return <HomeHeading />;
  }
  return <PageHeading />;
}
```

```javascript
// Using if operator with state
render() {
  const isHome = this.state.isHome;
  let heading = null;
  if (isHome) {
    heading = <HomeHeading />;
  } else {
    heading = <PageHeading />;
  }

  return (
    <div>
      {heading}
    </div>
  );
}
```

```javascript
// Using ternary operator
<div>
  {isHome ? <HomeHeading /> : <PageHeading />}
</div>
```

```javascript
// Using logical operator
<div>
  {messages.length > 0 &&
    <h1>
      You have messages
    </h1>
  }
</div>
```

```javascript
// Prevent component from rendering
function Modal(props) {
  if (!props.isShow) {
    return null;
  }

  return (
    <div>
      Modal
    </div>
  );
}
```

**[⬆ Go to top](#table-of-contents)**

### Portal
```javascript
import { createPortal } from "react-dom";

class MyPortalComponent extends React.Component {
  render() {
    return createPortal(
      this.props.children,
      document.getElementById("node"),
    );
  }
}
```
**[⬆ Go to top](#table-of-contents)**

### Fragment
```javascript
const Fragment = React.Fragment;

render() {
  return (
    <Fragment>
      Some text.
      <h2>A heading</h2>
      Even more text.
    </Fragment>
  );
}
```

```javascript
render() {
  return (
    <React.Fragment>
      Some text.
      <h2>A heading</h2>
      Even more text.
    <React.Fragment>
  );
}
```

```javascript
render() {
  return (
    <>
      <ComponentA />
      <ComponentB />
    </>
  );
}
```
**[⬆ Go to top](#table-of-contents)**

### Forms

#### Controlled Components
```javascript
// In controlled component, each state mutation have an handler function
class Form extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: ''};

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(e) {
    this.setState({value: e.target.value});
  }

  handleSubmit(e) {
    alert('Submitted value: ' + this.state.value);
    e.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <input type="text" value={this.state.value} onChange={this.handleChange} />
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```

```javascript
// Force to uppercase in handler
handleChange(e) {
  this.setState({value: e.target.value.toUpperCase()});
}
```

```javascript
// <textarea> in React use a value attribute
<textarea value={this.state.value} onChange={this.handleChange} />
```

```javascript
// <select> use a value and not a selected attribute
<select value={this.state.value} onChange={this.handleChange}>
  <option value="a">Option A</option>
  <option value="b">Option B</option>
</select>
```

```javascript
// <select value can have an array for multiple values
<select multiple={true} value={['a', 'b']}>
```

```javascript
// Handle multiple inputs with name attribute
handleInputChange(e) {
  const target = e.target;
  const value = target.value;
  const name = target.name;

  this.setState({
    [name]: value
  });
}

render() {
  return (
    <form>
      <input name="firstName" onChange={this.handleInputChange} />
      <input name="lastName" onChange={this.handleInputChange} />
    </form>
  );
}
```
**[⬆ Go to top](#table-of-contents)**

### React without JSX
```javascript
// This two elements are similar :
const element = (
  <h1 className="heading">
    Hello!
  </h1>
);

const element = React.createElement(
  'h1',
  {className: 'heading'},
  'Hello!'
);
```
**[⬆ Go to top](#table-of-contents)**

### Typechecking props with PropTypes
```javascript
// Use PropTypes
import PropTypes from 'prop-types';
```

```javascript
// Prop is an optional array
MyComponent.propTypes = {
  optionalArray: PropTypes.array,
};
```

```javascript
// Prop is an optional boolean
MyComponent.propTypes = {
  optionalBool: PropTypes.bool,
};
```

```javascript
// Prop is an optional function
MyComponent.propTypes = {
  optionalFunc: PropTypes.func,
};
```

```javascript
// Prop is an optional number (integer, float...)
MyComponent.propTypes = {
  optionalNumber: PropTypes.number,
};
```

```javascript
// Prop is an optional object
MyComponent.propTypes = {
  optionalObject: PropTypes.object,
};
```

```javascript
// Prop is an optional string
MyComponent.propTypes = {
  optionalString: PropTypes.string,
};
```

```javascript
// Prop is an optional symbol
MyComponent.propTypes = {
  optionalSymbol: PropTypes.symbol,
};
```

```javascript
// Prop is an optional node (numbers, strings, elements, array, fragment)
MyComponent.propTypes = {
  optionalNode: PropTypes.node,
};
```
**[⬆ Go to top](#table-of-contents)**

### Create React App
```bash
# Create new app
create-react-app my-app
```
**[⬆ Go to top](#table-of-contents)**

### Fetch datas
```javascript
// Use componentDidMount hook with fetch
class PostsList extends Component {
  constructor(props) {
    super(props);
    this.state = {posts: []};
  }

  componentDidMount() {
    fetch('https://example.com/posts')
      .then(response => response.json())
      .then(data => this.setState({ posts: data.posts }));
      .catch(error => console.log(error));
  }
}
```

```javascript
// Use Axios library to fetch datas
import axios from 'axios';

componentDidMount() {
  axios.get('/post', {
    params: {ID: 123}
  })
  .then(function (response) {
    console.log(response);
  })
  .catch(function (error) {
    console.log(error);
  });
}
```

**[⬆ Go to top](#table-of-contents)**

## 2 - Redux
### Install Redux
```bash
npm install --save redux
# Install react binding
npm install --save react-redux
# Install dev tools
npm install --save-dev redux-devtools
```

### Actions
```javascript
// Declare action type
const SUBMIT_FORM = 'SUBMIT_FORM'
```

```javascript
// Action shape with payload
{
  type: SUBMIT_FORM,
  payload: {
    firstName: 'John',
    lastName: 'Doe',
  }
}
```

```javascript
// Action shape without payload
{
  type: SUBMIT_FORM,
}
```

```javascript
// Declare action creator
function submitForm(formData) {
  return {
    type: SUBMIT_FORM,
    payload: {
      firstName: formData.firstName,
      lastName: formData.lastName,
    }
  }
}
```

### Reducers
```javascript
// Declare an initial state
const initialState = {
  firstName: '',
  lastName: '',
  city: '',
}
```

```javascript
// Declare a minimal reducer
function userReducer(state = initialState, action) {
  return state;
}
```

```javascript
// Handle action in reducer
function userReducer(state = initialState, action) {
  switch (action.type) {
   case SUBMIT_FORM:
     return {
       ...state,
       firstName: action.payload.firstName,
       lastName: action.payload.lastName,
       city: action.payload.city,
     };
   default:
     return state;
 }
}
```

**[⬆ Go to top](#table-of-contents)**
