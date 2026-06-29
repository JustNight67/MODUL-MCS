---
weight: 18
title: "Prosedur Praktikum"
description: "prosedur pembuatan Provider dan Authentication untuk praktikum MCS"
icon: "Assignment"
date: "2025-09-13T16:48:46+07:00"
lastmod: "2025-09-13T16:48:46+07:00"
toc: true
---

## Tampilan Aplikasi

Berikut merupakan tampilan dari aplikasi yang akan dibentuk pada praktikum bab 3.

<div style="display: flex; justify-content: center; gap: 20px;">
    <div style="flex: 1; text-align: center;">
        <img src="/images/babThree/Ba3-4.png" style="max-width: 60%; height: auto;">
    </div>
    <div style="flex: 1; text-align: center;">
        <img src="/images/babThree/Ba3-5.png" style="max-width: 60%; height: auto;">
    </div>
    <div style="flex: 1; text-align: center;">
        <img src="/images/babThree/Ba3-6.png" style="max-width: 60%; height: auto;">
    </div>
</div>

<p style="text-align: center;"><b>Gambar 3.4</b> Tampilan Halaman Aplikasi yang Akan diimplementasikan </p>

**Penjelasan terkait bagaimana cara aplikasi bekerja akan diterangkan oleh asisten yang mengajar.**

## Implementasi Aplikasi

Praktikum yang akan dilakukan pada pertemuan ketiga ini merupakan lanjutan dari praktikum yang telah dilakukan pada pertemuan kedua. Pada praktikum ini, aplikasi yang telah berisikan list kucing akan diberikan halaman tambahan, yakni halaman login dimana pada saat aplikasi dijalankan, pengguna tidak dapat langsung melihat halaman yang berisikan jenis-jenis kucing, melainkan pengguna akan diarahkan ke halaman login terlebih dahulu.

### Konfigurasi Firebase

Dalam mengimplementasikan halaman login pada aplikasi, kita menggunakan tools tambahan yang disediakan oleh Google, yakni **firebase**. Pertama-tama bukalah website **https://firebase.google.com/** dan masuklah ke dalam bagian go to console yang dapat diakses pada appbar.

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-7.png" alt="Gambar 3.5 - Tampilan Halaman Website Firebase" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.5</b> Tampilan Halaman Website Firebase</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-8.png" alt="Gambar 3.6 - Tampilan Halaman Menu Console Firebase" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.6</b> Tampilan Halaman Menu Console Firebase</p>

Setelah masuk ke dalam menu “go to console” tekanlah menu “create a new Firebase Projcet” untuk membuat project baru. Pada saat pembuatan project terdapat beberapa konfigurasi yang diminta, seperti nama project, AI assistance, dan google analytics.

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-9.png" alt="Gambar 3.7 - Proses Pembuatan Nama Project" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.7</b> Proses Pembuatan Nama Project</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-10.png" alt="Gambar 3.8 - Proses Konfigurasi AI Assistance" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.8</b> Proses Konfigurasi AI Assistance</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-11.png" alt="Gambar 3.9 - Proses Konfiguasi Google Analytic" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.9</b> Proses Konfiguasi Google Analytic</p>

<span></span>

Setelah melewati beberapa konfigurasi dasar dari firebase, tampilan dari halaman website akan berubah, seperti yang terlihat pada gambar. Jika tampilan dari website sudah seperti pada gambar tersebut, tekanlah navigation menu **build** yang ada pada bagian sebelah kiri halaman website untuk menampilkan seluruh fitur yang disediakan oleh firebase yang dapat kita digunakan. Pilihlah fitur **authentication** kemudian tekanlah menu **get started** untuk mulai menggunakan fitur tersebut.

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-12.png" alt="Gambar 3.10 - Proses Pemilihan Fitur Authentication" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.10</b> Proses Pemilihan Fitur Authentication</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-13.png" alt="Gambar 3.11 - Proses Penggunaan Pertama Fitur Authentication" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.11</b> Proses Penggunaan Pertama Fitur Authentication</p>

Setelah proses pembuatan project berhasil, pilihlah provider **email / password** yang terdapat pada bagian native providers sebagai media authentication pada praktikum ini. Kemudian centang menu **enable** dan klik **save** untuk menyimpan hasil konfigurasi.

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-14.png" alt="Gambar 3.12 - Proses Pemilihan Metode Authentication" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.12</b> Proses Pemilihan Metode Authentication</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-15.png" alt="Gambar 3.13 - Proses Konfigurasi Metode Authentication" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.13</b> Proses Konfigurasi Metode Authentication</p>

Berikutnya masuklah ke dalam menu **users** untuk menambahkan user baru untuk authentication. Pada menu tersebut klik bagian **add user** dan isikan **email** serta **password**. Kemudian tekanlah button **add user** untuk menambahkan user baru ke dalam firebase.

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-16.png" alt="Gambar 3.14 - Proses Pembuatan Akun" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.14</b> Proses Pembuatan Akun</p>

Setelah user baru berhasil dibuat, langkah selanjutnya yang dilakukan adalah melakukan konfigurasi firebase dengan project flutter. Konfigurasi firebase dengan flutter project dilakukan dengan menggunakan **Command Line Interface (CLI)** yang prosesnya melalui beberapa tahapan, antara lain:

1.	Pastikan laptop / PC sudah terinstall **node.js.** Jika laptop / PC belum terinstall node.js, maka harap mengunduhnya terlebih dahulu pada halaman website **https://nodejs.org/en.**
2.	Pastikan path **C:\Users<nama user pada perangkat>\AppData\Local\Pub\Cache\bin** telah diinput pada bagian path yang ada pada environtment variables.
3.	Bukalah **command prompt (CMD)** atau **windows powershell**.
4.	Ketikan perintah **npm install -g firebase-tools** pada terminal yang telah dibuka dan tunggulah hingga proses installasi selesai. Perintah tersebut digunakan untuk menginstall firebase CLI pada perangkat secara global dengan menggunakan npm.
    ```
    npm install -g firebase-tools
    ```
5.	Bukalah project flutter yang telah dikerjakan pada pertemuan praktikum sebelumnya (praktikum bab 2) dan masuklah ke dalam terminal project tersebut.
6.	Ketikan perintah **firebase login** untuk menghubungkan project dengan layanan firebase. Jika baru pertama kali menggunakan firebase dan belum pernah menghubungkan project flutter dengan firebase, maka nanti flutter akan mengarahkan ke sebuah halaman yang meminta akun untuk dihubungkan ke Firebase CLI.
    ```
    firebase login
    ```

7.	Setelah berhasil login ke dalam firebase, ketikan perintah **firebase projects:list** untuk melihat seluruh project yang ada pada akun tersebut.
    ```
    firebase projects:list
    ```
8.	Ketikan perintah **dart pub global activate flutterfire_cli** untuk menginstall flutterfire cli dan tunggu hingga proses installasi selesai.
    ```
    dart pub global activate flutterfire_cli 
    ```
9.	Setelah proses installasi selesai, ketikan perintah **flutterfire configure** untuk mengonfigurasikan project flutter ke firebase. Dalam proses ini, terdapat beberapa langkah yang harus diikuti agar proses konfigurasi dapat berjalan dengan baik. **Praktikan diharapkan untuk memperhatikan dengan seksama penjelasan yang diberikan oleh PJ yang mengajar**.
    ```
    flutterfire configure
    ```
10.	Setelah proses konfigurasi ke firebase telah selesai, pada folder lib project flutter akan muncul sebuah file bernama **firebase_options.dart** secara otomatis. File tersebut berisikan konfigurasi untuk menghubungkan firebase dengan project Flutter.

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-17.png" alt="Gambar 3.15 - File Hasil Konfigurasi Firebase" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.15</b> File Hasil Konfigurasi Firebase</p>

<span></span>

### Pembuatan Aplikasi

Setelah file firebase_options.dart muncul, tambahkan 4 depedencies baru, yakni **firebase_core, firebase_auth, provider** dan **lottie** ke dalam file pubspec.yaml pada bagian depedencies. Selain itu, hilangkan komentar pada bagian **assets:** dan ubahlah path yang ada pada bagian **assets:** menjadi seperti pada Gambar 3.16.

{{< alert context="info" text="Code Untuk **JSON** silahkan di copy melalui [link ini](https://drive.google.com/drive/u/3/folders/12s7k5sbgOx_zd6swqNLMVndkOyZXtNUI)." />}}

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-18.png" alt="Gambar 3.16 - Package yang digunakan" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.16</b> Package yang digunakan</p>

Berikutnya tambahkan beberapa file dan folder ke dalam folder lib, sehingga struktur tree project pada folder lib akan terlihat, seperti pada gambar berikut:

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-19.png" alt="Gambar 3.17 - Struktur Tree Project" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.17</b> Struktur Tree Project</p>

Setelah menambahkan beberapa folder dan file ke dalam folder lib, masuklah ke dalam file **app_provider.dart** yang terdapat dalam folder **provider** dan masukkanlah kode berikut ke dalamnya.

{{< alert context="info" text="Code **app_provider.dart** akan dipaparkan oleh **PJ Shift**." />}}

<span></span>

Dalam file tersebut, terdapat class **AppProvider** yang mengextends **ChangeNotifier** yang berfungsi sebagai notifikasi bagi widget lain ketika adanya suatu perubahan terhadap data atau state, sehingga tampilan aplikasi dapat diperbarui secara otomatis. Class ini memiliki beberapa pendefinisian terhadap variabel dan method yang akan digunakan dalam membuat aplikasi authentication.

1.  **formKey** merupakan variabel unik yang digunakan untuk mengontrol seluruh field input yang dibungkus oleh widget Form().
2.  **usernameController** merupakan variabel yang menyimpan inisialisasi terhadap TextEditingController() yang berfungsi untuk mengontrol dan mengambil data yang diinput oleh pengguna pada field username.
3.  **passController** merupakan variabel yang menyimpan inisialisasi terhadap TextEditingController() yang berfungsi untuk mengontrol dan mengambil data yang diinput oleh pengguna pada field password.
4.  **firebaseAuthentication** berfungsi sebagai variabel yang menyimpan inisialisasi firebase authentication ke dalam project. Inisialisasi ini digunakan agar pada saat pembangunan aplikasi, kita dapat menggunakan beberapa method yang berkaitan dengan authentication, seperti **signInWithEmailAndPassword(), signInAnonymously(), signOut()** dan metode authentication lainnya.
5.  **visibilityIcon** yang diberi nilai default **true**. Variabel ini nantinya akan digunakan untuk logic pada icon mata yang ada pada field password.
6.  **hintUsernameText** merupakan variabel yang berisikan inisialisasi text yang akan digunakan sebagai petunjuk untuk field username.
7.  **hintPassText** merupakan variabel yang berisikan inisialisasi text yang digunakan sebagai petunjuk untuk field password.
8.  **loginButtonText** merupakan variabel yang berisikan inisialisasi text yang digunakan pada tombol login aplikasi.
9.  **backgroundColor** merupakan variabel yang berisikan pendefinisian terhadap warna background aplikasi.
10. **iconColor** merupakan variabel yang berisikan pendefinisian terhadap warna icon aplikasi.

<span></span>

Kemudian pada *class* tersebut juga terdapat pendefinisian terhadap beberapa method yang akan digunakan, antara lain:
1.  Method **loginToApp()** () merupakan method yang bersifat asynchronous. Method ini digunakan untuk menangani proses verifikasi login firebase dengan pemanggilan method **signInWithEmailAndPassword()**. Data yang digunakan untuk login diambil dari input pengguna dan diambil dengan menggunakan parameter.
2.  Method **logoutAccout()** merupakan method yang bersifat asynchronous yang akan menangani proses logout dari firebase.
3.  Method **validationForm()** merupakan method yang digunakan untuk memenangani proses validasi data berdasarkan data yang telah diinput oleh pengguna. Method ini akan memeriksa seluruh field yang ada dan mengirimkan data yang diterima dari masing-masing field ke method loginToApp() untuk diproses oleh firebase.
4.  Method **resetForm()** merupakan method yang berisikan beberapa baris kode yang digunakan untuk menghapus dan mengosongkan nilai dari field input dan digunakan juga untuk mereset status validasi dari widget.

Berikutnya bukalah file **login_page.dart** dan masukkanlah kode program berikut:

{{< alert context="info" text="Code **login_page.dart** akan dipaparkan oleh **PJ Shift**." />}}

<span></span>

Halaman login_page.dart berisikan baris kode program yang akan membangun tampilan dari halaman login aplikasi dan merupakan tampilan pertama yang akan ditampilkan oleh aplikasi. Halaman ini akan mengextends StatefulWidget dan mengembalikan widget **Consumer()** yang merupakan widget yang tersedia jika kita menggunakan Provider. Widget ini dapat membantu kita dalam mengakses instance dari provider yang di dalamnya terdapat beberapa variabel atau method yang telah didefinisikan. Widget ini juga akan melakukan rebuild UI yang ada di dalamnya ketika Consumer mendapati perubahan pada salah satu state, sehingga pengguna dapat langsung melihat perubahan data tersebut pada tampilan aplikasi.

Widget ini memiliki properti builder: yang didalamnya terdapat 3 parameter, antara lain **context, provider, dan child**. Parameter provider merupakan parameter yang merupakan instance dari class provider yang telah dibuat sebelumnya. Pada praktikum ini, parameter tersebut diberi nama sebagai **appProvider**, sehingga ketika ingin mengakses salah satu variabel atau method yang telah didefinisikan pada class AppProvider() kita hanya cukup memanggil appProvider yang diikuti dengan pemanggilan nama variabel atau method yang ingin digunakan.

Widget ini mengembalikan widget Scaffold() untuk membentuk halamannya dimana widget langsung menggunakan properti body: yang mengembalikan widget Form(). Widget tesebut digunakan untuk membantu kita dalam proses validasi nilai input yang didapatkan dari pemanggilan terhadap widget TextFormField(). Implementasi dari provider pertama kali dapat dilihat pada properti **key:** dengan pemanggilan terhadap **appProvider** yang diikuti dengan pemanggilan terhadap variabel **formKey** yang telah terdefinisikan di dalam class AppProvider(). Penggunaan dari provider lainnya dapat dilihat pada properti **controller:** yang ada di setiap widget TextFormField, properti **suffixIcon** yang ada pada widget TextFormField password, dan **button untuk login**.

Berikutnya masuklah ke dalam file **home_page.dart** dan ubahlah kode di dalamnya menggunakan kode program berikut:

{{< alert context="info" text="Code **home_page.dart** akan dipaparkan oleh **PJ Shift**." />}}

<span></span>

Perubahan kode tersebut dilakukan pada 2 bagian, pertama pada bagian pengembalian widget yang awalnya langsung mengembalikan widget Scaffold() dirubah menjadi widget Consumer(), sehingga widget Scaffold() berada di dalam widget Consumer(). Kemudian perubahan kedua terjadi pada bagian widget AppBar() dimana terdapat penambahan properti **action:** yang berisikan icon berbentuk logout. Icon tersebut nantinya dapat ditekan dan pada saat icon ditekan, maka sistem akan memanggil method **logoutApp()** dan **resetForm()** yang tersimpan di dalam class AppProvider. Kedua method tersebut akan membuat pengguna keluar dari akun tersebut dan kembali ke halaman login serta mengosongkan field input yang ada pada halaman login.

Selanjutnya masuklah ke dalam file **auth_page_gate.dart** dan masukkanlah kode program berikut:

{{< alert context="info" text="Code **auth_page_gate.dart** akan dipaparkan oleh **PJ Shift**." />}}

<span></span>

Class **AuthPageGate** merupakan class yang berisikan beberapa baris kode program yang akan mengatur halaman mana yang akan ditampilkan. Class ini mengembalikan widget Consumer() yang di dalamnya terdapat pemanggilan terhadap widget Scaffold(). Pada widget Scaffold() dipanggil properti body: yang mengembalikan widget **StreamBuilder()** yang di dalamnya terdapat properti **stream:** yang akan memantau data stream secara terus-menerus, sehingga tampilan UI dari halaman tersebut akan direbuild secara real time jika terdapat data yang berubah. Terdapat 2 kondisi berbeda yang akan ditampilkan oleh aplikasi, yakni kondisi pertama jika pada saat proses stream terdapat data (pengguna telah melakukan login), maka aplikasi akan langsung menampilkan halaman home yang berisikan list dari jenis-jenis kucing. Namun, jika pada saat stream sistem tidak menemukan data (pengguna belum pernah login atau sudah logout), maka tampilan yang akan ditampilkan adalah halaman login.

Berikutnya, masuklah ke dalam file **main.dart** dan ubahlah kode di dalamnya dengan menggunakan kode program berikut:

{{< alert context="info" text="Code **main.dart** akan dipaparkan oleh **PJ Shift**." />}}

Dalam file **main.dart** terdapat penambahan terhadap function main() dan class MyApp. Function main() diubah menjadi bentuk asynchronous yang di dalamnya terdapat kode program** WidgetsFlutterBinding.ensureInitialized();** yang akan memastikan bahwa seluruh widget yang akan digunakan telah selesai diinisialisasi dengan baik. Kemudian di bawahnya terdapat kode program await **Firebase.initializeApp(options: DefaultFirebaseOptions.currentPlatform)** yang akan membuat flutter menunggu terlebih dahulu sampai firebase berhasil terinisialisasi.

Kemudian class **MyApp** akan mengembalikan widget MultiProvider yang memungkinkan penggunaan beberapa provider. Provider yang akan digunakan pada praktikum ini didefinisikan pada properti **providers:** yang tersimpan dalam bentuk list. Dalam praktikum ini didefinisikan **ChangeNotifierProvider** yang mengembalikan class AppProvider() yang mengextends ChangeNotifier. ChangeNotifierProvider menyediakan instance dari class AppProvider yang akan digunakan pada aplikasi sebagai *state management*.
