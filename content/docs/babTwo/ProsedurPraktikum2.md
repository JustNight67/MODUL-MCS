---
weight: 14
title: "Prosedur Praktikum"
description: "prosedur menggunakan ListView.builder untuk praktikum MCS"
icon: "Assignment"
date: "2025-09-13T16:48:46+07:00"
lastmod: "2025-09-13T16:48:46+07:00"
toc: true
---

## Tampilan Aplikasi

Berikut merupakan tampilan dari aplikasi yang akan dibentuk pada praktikum bab 2.

<div style="display: flex; justify-content: center; gap: 20px;">
    <div style="flex: 1; text-align: center;">
        <img src="/images/babTwo/Ba2-1.png" style="max-width: 60%; height: auto;">
    </div>
    <div style="flex: 1; text-align: center;">
        <img src="/images/babTwo/Ba2-2.png" style="max-width: 60%; height: auto;">
    </div>
</div>

<p style="text-align: center;"><b>Gambar 2.1</b> Tampilan Halaman Aplikasi yang Akan diimplementasikan </p>

**Penjelasan terkait bagaimana cara aplikasi bekerja akan diterangkan oleh asisten yang mengajar.**

## Implementasi Aplikasi

Dalam mengimplementasikan tampilan dari desain aplikasi di atas, terdapat beberapa langkah yang harus dilewati terlebih dahulu agar proses praktikum dapat berjalan dengan lancar dan terselesaikan sesuai dengan apa yang dituju. Langkah-langlah dalam pembuatan project baru sama seperti yang telah dilakukan pada praktikum pertemuan sebelumnya.

<div class="d-flex justify-content-center w-60">
<img src="/images/babTwo/Ba2-3.png" alt="Gambar 2.2 - Tampilan Awal Software Android Studio" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 2.2</b> Tampilan Awal Software Android Studio</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babTwo/Ba2-4.png" alt="Gambar 2.3 - Proses Pembuatan Project Baru" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 2.3</b> Proses Pembuatan Project Baru </p>

Jika file project sudah berhasil terbentuk, pastikan kembali bahwa tampilan yang diberikan oleh android studio sudah berada pada menu project. Jika tampilan menu sudah berada pada bagian project, bukalah file **pubspec.yaml** dan scroll file tersebut hingga mendapatkan bagian **depedencies**. Pada file ini, kita akan menambahkan package baru yang diambil melalui halaman website **https://pub.dev/**, yakni package **google_fonts**. Package ini digunakan untuk memberikan styling terhadap widget text yang digunakan pada aplikasi. Dengan menggunakan package ini, kita dapat memperindah teks aplikasi dengan tema font yang disediakan oleh google.

<div class="d-flex justify-content-center w-60">
<img src="/images/babTwo/Ba2-5.png" alt="Gambar 2.4 - Package yang digunakan" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 2.4</b> Package yang digunakan </p>

Setelah memasukkan package google_fonts ke dalam project flutter, langkah selanjutnya adalah membuat beberapa file dan folder yang dibentuk di dalam folder **lib**, sehingga tree project pada folder lib akan terlihat, seperti pada gambar berikut:

<div class="d-flex justify-content-center w-60">
<img src="/images/babTwo/Ba2-6.png" alt="Gambar 2.5 - Struktur Tree Project" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 2.5</b> Struktur Tree Project </p>

Berikutnya masuklah ke dalam file **cat_model.dart** yang ada pada folder model dan ketikan kode program berikut:

```dart
class CatModel {
    String urlImage;
    String name;
    String desc;

    CatModel({
        required this.urlImage,
        required this.name,
        required this.desc});
}
```

<span></span>

Pada file tersebut, dibuatlah class baru bernama **CatModel()** yang di dalamnya terdapat beberapa constructor. Class ini digunakan sebagai kerangka dalam pembentukan sebuah data. Dalam class ini terdapat 3 variabel yang didefinisikan, yakni **urlImage, name,** dan **desc** dimana masing-masing variabel tersebut bersifat **required** pada saat pembuatan constructor. Hal tersebut menandakan bahwa ketika pengguna memanggil class tersebut, maka secara otomatis sistem meminta data untuk urlImage, name, dan desc dari data yang ingin ditambahkan. Kemudian bukalah file **cat_data.dart** yang tersimpan di dalam folder data dan masukkan kode program berikut:

```dart
List<CatModel> cats = [
  CatModel(
    urlImage:
        "https://raw.githubusercontent.com/Fahmisbas/acsl-mcs/master/Bab%203%20-%20RecyclerView%20%26%20OnItemClickListener/cats/persia.jpg",
    name: "Persia",
    desc:
        '''Persia merupakan jenis kucing dengan bulu panjang yang lebat dan wajah bulat yang menggemaskan. Mereka dikenal dengan sifat yang tenang, penyayang, dan cocok sebagai kucing peliharaan dalam ruangan.''',
  ),
  CatModel(
    urlImage:
        "https://raw.githubusercontent.com/Fahmisbas/acsl-mcs/master/Bab%203%20-%20RecyclerView%20%26%20OnItemClickListener/cats/ragdoll.png",
    name: "Ragdoll",
    desc:
        '''Ragdoll merupakan kucing besar dengan bulu panjang yang halus dan mata biru memikat. Mereka terkenal dengan kecenderungan mereka untuk rileks dan melonggar saat diangkat, mirip dengan boneka ragdoll, dan sangat penyayang.''',
  ),
  CatModel(
    urlImage:
        "https://raw.githubusercontent.com/Fahmisbas/acsl-mcs/master/Bab%203%20-%20RecyclerView%20%26%20OnItemClickListener/cats/siam.jpeg",
    name: "Siam",
    desc:
        '''Siam merupakan kucing dengan bulu pendek, mata biru tajam, dan tubuh yang ramping. Mereka dikenal sebagai kucing vokal yang suka berbicara dan memiliki kepribadian yang aktif serta ramah.''',
  ),
  CatModel(
    urlImage:
        "https://raw.githubusercontent.com/Fahmisbas/acsl-mcs/master/Bab%203%20-%20RecyclerView%20%26%20OnItemClickListener/cats/sphynx.jpg",
    name: "Sphynx",
    desc:
        '''Sphynx merupakan jenis kucing tanpa bulu yang memiliki kulit lembut seperti kulit jeruk. Mereka sering menjadi perhatian dengan penampilan yang unik dan ramah serta cerdas dalam perilaku mereka.''',
  ),
  CatModel(
    urlImage:
        "https://raw.githubusercontent.com/Fahmisbas/acsl-mcs/master/Bab%203%20-%20RecyclerView%20%26%20OnItemClickListener/cats/maine%20coon.jpg",
    name: "Maine Coon",
    desc:
        '''Maine Coon merupakan salah satu kucing terbesar dengan bulu panjang dan ekor berbulu tebal. Mereka memiliki sifat yang ramah, lembut, dan cenderung energik, serta memiliki fisik yang kuat.''',
  ),
  CatModel(
    urlImage:
        "https://raw.githubusercontent.com/Fahmisbas/acsl-mcs/master/Bab%203%20-%20RecyclerView%20%26%20OnItemClickListener/cats/munchkin.jpg",
    name: "Munchkin",
    desc:
        '''Munchkin merupakan jenis kucing dengan tubuh pendek dan kaki yang lebih pendek dari kucing biasa. Mereka memiliki penampilan unik yang lucu dan aktif dalam bermain.''',
  ),
  CatModel(
    urlImage:
        "https://raw.githubusercontent.com/Fahmisbas/acsl-mcs/master/Bab%203%20-%20RecyclerView%20%26%20OnItemClickListener/cats/bengal.png",
    name: "Bengal",
    desc:
        '''Bengal memiliki bulu yang berkilau dengan motif belang yang mirip macan tutul. Mereka aktif, cerdas, dan suka bermain, sering kali memiliki energi yang tinggi.''',
  ),
  CatModel(
    urlImage:
        "https://raw.githubusercontent.com/Fahmisbas/acsl-mcs/master/Bab%203%20-%20RecyclerView%20%26%20OnItemClickListener/cats/britain%20shorthair.jpg",
    name: "Britain Shorthair",
    desc:
        '''British Shorthair memiliki penampilan gemuk dengan wajah yang bulat dan mata besar. Mereka cenderung tenang, santai, dan mudah diurus, membuat mereka menjadi kucing peliharaan yang populer.''',
  ),
];
```

<span></span>

File ini berisikan kumpulan data dummy yang tersimpan dalam variabel **cats** yang bertipe list. Seluruh data dummy tersebut dibentuk dengan menggunakan kerangka yang sebelumnya telah dibuat pada file cat_model.dart. Untuk menggunakan model kerangka yang telah dibuat sebelumnya, diperlukan pemanggilan terhadap class CatModel() pada saat mendefinisikan tipe data list untuk variabel cats. Class CatModel() ini perlu dipanggil jika kita ingin menggunakan kerangka yang telah dibuat, karena di dalam class CatModel() memiliki constructor yang berisikan kerangka untuk pengisian data.

Kemudian bukalah file **main.dart** untuk mendefinisikan beberapa konfigurasi yang akan digunakan pada aplikasi tersebut dan ketikan kode program berikut:

{{< alert context="info" text="Code **main.dart** akan dipaparkan oleh **PJ Shift**." />}}

File ini hanya berisikan konfigurasi dasar yang diperlukan agar seluruh kode program dapat dijalankan dan memberikan tema terhadap aplikasi. File ini berisikan fungsi **main()** yang di dalamnya terdapat fungsi runApp() yang akan memanggil class **MyApp()** yang mengextends StatelessWidget. Class ini akan mengembalikan widget **MaterialApp()** yang di dalamnya terdapat beberapa konfigurasi sederhana untuk aplikasi. Konfigurasi ini merupakan konfigurasi yang digunakan pada pertemuan bab sebelumnya, hanya saja terdapat konfigurasi tambahan yang dilakukan pada properti **theme:** yang memanggil widget ThemeData() dengan nilai pada properti **colorScheme: const ColorScheme.dark()** yang akan memberikan tema gelap pada aplikasi.

Setelah melakukan konfigurasi dasar pada file main.dart, langkah selanjutnya adalah membangun tampilan dari halaman home dengan menggunakan kode program berikut:

{{< alert context="info" text="Code **home_page.dart** akan dipaparkan oleh **PJ Shift**." />}}

Class **HomePage** merupakan class pertama yang akan ditampilkan pada saat aplikasi dijalankan. Class ini akan mengextends StatefulWidget dan mengembalikan widget **Scaffold()** untuk membangun halamannya. Untuk membentuk halaman home yang berisikan daftar jenis-jenis kucing, penulisan kode dibagi menjadi ke dalam beberapa bagian, seperti **app bar** dan **body**.

<div class="d-flex justify-content-center w-60">
<img src="/images/babTwo/Ba2-7.png" alt="Gambar 2.6 - Tampilan AppBar Aplikasi" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 2.6</b> Tampilan AppBar Aplikasi </p>

App bar pada aplikasi dibentuk dengan menggunakan widget **AppBar()** yang dikonfigurasi pada properti appBar: yang disediakan oleh widget Scaffold(). Pada widget AppBar() terdapat beberapa properti yang digunakan, seperti **title:** yang digunakan untuk memberikan judul pada AppBar dari aplikasi dengan mengembalikan widget Text(). Kemudian terdapat properti **centerTitle: true** untuk memposisikan title app bar berada di bagian dan properti **backgroundColor:** yang digunakan untuk memberikan warna background pada app bar aplikasi.

Kemudian pada properti **body:** digunakan widget ListView() untuk membangun fondasi awal dari bagian badan aplikasi. Widget ini memungkinkan halaman aplikasi dapat discroll, sehingga seluruh content yang ingin ditampilkan dapat terlihat secara keseluruhan dengan cara menggeser layar perangkat yang digunakan.

<div class="d-flex justify-content-center w-60">
<img src="/images/babTwo/Ba2-8.png" alt="Gambar 2.7 - Tampilan Halaman Utama" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 2.7</b> Tampilan Halaman Utama </p>

{{< alert context="info" text="Code **Tampilan Halaman Utama** akan dipaparkan oleh **PJ Shift**." />}}

<span></span>

Widget ListView() memiliki properti children: yang dapat menampung banyak widget di dalamnya. Pada bagian awal, terdapat pemanggilan terhadap widget **Text()** yang dibungkus dengan menggunakan widget Center() agar teks yang dihasilkan berada pada bagian tengah layar aplikasi. Widget **Text()** tersebut akan menampilkan string bertuliskan “Jenis-jenis Kucing” dengan pemberian styling terhadap jenis font, ukuran, dan ketebalan dari huruf tersebut. Styling tersebut menggunakan package yang telah ditambahkan pada saat awal praktikum, yakni package google_fonts. *Package* tersebut dapat dikonfigurasi pada properti **style:** dengan melakukan pemanggilan terhadap **GoogleFonts**. dan diikuti dengan jenis font yang akan digunakan. Kemudian untuk mengatur ukuran dan ketebalan font, dapat dilakukan pada properti **fontSize:** dan **fontWeight:**.

Kemudian di bawah widget Text() diberikan jarak sebesar 24 pixel dengan memanggil widget **SizedBox()**. Berikutnya untuk memanggil daftar kucing yang jumlahnya dapat berubah-ubah sesuai dengan keinginan pengguna, widget **ListView.builder()** dapat menjadi opsi pilihannya. Widget ini memiliki fungsi yang sama seperti widget ListView(), tetapi dalam widget ini terdapat properti **itemCount:** yang berfungsi untuk menetapkan seberapa banyak data yang akan ditampilkan pada daftar tersebut.

{{< alert context="info" text="Code **ListView.builder()** akan dipaparkan oleh **PJ Shift**." />}}

<span></span>

Selain menggunakan properti itemCount: untuk menentukan jumlah content yang ingin ditampilkan, terdapat penggunaan properti **shrinkWrap:** yang akan menyesuaikan tinggi berdasarkan jumlah content yang ditampilkan dan properti **physics: NeverScrollableScrollPhysics()** yang akan membuat item yang berada di dalam ListView.builder() tidak dapat dilakukan scroll. Hal ini sangat diperlukan agar tidak terdapat double scrolling pada satu halaman aplikasi. Kemudian terdapat properti **itemBuilder:** yang digunakan untuk membangun widget lain di dalam ListView.builder().

Pada praktikum ini, banyaknya content yang akan ditampilkan ditentukan berdasarkan banyaknya jumlah data yang tersimpan dalam variabel cats pada file cat_data.dart. Total jumlah data yang tersimpan pada variabel tersebut diambil dengan menggunakan argumen **cats.length**. Kemudian pada properti itemBuilder: terdapat sebuah deklarasi **CatModel cat = cats[index]** untuk memudahkan pengaksesan data yang tersimpan pada variabel cats berdasarkan indexnya.

<span></span>

Widget ListView.builder() akan mengembalikan sebuah **Container()** yang di dalamnya terdapat pemanggilan terhadap widget **Row()**. Widget Row() tersebut akan membuat widget di dalamnya tersusun secara horizontal. Adapun content yang berada di dalam widget tersebut adalah gambar dan nama kucing. Gambar kucing tersebut dipanggil dengan pemanggilan terhadap variabel cat yang diikuti dengan pemanggilan terhadap model **urlImage** (cat.urlImage). Untuk memanggil gambar tersebut diperlukan penggunaan dari widget **Image.network()**. Gambar tersebut dibungkus dengan menggunakan widget **SizedBox()** dengan ukuran tinggi dan lebarnya diambil berdasarkan ukuran lebar layar perangkat dibagi dengan 4 dan di ujung dari setiap SizedBox() tersebut distyling dengan menggunakan BorderRadius.Circular() sebesar 18 agar bentuk gambar tidak terlalu kotak. Kemudian terdapat widget **Text()** yang akan mengembalikan nama dari setiap kucingnya dengan menggunakan perintah **cat.name**. Tulisan tersebut kemudian distyling dengan menggunakan package google_fonts untuk memperindah tampilan.

Untuk membuat daftar tersebut dapat disentuh dan menampilkan detail dari setiap data kucing, maka widget Row() yang membungkus gambar dan nama kucing harus dibungkus dengan menggunakan widget **GestureDetector()**. Widget ini memiliki properti **onTap:** yang dapat digunakan untuk memberikan suatu tindakan pada saat pengguna menekan salah satu daftar kucing tersebut. Tindakan yang diberikan oleh sistem pada saat pengguna menekan salah satu daftar kucing tersebut adalah melakukan direct ke halaman detail kucing dengan menggunakan perintah **Navigator.push()**. Data yang dibawa ke halaman detail merupakan data yang dikirimkan oleh class HomePage berdasarkan index yang diakses.

Setelah melakukan penulisan kode pada halaman utama, langkah selanjutnya adalah menuliskan kode untuk halaman detail. Penulisan kode tersebut dilakukan pada file **detail_page.dart**. Berikut merupakan kode yang digunakan pada file tersebut:

{{< alert context="info" text="Code **detail_page.dart** akan dipaparkan oleh **PJ Shift**." />}}

Halaman detail kucing dibentuk dari class **DetailPage** yang mengextends StatefulWidget. Class tersebut memiliki parameter catModel yang bertipe data CatModel. Class ini akan mengembalikan widget **Scaffold()** untuk membentuk halaman aplikasi dimana terdapat 2 bagian, yakni app bar dan body. Bagian app bar pada halaman detail ini akan menampilkan nama kucing yang dipilih pada halaman sebelunya. Nama kucing tersebut nantinya akan berada pada bagian tengah dan app bar tersebut distyling dengan menggunakan package google_fonts. Berikutnya pada properti **body:** digunakan widget ListView() yang di dalamnya akan mengembalikan widget **Image.network()** untuk mengembalikan gambar kucing dan widget **Text()** yang akan menampilkan deskripsi dari kucing yang telah dipilih pada halaman sebelumnya.
