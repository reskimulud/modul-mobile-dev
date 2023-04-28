# Properties

Sebuah kelas dalam Kotlin tentu memiliki properti. Masing - masing kelas memiliki properti yang berbeda. Contoh sebelumnya pada kelas `Animal`, properti yang dimiliki berupa `name`, `weight`, `age` dan `isMammal`.

Sama seperti variabel yang sudah kita pelajari pada sub-modul **Data Types**, properti dapat dideklarasikan sebagai nilai _mutable_ dengan menggunakan `var` atau sebagai nilai _read-only_ dengan menggunakan `val`.

```kotlin
class Animal(
    val name: String,
    val weight: Double,
    val age: Int,
    val isMammal: Boolean
)
```

Pada kode di atas, kita mendeklarasikan properti `name`, `weight`, `age` dan `isMammal` sebagai nilai _read-only_ dengan menggunakan `val`. Artinya, kita tidak dapat mengubah nilai dari properti tersebut setelah objek dari kelas `Animal` dibuat.

## Property Accessor

Secara standar ketika properti pada kelas dibuat _mutable_, maka Kotlin akan menghasilkan fungsi _**getter**_ dan _**setter**_ pada properti tersebut. Jika properti pada sebuah kelas dibuat _read-only_, Kotlin hanya akan menghasilkan fungsi _getter_ pada properti tersebut. Namun sebenarnya Anda bisa membuat fungsi _getter_ dan _setter_ secara manual jika pada kasus tertentu Anda perlu untuk override fungsi tersebut.

Perhatikan kode berikut:

```kotlin
class Animal{
    var name: String = "Jimeng"
}
 
fun main(){
    val myCat = Animal()
    println("Nama: ${myCat.name}" )
    myCat.name = "Goose"
    println("Nama: ${myCat.name}")
}
 
/*
output:
Nama: Jimeng
Nama: Goose
*/
```

Pada kode  `${myCat.name}` sebenarnya terjadi proses pemanggilan fungsi _getter_ pada properti `name`. Namun kita tidak melakukan override pada fungsi getter  sehingga fungsi tersebut hanya mengembalikan nilai `name` saja. Begitu juga pada kode myCat.`name = "Goose"` pada kode tersebut terjadi pemanggilan fungsi _setter_ pada properti `name`.

Tetapi jika kita melakukan override pada fungsi _getter_ dan juga _setter_ , maka kita dapat menambahkan kode lain pada fungsi _getter_ sesuai dengan kebutuhan. Mari kita coba modifikasi kode sebelumnya menjadi:

```kotlin
class Animal{
    var name: String = "Jimeng"
        get() {
            println("Fungsi getter terpanggil")
            return field
        }
        set(value) {
            println("Fungsi setter terpanggil")
            field = value
        }
}

fun main(){
    val myCat = Animal()
    println("Nama: ${myCat.name}" )
    myCat.name = "Goose"
    println("Nama: ${myCat.name}")
}

/*
output:
Fungsi getter terpanggil
Nama: Dicoding Miaw
Fungsi setter terpanggil
Fungsi getter terpanggil
Nama: Goose
*/
```

Urutan pendefinisian fungsi `get()` dan `set()` tidaklah penting, kita dapat mendefinisikan fungsi `get()` tanpa mendefinisikan fungsi `set()` dan juga sebaliknya. Yang terpenting pendeklarasiannya dilakukan setelah mendeklarasikan properti tersebut. Pada fungsi `get()`, kita perlu mengembalikan nilai sesuai tipe data dari propertinya atau kita dapat mengembalikan nilai dari properti itu sendiri dengan menggunakan _keyword_ `field`. Sedangkan untuk fungsi `set()` kita memerlukan sebuah parameter. Ini merupakan sebuah nilai baru yang nantinya akan dijadikan nilai properti. Pada kode di atas parameter tersebut ditetapkan dengan nama `value`.

## Property Delegation

Pengelolaan properti kelas baik itu memberikan atau merubah sebuah nilai dapat didelegasikan kepada kelas lain. Dengan ini kita dapat meminimalisir _boilerplate_ dalam penulisan _getter_ dan _setter_ (jika properties menggunakan **var**) pada setiap kelas yang kita buat. Sebagai contoh, kita memiliki tiga buah kelas yang di dalamnya memiliki satu properti String. Jika kita ingin menerapkan _getter_ dan _setter_ pada setiap properti kelasnya, maka kita perlu menuliskan _getter_ dan _setter_ tersebut pada seluruh kelas. Hal tersebut dapat mengurangi efisiensi dalam menuliskan kode karena terlalu banyak kode yang harus kita tulis secara berulang. Solusinya, kita perlu membuat sebuah kelas yang memang bertugas untuk mengatur atau mengelola fungsi _getter_ dan _setter_ untuk sebuah properti kelas. Teknik tersebut pada Kotlin dinamakan **Delegate**.

Sebelum mendelegasikan sebuah properti kita perlu membuat kelas delegasi terlebih dahulu. Mari kita buat sebuah kelas delegasi.

```kotlin
import kotlin.reflect.KProperty
 
 
class DelegateName {
    private var value: String = "Default"
 
    operator fun getValue(classRef: Any?, property: KProperty<*>) : String {
        println("Fungsi ini sama seperti getter untuk properti ${property.name} pada class $classRef")
        return value
    }
 
    operator fun setValue(classRef: Any?, property: KProperty<*>, newValue: String){
        println("Fungsi ini sama seperti setter untuk properti ${property.name} pada class $classRef")
        println("Nilai ${property.name} dari: $value akan berubah menjadi $newValue")
        value = newValue
    }
}
```

Kemudian untuk mendelegasikan sebuah properti kelas, kita gunakan _keyword_ `by` dalam menginisialisasi properti tersebut kemudian diikuti dengan namanya. Perhatikan kode berikut:

```kotlin
class Animal {
    var name: String by DelegateName()
}

fun main(){
    val myCat = Animal()
    myCat.name = "Goose"
    println(myCat.name)
}

/*
output:
Fungsi ini sama seperti setter untuk properti name pada class Animal@7f31245a
Nilai name dari: Default akan berubah menjadi Goose
Fungsi ini sama seperti getter untuk properti name pada class Animal@7f31245a
Goose
*/
```

**[<< Sebelumnya](m13-class-object.md)**  | **[Selanjutnya >>](m15-constructor.md)**
