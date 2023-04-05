# Tipe ata dan Variable

Tipe data adalah sebuah pengklasifikasian data berdasarkan jenis data tersebut. Untuk mengembangkan sebuah program, ada beberapa tipe data yang akan kita pelajari. Di antaranya adalah **Character**, **String**, **Array**, **Numbers** dan **Booleans**. Semuanya akan dibahas pada modul ini.

## Vaariable

Namun sebelumnya, ada satu hal yang kita perlu tahu terlebih dahulu, yaitu **Variabel**. Umumnya variabel digunakan untuk menyimpan informasi atau nilai yang akan dikelola di dalam sebuah program. Sebuah variabel akan membutuhkan kata kunci `var` atau `val`, **identifier**, **type** dan **initialization**. Kira-kira strukturnya seperti berikut:

```kotlin
var <identifier>: <type> = <initialization>
```

Berikut adalah contoh variabel dengan tipe String:

```kotlin
var name: String = "Reski Mulud Muchamad"
```

Berikut adalah detail penjelasan dari pembuatan variable di atas:

* **`var` atau `val`**
  `var` atau `val` digunakan untuk mengontrol nilai dari sebuah variabel. Dengan kata kunci `var` kita bisa mengubah nilai yang sudah kita inisialisasikan. Sebagai contoh:

  ```kotlin
  var name: String = "Reski"
  name = "Reski Mulud Muchamad"
  ```

  Variabel `name` yang awalnya memiliki nilai **“Reski”** sekarang sudah diubah menjadi **“Reski Mulud Muchamad”**. Sedangkan jika kita menggunakan kata kunci `val`, kita tidak bisa mengubah nilai yang sebelumnya sudah kita inisialisasi. Jika kita memaksa untuk mengubahnya, maka akan terjadi eror seperti berikut:

  ```kotlin
  val name: String = "Reski"
  name = "Reski Mulud Muchamad" //Val cannot be reassigned
  ```

* **identivier**
  _Identifier_ merupakan nama dari sebuah variabel. Pada contoh kode di atas yang merupakan _identifier_ adalah **name**. Perlu diketahui bahwa di dalam sebuah program kita tidak bisa membuat lebih dari 1 (satu) variabel dengan nama sama.

[Masih berlanjut]

**[<< Sebelumnya](m1-fundamental-kotlin.md)**  | **[Selanjutnya >>](m3-function-kotlin.md)**
