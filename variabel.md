# Variabel

Variabel dapat dianalogikan seperti sebuah tempat penyimpanan, yang isi nya dapat diambil atau dimodifikasi.

Variabel dalam bahasa Golang dideklarasikan secara eksplisit, dengan tipe data tertentu.

Adapun deklarasi variabel dapat menggunakan kata kunci ```var```:

```
var name string
```

```var``` kata kunci var mendefinisikan satu atau lebih variabel, contoh di atas mendeklarasikan variabel dengan nama ```name``` dengan tipe data ```string```

```
var name, address, phone string
```

Contoh di atas mendeklarasikan beberapa variable menggunakan kata kunci ```var```

Deklarasi variable dapat juga menyertakan inisiasi nilai:

```
var name, address = "Somat", "Jakarta"
```

Jika deklarasi variabel menyertakan nilai awal (nilai inisiasi), maka tipe data dari variabel tersebut boleh tidak disebutkan, seperti contoh di atas.

## Deklarasi Variabel Dengan Jalan Pintas

Di dalam fungsi, deklarasi variabel dapat dilakukan dengan jalan pintas, yaitu dengan menggunakan ```:=```

```
package main

import (
	"fmt"
)

func main() {
    name, address := "Somat", "Jakarta"
    fmt.Println("Hello, ", name, address)
}

```
