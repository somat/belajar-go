# Bekerja Dengan String

Golang mulai versi 1.10 memiliki type ```strings.Builder``` untuk keperluan bekerja dengan string yang dinamis.

Tipe ```string``` merupakan tipe yang immutable sehingga ketika kita ingin mengubah nilai sebuah variable string maka kita sebenarnya membuat alokasi baru di memori.

Contoh penggunaan string Builder:

```
package main

import (
	"fmt"
	"strings"
)

func main() {
	params := make(map[string]string)
	params["q"] = "somat"

	sql := buildSQL(params)

	fmt.Println(sql)
}

func buildSQL(params map[string]string) string {
	var sql strings.Builder

	sql.WriteString("SELECT * FROM students WHERE active IS TRUE ")
	if q, ok := params["q"]; ok {
		sql.WriteString("AND name LIKE '%" + q + "%'")
	}

	return sql.String()
}
```