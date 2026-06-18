---
weight: 21
title: "Prosedur Praktikum"
description: "Proses pembuatan API pada praktikum MCS"
icon: "Assignment"
date: "2025-10-13T12:24:40+07:00"
lastmod: "2025-10-13T12:24:40+07:00"
toc: true
---

## Tampilan Aplikasi

Berikut merupakan tampilan dari aplikasi yang akan dibentuk pada praktikum bab 4.

<div style="display: flex; justify-content: center; gap: 20px;">
    <div style="flex: 1; text-align: center;">
        <img src="/images/babFour/Ba4-2.png" style="max-width: 100%; height: auto;">
    </div>
    <div style="flex: 1; text-align: center;">
        <img src="/images/babFour/Ba4-3.png" style="max-width: 100%; height: auto;">
    </div>
</div>

<p style="text-align: center;"><b>Gambar 4.2</b> Tampilan Halaman Aplikasi yang Akan diimplementasikan </p>

**Penjelasan terkait bagaimana cara aplikasi bekerja akan diterangkan oleh asisten yang mengajar.**

## Implementasi Aplikasi

Dalam mengimplementasikan tampilan dari desain aplikasi di atas, terdapat beberapa langkah yang harus dilewati terlebih dahulu agar proses praktikum dapat berjalan dengan lancar dan terselesaikan sesuai dengan apa yang dituju. Sebelum membuat project flutter yang baru, praktikan diharapkan untuk mengakses halaman website **https://newsapi.org/** dan mendaftarkan akun gmail masing-masing untuk mendapatkan API key yang nantinya akan digunakan dalam proses praktikum.

Setelah akun berhasil didaftarkan dan telah mendapatkan API key dari NewsAPI, barulah praktikan dapat membuat project flutter baru pada software android studio.

<div class="d-flex justify-content-center w-60">
<img src="/images/babFour/Ba4-4.png" alt="Gambar 4.3 - Tampilan Awal Software Android Studio" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 4.3</b> Tampilan Awal Software Android Studio</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babFour/Ba4-5.png" alt="Gambar 4.4 - Proses Pembuatan Project Baru" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 4.4</b> Proses Pembuatan Project Baru</p>

Setelah file project berhasil terbentuk, pastikan kembali bahwa tampilan yang diberikan oleh android studio sudah berada pada menu **project**. Jika sudah, bukalah file **AndroidManifest.xml** dan tambahkan izin berikut pada file tersebut.

<div class="d-flex justify-content-center w-60">
<img src="/images/babFour/Ba4-6.png" alt="Gambar 4.5 - Konfigurasi Pengaksesan Internet" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 4.5</b> Konfigurasi Pengaksesan Internet</p>

File tersebut dapat diakses melalui path **android > app > src > main > AndroidManifest.xml**. Kemudian, masuklah ke dalam file **pubspec.yaml** dan tambahkan package berikut ke dalam bagian **depedencies**.

<div class="d-flex justify-content-center w-60">
<img src="/images/babFour/Ba4-7.png" alt="Gambar 4.6 - Package yang digunakan" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 4.6</b> Package yang digunakan</p>

Dalam praktikum kali ini, kita menggunakan 5 package tambahan, antara lain **http, provider, google_fonts, intl, dan flutter_staggered_grid_view**. Kemudian tambahkanlah beberapa file dan folder ke dalam folder **lib**, sehingga struktur tree project menjadi seperti pada gambar berikut:

<div class="d-flex justify-content-center w-60">
<img src="/images/babFour/Ba4-8.png" alt="Gambar 4.7 - Struktur Tree Project" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 4.7</b> Struktur Tree Project</p>

Masuklah ke dalam file **news_model.dart** dan masukkanlah kode program berikut:

{{< alert context="info" text="Code **news_model.dart** akan dipaparkan oleh **PJ Shift**." />}}

File tersebut berisikan beberapa baris program yang digunakan dalam membuat model yang dapat merepresentasikan data dalam bentuk dart objek. Hal ini diperlukan agar proses consume data API menjadi lebih mudah dan lebih terstruktur dalam pengembangan aplikasi. Terdapat 2 class yang dibangun berdasarkan data yang diberikan oleh News API, yakni **NewsSource{}** yang di dalamnya berisikan id dan name serta **NewsModel{}** yang berisikan lebih banyak attribute, seperti source, author, title, description, url, urlToImage, publishedAt, dan content. Model dari NewsSource{} digunakan untuk merepresentasikan data yang tersimpan pada array **source**. Pada class tersebut terdapat constructor yang bersifat **required** yang mengembalikan 2 nilai yang telah didefinisikan sebelumnya. Kemudian terdapat pemanggilan terhadap **factory NewsSource.fromJson()** yang akan melakukan mapping nilai terhadap struktur JSON dan disimpan ke dalam bentuk objek dart yang telah dibuat sebelumnya.

Model yang dibentuk pada NewsModel{} merupakan model yang merepresentasikan data API secara umum. NewsModel{} memiliki constructor yang lebih banyak dibandingkan dengan NewsSource{}, karena data yang tersimpan di dalam array induk pada NewsAPI jauh lebih banyak dibandingkan dengan NewsSource{} yang hanya menyimpan data untuk id dan name. Model ini juga mengembalikan nilai dari setiap key API ke dalam bentuk dart objek dengan cara mapping terhadap data JSON tersebut dengan menggunakan perintah **factoryNewsModel.fromJson()**.

Berikutnya masuklah ke dalam file **news_service.dart** dan masukkan kode program berikut di dalamnya:

{{< alert context="info" text="Code **news_service.dart** akan dipaparkan oleh **PJ Shift**." />}}

Class **NewsService{}** berisikan logika program yang diperlukan untuk mengambil data dari API. Dalam class tersebut, terdapat variabel **universalUrl** yang mengembalikan sebuah url yang di dalamnya menyediakan sekumpulan data berita yang sudah dapat langsung dikonsumsi. Selain itu, class tersebut juga memiliki metode **getAllDataNews()** yang berisikan kode program untuk menangani proses request data ke API. Dalam proses tersebut, sistem akan meminta request ke url yang telah ditetapkan dengan menggunakan metode **http.get()** dan disimpan dalam variabel response. Kemudian sistem akan mengecek statusCode yang dihasilkan pada saat proses request berlangsung. Jika statusCode menunjukkan angka 200, maka sistem akan mengambil bagian body dari data API tersebut dan disimpan ke dalam variabel responseBody. Kemudian bagian body yang diambil adalah bagian key **articles** yang disimpan dalam variabel articlesResponse dalam bentuk list. Kemudian body articles yang telah diambil dikonversi ke dalam bentuk dart objek dengan pemanggilan terhadap metode **NewsModel.fromJson()**.

Selanjutnya dibentuklah class provider bernama **AppProvider** yang mengextends ChangeNotifier. Berikut kode yang digunakan pada class AppProvider:

{{< alert context="info" text="Code **app_provider.dart** akan dipaparkan oleh **PJ Shift**." />}}

Dalam *class* provider tersebut, didefinisikan beberapa variabel dan juga method yang anntinya akan digunakan pada pembangunan aplikasi tersebut.

1.	Variabel **source, authorName, titleOfArticle, descOfArticle, urlOfArticle, imageOfArticle, publishDateTime,** dan **contentOfArticle** merupakan variabel yang akan menyimpan value dari masing-masing key yang telah diambil pada API.
2.	Variabel **index** merupakan variabel yang akan menampung index / urutan dari setiap data article yang ada.
3.	Variabel **titleFontStyle, subTitleFontStyle, subTitleFontWithStrokeStyle** dan **universalFontStyle** merupakan variabel bertipe TextStyle yang akan memberikan styling terhadap widget Text dengan menggunakan jenis font yang disediakan oleh package google_fonts.
4.	Method **goToDetailNews()** bersifat asynchronus yang berisikan 4 constructor bersifat required, yakni **context, newsModel, index** dan **navigationPage**. Method ini akan mengambil dan menyimpan seluruh data yang ada pada halaman sebelumnya ke dalam masing-masing objek dan akan menavigasikan aplikasi ke halaman berikutnya.

Berikutnya masuklah ke dalam file **main.dart** terlebih dahulu untuk memberikan konfigurasi dasar pada aplikasi yang akan dibuat.

{{< alert context="info" text="Code **main.dart** akan dipaparkan oleh **PJ Shift**." />}}

Struktur kode yang digunakan pada file tersebut sama seperti yang digunakan pada praktikum pertemuan ke-3 yang mengembalikkan widget MultiProvider terlebih dahulu sebelum nantinya mendefinisikan konfigurasi umum untuk aplikasi.

Setelah melakukan konfigurasi umum untuk aplikasi, selanjutnya kita akan melakukan penulisan kode untuk halaman home (halaman awal aplikasi). Halaman ini dibentuk dengan mengextends StatefulWidget dan mengembalikan widget **Consumer()**. Widget ini memiliki parameter appProvider yang berfungsi sebagai variabel yang akan menginstance class AppProvider yang telah dibuat dan mempermudah dalam penggunaan variabel atau method yang telah dibentuk pada class AppProvider.

{{< alert context="info" text="Code **Consumer()** akan dipaparkan oleh **PJ Shift**." />}}

Bagian content dari halaman home dibungkus dengan menggunakan widget **FutureBuilder()** yang merupakan salah satu widget yang dapat digunakan untuk menampilkan data yang tersimpan dalam API. Widget tersebut memiliki properti bertipe **required**, yakni **future:** yang bertujuan untuk memantau state dari proses pengambilan data API. Pada aplikasi yang dikembangkan kali ini, terdapat 3 state berbeda yang ditampilkan sesuai dengan kondisi yang sedang dilewati oleh aplikasi, yakni ketika proses pengambilan data berlangsung, handling error, dan state ketika data berhasil diambil.

<div class="d-flex justify-content-center w-60">
<img src="/images/babFour/Ba4-9.png" alt="Gambar 4.8 - List Berita" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 4.8</b> List Berita</p>

{{< alert context="info" text="Code **MasonryGridView.count()** akan dipaparkan oleh **PJ Shift**." />}}

Bagian list berita dibentuk dengan menggunakan widget **MasonryGridView.count** yang akan mengenerate content berdasarkan dengan ukuran dari masing-masing content yang diambil. Sehingga, ukuran dari satu content dengan content yang lainnya belum tentu sama. Isi konten dari berita akan ditampilkan dalam bentuk 3 kolom dengan jarak vertical antar berita sebesar 8 dan jarak horizontal antar berita sebesar 10. Isi konten yang ditampilkan pada aplikasi tersebut meliputi gambar dan judul berita. Selain itu, agar masing-masing berita tersebut dapat diakses informasi detailnya, widget Column() yang membungkus kedua konten tersebut dibungkus lagi dengan widget **InkWell()** yang di dalamnya terdapat properti onTap:, sehingga berita tersebut dapat ditekan dan menuju ke halaman yang berisikan detail berita (DetailNewsPage()).

Selanjutnya bukalah file **detail_page.dart** dan masukkanlah kode program berikut:

{{< alert context="info" text="Code **detail_page.dart** akan dipaparkan oleh **PJ Shift**." />}}

Halaman ini merupakan halaman lanjutan ketika pengguna menekan salah satu berita yang ada pada halaman home. Halaman ini dibentuk dengan menggunakan widget **ListView()** dan menampilkan beberapa informasi, seperti gambar, judul, nama penulis, tanggal publikasi, dan deskripsi dari berita tersebut.
