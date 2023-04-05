# Arrays

## Apa itu Array?

Array adalah sebuah tipe data yang digunakan untuk menyimpan sekumpulan data dengan tipe data yang sama. Array pada Kotlin memiliki tipe data yang bersifat **immutable**. Artinya, kita tidak bisa mengubah ukuran dari sebuah Array setelah kita deklarasikan. Jika kita ingin mengubah ukuran dari sebuah Array, maka kita harus membuat Array baru.

## Membuat Array

Untuk membuat sebuah Array, kita bisa menggunakan fungsi `arrayOf()`. Berikut adalah contoh penggunaan fungsi tersebut:

```kotlin
fun main() {
    val names = arrayOf("Reski", "Mulud")
    println(names[0])
    println(names[1])
}
```

## Mengakses Array

Untuk mengakses sebuah Array, kita bisa menggunakan indeks dari Array tersebut. Indeks pada Array dimulai dari 0. Berikut adalah contoh penggunaan indeks pada Array:

```kotlin
fun main() {
    val names = arrayOf("Reski", "Mulud")
    println(names[0])
    println(names[1])
}
```

## Array dengan Tipe Data Tertentu

Kita bisa membuat Array dengan tipe data tertentu. Berikut adalah contoh penggunaan Array dengan tipe data tertentu:

```kotlin
fun main() {
    val names: Array<String> = arrayOf("Reski", "Mulud")
    println(names[0])
    println(names[1])
}
```

## Array dengan Tipe Data Tertentu dan Ukuran Tertentu

Kita bisa membuat Array dengan tipe data tertentu dan ukuran tertentu. Berikut adalah contoh penggunaan Array dengan tipe data tertentu dan ukuran tertentu:

```kotlin
fun main() {
    val names: Array<String> = arrayOfNulls(2)
    names[0] = "Reski"
    names[1] = "Mulud"
    println(names[0])
    println(names[1])
}
```

## Array dengan Tipe Data Primitive

Kita bisa membuat Array dengan tipe data primitive.

* intArrayOf() : IntArray
* booleanArrayOf() : BooleanArray
* charArrayOf() : CharArray
* longArrayOf() : LongArray
* shortArrayOf() : ShortArray
* byteArrayOf() : ByteArray

Berikut adalah contoh penggunaan Array dengan tipe data primitive:

```kotlin
fun main() {
    val numbers: IntArray = intArrayOf(1, 2, 3)
    println(numbers[0])
    println(numbers[1])
    println(numbers[2])
}
```

**[<< Sebelumnya](m4-if-else.md)**  | **[Selanjutnya >>](m6-null.md)**
