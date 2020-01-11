1. What problem does the context API help solve?
Context API allows us to store data on a context object, and retrieve that data in the necessary components from the context object, not props!


1. In your own words, describe `actions`, `reducers` and the `store` and their role in Redux. What does each piece do? Why is the store known as a 'single source of truth' in a redux application?

Store sees all, remembers all.
Reducers are the guides.
Actions are the doers

Redux is a small, light-weight state container for use when building JavaScript applications. Remember, Redux has nothing to do with React other than the fact that many developers use them together. Redux is a predictable state management library for JavaScript applications and is the most popular State container for React applications.

As components grow and deal with larger sets of data, storing and transporting  state across the entire app becomes cumbersome as well. Reducers offer one possible way to address this problem within the component. At the level of the application, an elegant combination of the Context API with reducers provides one possible way that React developers can manage global state.

The  Store:  a single javaScript  Object that  is a single  immutable state tree in Redux  where all state changes are explicitly handled by dispatching actions. Everything that changes within your application is represented by The store.

Actions: dispatched actions handle state changes that originate from the store and are processed by reducers
Reducers: processes dispatched actions that accepts the previous state and the action and returns the next state of your application
This system makes it easy  to predict which action will be dispatched based on some event or interaction. This all leads to very predictable state management.


1. What is the difference between Application state and Component state? When would be a good time to use one over the other?
Application state is Immutable: When the app  state changes, we clone the state object, modify the clone, and replace the original state with the new copy. We never mutate the original object, and we never write to our store object.

Pure functions change our state. Given the same input, a pure function returns the same output every time. All functions (reducers) in Redux must be pure functions. Meaning they take in some state and a description of what changes took place and return a copy of our state.

Application state is global while component state is local. Component state lives within the component and can only be updated within that component and passed down to it's children via props. Flux and Redux use stores to hold the application state so components anywhere in the app can access it with hooks.

Whenever state needs to be shared by multiple components/pages some data must persist over route changes and that data goes into the redux store in the App State. Presentational components that merely receive data and pass the data down through props use component state.


1. Describe `redux-thunk`, what does it allow us to do? How does it change our `action-creators`?
Redux Thunk is a middleware created by Dan Abramov, that provides the ability to handle asynchronous operations inside our Action Creators.
By nature Redux is synchronous. Because of this we need to apply some middleware such as redux-thunk  to extend the functionality of our Redux package to allow for things like, promises which are asynchronous. Middleware in Redux is very common and gives us a chance to do a few different things with the data passing from action creators to the reducers. Middleware is a powerful extension point for Redux. We can use middleware to add new functionality to Redux.

Middleware intercepts some process, runs a function at the intercept point, then (usually) continues the process. Or, sometimes middleware stops the process entirely.

When whatever “process” in question is kicked off, there is usually data that is flowing through different functions. With middleware, when we “intercept” the process, we are usually trying to use that flowing data.


1. What is your favorite state management system you've learned and this sprint? Please explain why!


 I think I prefer Redux because it sounds more powerful by being able to snatch state, manipulate state and spit out the new state (but learning the syntax and the potential for typos/bugs makes me a little wary of Redux) I'd like to practice with Redux more.