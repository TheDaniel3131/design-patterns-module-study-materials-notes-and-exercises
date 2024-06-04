# Lesson 4

## λ Calculus and Functional Programming Language
- To analyze the interaction between functional abstraction and function application in a mathematical context.
- Functional programming languages are essentially variations of the λ-calculus, allowing their semantics and implementation to be examined within this framework.
- Denotational semantics, a popular method for formally specifying languages, originated from lambda calculus research and employs higher-order functions.
- Function abstraction is represented as λx.E, with x as the formal parameter and E as the function body.
- Function application is denoted as E1.E2, signifying the application of function E1 to actual argument E2.

## Tenets of Lambda Calculus
- Everything is a function.
- There are no notions of state or side effects.
- The order of evalutation is irrelevant.
- All functions are unary which only takes one argument.

## Function Abstraction & Application
- Breaks a particular problem into a series of steps.
- Not arbitrary.
- If a step cannot be mapped to a function then it is not a useful step.

- Function Applicatio: apply function to an argument and obtain a value as output.

## Lambda Expression
- A short function.
- Block of code can pass arguments to a function call.
- Known as Anonymous Class or Blocks.
- Can created without belong to any class.
- Essentially an object can be passed around in functional java language.

## JavaScript Class Expression
![image](https://github.com/TheDaniel3131/design-patterns-module-study-materials-notes-and-exercises/assets/71692327/d05bb182-4769-46c4-af22-0f15f75d2d6b)

## Lambda Expressions: Arrow Function
![image](https://github.com/TheDaniel3131/design-patterns-module-study-materials-notes-and-exercises/assets/71692327/1793dd5b-ed44-4afa-9bf5-8c1c0ebb79a9)

## Function Vs Methods in JavaScript
- A function is a piece of code that can be called by its name. It can be used to pass arguments that it can operate on and return values optionally. 
- A method is a piece of code that must be called by its name that is associated with an object.

```javascript
//A Simple Function
var simple = (a) => {return a} // A simple function
simple(5) //called by its name

//A Simple Method
var obj = {simple : (a) => {return a} }
obj.simple(5) //called by its name along with its associated object
```
### Lambda Parameters
- Take parameters like functions.
- Have to match parameters of the function.
  1. Zero parameter.
  2. One parameter.
  3. Multiple parameters.

- The lambda expression's body is specified to the right of the "=>" arrow.
- If there are multiple lines, we need to use brackets.
- We can also add a return statement to get the lambda expression's result.

## Lambda / Arrow Function
In general, lambda expressions are used to create functions in the same way as function declarations, except that no name is specified for the function and the return keyword and braces are omitted (if there is only one parameter, the parentheses around the parameter list can also be omitted, as in the examples we have seen).

(parameters) => expression

The resulting function is just as much a function as one that is created using a function declaration statement. The only difference is that it has not been associated with any name in the environment.

![image](https://github.com/TheDaniel3131/design-patterns-module-study-materials-notes-and-exercises/assets/71692327/18ac7f89-3cc7-405a-bd35-3c8074c5a2ff)


```javascript
// Traditional anonymous function
(function (a) {
  return a + 100;
});

// 1. Remove the word "function" and place arrow between the argument and opening body brace
(a) => {
  return a + 100;
};
// 2. Remove the body braces and word "return" — the return is implied.
(a) => a + 100;


// 3. Remove the parameter parentheses
a => a + 100;

The braces can only be omitted if the function directly returns an expression. If the body has additional lines of processing, the braces are required — and so is the return keyword. Arrow functions cannot guess what or when you want to return.
```

```javascript
/ Traditional anonymous function

(function (a, b) {
  return a + b + 100;
});

// Arrow function
(a, b) => a + b + 100;

const a = 4;
const b = 2;
// Traditional anonymous function (no parameters)

(function () {
  return a + b + 100;
});

// Arrow function (no parameters)
() => a + b + 100;
```

```javascript
() => expression

param => expression

(param) => expression

(param1, paramN) => expression

() => {
  statements
}

param => {
  statements
}

(param1, paramN) => {
  statements
}
```

```javascript
If the body of your arrow function is a single return statement but the expression to be returned is an object literal, then you have to put the object literal inside parentheses to avoid syntactic ambiguity between the curly braces of a function body and the curly braces of an object literal:

const f = x => { return { value: x }; }; // Good: f()
returns an object
const g = x => ({ value: x }); // Good: g()
returns an object
const h = x => { value: x }; // Bad: h() returns
nothing
const i = x => { v: x, w: x }; // Bad: Syntax
Error

```
