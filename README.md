## 📘 Browser

### 1. What happens when you type in a URL?

1. You enter a URL into a web browser
2. The browser looks up the IP address for the domain name via DNS
3. The browser sends a HTTP request to the server
4. The server sends back a HTTP response
5. The browser begins rendering the HTML
6. The browser sends requests for additional objects embedded in HTML (images, css, JavaScript) and repeats steps 3-5.
7. Once the page is loaded, the browser sends further async requests as needed.

[Read more](https://wsvincent.com/what-happens-when-url/#:~:text=You%20enter%20a%20URL%20into,sends%20back%20a%20HTTP%20response)

## 📘 CSS

### 1. Box model

- `Content`: The content of the box, where text and images appear
- `Padding`: Clears an area around the content. The padding is transparent
- `Border`: A border that goes around the padding and content
- `Margin`: Clears an area outside the border. The margin is transparent

[Read more](https://www.w3schools.com/css/css_boxmodel.asp)

### 2. CSS box-sizing Property

- `box-sizing: content-box`: Default. The width and height properties (and min/max properties) includes only the content. Border and padding are not included.
- `box-sizing: border-box`: The width and height properties (and min/max properties) includes content, padding and border.

[Read more](https://www.w3schools.com/cssref/css3_pr_box-sizing.asp)

### 3. How to vertical center

There are have many ways for vertical center in css. Here are a few typical ways:

#### Use Flexbox:

```
  .parent {
    display: flex;
    justify-content: center;
    align-items: center;
  }
```

#### Use Grid Layout

```
  .parent {
    display: grid;
    justify-self: center;
    align-self: center;
  }
```

#### Use Position Property

```
  .parent {
    height: 200px;
    position: relative;
  }

  .child {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
```

#### Use Table Property

```
  .parent {
    display: table;
  }

  .child {
    display: table-cell;
    text-align: center;
    vertical-align: middle;
  }
```

[Read more](https://blog.logrocket.com/13-ways-to-vertical-center/)

### 4. position: fixed vs position: absolute

- `position: absolute`: The attributes of this will be relative to the next parent element with relative (or absolute) positioning.
- `position: fixed`: A `fixed` position element is positioned relative to the viewport, or the browser window itself.

[Read more](https://css-tricks.com/absolute-relative-fixed-positioining-how-do-they-differ/)

### 5. Animation:

```
div {
  width: 100px;
  height: 100px;
  background-color: red;
  position: relative;
  animation: example 4s;
}

@keyframes example {
  0%   {background-color:red; left:0px; top:0px;}
  25%  {background-color:yellow; left:200px; top:0px;}
  50%  {background-color:blue; left:200px; top:200px;}
  75%  {background-color:green; left:0px; top:200px;}
  100% {background-color:red; left:0px; top:0px;}
}
```

[Read more](https://www.w3schools.com/css/css3_animations.asp)

## 📘 HTML

### 1. How to add CSS to HTML file

#### External CSS

```
<head>
  <link rel="stylesheet" type="text/css" href="exampleStyle.css">
</head>
```

#### Internal CSS

```
<head>
  <style>
    body {
      background-color: linen;
    }

    h1 {
      color: maroon;
      margin-left: 40px;
    }
  </style>
</head>
```

#### Inline CSS

```
<body>
  <h1 style="color:blue;text-align:center;">This is a heading</h1>
  <p style="color:red;">This is a paragraph.</p>
</body>
```

[Read more](https://www.w3schools.com/css/css_howto.asp)

### 2. How to add JS to HTML file

- Define a pair of `<script></script>` tags in the HTML and sandwich the Javascript code in between.
- Create an external Javascript file, then define `<script src="jsFile.js"></script>` in the HTML.
- Directly code the Javascript into the HTML element to deal with certain user actions. For example, `<input type="button" value="Test" onclick="alert('Testing!')"/>`

#### Summary

- There are 3 ways to include Javascript into HTML:
- Sandwich the Javascript in between a pair of `<script>` tags.
- Point to an external Javascript file using the `<script>` tag and src attribute.
- Code it inline into the elements. Usually to handle events and user actions, for example, onclick, onhover, and onkeypress.
- It is all right to put `<script>` tags in both the `<head>` and `<body>` sections, but the order of the scripts do matter.
- If you do not define the full URL within the src of a `<script>` tag, the browser will automatically assume a relative path with the current URL.
- Computers do not need line breaks and comments, we can safely strip these in our Javascript and make things load faster – This process is called minification.
- Scripts are loaded in the order of “from top to bottom”.

> **Placing scripts at the bottom of the `<body>` element improves the display speed, because script interpretation slows down the display.**

[Read more](https://code-boxx.com/javascript-in-html/)

### 3. `async` Attribute vs `defer` Attribute in `<script>`

- `async`: `async` downloads the file during HTML parsing and will pause the HTML parser to execute it when it has finished downloading.
- `defer`: `defer` downloads the file during HTML parsing and will only execute it after the parser has completed. `defer` scripts are also guaranteed to execute in the order that they appear in the document.

- We can use the defer attribute to push the loading of the script to the last.
- We can also use the async attribute to make the script load asynchronously with the rest.

[Read more](https://www.growingwiththeweb.com/2014/02/async-vs-defer-attributes.html)

## 📘 Javascript

### 1. Javascript vs Typescript

### 2. Promise vs Async/ await

### 3. How to catch a error of a promise

### 4. Var, let, const

### 5. Can replace the value in object declared with const?

### 6. Closure

### 7. map, filter, reduce, split, slice, splice, find,...

### 8. map vs filter vs reduce

### 9. splice vs slice

### 10. Javascript Prototypes

### 11. Implement find function for it works with IE 10.

## 📘 ReactJS

### 1. What is jsx file?
- JSX stands for JavaScript XML.
- JSX allows us to write HTML in React.
- JSX makes it easier to write and add HTML in React.

```
const myelement = <h1>I Love JSX!</h1>;
ReactDOM.render(myelement, document.getElementById('root'));
```

> Browsers can't read JSX tags because JSX is not a regular object in javascript. Basically, it's a popular new dialect that simply integrates HTML templates into Javascript code. Requires WebPack or Babel to compile it to Javascript code for browser can be read.

[Read more](https://reactjs.org/docs/introducing-jsx.html)

### 3. Functional Component (Stateless) vs Class Component (Statefull)
#### Render JSX
```
import React from "react";

function FunctionalComponent() {
 return <h1>Hello, world</h1>;
}
```

```
import React, { Component } from "react";

class ClassComponent extends Component {
 render() {
   return <h1>Hello, world</h1>;
 }
}
```

#### Passing props
```
const FunctionalComponent = (props) => {
 return <h1>Hello, {props.name}</h1>;
};
```

```
class ClassComponent extends React.Component {
  render() {
    const { name } = this.props;
    return <h1>Hello, { name }</h1>;
 }
}
```

#### Handling state

```
const FunctionalComponent = () => {
 const [count, setCount] = React.useState(0);

 return (
   <div>
     <p>count: {count}</p>
     <button onClick={() => setCount(count + 1)}>Click</button>
   </div>
 );
};
```

```
class ClassComponent extends React.Component {
 constructor(props) {
   super(props);
   this.state = {
     count: 0
   };
 }

 render() {
   return (
     <div>
       <p>count: {this.state.count} times</p>
       <button onClick={() => this.setState({ count: this.state.count + 1 })}>
         Click
       </button>
     </div>
   );
 }
}
```

#### Lifecycle Methods
#### 1. On Mounting (componentDidMount)

```
const FunctionalComponent = () => {
 React.useEffect(() => {
   console.log("Hello");
 }, []);
 return <h1>Hello, World</h1>;
};
```

```
class ClassComponent extends React.Component {
 componentDidMount() {
   console.log("Hello");
 }

 render() {
   return <h1>Hello, World</h1>;
 }
}
```

#### 2. On Unmounting (componentWillUnmount)

```
const FunctionalComponent = () => {
 React.useEffect(() => {
   return () => {
     console.log("Bye");
   };
 }, []);
 return <h1>Bye, World</h1>;
};
```

```
class ClassComponent extends React.Component {
 componentWillUnmount() {
   console.log("Bye");
 }

 render() {
   return <h1>Bye, World</h1>;
 }
}
```

[Read more](https://www.twilio.com/blog/react-choose-functional-components#:~:text=Rendering%20JSX,JavaScript%20class%20that%20extends%20React.&text=The%20JSX%20to%20render%20will%20be%20returned%20inside%20the%20render%20method.)

### 4. Props vs State

| Props                                                                               |                                State                                 |
| ----------------------------------------------------------------------------------- | :------------------------------------------------------------------: |
| Props are read-only.                                                                |                  State changes can be asynchronous.                  |
| Props are immutable.                                                                |                          State is mutable.                           |
| Props allow you to pass data from one component to other components as an argument. |            State holds information about the components.             |
| Props are used to communicate between components.                                   | States can be used for rendering dynamic changes with the component. |
| Stateless component can have Props.                                                 |               Stateless components cannot have State.                |
| Props make components reusable.                                                     |                State cannot make components reusable.                |
| Props are external and controlled by whatever renders the component.                | The State is internal and controlled by the React Component itself.  |

The below table will guide you about the changing in props and state.

| Condition                                    | Props | State |
| -------------------------------------------- | :---: | ----: |
| Can get initial value from parent Component? |  Yes  |   Yes |
| Can be changed by parent Component?          |  Yes  |    No |
| Can set default values inside Component?     |  Yes  |   Yes |
| Can change inside Component?                 |  No   |   Yes |
| Can set initial value for child Components?  |  Yes  |   Yes |
| Can change in child Components?              |  Yes  |    No |

[Read more](https://www.javatpoint.com/react-state-vs-props)

### 5. Life Cycle in ReactJS

- **Mounting** – Birth of your component
- **Update** – Growth of your component
- **Unmount** – Death of your component

![alt text](https://res.cloudinary.com/djeghcumw/image/upload/v1559793682/blog/1_cEWErpe-oY-_S1dOaT1NtA.jpg "React Life Cycle")

#### Summary
1. React component lifecycle has three categories – Mounting, Updating and Unmounting.
2. The render() is the most used lifecycle method.
  - It is a pure function.
  - You cannot set state in render()
3. The componentDidMount() happens as soon as your component is mounted.
  - You can set state here but with caution.
4. The componentDidUpdate() happens as soon as the updating happens.
  - You can set state here but with caution.
5. The componentWillUnmount() happens just before the component unmounts and is destroyed.
  - This is a good place to cleanup all the data.
  - You cannot set state here.
6. The shouldComponentUpdate() can be used rarely.
  - It can be called if you need to tell React not to re-render for a certain state or prop change.
  - This needs to be used with caution only for certain performance optimizations.
7. The two new lifecycle methods are getDerivedStateFromProps() and getSnapshotBeforeUpdate().
  - They need to be used only occasionally.
  - Not many examples are out there for these two methods and they are still being discussed and will have more references in the future.

[Read more](https://programmingwithmosh.com/javascript/react-lifecycle-methods/)

### 6. What is function replace to `componentDidMount` in react hooks?
```
useEffect(() => {
  console.log('This is componentDidMount in react hooks!')
}, []);
```

[Read more](https://reactjs.org/docs/hooks-reference.html#useeffect)

### 7. useState, useEffect, useCallBack, useMemo,...
[Read more](https://reactjs.org/docs/hooks-reference.html)

## 📘 REST API

### 1. How many methods in the RESTful API?
There are 5 main methods in RESTful API:
- `HTTP GET`: **retrieve resource representation/information only** – and not to modify it in any way.
- `HTTP POST`: Use POST APIs to **create new subordinate resources**, e.g., a file is subordinate to a directory containing it or a row is subordinate to a database table.
- `HTTP PUT`: Use PUT APIs primarily **to update existing resource** (if the resource does not exist, then API may decide to create a new resource or not).
- `HTTP DELETE`: DELETE APIs are used **to delete resources** (identified by the Request-URI).
- `HTTP PATCH`: HTTP PATCH requests are **to make partial update on a resource**.

| HTTP METHOD |         CRUD          |                                        ENTIRE COLLECTION (E.G. /USERS) / SPECIFIC ITEM (E.G. /USERS/123) |
| ----------- | :-------------------: | -------------------------------------------------------------------------------------------------------: |
| POST        |        Create         |                             201 (Created), ‘Location’ header with link to /users/{id} containing new ID. | Avoid using POST on single resource                                            |
| GET         |         Read          |                    200 (OK), list of users. Use pagination, sorting and filtering to navigate big lists. | 200 (OK), single user. 404 (Not Found), if ID not found or invalid.            |
| PUT         |    Update/Replace     | 405 (Method not allowed), unless you want to update every resource in the entire collection of resource. | 200 (OK) or 204 (No Content). Use 404 (Not Found), if ID not found or invalid. |
| PATCH       | Partial Update/Modify |                               405 (Method not allowed), unless you want to modify the collection itself. | 200 (OK) or 204 (No Content). Use 404 (Not Found), if ID not found or invalid. |
| DELETE      |        Delete         |             405 (Method not allowed), unless you want to delete the whole collection — use with caution. | 200 (OK). 404 (Not Found), if ID not found or invalid.                         |


[Read more](https://restfulapi.net/http-methods/)

### 2. How to apply the token to `Axios` and use it to every where in your project?

#### Use [axios interceptors](https://github.com/axios/axios#interceptors) to intercept any requests and add authorization headers.
```
// Add a request interceptor
axios.interceptors.request.use(function (config) {
    const token = store.getState().session.token;
    config.headers.Authorization =  token;

    return config;
});
```

#### Set default header which will be sent with every request you make.
```
axios.defaults.headers.common['Authorization'] = AUTH_TOKEN;
```
[Read more](https://stackoverflow.com/questions/43051291/attach-authorization-header-for-all-axios-requests)
