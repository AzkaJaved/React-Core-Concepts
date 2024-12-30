# Function Declartion vs function expressions:

# Function Declartion

to declartion a function , "function" keyword is used and we specify a name for the function
--> function Sum (){}

# Function Expression

you can create a function expression and assign it to a variable that can be called later.You can do this in two ways.

# 1-Function Expression with function keyword:

one way is to use the function keyword wwithout anyname which will make it an anonymous function.Here is how:
---> const Sum = function(){}
If you use a function keyword without a name , we create a function expression which we have to assign to variable else we get an error.here is how
---> function (){
-----> return a+b
---> }

# error:Syntax Error :Function statements require a function name

# 2- Arror function expressions:

you can also create function expressions with arrow functions.arrow functions can not be declared they can only be expressed .
---> const sum = (args) => {}

# Function expressions can not be used before their declaration:

You can use a declared functionbefore the lineit was initialized,here is how:
sum(1, 2);
function sum(a, b) {
console.log(a + b);
}

here we used function sum on line before it was even declared and there is no error,What happens here was hoisting.
Sum is hoisted to the top of the code before the whole code was executed.This makes sum accessible before the line where it was actually created in the code.

# Hoisting:

All functions and variables are hoisted but when it comes to the function expressions,they can not be used before their initialization they are not hoisted.

# Error : We get an error: ReferenceError: Cannot access 'sum' before initialization

We get this error because when you declare variables with let or const (like we did for sum here), they are hoisted, but without a default initialization

# only declared functions can be used before initialization.
