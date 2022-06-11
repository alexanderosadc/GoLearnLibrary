A defer statement defers the execution of a function until the surrounding function returns. The deferred call's arguments are evaluated immediately, but the function call is not executed until the surrounding function returns.

```
func main() {
	defer fmt.Println("world")

	fmt.Println("hello")
}
// Returns
hello
world
```

## Stacking Deffers
Deferred function calls are pushed onto a stack. When a function returns, its deferred calls are executed in last-in-first-out order.

```
for i := 0; i < 10; i++ {
		defer fmt.Println(i)
	}
```

## Rules of deffer functions
1. A deferred function’s arguments are evaluated when the defer statement is evaluated.
2. Deferred function calls are executed in Last In First Out order after the surrounding function returns.
3. 3.  Deferred functions may read and assign to the returning function’s named return values.

[[Panic]]