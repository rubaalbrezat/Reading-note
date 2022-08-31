# State and Props
## React lifecycle

## q1) Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?

Render phase happens first.


## q2)What is the very first thing to happen in the lifecycle of React?

Mounting: During the mounting process, an instance of a component is produced and injected into the DOM.


## q3) Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates

constructor
render
componentDidMount
React Updates
componentWillUnmount

## q4) What does componentDidMount do?

The moment a component is installed, this function is called. This is the place to put anything that requires a network request to load or that needs to initialize the DOM. Any subscriptions should be set up using this manner. Don't forget to unsubscribe in componentWillUnmount if you do that ().



# React State Vs Props

## q1) What types of things can you pass in the props?
props is like arguments to a function, when we create a component inside a react, we pass the props we want to render.

## q2 What is the big difference between props and state?
we pass props into a component and we can't update them inside the components, and state is handled and can be updated inside of that component.

## q3) When do we re-render our application?


when we change the state inside our application.

## q4) What are some examples of things that we could store in state?

we store things that we can updated, and our app rerender depends on this data, example for this is inside a form, so we store what user updates.