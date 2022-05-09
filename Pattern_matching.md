# Pattern matching
You can match different patterns using a `match` block. 
We can rewrite the `factorial` function we wrote in the section about functions in the following way:
```
factorial (n : int32) -> int32 {
    match (n) { 
        | 0 -> 1
        | n -> n * factorial(n - 1)
    }
}
```
```
fib (n) -> int32 {
    return match (n) {
        | 0 || 1 -> 1
        | fib(n - 1) + fib(n - 2)
    }
}
```
```
levenshtein_dist (a : str, b : str) -> int32 {
    return match (a, b) {
        | _, "" -> len(a)
        | "", _ -> len(b)
        | c:cs, c':cs' -> {
            if (c == c') {
                levenshtein_dist(cs, cs');
            } else {
                1 + min(
                    [(cs, cs'), (cs, b), (a, cs')]
                        .map(levenshtein_dist)  
                );
            }
        } 
    }
}
```
