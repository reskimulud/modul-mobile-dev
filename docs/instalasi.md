# Persiapan dan Instalasi

Di modul ini akan dijelaskan panduan bagaimana cara menginstall tools-tools yang sudah dijelaskan di modul sebelumnya, juga akan dijelaskan untuk pembuatan akun dari platform tersebut. Tidak perlu berlama-lama, mari kita ikuti langkahnya satu-persatu.

# Membuat akun GitHub

Untuk Anda yang baru pertama kali mendaftar akun GitHub, maka persiapkan terlebih dahulu alamat email yang aktif dan belum pernah digunakan untuk mendaftar GitHub sebelumnya. Alamat email bisa menggunakan google.mail, yahoo, ymail, hotmail, ataupun custom mail.

![setup-node1](images/akun-github1.jpeg)

Masuk ke halaman [github.com](https://github.com) untuk membuka halaman utama, kemudian pilihmenu Sign Up.

Masukkanlah data sesuai dengan yang diminta oleh form pendaftaran. Setiap data yang dimasukkan akan dilakukan pemeriksaan, sehingga semua kolom input harus bercentang hijau agar dapat melanjutkan pendaftaran.

![akun-github](images/akun-github2.png)

Pada Verify your account, Anda akan diminta untuk menyamakan antara teks perintah dengan gambar yang tampil. Setelah memasukkan username, email, dan password, lanjutkan dengan mengeklik Create account.

Setelah proses pendaftaran akun baru, Anda diminta untuk memasukkan kode unik yang bisa didapatkan dari email. Kode unik tersebut digunakan untuk memverifikasi akun email yang digunakan selama pendaftaran akun GitHub. Bukalah kotak masuk pada email pendaftaran untuk melihat kode tersebut, kemudian masukkanlah ke dalam form pendaftaran tersebut.

![akun-github](images/akun-github3.jpeg) &nbsp;
![akun-github](images/akun-github4.jpeg)

> Jika kode verifikasi tidak dimasukkan ke dalam form pendaftaran, akun GitHub Anda tidak akan diverifikasi.

Setelah menginput kode verifikasi, Anda akan dihadapkan dengan tampilan selamat datang. Pada halaman tersebut akan ada tiga menu utama yaitu **membuat repository baru**, **membuat organisasi**, dan **mempelajari cara menggunakan GitHub**. Mari kita abaikan terlebih dahulu langkah ini, silakan tekan **Skip this for now** untuk langsung menuju halaman *dashboard*.

![akun-github](images/akun-github5.jpeg)

Selanjutnya akan diarahkan ke Dashboard.

![akun-github](images/dashboard-github.png)

---

# Instalasi Git

Untuk menginstall Git, pertama kunjungi web [git-scm.com](https://git-scm.com). Secara otomatis akan terdeteksi sistem operasi yang kita gunakan dan versi terbaru Git. Langsung saja klik **Download for Windows**

![git](images/git.png)

Jalankan file instalasi nya dan ikuti setiap instruksinya

![git](images/setup-git1.jpg)
![git](images/setup-git2.jpg)
![git](images/setup-git3.jpg)
![git](images/setup-git4.jpg)

Selanjutnya pengaturan PATH Environment. Pilih yang tengah agar perintah `git` dapat di kenali di Command Prompt (CMD). Setelah itu klik Next.

![git](images/setup-git5.jpg)

Selanjutnya ikuti seperti langkah-langgkah dibawah

![git](images/setup-git6.jpg)
![git](images/setup-git7.jpg)
![git](images/setup-git8.jpg)
![git](images/setup-git9.jpg)

Proses instalasi sedang berjalan, tunggu beberapa saat!

![git](images/setup-git10.jpg)

Setelah selesai, langsung klik Finish

![git](images/setup-git11.jpg)

Selamat, kamu telah selesai menginstall Git di komputer anda. Untuk memastikan bahwa git sudah terinstall, jalankan perintah berikut

```bash
git --version
```

![git](images/termintal-git1.png)

Selanjutnya lakukan konfigurasi berikut sebelum menggunakan Git yaitu menambahkan email dan nama

```bash
git config --global user.name "Reski Mulud Muchamad"
git config --global user.email "reski.mulud@gmail.com"
```

> **Penting:** Pastikan email yang dimasukan sama dengan email yang terdaftar di GitHub

Selamat. Maka jika sudah melakukan langkah tersebut kita siap menggunakan Git.

---

Karena sebelumnya sudah belajar web di mata kuliah Pemrograman Web I dna II, maka saya asumsikan sudah menginstall MySQL menggunakan **XAMPP**. Jangan lupa buka XAMPP nya dan klik `start` untuk MySQL sampai berubah menjadi hijau.

![xampp](images/xampp.png)

Setelah itu buka [localhost/phpmyadmin](http://localhost/phpmyadmin) di browser, dan kita siap menggunakan MySQL.

![phpmyadmin](images/phpmyadmin.png)

---

# Instalasi Postman

Untuk memasang Postman pada komputer Anda, silakan kunjungi halaman unduh Postman di [postman.com/downloads](https://postman.com/downloads).

![postman](images/postman.png)

Klik tombol **Windows 64-bit** sesuai tipe bit Windows yang digunakan untuk mulai mengunduh aplikasi Postman. Tunggu hingga proses unduh selesai.

Setelah selesai, buka berkas instalasi Postman untuk memulai proses instalasi.

![postman](images/setup-postman.png)

Tunggu hingga proses instalasi selesai. Kemudian aplikasi Postman akan terbuka dengan sendirinya.

Sebelum menggunakannya, Anda ditawari untuk membuat akun Postman. Pendaftaran ini bersifat opsional, Anda bisa mendaftar ataupun melewatinya dengan klik Skip and go to the app.

![postman](images/setup-postman1.png)

Maka halaman dashboard postman akan terbuka

![postman](images/setup-postman2.png)

> Untuk penggunaan Postman secara lengkap akan dijelaskan bersamaan dengan penyampaian materi.

---

# Catatan

Jika sebelumnya telah menginstall beberapa tools di atas maka bisa lewati step tersebut. Dan jika menemukan kendala saat menginstall atau membuat akun langsung hubungi saya atau bisa juga **berikan komentar di Classrom**.

Selamat! Sekarang kita sudah siap untuk memulai membuat hal yang keren saat dikelas nanti, tetap SEMANGAT!!!

---

**[<< Sebelumnya](pre-requisite.md)**  | **[Selanjutnya >>](m1-fundamental-kotlin.md)**
