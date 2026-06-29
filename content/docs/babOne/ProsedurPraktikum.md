---
weight: 12
title: "Prosedur Praktikum"
description: "Memahami Widget-Widget dasar yang digunakan pada praktikum MCS"
icon: "Assignment"
date: "2025-08-24T18:41:23+07:00"
lastmod: "2025-08-24T18:41:23+07:00"
toc: true
---

## Tampilan Aplikasi

Berikut merupakan tampilan dari aplikasi yang akan dibentuk pada praktikum BAB 1.

<div style="display: flex; justify-content: center; gap: 20px;">
    <div style="flex: 1; text-align: center;">
        <img src="/images/babOne/Ba1-1.png" style="max-width: 60%; height: auto;">
    </div>
    <div style="flex: 1; text-align: center;">
        <img src="/images/babOne/Ba1-2.png" style="max-width: 60%; height: auto;">
    </div>
</div>

<p style="text-align: center;"><b>Gambar 1.1</b> Tampilan Halaman Aplikasi yang Akan diimplementasikan</p>

**Penjelasan terkait bagaimana cara aplikasi bekerja akan diterangkan oleh asisten yang mengajar.**

## Implementasi Aplikasi

Dalam Mengimplementasikan tampilan dari desain aplikasi di atas, terdapat beberapa langkah yang harus dilewati terlebih dahulu agar proses praktikum dapat berjalan dengan lancar dan terselesaikan sesuai dengan apa yang dituju. Untuk membuat *project* flutter pada android studio, pilihlah menu **New Flutter Project** yang terdapat pada halaman utama android studio. Kemudian tentukanlah nama *project* dan tempat untuk menyimpan file *project* tersebut. **Pastikan nama file diketik dengan format lowercase dan jika nama file lebih dari 1 kata, maka pisahkan dengan format snake_case**.

<div class="d-flex justify-content-center w-60">
<img src="/images/babOne/Ba1-3.png" alt="Gambar 1.2 - Tampilan Awal Software Android Studio" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 1.2</b> Tampilan Awal Software Android Studio</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babOne/Ba1-4.png" alt="Gambar 1.3 - Proses Pembuatan Project Baru" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 1.3</b> Proses Pembuatan Project Baru</p>

Jika file *project* sudah berhasil berhasil terbentuk, pastikan tampilan awal android studio sudah berada pada menu **project** untuk mempermudah dalam pengerjaan suatu project. Setelah berada pada menu project, android studio akan menampilkan beberapa file konfigurasi yang digunakan dalam membangun project flutter, seperti android, ios, lib, linux, macos, dan file-file lainnya. Namun, untuk membentuk sebuah aplikasi dengan flutter folder yang difokuskan adalah folder **lib**.

<div class="d-flex justify-content-center w-60">
<img src="/images/babOne/Ba1-5.png" alt="Gambar 1.4 - Tampilan Default Android Studio" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 1.4</b> Tampilan Default Android Studio</p>

Bukalah folder lib yang telah disediakan oleh flutter, maka akan terlihat 1 file dengan exstension dart bernama **main.dart** yang merupakan file utama sekaligus file yang akan dijalankan paling pertama saat program dijalankan. Ubahlah kode program default yang ada pada file tersebut dengan kode program berikut:

```dart
void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
    title: 'MCS BAB 1',
      debugShowCheckedModeBanner: false,
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepPurple),
        useMaterial3: true,
      ),
      home: const HomePage(),
    );
  }
}

```

Pada saat membangun project menggunakan flutter, fungsi **main()** merupakan fungsi utama yang wajib dihadirkan dan merupakan fungsi yang paling pertama dijalankan. Dalam fungsi ini, program akan memanggil fungsi runApp() yang akan menghubungkan kode program dart dengan flutter. Fungsi ini akan memanggil class **MyApp()** yang mengextends StetlessWidget.

Setelah membangun fondasi awal dari aplikasi, langkah berikutnya yang dilakukan adalah membuat file baru bernama home_page.dart yang akan membentuk halaman home aplikasi dengan menggunakan beberapa baris kode program. Berikut merupakan kode program yang digunakan dalam membentuk halaman home aplikasi tersebut:

{{< alert context="info" text="Code **home_page.dart** akan dipaparkan oleh **PJ Shift**." />}}

<span></span>

Class HomePage merupakan class pertama yang akan dipanggil pada saat argumen home: pada widget MaterialApp() dijalankan. Class ini akan mengextends statefulwidget untuk membagnun halamannya. Untuk membentuk halaman home, penulisan kode dibagi ke dalam beberapa bagian.

```dart
int start = 0;
int result = 0;
TextEditingController input1Controller = TextEditingController();
TextEditingController input2Controller = TextEditingController();
TextEditingController messageController = TextEditingController();
final Uri flutterUrl = Uri.parse("https://flutter.dev");

```

Bagian pertama yang dilakukan adalah mendefinisikan beberapa variabel yang nantinya akan digunakan untuk membangun halaman home. Pada pendefinisian tersebut, terdapat 2 variabel bertipe integer, yakni variabel start dan result yang memiliki nilai default 0. Kemudian terdapat 3 variabel bertipe TextEditingController dimana masing-masing variabel tersebut akan menyimpan objek controller dari TextEditingController() yang dapat digunakan untuk meminta dan mengambil input data dari pengguna. Kemudian, terdapat variabel flutterUrl yang berisikan sebuah url dari website official flutter. Variabel ini akan melakukan konversi terlebih dahulu dari bentuk String menjadi ke dalam bentuk objek uri yang dipahami oleh dart dengan menggunakan perintah **Uri.parse()**.

Setelah mendefinisikan beberapa variabel yang akan digunakan untuk membangun halaman home, langkah selanjutnya yang dilakukan adalah membuat beberapa fungsi yang nantinya akan digunakan juga pada halaman home. Terdapat beberapa fungsi yang akan dibangun, seperti fungsi **increment(), decrement(), sumOf(), substractionFrom(), resetResult(),** dan **dispose()**.

{{< alert context="info" text="Code **Function** akan dipaparkan oleh **PJ Shift**." />}}

<span></span>

Fungsi **increment()** berisikan beberapa baris program yang akan menghandle button **arrow_forward_ios** dalam menambahkan nilai dari variabel start. Sedangkan fungsi **decrement()** akan berisikan beberapa baris program yang akan menghandle pengurangan nilai dari variabel start dan diberikan sedikit pengkondisian, dimana ketika variabel start bernilai 0, maka fungsi ini tidak akan mengurangi nilai pada variabel start dan berhenti pada nilai 0.

Fungsi **sumOf()** berisikan beberapa baris program yang akan menambahkan 2 nilai yang diinput oleh pengguna ke dalam 2 field berbeda. Sdangkan, fungsi **substractionFrom()** berisikan baris kode program yang akan mengurangi 2 nilai yang telah diinput oleh pengguna. Nilai yang dihasilkan dari fungsi sumOf() dan substractionFrom() akan disimpan dalam variabel result. Kemudian fungsi **resetResult()** berisikan beberapa baris program yang akan mengosongkan kembali nilai pada variabel input1Controller, input2Controller, dan mereset kembali nilai dari variabel start. Fungsi **dispose()** digunakan untuk mencegah terjadinya kebocoran memori yang dapat disebabkan oleh controller.

Setelah mendefinisikan beberapa variabel dan fungsi yang akan digunakan, langkah berikutnhya yang dilakukan adalah membangun tampilan dari halaman home. Untuk membangun halaman dari sebuah aplikasi menggunkaan flutter, diperlukan pengembalian terhadap widget **Scaffold()**. Berbeda dengan widget MaterialApp() yang hanya berisikan beberapa properti untuk konfigurasi aplikasi, widget Scaffold() digunakan untuk membangun tampilan aplikasi yang dipisahkan dalam properti **appBar:** dan **body:**

<div class="d-flex justify-content-center w-60">
<img src="/images/babOne/Ba1-6.png" alt="Gambar 1.5 - Tampilan AppBar Aplikasi" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 1.5</b> Tampilan AppBar Aplikasi</p>

```dart
return Scaffold(
  appBar: AppBar(
    backgroundColor: const Color(0xff102C57),
    title: const Text("MCS BAB 1", style: TextStyle(color: Colors.white)),
    centerTitle: true,
  ),
  // ...
);
```

Tampilan appbar yang dibentuk pada praktikum ini hanyalah tampilan appbar sederhana yang bertuliskan MCS BAB 1 yang berada di bagian tengah. Selain itu, appbar pada aplikasi ini diberikan styling warna dengan kode hexa 0xff102C57. Kode hexa dari warna yang lainnya dapat dicari pada website [colorhunt](https://colorhunt.co).

Selanjutnya properti body: digunkan untuk membangun bagian badan dari halaman aplikasi. Properti ini dibangun dengan menggunakan widget ListView() yang dapat memungkinkan pengguna untuk melakukan scroll terhadap aplikasi. Widget ini mengembalikan properti children: yang dapat menampung banyak widget di dalamnya.

<div class="d-flex justify-content-center w-60">
<img src="/images/babOne/Ba1-7.png" alt="Gambar 1.6 - Area untuk Menambahkan Angka" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 1.6</b> Area untuk Menambahkan Angka</p>

{{< alert context="info" text="Code **body** akan dipaparkan oleh **PJ Shift**." />}}

Widget **SizedBox()** digunakan untuk memberikan jarak antar widget. Sizedbox() memiliki properti **height:** yang akan memberikan jarak secara vertical dan properti **width:** yang akan memberikan jarak secara horizontal. Kemudian widget **Center()** digunakan untuk membuat seluruh widget yang ada di dalamnya berada pada bagian tengah layar aplikasi. Widget ini memiliki properti child: yang memanggil widget **Text()** untuk mengembalikan nilai yang tersimpan pada variabel start. Nilai awal yang ditampilkan pada bagian ini adalah 0 yang kemudian nanti akan berubah sesuai dengan button yang ditekan.

Widget **Row()** berfungsi untuk membuat seluruh widget yang ada di dalamnya disusun secara horizontal. Sama seperti widget ListView(), widget ini juga dapat menampung banyak widget di dalamnya. Dalam widget ini, terdapat 2 widget **ElevatedButton()** yang digunakan untuk mengontrol perubahan angka start yang tertera di atasnya. ElevatedButton() pertama diberikan styling berupa icon panah ke kiri dengan warna hexacode 0xffE4003A. Properti onPressed: pada button ini diberikan fungsi decrement() untuk menurunkan angka Sedangkan, ElevatedButton() digunakan untuk menaikkan angka dengan pemanggilan fungsi increment() pada properti onPressed: dengan styling icon panah ke kanan dan dengan menggunakan warna hexacode 0xff5CB338.

<div class="d-flex justify-content-center w-60">
<img src="/images/babOne/Ba1-8.png" alt="Gambar 1.7 - Area untuk Menjumlahkan Angka" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 1.7</b> Area untuk Menjumlahkan Angka</p>

{{< alert context="info" text="Code **Field** akan dipaparkan oleh **PJ Shift**." />}}

<span></span>

Kemudian di bawah 2 ElevatedButton tersebut, terdapat 2 widget **TextFormField()** yang berfungsi untuk menerima nilai input berupa angka yang akan dimasukkan oleh pengguna. Kedua widget tersebut hanya dapat menerima nilai input berupa angka yang berada dalam range 0 – 9 dengan radius setiap sudutnya sebesar 16. Pada masing-masing TextFormField() terdapat properti controller yang berfungsi sebagai penanda agar ketika pengguna menginput nilai pada satu controller, nilai input tersebut hanya masuk ke dalam controller yang diakses. Untuk membedakannya, properti controller pada TextFormField() pertama diambil dari variabel **input1Controller**. Sedangkan pada TexFormField() kedua diambil dari variabel **input2Controller**.

Berikutnya, di bawah widget TextFormField() kedua terdapat pemanggilan terhadap widget Row() yang di dalamnya menampung 2 widget ElevatedButton(). Widget ElevatedButton() pertama berfungsi untuk menjumlahkan 2 nilai yang diinput pada 2 TextFormField() sebelumnya. Widget ini akan memanggil fungsi sumOf() yang berfungsi untuk menjumlahkan 2 angka yang telah dimasukkan pada input1Controller dan input2Controller. Sedangkan pada ElevatedButton() kedua digunakan untuk mengurangi 2 angka yang telah dimasukkan pada input1Controller dan input2Controller dengan pemanggilan terhadap fungsi substractionFrom(). Fungsi sumOf() dan substractionFrom() memiliki 2 konstruktor, yakni argumen x dan y yang bertipe data integer sehingga input1Controller dan input2Controller harus dikonversikan terlebih dahulu ke dalam bentuk integer.

<span></span>

Hasil penjumlahan dan pengurangan tersebut akan ditampung di dalam variabel result dan akan ditampilkan kepada pengguna dalam bentuk text. Dibawah area tersebut, terdapat icon **restart** yang berbentuk melingkar yang dibungkus oleh **GestureDetector()**. Widget ini berguna untuk membuat setiap widget yang diturunkannya dapat memiliki sebuah aksi ketika pengguna berinteraksi. Icon tersebut berfungsi untuk mengosongkan kembali input1Controller, input2Controller dan result.

<div class="d-flex justify-content-center w-60">
<img src="/images/babOne/Ba1-9.png" alt="Gambar 1.8 - Area untuk Mengirim Pesan" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 1.8</b> Area untuk Mengirim Pesan</p>

{{< alert context="info" text="Code **GestureDetector** akan dipaparkan oleh **PJ Shift**." />}}

Berikutnya terdapat field besar yang juga akan menerima input dari pengguna berupa teks panjang yang nantinya dapat dikirimkan ke halaman selanjutnya, yakni halaman reveiver page. Namun, sebelum membangun area ini, diperlukan sebuah file bernama **receiver_page.dart** yang akan menerima dan menampilkan pesan yang dituliskan oleh pengguna pada field tersebut. Berikut merupakan kode yang digunakan pada file receiver_page.dart:

{{< alert context="info" text="Code **receiver_page.dart** akan dipaparkan oleh **PJ Shift**." />}}

Class ReceiverPage() memiliki sebuah parameter yang diambil dari variabel message. Hal tersebut digunakan untuk menampung nilai input yang dimasukkan di class sebelumnya. Hasil dari input pesan tersebut nantinya akan ditampilkan pada bagian tengah halaman aplikasi dengan penggunaan dari widget Center().

Setelah membuat file receiver_page.dart dan menuliskan kode di atas, kembalilah ke file home_page.dart dan lanjutkan penulisan kode pada bagian TextFormField() yang berada di bawah area button restart. Area tersebut di bungkus dalam widget Row() yang di dalamnya terdapat widget TextFormField() yang digunakan untuk menerima nilai input dari pengguna. TextFormField() tersebut memiliki styling terhadap setiap ujung dari bordernya dengan ukuran 16 dan terdapat penggunaan properti **hintText:** yang akan memberikan kalimat petunjuk terhadap field tersebut. Kemudian widget selanjutnya yang digunakan adalah widget icon yang dibungkus dengan widget GestureDetector(). Widget ini akan membuat icon send yang ada di sebelah TextFormField dapat disentuh dan akan membuat tampilan aplikasi mengarah pada halaman yang lain, yakni halaman ReceiverPage dengan membawa pesan yang telah di input oleh pengguna ke dalam field.
