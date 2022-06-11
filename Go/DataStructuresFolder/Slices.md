An array has a fixed size. A slice, on the other hand, is a dynamically-sized, flexible view into the elements of an array. In practice, slices are much more common than arrays.
The type `[]T` is a slice with elements of type `T`.

**NOTE**: A slice does not store any data, it just describes a section of an underlying array. Changing the elements of a slice modifies the corresponding elements of its underlying array.

Slice has:
* **Length** - number of elements it contains;
* **Capacity** - is the number of elements in the underlying array, counting from the first element in the slice;
The length and capacity of a slice `s` can be obtained using the expressions `len(s)` and `cap(s)`.

**Nil slices**
The zero value of a slice is `nil`.
A nil slice has a length and capacity of 0 and has no underlying array.

Other slices that share the same underlying array will see those changes.

A slice is formed by specifying two indices, a low and high bound, separated by a colon:
```
a[low : high]
```

This selects a half-open range which includes the first element, but excludes the last one.

```
unc main() {
	primes := [6]int{2, 3, 5, 7, 11, 13}

	var s []int = primes[1:4]
	fmt.Println(s)
}
/// [3 5 7]
```

## Slice Literals

```
[]bool{true, true, false}
```

```
package main

import "fmt"

func main() {
	q := []int{2, 3, 5, 7, 11, 13}
	fmt.Println(q)

	r := []bool{true, false, true, true, false, true}
	fmt.Println(r)

	s := []struct {
		i int
		b bool
	}{
		{2, true},
		{3, false},
		{5, true},
		{7, true},
		{11, false},
		{13, true},
	}
	fmt.Println(s)
}
///[2 3 5 7 11 13]
///[true false true true false true]
///[{2 true} {3 false} {5 true} {7 true} {11 false} {13 true}]
```

[[Slice Defaults]]
[[Appending to Slice]]