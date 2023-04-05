# Break dan Continue

Ketika melakukan perulangan, terkadang kita dihadapkan dengan data yang tak sesuai harapan. Contoh, seperti berikut:

```kotlin
fun main() {
  val listOfInt = listOf(1, 2, 3, null, 5, null, 7)
  for (i in listOfInt) {
    print(i)
  }
}

// Output:
// 123null5null7
```

Pada kode di atas, kita melakukan perulangan pada `listOfInt` yang berisi tipe data `Int?` (nullable). Karena `null` bukan merupakan tipe data `Int`, maka kita akan mendapatkan error **NullPointerException (NPE)** saat melakukan perulangan. Lalu bagaimana kita melewatkan atau menghentikan proses perulangan jika nilai yang dihasilkan bernilai null? Nah, di sini kita bisa menggunakan **Break** dan **Continue**.

## Break

Break digunakan untuk menghentikan proses perulangan. Berikut contoh penggunaannya:

```kotlin
fun main() {
  val listOfInt = listOf(1, 2, 3, null, 5, null, 7)
  for (i in listOfInt) {
    if (i == null) break
    print(i)
  }
}

// Output:
// 123
```

Pada kode di atas, kita menggunakan `if` untuk memeriksa apakah nilai yang dihasilkan bernilai `null`. Jika iya, maka kita akan menghentikan proses perulangan dengan menggunakan `break`.

## Continue

Continue digunakan untuk melewatkan proses perulangan. Berikut contoh penggunaannya:

```kotlin
fun main() {
  val listOfInt = listOf(1, 2, 3, null, 5, null, 7)
  for (i in listOfInt) {
    if (i == null) continue
    print(i)
  }
}

// Output:
// 12357
```

Pada kode di atas, kita menggunakan `if` untuk memeriksa apakah nilai yang dihasilkan bernilai `null`. Jika iya, maka kita akan melewatkan proses perulangan dengan menggunakan `continue`.

## Break dan Continue Label

Pada Kotlin, sebuah _expression_ dapat ditandai dengan sebuah label. Label pada Kotlin memiliki sebuah identifier yang diikuti dengan tanda **@**. Contoh dari sebuah label adalah **foo@** atau **bar@**.

Untuk melabeli sebuah _expression_, kita cukup menempatkan label di depannya. Contohnya seperti berikut:

```kotlin
fun main() {
  val listOfInt = listOf(1, 2, 3, null, 5, null, 7)
  loop@ for (i in listOfInt) {
    if (i == null) continue@loop
    print(i)
  }
}

// Output:
// 12357
```

Pada kode di atas, kita menambahkan label **loop@** di depan _expression_ `for`. Lalu kita menggunakan label tersebut untuk menandai _expression_ `continue` sehingga proses perulangan akan dilanjutkan.

## Break dan Continue Label Nested

Kita juga dapat menggunakan label untuk melakukan break dan continue pada perulangan yang bersarang. Berikut contoh penggunaannya:

```kotlin
fun main() {
  val listOfInt = listOf(1, 2, 3, null, 5, null, 7)
  loop@ for (i in listOfInt) {
    for (j in 1..3) {
      if (i == null) continue@loop
      print(i)
    }
  }
}

// Output:
// 111222333555777
```

Pada kode diatas, `break` yang sudah ditandai dengan label akan dilompati ke titik awal proses perulangan yang sudah ditandai dengan label. `break` akan menghentikan proses perulangan terluar dari dalam proses perulangan, di mana break tersebut dipanggil.

**[<< Sebelumnya](m10-for-loop.md)**  <!-- | **[Selanjutnya >>]()** -->
