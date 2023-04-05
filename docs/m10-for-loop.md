# For Loop

Sama seperti **While** dan **Do While**, **For** merupakan konsep perulangan pada blok yang sama selama hasil evaluasi kondisi yang diberikan terpenuhi atau bernilai **true**. For dapat digunakan pada **Ranges**, **Collections**, **Arrays** dan apapun yang menyediakan _iterator_. Contoh dari For loop sendiri adalah sebagai berikut:

## For dan Range

```kotlin
fun main() {
  val range = 1..5
  for (i in range) {
      println("Hello World")
  }
}

// Output:
// Hello World
// Hello World
// Hello World
// Hello World
// Hello World
```

Perhatikan kode di atas, kita menggunakan **Range** untuk melakukan perulangan. Range adalah sebuah kumpulan angka yang berurutan. Range pada Kotlin memiliki 3 jenis, yaitu **IntRange**, **LongRange**, dan **CharRange**. Untuk membuat **Range** kita bisa menggunakan operator **..**. Operator ini akan menghasilkan **IntRange** jika kita menggunakan angka bulat, **LongRange** jika kita menggunakan angka desimal, dan **CharRange** jika kita menggunakan karakter.

Karena menggunakan range expression, kita juga dapat menuliskannya seperti berikut:

```kotlin
fun main() {
  val range = 1.rangeTo(5)
  for (i in range) {
    println("Hello World")
  }
}
```

Selain itu, kita juga dapat menuliskan For loop menggunakan range expression seperti berikut:

```kotlin
fun main() {
  val range = 1.rangeTo(10) step 2
  for (i in range) {
    println("value is $i")
  }
}

// Output:
// value is 1
// value is 3
// value is 5
// value is 7
// value is 9
```

Pada kode di atas, kita menambahkan ekstensi `step` yang akan mengembalikan nilai baru dengan tipe `IntProgression` dengan jarak nilai sebelumnya adalah 3.

Kita juga dapat mengakses indeks untuk setiap elemen yang ada pada Ranges dengan memanfaatkan fungsi `withIndex()` seperti berikut:

```kotlin
fun main() {
  val range = 1.rangeTo(5)
  for ((index, value) in range.withIndex()) {
    println("value at index $index is $value")
  }
}

// Output:
// value at index 0 is 1
// value at index 1 is 2
// value at index 2 is 3
// value at index 3 is 4
// value at index 4 is 5
```

## ForEach

ForEach adalah fungsi yang dapat digunakan untuk melakukan iterasi pada setiap elemen dari sebuah Collection. Berikut contoh penggunaannya:

```kotlin
fun main() {
  val list = listOf("Hello", "World", "Kotlin")
  list.forEach { println(it) }
}

// Output:
// Hello
// World
// Kotlin
```

 Jika kita mendapatkan indeks dari tiap nilai yang dicakup kita bisa menggunakan ekstensi `forEachIndexed` seperti berikut:

```kotlin
fun main() {
  val list = listOf("Hello", "World", "Kotlin")
  list.forEachIndexed { index, value -> println("value at index $index is $value") }
}

// Output:
// value at index 0 is Hello
// value at index 1 is World
// value at index 2 is Kotlin
```

`forEachIndexed` memiliki dua argumen. Pertama adalah `index` yang merupakan indeks dari tiap nilai. Kedua adalah `value` yang merupakan nilai tunggal yang dicakup oleh `ranges` itu sendiri. Jika kita hanya ingin menggunakan argumen `index`, maka kita bisa mengubah argumen `value` menjadi `_` seperti berikut:

```kotlin
fun main() {
  val list = listOf("Hello", "World", "Kotlin")
  list.forEachIndexed { index, _ -> println("value at index $index") }
}

// Output:
// value at index 0
// value at index 1
// value at index 2
```

> Sebenarnya ini merupakan sebuah aturan di mana ketika argumen dari sebuah lambda expression tidak digunakan, kita disarankan agar mengubahnya menjadi `_` untuk menggantikan nama dari argumen tersebut

**[<< Sebelumnya](m9-while-loop.md)**  | **[Selanjutnya >>](m11-break-continue.md)**
