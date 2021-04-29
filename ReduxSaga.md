# Redux-Saga.

- **Redux**-**saga** is a **redux** middleware library.
- It is designed to make handling side effects in your **redux** app nice and simple. 
- It achieves this by leveraging an ES6 feature called Generators, allowing us to write asynchronous code that looks synchronous, and is very easy to test.
- The mental model is that a saga is like a separate thread in your application that's solely responsible for side effects. 
- It is a redux middleware, which means this thread can be started, paused and cancelled from the main application with normal redux actions, it has access to the full redux application state and it can dispatch redux actions as well.

## Generators in ES6

- Generators are basically functions that can be paused and resumed as many times as we want
- Syntax : 
  - function *g1(){} 
  - putting an asterisk infront of function name makes it a generator
  - It provides yield keyword to provide values to the user

## Working of Redux-Saga

- We dispatch an action normally
- We have a watcher that watches for a particular action, and whenever the action gets dispatched, watcher catches the action
- As soon as it catches it, the first job is to perform the asynchronous task ex- saving the data on the server, once it is done
- It dispatches another action(not the same action as before), that would reach the reducer

## Flow without Redux-Saga

- Button pressed -> dispatches some action -> reducer catches the action and performs (either increments or decrements) accordingly
- There's no asynchronous activity involved here
- What if I want to store that state on the server?

## Flow with Redux-Saga

- Button pressed -> dispatches some action -> Watcher watching for a particular action catches the action -> Watcher executes the asynchronous task(save the state on the server in this case) -> dispatches another action -> reducer catches the action and performs (either increments or decrements) accordingly

![image-20210224104536845](C:%5CUsers%5CDG086275%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20210224104536845.png)