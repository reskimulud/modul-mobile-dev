# Class dan Object

## Apa itu Class

Seperti yang telah dijelaskan sebelumnya, **Class** merupakan sebuah _blueprint_. Dalam sebuah kelas, kita menentukan atribut dan perilaku sebagai sebuah blueprint. Sebagai contoh, kelas Kendaraan memiliki atribut seperti roda, warna, nomor kendaraan, dan merk, serta perilaku seperti maju, mundur, belok kanan, belok kiri, dan berhenti. Sebaliknya, kelas Hewan memiliki atribut seperti nama, berat, umur, dan apakah termasuk mamalia atau bukan, serta perilaku seperti makan, tidur, dan berjalan.

Tiap kelas memiliki atribute dan behaviour, atau yang lebih dikenal di Kotlin sebagai properties dan function. Properties pada sebuah kelas memiliki tipe data yang dapat ditentukan, seperti pada contoh kelas Hewan, properti berat memiliki tipe data Double, properti nama memiliki tipe data String, properti umur memiliki tipe data Int, dan properti indikasi mamalia memiliki tipe data Boolean. Jika kita menggambarkan kelas Hewan dalam tabel, maka akan terlihat seperti ini:

|     Properties      |
|---------------------|
| + nama: String <br> + berat: Double <br> + berat: Double <br> + umur: Int <br> + mamalia: Boolean    |
| - makan() <br> - tidur()  <br> - berjalan()  |

- (+) merupakan properties
- (-) merupakan function

## Membuat Class

Untuk mendefinisikan kelas dalam Kotlin, cukup gunakan kata kunci `class` diikuti dengan nama kelas yang akan dibuat. Mari kita buat contoh kelas pada Kotlin:

```kotlin
class Animal
```

Lalu tambahkan properti dan fungsi pada kelas tersebut.

```kotlin
class Animal {
    val name: String
    val weight: Double
    val age: Int
    val isMammal: Boolean

    fun eat() {
        println("$name is eating")
    }

    fun sleep() {
        println("$name is sleeping")
    }

    fun walk() {
        println("$name is walking")
    }
}
```

Untuk membuat object dari sebuah class, perhatikan struktur berikut :

```kotlin
var nameOfObject = NameOfClass([property1, property2, ...])
```

Sama seperti variabel, kita bisa gunakan `val` atau `var`, dilanjutkan dengan nama objek yang akan anda buat. Tanda `=` menunjukan bahwa kita akan menginisialisasi suatu objek, kemudian diikuti dengan nama kelas dan tanda kurung. Tanda kurung tersebut menunjukan bahwa kita membuat sebuah objek baru. Di dalam tanda kurung kita dapat menambahkan nilai properti sesuai yang dibutuhkan pada **primary constructor** kelasnya.

Maka jika kita buat object dari kelas Animal, maka akan menjadi seperti ini:

```kotlin
var myCat = Animal("Oyen", 4.2, 2, true)
```

Kita buat secara keseluruhan

```kotlin
class Animal(val name: String, val weight: Double, val age: Int, val isMammal: Boolean) {
    fun eat() {
        println("$name is eating")
    }

    fun sleep() {
        println("$name is sleeping")
    }

    fun walk() {
        println("$name is walking")
    }
}

fun main() {
  val myCat = Animal("Oyen", 4.2, 2, true)
  println("Nama: ${myCat.name}, Berat: ${myCat.weight}, Umur: ${myCat.age}, Mamalia: ${myCat.isMammal}")
  myCat.eat()
  myCat.sleep()
  myCat.walk()
}

// Output
Nama: Oyen, Berat: 4.2, Umur: 2, Mamalia: true
Oyen is eating
Oyen is sleeping
Oyen is walking
```

**[<< Sebelumnya](m12-oop.md)**  | **[Selanjutnya >>](m14-properties.md)**
