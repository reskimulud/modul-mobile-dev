# If  Else Expression

Pada materi sebelumnya kita sudah belajar tentang tipe data dan variable. Pada materi ini kita akan belajar tentang penggunaan if else pada Kotlin. If else merupakan salah satu control flow yang ada pada Kotlin. If else digunakan untuk melakukan pengecekan kondisi. Jika kondisi tersebut bernilai true, maka kode yang ada di dalam if akan dijalankan. Jika kondisi tersebut bernilai false, maka kode yang ada di dalam else akan dijalankan. Berikut adalah contoh penggunaan if else:

```kotlin
fun main() {
    val name = "Reski Mulud Muchamad"
    val age = 23

    if (age > 20) {
        println("$name is adult")
    } else {
        println("$name is not adult")
    }
}
```

## If Else If

Kita juga bisa melakukan pengecekan kondisi lebih dari satu. Untuk melakukan pengecekan kondisi lebih dari satu, kita bisa menggunakan if else if. Berikut adalah contoh penggunaan if else if:

```kotlin
fun main() {
    val name = "Reski Mulud Muchamad"
    val age = 23

    if (age > 20) {
        println("$name is adult")
    } else if (age > 17) {
        println("$name is teenager")
    } else {
        println("$name is not adult")
    }
}
```

## If Expression

Kita juga bisa menggunakan if expression. If expression digunakan untuk mengembalikan nilai. Berikut adalah contoh penggunaan if expression:

```kotlin
fun main() {
    val name = "Reski Mulud Muchamad"
    val age = 23

    val result = if (age > 20) {
        "$name is adult"
    } else {
        "$name is not adult"
    }

    println(result)
}
```

**[<< Sebelumnya](m3-function-kotlin.md)**  | **[Selanjutnya >>](m5-arrays.md)**
