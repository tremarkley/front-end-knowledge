What is the difference between null and undefined?
- Undefined means a variable has been declared but has not yet been assigned a value. On the other hand, null is an assignment value. It can be assigned to a variable as a representation of no value.

What is a typical use case for anonymous functions?
- Typical use case is to pass them as an argument into other functions.

What are the use cases for arrow functions?
- Shorter syntax
- An arrow function does not have its own this; the this value of the enclosing execution context is used. Thus, in the following code, the this within the function that is passed to setInterval has the same value as this in the enclosing function:
``` javascript
function Person(){
  this.age = 0;

  setInterval(() => {
    this.age++; // |this| properly refers to the person object
  }, 1000);
}

var p = new Person();
```