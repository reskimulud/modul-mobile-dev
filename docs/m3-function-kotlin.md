# Function

Function atau fungsi merupakan sebuah prosedur yang memiliki keterkaitan dengan pesan dan objek. Ketika kita memanggil sebuah fungsi maka sebuah _mini-program_ akan dijalankan. Fungsi sendiri bisa diartikan sebagai cara sederhana untuk mengatur program buatan kita.

## Struktur Function

Sebuah fungsi dapat kita gunakan untuk mengembalikan nilai. Pemanggilan sebuah fungsi sendiri, bisa diberi argumen atau tidak. Berikut adalah struktur dari sebuah fungsi:

```kotlin
fun functionName(param1: Type1, param2: Type2, ...): ReturnType {
    return result
}
```

- `fun` merupakan kata kunci yang digunakan untuk mendeklarasikan sebuah fungsi.
- `functionName` merupakan nama dari fungsi tersebut.
- `param1`, `param2`, dst merupakan parameter yang akan digunakan oleh fungsi tersebut.
- `Type1`, `Type2`, dst merupakan tipe data dari parameter yang digunakan.

## Pendeklarasian Function

Pendeklarasian fungsi pada Kotlin diawali dengan kata kunci `fun` kemudian dilanjutkan dengan nama fungsi yang dikehendaki. Selanjutnya adalah parameter yang berada pada fungsi yang dideklarasikan. Awali dengan nama parameter dan ikuti dengan tipe parameter itu sendiri yang dipisahkan oleh karakter colon (`:`). Setiap parameter yang berada pada sebuah fungsi dipisahkan oleh karakter koma dan berada di dalam tanda kurung.

```kotlin
fun sayHello(name: String)
```

Setelah menentukan nama dan parameter, selanjutnya adalah menentukan tipe kembalian dari fungsi yang dibuat. Perlu diketahui fungsi pada Kotlin selalu mengembalikan nilai. Tipe kembalian adalah nilai yang akan dikembalikan ketika fungsi tersebut dipanggil. Tipe kembalian dari sebuah fungsi dituliskan setelah parameter dan diawali dengan karakter colon (`:`). Tipe kembalian dari sebuah fungsi tidak wajib dituliskan. Jika tidak dituliskan maka secara otomatis akan dianggap sebagai fungsi yang tidak mengembalikan nilai.

```kotlin
fun sayHello(name: String): String
```

Fungsi di atas akan mengembalikan nilai berupa String. Setelah menentukan tipe nilai kembalian, barulah kita menentukan function body di mana di dalamnya terdapat expression atau statement untuk dijalankan. Function body berada di dalam curly braces (`{}`) setelah tipe nilai kembalian.

```kotlin
fun sayHello(name: String): String {
    return "Hello $name"
}
```

Nilai yang akan dikembalikan diikuti oleh kata kunci `return`. Jika di dalam suatu fungsi hanya memiliki satu expression untuk menentukan nilai kembalian, maka fungsi tersebut bisa diubah menjadi expression body. Kita hanya perlu menambahkan tanda `=` dan menuliskannya seperti berikut:

```kotlin
fun sayHello(name: String): String = "Hello $name"
```

Jika kita tidak ingin fungsi yang dibuat mengembalikan nilai, kita bisa menggunakan `Unit` sebagai tipe nilai kembaliannya. Contohnya seperti berikut:

```kotlin
fun sayHello(name: String): Unit {
    println("Hello $name")
}
```

Ketika menggunakan tipe kembalian `Unit`, Kotlin memungkinkan kita untuk menghilangkannya. Kenapa demikian? Kompiler akan mendeteksinya sebagai tipe kembalian yang redundant:

```kotlin
fun sayHello(name: String) {
    println("Hello $name")
}
```

## Memanggil Function

Setelah mendeklarasikan sebuah fungsi, selanjutnya adalah memanggil fungsi tersebut. Memanggil fungsi sama seperti memanggil fungsi pada bahasa pemrograman lainnya. Berikut adalah contoh pemanggilan fungsi:

```kotlin
fun sayHello(name: String): String = "Hello $name"

fun main() {
    val name = "Reski Mulud"
    val result = sayHello(name)
    println(result)
}
```

## Function Overloading

Function overloading adalah kemampuan sebuah fungsi untuk memiliki nama yang sama dengan fungsi lainnya. Namun, fungsi tersebut memiliki parameter yang berbeda. Berikut adalah contoh fungsi overloading:

```kotlin
fun sayHello(name: String): String = "Hello $name"

fun sayHello(name: String, age: Int): String = "Hello $name, you are $age years old"

fun main() {
    val name = "Reski Mulud"
    val age = 20
    val result = sayHello(name, age)
    println(result)
}
```

## Default Parameter

Kita bisa memberikan nilai default pada parameter yang ada pada sebuah fungsi. Nilai default tersebut akan digunakan ketika parameter tersebut tidak diisi saat fungsi tersebut dipanggil. Berikut adalah contoh penggunaan default parameter:

```kotlin
fun sayHello(name: String = "Reski Mulud"): String = "Hello $name"

fun main() {
    val result = sayHello()
    println(result)
}
```

## Named Parameter

Kita bisa memberikan nama pada parameter yang ada pada sebuah fungsi. Nama parameter tersebut akan digunakan ketika fungsi tersebut dipanggil. Berikut adalah contoh penggunaan named parameter:

```kotlin
fun sayHello(name: String, age: Int): String = "Hello $name, you are $age years old"

fun main() {
    val result = sayHello(age = 20, name = "Reski Mulud")
    println(result)
}
```

## Variadic Parameter

Kita bisa membuat fungsi yang memiliki jumlah parameter yang tidak terbatas. Untuk membuat fungsi tersebut, kita bisa menggunakan variadic parameter. Variadic parameter merupakan parameter yang memiliki tipe data `vararg`. Berikut adalah contoh penggunaan variadic parameter:

```kotlin
fun sayHello(vararg names: String): String {
    var result = ""
    for (name in names) {
        result += "Hello $name\n"
    }
    return result
}

fun main() {
    val result = sayHello("Reski Mulud", "Reski Mulud", "Reski Mulud")
    println(result)
}
```

## Infix Function

Kita bisa membuat fungsi menjadi infix function. Infix function adalah fungsi yang bisa dipanggil tanpa menggunakan tanda titik dan kurung. Berikut adalah contoh penggunaan infix function:

```kotlin
infix fun Int.plus(value: Int): Int = this + value

fun main() {
    val result = 10 plus 10
    println(result)
}
```

**[<< Sebelumnya](m1-fundamental-kotlin.md)**  | **[Selanjutnya >>](m3-function-kotlin.md)**
