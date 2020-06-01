# Range

Perintah ```Range``` digunakan untuk melakukan pengulangan atas elemen dari berbagai macam tipe data.

```
package main

import (
	"fmt"
)

func main() {
    x := []string{"A", "B", "C"}
    for i, v := range x {
        fmt.Println(i, v)
    }
}
```
