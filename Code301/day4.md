# React and Forms

## React Docs - Forms
 

## q1) What is a ‘Controlled Component’?

it is an element that when its value will change, it will be updated by setState and passed by props, this change will be notified by the parent component and will control it.

## q2)  Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.

No, because we used the controlled component in the form, like the onChange property, that is means you will get the updated data directly whenever the user changes anything in the input field. it will be updated in your states. and when you submit the form you will have the updated value that the user has entered.

## q3 How do we target what the user is entering if we have an event handler on an input field?

by storing this value by setState in the onChange function, the target will be event.target.name.value.
 

# The Conditional (Ternary) Operator Explained
 

## q1) Why would we use a ternary operator?

because it is easy to use, and it is shorter than if & else statements and it does the same functionality.
## q2) Rewrite the following statement using a ternary statement:

if(x===y){

console.log(true);

} else {

console.log(false);

}

solution using ternary If:
x===y ? console.log(true) : console.log(false)

#Things I want to know more about
 all is good