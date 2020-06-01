# Map

Golang provides a built-in map type that implements a hash table.

## Deklarasi

Secara umum bentuk map adalah:

```
map[KeyType]ValueType
```

Di mana:
* ```KeyType``` dapat berupa tipe data apapun yang dapat dikomparasi
* ```ValueType``` dapat berupa semua tipe data

Hal yang tidak disarankan untuk mendeklarasikan ```map``` dengan :

```
var m map[string]int
```

Nilai ```m``` adalah ```nil```, jika variabel tersebut diberikan nilai maka akan menyebabkan ```panic```, karena tipe map adalah tipe reference, seperti pointer.

Untuk mendeklarasikan map sebaiknya lakukan dengan:

```
m := make(map[string]int)
```

Menggunakan perintah ```make``` akan mengalokasikan dan menginisiasi map.