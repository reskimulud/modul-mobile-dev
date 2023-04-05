# While Loop

Bayangkan ketika kita ditugaskan untuk mencetak beberapa baris teks yang sama ke dalam konsol seperti berikut:

```kotlin
println("Hello World")
println("Hello World")
println("Hello World")
println("Hello World")
println("Hello World")
```

Untuk mengatasinya kita bisa menggunakan perulangan. Perulangan adalah proses perulangan blok yang sama tanpa henti sampai kondisi yang diberikan tidak terpenuhi atau bernilai false.

## While

Perulangan while adalah perulangan yang akan terus berjalan selama kondisi yang diberikan bernilai true. Berikut contoh penggunaannya:

```kotlin
fun main() {
  var i = 1
  while (i <= 5) {
      println("Hello World")
      i++
  }
}

// Output:
// Hello World
// Hello World
// Hello World
// Hello World
// Hello World
```

Perhatikan kondisi dari While di atas, selama nilai dari variabel **i** kurang dari sama dengan **5** maka kode yang di dalamnya akan terus dilakukan. Lalu ketika kondisi tersebut sudah tak terpenuhi maka proses perulangan akan dihentikan.

While bersifat _**Entry Controlled Loop**_. Artinya, kondisi yang diberikan akan dievaluasi terlebih dahulu. Jika kondisi tersebut terpenuhi maka proses perulangan akan dijalankan.

Jika kondisi yang diberikan tidak terpenuhi sejak awal maka proses perulangan tidak akan dijalankan. Untuk mengujinya Anda bisa menulis dan menjalankan kode berikut:

```kotlin
fun main() {
  var i = 6
  while (i <= 5) {
      println("Hello World")
      i++
  }
}

// Output:
// (Tidak ada output)
```

## Do While

Perulangan do while adalah perulangan yang akan terus berjalan selama kondisi yang diberikan bernilai true. Perbedaannya dengan while adalah do while bersifat _**Exit Controlled Loop**_. Artinya, kondisi yang diberikan akan dievaluasi setelah proses perulangan selesai dijalankan. Berikut contoh penggunaannya:

```kotlin
fun main() {
  var i = 1
  do {
      println("Hello World")
      i++
  } while (i <= 5)
}

// Output:
// Hello World
// Hello World
// Hello World
// Hello World
// Hello World
```

Perhatikan kondisi dari do while di atas, selama nilai dari variabel **i** kurang dari sama dengan **5** maka kode yang di dalamnya akan terus dilakukan. Lalu ketika kondisi tersebut sudah tak terpenuhi maka proses perulangan akan dihentikan.

Jika kondisi yang diberikan tidak terpenuhi sejak awal maka proses perulangan akan dijalankan sekali saja. Untuk mengujinya Anda bisa menulis dan menjalankan kode berikut:

```kotlin
fun main() {
  var i = 6
  do {
      println("Hello World")
      i++
  } while (i <= 5)
}

// Output:
// Hello World
```

## Perbedaan While dan Do While

Perbedaan utama antara while dan do while adalah pada kondisi yang diberikan. Pada while kondisi yang diberikan akan dievaluasi terlebih dahulu sebelum proses perulangan dijalankan. Sedangkan pada do while kondisi yang diberikan akan dievaluasi setelah proses perulangan selesai dijalankan.

Perbedaan lainnya adalah pada kondisi yang diberikan. Pada while kondisi yang diberikan harus bernilai true agar proses perulangan dijalankan. Sedangkan pada do while kondisi yang diberikan tidak harus bernilai true agar proses perulangan dijalankan.

## Infinite Loop

Perulangan yang tidak memiliki kondisi yang diberikan atau kondisi yang diberikan selalu bernilai true akan terus berjalan tanpa henti sampai program dihentikan secara paksa. Berikut contoh penggunaannya:

```kotlin
fun main() {
  while (true) {
      println("Hello World")
  }
}
```

Kode di atas akan terus mencetak teks "Hello World" ke dalam konsol sampai program dihentikan secara paksa.

**[<< Sebelumnya](m8-when.md)**  | **[Selanjutnya >>](m10-for-loop.md)**
