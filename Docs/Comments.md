# Comments
Comments can either be single line or multiline. 
Anything after the `//` as well as between `///` and `///` is ignored by the compiler.
```
// this is a single line comment

///
this is a multiline comment
All of this is ignored by the compiler
Until it is ended
///
```
It is recommended to keep comments on their own lines, but they can trail after code.

Thus
```
// call function
function();
```
is preferred over
```
function(); // call function
```
