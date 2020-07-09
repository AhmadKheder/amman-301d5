# The Call Stack
A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.

Example of infinite loop of the call stack that will exceed the **size of the call stack**
![](https://i.ytimg.com/vi/VbJRTyTbbZw/maxresdefault.jpg)
**That was STACK OVERFLOW**


# What causes a stack overflow?
A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.
```javascript
function callMyself(){
  callMyself();
}

callMyself();
```

The `callMyself()` will run until the browser throws a “Maximum call size exceeded”. And that is a stack overflow.
 
The key takeaways from the call stack are:
1. It is single-threaded. Meaning it can only do one thing at a time.
2. Code execution is synchronous.
3. A function invocation creates a stack frame that occupies a temporary memory.
4. It works as a LIFO — Last In, First Out data structure.

# JavaScript error messages && debugging
## Types of error messages:
1. Reference errors:
This is as simple as when you try to use a variable that is not yet declared you get this type os errors.
`console.log(foo) // Uncaught ReferenceError: foo is not defined`


This is also a common thing when using `const` and `let`, *they are hoisted like var and function but there is a time between the hoisting and being declared *so when you try to access them a reference error occurs, the fact that this happens to let and const is called __Temporal Dead Zone__ (TDZ).
`foo = 'Hello' // Uncaught ReferenceError: foo is not defined
let foo`

2. Syntax errors:


this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

`JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1`




solution:`JSON.parse('{"foo":"bar"}')`

3. Range errors:
An array for instance cannot have a negative length, why would you mess with the array length? Some people use it to set an array to empty, something of the likes of:
`var foo = [0, 0]
foo.length = foo.length - 2 // (or foo.length - foo.length)
foo // would log [] instead of [0, 0]`

4. Type errors:

this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

`var foo = {}
foo.bar // undefined
foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined`










