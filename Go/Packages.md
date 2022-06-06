Every Go program is made up of packages.
Programs start running in package `main`
**Import** : 
```
import (
	"fmt"
	"math/rand"
)
```
By convention, the package name is the same as the last element of the import path. For instance, the `"math/rand"` package comprises files that begin with the statement `package rand`.

**Export functions and variables**
In Go, a name is exported if it begins with a capital letter. For example, `Pizza` is an exported name, as is `Pi`, which is exported from the `math` package.

```
package main

import (
	"fmt"
	"math"
)

func main() {
	fmt.Println(math.Pi)
}
```
