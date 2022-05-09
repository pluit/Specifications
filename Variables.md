# Variables
Variables are strongly typed and declared with the `let` keyword 
and immutable unless specified otherwise by the `variable` modifier.
```
// immutable
let x = 5;

// mutable
let variable y = 10;
```
If the compiler cannot infer the type of variable, it needs to be explicitly typed
```
let x : int32 = foo();
let y : str = bar();
let z : Tree<str> = baz();
```
