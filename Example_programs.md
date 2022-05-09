# Prime checker
```
static {
    use std.IO;
    use std.Math;
}

main () {
    list_primes();
}

list_primes () {
    [1..10].filter(is_prime)
        .for_each(print);
}

is_prime (n: int) -> bool {
    [1..sqrt(n)].none(x -> x % 2 == 0);
}
```

```
static {
    use std.ctrl;
}

data Tree<A> {
    Leaf | Node Tree<A> A Tree<A>
    
    @literal (literal: str) -> Maybe<Tree<A>> {
        // todo
        return empty();
    }
}

contains <Eq A> (value: A, tree: Tree<A>) {
    return match (tree) {
        ~ Node t1 v t2 -> 
            v == value | t2.contains(value) | t1.contains(value)
        ~ Leaf -> false
    }
}
```
