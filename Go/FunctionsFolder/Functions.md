Declaration of parameter type comes after variable name.
```
package main

import "fmt"

func add(x int, y int) int {
	return x + y
}

func main() {
	fmt.Println(add(42, 13))
}
```

The return type of the function comes after parameter declaration.

When two or more consecutive named function parameters share a type, you can omit the type from all but the last.

```
func add(x, y int) int {
	return x + y
}
```

[[Multiple Results]]
[[Named return values]]
[[Functions are values]]
[[Closures]]