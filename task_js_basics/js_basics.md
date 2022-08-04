## Basic JS

To be honest, I adore FreeCodeCamp, I took the js libraries course and completed 5 tasks for sertification, you can check my [codepen](https://codepen.io/ksalpern/) to see these projects. Also to improve my js knowledge I do at least one codewars task everyday, you can check my [challenge](https://github.com/ksalpern/codewars)

### Main things about JS

1. Javascript is always executed sequentially

2. Primitive values are NOT name/value pairs. They are single values.

3. An object in Javascript is simply a collection of name/value pairs.

4. Defining a variable as an Object Literal accomplishes pretty much the same thing as defining a variable equal to 'new Object()'. However, it's faster and easier to type up an object literal.

5. Immediately Invoked Function Expressions are usually used to place code into its own execution context not to conflict with the global scope.

### Interesting things about JS

1. Sum of String and Numbers

> '500' + 1; //'5001'

Pretty strange, right?

But if you sum a string with a number then there will be no doubt:

> 500 + '1'; //501

2. Equal will not give you the result

In javascript to declare a variable we have to use ‘=’ but to check equality of two variables we have to use ‘==’ or ‘===’ for matching data and data types.

Here is an example:

```
var a = ‘100’; // assigning values to a variable with ‘=’
var b = 100; // assigning values to a variable with ‘=’
a == b; // comparing two variables
a === b; // comparing two variables, but this operator also checks datatype and compares two values.
```

Go back to [README](../README.md)