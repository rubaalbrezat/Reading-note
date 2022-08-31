# Lists and Keys

## q1)What does .map() return?
it will return an array with the same length of the looping array. with the same or new values.


## q2)If I want to loop through an array and display each value in JSX, how do I do that in React?

include the entire listItems array inside a <ul> element


## q3)Each list item needs a unique ____.
key

## q4)What is the purpose of a key?

Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity


# The Spread Operator

## What is the spread operator?
avaScript, spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments.

## q2)List 4 things that the spread operator can do
1. split array items to arguments.
2. combining or copying arrays.
3. adding items in React state.
4. using arrays as arguments in math functions.

## q3)Give an example of using the spread operator to combine two arrays
function sum(x, y, z) { return x + y + z; }

const evenNumbers = [2, 4, 6];
const oddNumbers  = [1, 3, 5];

let combineNumbers = {...evenNumbers,...oddNumbers}
 expected output: {evenNumbers: [2, 4, 6], oddNumbers: [1, 3, 5]}



## q4)Give an example of using the spread operator to add a new item to an array.
Give an example of using the spread operator to add a new item to an array.

const fruits = ['🍏','🍊','🍌','🍉','🍍']
const moreFruits = [...fruits];
console.log(moreFruits) // Array(5) [ "🍏", "🍊", "🍌", "🍉", "🍍" ]
console.log(...[...fruits,'...',...moreFruits]) // 🍑 🍊 🍌 🍉 🍍 ... 🍏 🍊 🍌 🍉 🍍

## q5)Give an example of using the spread operator to combine two objects into one.

var a = { 1: { 687: { name:'test1' }}}
var b = { 1: { 689: { name:'test2' } } }
var c = { ...a, ...b }
expected output { "1": { "689": { "name": "test2" } } }

# Videos
## q1) In the video, what is the first step that the developer does to pass functions between components?
In the video, what is the first step that the developer does to pass functions between components?

create a function 'increment' where the state he want to change is in

## q2) In your own words, what does the increment function do?

when ever you you press on the button or what ever you attached to the listener you added, the count will increase by one
## q3) How can you pass a method from a parent component into a child component?

call it on the element you want to use it on, like button, example <button onclick="this.increment">

## q4) How does the child component invoke a method that was passed to it from a parent component?

when you click on the element attached to the method, for example in the video it was a button, another example is when you press on a photo

# Things I want to know more about
 now all every thing is good.