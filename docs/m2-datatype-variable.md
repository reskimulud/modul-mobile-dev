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

* **dentifier**

  _Identifier_ merupakan nama dari sebuah variabel. Pada contoh kode di atas yang merupakan _identifier_ adalah **name**. Perlu diketahui bahwa di dalam sebuah program kita tidak bisa membuat lebih dari 1 (satu) variabel dengan nama sama.

* **Type**

  Pada bagian inilah kita menentukan tipe data dari variabel tersebut. Tipe data dibutuhkan agar kompiler dapat mengetahui bagaimana sebuah data akan digunakan. Tipe data dari contoh variabel di atas adalah **String**. Karena Kotlin mendukung type _inference_ maka kita diperbolehkan untuk tidak menuliskan tipe data secara eksplisit:

  ```kotlin
  val name = "Reski Mulud Muchamad"
  ```

* **Initialization**

  _Initialization_ adalah nilai awal dari sebuah variabel. Pada contoh kode di atas nilai awal dari variabel **name** adalah **“Reski Mulud Muchamad”**.

## Tipe Data

### Character

Tipe data **Character** digunakan untuk menyimpan karakter tunggal. Karakter tunggal ini bisa berupa huruf, angka, simbol, dan lain-lain. Untuk mendeklarasikan variabel dengan tipe data **Character** kita bisa menggunakan tanda petik tunggal (‘). Contoh:

```kotlin
val character: Char = 'A'
```

Jika kita memasukkan lebih dari 1 karakter, maka akan terjadi error seperti berikut:

```kotlin
val character: Char = 'AB' //Type mismatch: inferred type is String but Char was expected
```

### String

Tipe data **String** digunakan untuk menyimpan karakter lebih dari 1. Karakter ini bisa berupa huruf, angka, simbol, dan lain-lain. Untuk mendeklarasikan variabel dengan tipe data **String** kita bisa menggunakan tanda petik ganda (“). Contoh:

```kotlin
var textString = "Mobile Programming"
```

Pada dasarnya sekumpulan karakter dalam String tersebut berbentuk Array, sehingga kita bisa mendapatkan karakter tunggal dengan mudah. Caranya, manfaatkan **indexing** seperti berikut:

```kotlin
fun main() {
  val textString = "Mobile Programming"
  val firstChar = textString[0]
  val lastChar = textString[textString.length - 1]

  println("First character: $firstChar")
}

// Output: First character: M
```

> **Indexing** merupakan sebuah cara yang memudahkan kita untuk mengakses elemen yang berada di dalam sebuah Collection dengan memanfaatkan index atau posisi dari elemen tersebut. Posisi dari sebuah elemen pada umumnya dimulai dari angka 0.

### Boolean

Tipe data **Boolean** digunakan untuk menyimpan nilai **true** atau **false**. Untuk mendeklarasikan variabel dengan tipe data **Boolean** kita bisa menggunakan kata kunci **true** atau **false**. Contoh:

```kotlin
val isTrue: Boolean = true
val isFalse: Boolean = false
```

### Numbers

Tipe data **Numbers** digunakan untuk menyimpan angka. Di Kotlin, tipe data Number disimpan dengan cara yang berbeda. Beberapa tipe bawaan yang merepresentasikan Numbers adalah Double, Long, Int, Short dan Byte. Setiap tipe data Number memiliki ukuran (satuan Bit) berbeda-beda, tergantung besaran nilai yang dapat simpan.

| Tipe Data | Satuan Bit | Nilai Minimum | Nilai Maksimum |
| --- | --- | --- | --- |
| Double | 64 | 4.9e-324 | 1.8e+308 |
| Float | 32 | 1.4e-045 | 3.4e+038 |
| Long | 64 | -9,223,372,036,854,775,808 | 9,223,372,036,854,775,807 |
| Int | 32 | -2,147,483,648 | 2,147,483,647 |
| Short | 16 | -32,768 | 32,767 |
| Byte | 8 | -128 | 127 |

Berikut adalah contoh untuk mendeklarasikan variabel dengan tipe data Number:

```kotlin
val double: Double = 100.0
val float: Float = 100.0f
val long: Long = 100L
val int: Int = 100
val short: Short = 10
val byte: Byte = 1
```

**[<< Sebelumnya](m1-fundamental-kotlin.md)**  | **[Selanjutnya >>](m3-function-kotlin.md)**
