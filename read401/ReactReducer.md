# React Reducer

1. How can we ensure that an effect hook runs only once?
  pass an empty array as the second argument to the useEffect hook

2. Can useState() update more than one state variable at the same time?
 No,The setState function is used to update the state. It accepts a new state value and enqueues a re-render of the component.
During subsequent re-renders, the first value returned by useState will always be the most recent state after applying updates.

3. Is useState() synchronous?
 the setState method is asynchronous
_____________________________

 # Vocabulary Terms

 State Hook
  use hook when you write a function component and realize you need to add some state to it

 component lifecycle
  The lifecycle of a component is the series of methods that are invoked in different stages of the component's existence.
