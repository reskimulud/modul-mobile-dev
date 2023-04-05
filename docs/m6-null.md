# Tipe Null

Ketika mengembangkan sebuah program, ada satu hal yang tak boleh kita abaikan. Ia adalah **NullPointerException (NPE)**, sebuah kesalahan yang terjadi saat ingin mengakses atau mengelola nilai dari sebuah variabel yang belum diinisialisasi atau variabel yang bernilai null. Karena sangat umum terjadi dan bisa berakibat fatal, NPE terkenal dengan istilah **“The Billion Dollar Mistake”**.

Dalam penanganannya, kita harus berhati-hati karena NPE menyebabkan aplikasi yang kita kembangkan, rusak saat dijalankan.

Pada Kotlin kita dimudahkan untuk mengelola variabel _**nullable**_ sehingga dapat meminimalisir terjadinya **NullPointerException**. Kotlin hadir dengan penanganan _nullability_ yang mudah. Kotlin mampu membedakan objek yang boleh bernilai null dan objek yang tidak boleh bernilai null pada saat objek tersebut dibuat.

## Tipe Data Nullable

Kotlin mendukung tipe data yang boleh bernilai null. Tipe data ini disebut dengan tipe data _nullable_. Tipe data _nullable_ ditandai dengan tanda tanya (?) setelah tipe data. Contoh:

```kotlin
var name: String? = null
```

Namun kita tidak bisa langsung mengakses atau mengelola nilai dari objek yang sudah kita tandai sebagai nullable. Sebagai contoh:

```kotlin
var name: String? = null
println(name.length) //Error: Kotlin: Null can not be a value of a non-null type String
```

Ketika kita menuliskan kode di atas, maka akan gagal dikompilasi dengan log eror berikut:

`Error:(4, 26) Kotlin: Only safe (?.) or non-null asserted (!!.) calls are allowed on a nullable receiver of type String?`

Lalu bagaimana cara kita mengakses atau mengelola nilai dari objek yang ditandai sebagai nullable? Cara mudahnya, periksa objek tersebut apakah bernilai **null** atau tidak:

```kotlin
var name: String? = null

if (name != null) {
    println(name.length)
} else {
    println("Name is null")
}
```

Ketika kita menuliskan kode di atas, maka akan berhasil dikompilasi dan akan menghasilkan output berikut:

```text
Name is null
```

## Safe Call Operator

Kotlin menyediakan operator yang disebut dengan **safe call operator** (?.) untuk mempermudah kita dalam mengakses atau mengelola nilai dari objek yang ditandai sebagai nullable. Operator ini akan mengembalikan nilai null jika objek yang ditandai sebagai nullable bernilai null. Contoh:

```kotlin
var name: String? = null
println(name?.length) //Output: null
```

## Safe Call Operator dengan Elvis Operator

Kotlin juga menyediakan operator yang disebut dengan **elvis operator** (?:) untuk mempermudah kita dalam mengakses atau mengelola nilai dari objek yang ditandai sebagai nullable. Operator ini akan mengembalikan nilai yang kita tentukan jika objek yang ditandai sebagai nullable bernilai null. Contoh:

```kotlin
var name: String? = null
println(name?.length ?: 0) //Output: 0
```

## Non-null Assertion Operator

Kotlin juga menyediakan operator yang disebut dengan **non-null assertion operator** (!!) untuk mempermudah kita dalam mengakses atau mengelola nilai dari objek yang ditandai sebagai nullable. Operator ini akan mengembalikan nilai yang kita tentukan jika objek yang ditandai sebagai nullable bernilai bukan null. Contoh:

```kotlin
var name: String? = null
println(name!!.length) //Output: Exception in thread "main" kotlin.KotlinNullPointerException
```

> Dengan menggunakan non-null assertion kompiler akan mengizinkan kita untuk mengakses atau mengelola nilai dari sebuah objek nullable. Namun penggunaan operator tersebut sangat tidak disarankan karena akan memaksa sebuah objek menjadi non-null. Sehingga ketika objek tersebut bernilai null, Anda tetap akan berjumpa dengan **NullPointerException**.

## Safe Cast Operator

Kotlin juga menyediakan operator yang disebut dengan **safe cast operator** (as?) untuk mempermudah kita dalam mengakses atau mengelola nilai dari objek yang ditandai sebagai nullable. Operator ini akan mengembalikan nilai null jika objek yang ditandai sebagai nullable bernilai null. Contoh:

```kotlin
var name: String? = null
println(name as? String) //Output: null
```

**[<< Sebelumnya](m5-arrays.md)**  | **[Selanjutnya >>](m7-control-flow.md)**
