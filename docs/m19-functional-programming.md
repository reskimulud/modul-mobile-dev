# Functional Programming

Seperti yang sudah disampaikan di awal, Kotlin merupakan sebuah _multiparadigm programming language_. Artinya selain merupakan bahasa pemrograman berorientasi objek, dalam penulisan sintaksnya Kotlin menggunakan gaya _functional programming_.

Perhatikan kode berikut:

```kotlin
val usersList: List<String> = getUsers()

fun getUsername(): List<String> {
  val names: MutableList<String> = mutableListOf()
  for (user in usersList) {
    names.add(user.name)
  }
  return names
}
```

Kode di atas merupakan contoh kode yang digunakan untuk mendapatkan nilai tertentu dari sebuah list (contoh di atas mengambil data nama dari sebuah list user). Kode di atas merupakan kode yang umum digunakan. Namun, dalam Kotlin, kita dapat menuliskan kode tersebut dengan lebih singkat menggunakan _functional programming_.

```kotlin
val usersList: List<String> = getUsers()

fun getUsername(): List<String> {
  return usersList.map { user -> user.name }
}
```

Itu adalah salah satu contoh dari _functional programming_ yang ada di Kotlin. Pada bagian ini kita akan membahas lebih dalam mengenai _functional programming_ pada Kotlin.

**[<< Sebelumnya](m18-abstract-interface.md)**  | **[Selanjutnya >>](m20-named-default-args)**
