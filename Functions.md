# Functions
functions are defined by a name and brackets, called the argument list, and a block.
```
do_something () {
    // do something
}
```
functions that don't have an explicit return type do not return anything and aren't able to do so.
```
increment (n : i32) -> int32 {
    return n + 1;
}
```
functions can also call other functions or themselves.
```
factorial (n: i32) -> int32 {
    return if (n <= 1) {
        1;
    } else {
        n * factorial(n - 1);
    }
}
```
