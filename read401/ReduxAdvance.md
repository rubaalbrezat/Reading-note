# Redux Advance

Redux Toolkit was introduced with a purpose to be the standard way to write redux logic. It is said to be an opinionated, batteries-included toolset for efficient Redux development. By using this, you can write all the code you need for your Redux store in a single file, including actions and reducers. Using this you can make your code more readable. Redux toolkit includes all the tools, you want for a Redux application. At the end of the day all you have is less code and faster setups of Redux in every scenario.

What is createSlice in Redux Toolkit?
createSlice is a higher order function that accepts an initial state, an object full of reducer functions and a slice name. It automatically generates action creators and action types that correspond to the reducers and state.

## createSlice
A function that accepts an initial state, an object of reducer functions, and a "slice name", and automatically generates action creators and action types that correspond to the reducers and state.

1. Implement createSilce method and export actions and reducer.
2. Dispatch action by making use of react hooks in functional component.
3. Configure the store