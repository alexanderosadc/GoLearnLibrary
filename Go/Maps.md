The zero value of a map is `nil`. A `nil` map has no keys, nor can keys be added.
The `make` function returns a map of the given type, initialized and ready for use.
```
package main

import "fmt"

type Vertex struct {
	Lat, Long float64
}

var m map[string]Vertex

func main() {
	m = make(map[string]Vertex)
	m["Bell Labs"] = Vertex{
		40.68433, -74.39967,
	}
	fmt.Println(m["Bell Labs"])
}
```

## Map literals

```
package main

import "fmt"

type Vertex struct {
	Lat, Long float64
}

var m = map[string]Vertex{
	"Bell Labs": Vertex{
		40.68433, -74.39967,
	},
	"Google": Vertex{
		37.42202, -122.08408,
	},
}

func main() {
	fmt.Println(m)
}
```

### Insert an element
```
m[key] = elem
```

### Retrieve the element
```
elem = m[key]
```

### Delete an Element
```
delete(m, key)
```

### Test that a key is present with a two-value assignment:
```
elem, ok := m[key]
/// ok is true if element with key is present in the map m
```

```

```