# When Expresion

Untuk menentukan *statement* atau *expression* kita menggunakan **If Expression**.  Selain itu kita juga bisa gunakan  **When Expression**,  yakni mekanisme yang memungkinkan nilai dari sebuah variabel/*expression*, mampu mengubah alur program.

Contoh sederhana dari penggunaan **When Expression** adalah sebagai berikut:

```kotlin
fun main() {
    val value = 10
    when (value) {
        1 -> println("Value is 1")
        2 -> println("Value is 2")
        3 -> println("Value is 3")
        else -> println("Value is not 1, 2, or 3")
    }
}
```

Kode di atas akan mencetak `Value is not 1, 2, or 3` karena nilai dari variabel `value` adalah 10.

`when` akan membandingkan nilai dari variabel `value` dengan setiap nilai yang ada di dalam `when`. Jika nilai dari variabel `value` sama dengan salah satu nilai yang ada di dalam `when`, maka kode yang ada di dalam `when` akan dijalankan. Jika tidak ada nilai yang sama, maka kode yang ada di dalam `else` akan dijalankan.

Sama halnya seperti if expression, when expression dapat mengembalikan nilai dan dapat disimpan di dalam sebuah variabel seperti berikut:

```kotlin
fun main() {
    val value = 10
    val result = when (value) {
        1 -> "Value is 1"
        2 -> "Value is 2"
        3 -> "Value is 3"
        else -> "Value is not 1, 2, or 3"
    }
    println(result)
}
```

`else` adalah hal wajib jika kita menggunakan when expression untuk mengembalikan nilai. Bagaimana jika kita melewatkannya? Akan tampil eror berikut:

```kotlin
fun main() {
    val value = 10
    val result = when (value) {
        1 -> "Value is 1"
        2 -> "Value is 2"
        3 -> "Value is 3"
    }
    println(result)
}
```

```bash
Exception in thread "main" java.lang.IllegalStateException: when expression must be exhaustive, add necessary else branch
  at MainKt.main(main.kt:6)
  at MainKt.main(main.kt)
```

Jika kita memiliki dua atau lebih baris kode yang akan kita jalankan di setiap branch, kita bisa memindahkannya ke dalam *curly braces* seperti berikut:

```kotlin
fun main() {
    val value = 10
    val stringOfValue = when (value) {
        1 -> {
            println("Value is 1")
            "Value is 1"
        }
        2 -> {
            println("Value is 2")
            "Value is 2"
        }
        3 -> {
            println("Value is 3")
            "Value is 3"
        }
        else -> {
            println("Value is not 1, 2, or 3")
            "Value is not 1, 2, or 3"
        }
    }

    println(stringOfValue)
}
```

when juga memungkinkan kita untuk memeriksa instance dengan tipe tertentu dari sebuah objek menggunakan is atau !is. Contohnya seperti berikut:

```kotlin
fun main() {
    val value: Any = 10
    when (value) {
        is Int -> println("$value is an integer")
        is String -> println("$value is a string")
        else -> println("$value is not an integer or a string")
    }
}
```

**[<< Sebelumnya](m7-control-flow.md)**  | **[Selanjutnya >>](m9-while.md)**
