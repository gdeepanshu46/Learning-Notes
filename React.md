# React.

## What is React?

- React is a library for building user interfaces.
- It runs on the client as a SPA(Single Page App), but can be used to build full stack apps by communicating by a server/API (eg. MERN stack)
- It is often referred to as a front-end "framework" because it is capable and directly comparable to a framework such as Angular or Vue.
- When we create a project with React.js, it gives us the boiler plate code that means we don't have to create files by our own, it does that work for us.

## Creating first project in React

```shell
npx create-react-app app-name
```

## Why would be use React?

- Structure the "view" layer of our application.
- Reusable components with their own state.
- JSX - Dynamic Markup
- Interactive UIs with Virtual DOM
- Performance and testing
- Very popular in the industry

## Pre-requisites

- Good handle on JS
- Data types, variables, functions, loops, etc
- Promises and asynchronous programming
- Array methods like forEach() and map()
- Fetch API and making HTTP requests

## What is Node.js?

- Node.js is an open source server environment
- Node.js is free
- Node.js uses asynchronous programming! (Multiple threads)
- Node.js runs on various platforms (Windows, Linux, Unix, Mac OS X, etc.)
- Node.js uses JavaScript on the server

## What is npm?

- **npm** is the world's largest **Software Registry**.
- The registry contains over 800,000 **code packages**.
- **npm** is installed with Node.js
- Open-source developers use **npm** to **share** software.
- Many organizations also use npm to manage private development.
- All **npm** packages are defined in files called **package.json**.
- The content of package.json must be written in **JSON**.
- At least two fields must be present in the definition file: **name** and **version**.
- npx is a package runner tool that comes with npm

## What is JSX

- **JSX** stands for JavaScript XML. 
- JSX allows us to write HTML in React. 
- JSX makes it easier to write and add HTML in React.
- JSX expressions must have only one parent element

## React Components

- When using React, think of your UI as a bunch of separate component

- Components are independent and reusable bits of code. 

- They serve the same purpose as JavaScript functions, but work in isolation and return HTML via a render() function.

- Components come in two types, Class components and Function components

  - ### Create a Class Component (Stateful Component)

    ```javascript
    class Car extends React.Component{
        render(){
            return (
                <h1> Hi, I am a Car! My brand name is {this.props.name} </h1>;
            )
        }
    }
    ```

    

  - ### Create a Function Component (Stateless Component)

    ```javascript
    function Car(props){
        return (
            <h2>Hi, I am also a Car! My brand name is {props.name} </h2>;
        )
    }
    ```

    

    - Note : Use ES6 Functional Component as much as possible but when we need to store the state of an object, use Class Component.

  - ### Component Constructor
    ```javascript
    class Car extends React.Component {
      constructor() {
        super();
        this.state = {color: "red"};
      }
      render() {
        return <h2>I am a Car!</h2>;
      }
    }
    ```

    - In React, component properties should be kept in an object called `state`.
    - States and Props make React dynamic, State does it from inside while prop does it from outside

- ### States

  - setState() method is used to change the state of a component, it takes state object as an argument
  - It is an asynchronous process
  - It works by 
    - creating a state object i.e. updated state object 
    - compares this newly created object with the already existing object at the virutal DOM
    - finds the difference between the two and updates the object in the virtual DOM
    - Conventions to follow while using setState() method
      - ![image-20210314181034876](C:%5CUsers%5CDG086275%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20210314181034876.png)
      - ![image-20210314181132494](C:%5CUsers%5CDG086275%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20210314181132494.png)

- **Props (Properties)**
- They are optional inputs a component can have
  - It allows a component to be dynamic
  - To specify props for a component, we specify them as attributes
  - Props is just an object containing attributes and their values that are passed by the parent component
  - Props are immutable means their value can't be changed

## React Hooks

- They are functions that let us hook into the React state and lifecycle features from function components

  - useState : returns a stateful value and a function to update it
  - useEffect : performs side effects in function components
  - useContext, useReducer, useRef etc

## Lists and Keys

- ![image-20210315110647711](C:%5CUsers%5CDG086275%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20210315110647711.png)
- ![image-20210315111716591](C:%5CUsers%5CDG086275%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20210315111716591.png)

```
Note : Adding button type as "submit", gives user the ability to submit the form by pressing enter key, which is always good and preferred
```

## Lifecycle Methods

- ![image-20210315124252508](C:%5CUsers%5CDG086275%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20210315124252508.png)
- ![image-20210315124339034](C:%5CUsers%5CDG086275%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20210315124339034.png)
- ![image-20210315124419191](C:%5CUsers%5CDG086275%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20210315124419191.png)
- ![image-20210315124453660](C:%5CUsers%5CDG086275%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20210315124453660.png)
- ![image-20210315124515877](C:%5CUsers%5CDG086275%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20210315124515877.png)
- ![image-20210315124555546](C:%5CUsers%5CDG086275%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20210315124555546.png)


## Learnt so far

- Create a React app 
- Files & folders 
- App component & JSX 
- Expressions in JSX  
- Creating a component 
- Component Props
- PropTypes 
- Styling  
- Button Component

