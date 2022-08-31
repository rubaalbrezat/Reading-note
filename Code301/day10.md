# In memory storage

## JavaScript Call Stack
## What is a ‘call’?

function invocation

## How many ‘calls’ can happen at once?

Since the call stack is single, function(s) execution is done one at a time.

## What does LIFO mean?

Last In, First Out, When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.

Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.



# Image Credit: CMU
![image](https://user-images.githubusercontent.com/108065452/182605819-72327b59-e1a6-42a9-a967-8e55be8fdb74.png)

## What causes a Stack Overflow?

A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

JavaScript error messages
## What is a ‘reference error’?

when try to use a variable that is not yet declared

## What is a ‘syntax error’?

this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

## What is a ‘range error’?

When try to manipulate an object with some kind of length and give it an invalid length

## What is a ‘type error’?

type error show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

## What is a breakpoint?

the point where our code breaks, we will be able to see what has happened before that point

## What does the word ‘debugger’ do in your code?

will achieve a breakpoint in the line of code we want to break at.
#  Things I want to know more about 
all is good