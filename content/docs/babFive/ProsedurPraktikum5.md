---
weight: 24
title: "Prosedur Praktikum"
description: "Memahami Definisi dari Thingspeak pada MCS"
icon: "Assignment"
date: "2025-10-13T12:31:10+07:00"
lastmod: "2025-10-20T18:05:10+07:00"
toc: true
---

## Tampilan Aplikasi

Berikut merupakan tampilan dari aplikasi yang akan dibentuk pada praktikum bab 5.

<div style="display: flex; justify-content: center; gap: 20px;">
    <div style="flex: 1; text-align: center;">
        <img src="/images/babFive/Ba5-4.png" style="max-width: 60%; height: auto;">
    </div>
    <div style="flex: 1; text-align: center;">
        <img src="/images/babFive/Ba5-5.png" style="max-width: 60%; height: auto;">
    </div>
</div>

<p style="text-align: center;"><b>Gambar 5.4</b> Tampilan Halaman Aplikasi yang Akan diimplementasikan </p>

**Penjelasan terkait bagaimana cara aplikasi bekerja akan diterangkan oleh asisten yang mengajar.**

## Implementasi Aplikasi

Dalam mengimplementasikan tampilan dari desain aplikasi di atas, terdapat beberapa langkah yang harus dilewati terlebih dahulu agar proses praktikum dapat berjalan dengan lancar dan terselesaikan sesuai dengan apa yang dituju. Sebelum membuat project flutter yang baru, praktikan diharapkan untuk membuat akun Thingspeak terlebih dahulu pada halaman website **https://thingspeak.mathworks.com/**. Kemudian, daftarkan email masing-masing pada halaman website tersebut.



<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-6.png" alt="Gambar 5.5 - Tampilan Halaman Website Thingspeak" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.5</b> Tampilan Halaman Website Thingspeak</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-7.png" alt="Gambar 5.6 - Proses Pembuatan Akun" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.6</b> Proses Pembuatan Akun</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-8.png" alt="Gambar 5.7 - Proses Pengisian Data Diri" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.7</b> Proses Pengisian Data Diri</p>

Pada saat registrasi akun, Thingspeak menyediakan 4 field yang harus diisikan, antara lain **email address, location, first name** dan **last name**. Pada bagian location, carilah country **Indonesia**. Setelah semua field diisikan, tekanlah tombol continue untuk melanjutkan ke tahap berikutnya. Setelah menekan tombol tersebut, pengguna akan mendapatkan email dari Thingspeak untuk melakukan verifikasi akun. Tekanlah tombol yang ada pada bagian email dan nantinya halaman Thingspeak akan berubah, seperti yang terlihat pada Gambar 5.8.

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-9.png" alt="Gambar 5.8 - Hasil Verifikasi Akun" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.8</b> Hasil Verifikasi Akun</p>

Setelah mendapatkan verifikasi dari Thingspeak, pengguna dapat melakukan konfigurasi password terhadap akun yang telah didaftarkan. Isilah field password yang telah disediakan dengan ketentuan yang telah ditetapkan oleh Thingspeak dan tekanlah tombol continue untuk mengakhiri proses registrasi akun.

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-10.png" alt="Gambar 5.9 - Konfigurasi Password Thingspeak" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.9</b> Konfigurasi Password Thingspeak</p>

<span></span>

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-11.png" alt="Gambar 5.10 - Tampilan Ketika Proses Registrasi Akun Berhasil" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.10</b> Tampilan Ketika Proses Registrasi Akun Berhasil</p>

Setelah berhasil mendaftarkan akun Thingspeak, pengguna dapat menekan tombol OK dan nantinya Thingspeak akan menampilkan halaman utama kepada pengguna. Thingspeak menyediakan 4 channel dan 8 field di setiap channel bagi pengguna yang menggunakan Thingspeak dengan gratis. Setiap 1 field dapat menyimpan 1 data, seperti suhu raungan yang dibaca oleh sensor DHT dan masuk ke microcontroller.

Pada praktikum kali ini, kita hanya membutuhkan 1 channel saja yang di dalamnya terdapat 3 fields, antara lain **suhu ruangan, kelembaban ruangan** dan **kelembaban tanah**. Maka dari itu, setelah berada pada halaman utama, praktikan dapat menekan tombol **New Channel** untuk membentuk channel baru dan mengisikan kolom field sebanyak 3 field, seperti yang terlihat pada Gambar 5.12.

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-12.png" alt="Gambar 5.11 - Proses Pembuatan Channel Baru" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.11</b> Proses Pembuatan Channel Baru</p>

<span></span>

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-13.png" alt="Gambar 5.12 - Proses Pembuatan Field" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.12</b> Proses Pembuatan Field</p>

Setelah mengisikan field tersebut, scroll halaman tersebut hingga menemukan tombol **Save Channel** dan tekanlah tombol tersebut untuk menyimpan hasil konfigurasi. Tampilan dari halaman website Thingspeak akan berubah, seperti yang terlihat pada Gambar 5.13. Pada halaman tersebut, akseslah menu** API keys** untuk melihat API keys yang diberikan oleh Thingspeak.

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-14.png" alt="Gambar 5.13 - Proses Pengaksesan Menu API Keys" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.13</b> Proses Pengaksesan Menu API Keys</p>

<span></span>

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-15.png" alt="Gambar 5.14 - Tampilan Menu API Keys" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.14</b> Tampilan Menu API Keys</p>

Write api keys dan Read api keys adalah kunci yang berbentuk susunan angka dan huruf yang nantinya akan digabungkan ke url utama sebagai endpoint. Kedua API keys tersebut digenerate secara otomatis, sehingga API keys antar pengguna tidak mungkin sama. Write API keys digunakan untuk mengirimkan data ke field yang telah disediakan, sedangkan read API keys digunakan untuk mengambil seluruh data yang telah tersimpan pada field masing-masing. Terdapat sedikit modifikasi untuk url dari **Read a Channel Fields**. Modifikasi tersebut dilakukan dengan menambakan **/last** setelah bagian nomor fields. Sehingga url akan berubah, seperti berikut:

```
https://api.thingspeak.com/channels/<Channel id>**/fields/<nomor field>/last.json?**api_key=Read API Keys
```

<span></span>

Perubahan url tersebut bertujuan untuk membaca dan menampilkan data paling akhir yang masuk pada masing-masing fields. Jika menggunakan url tersebut, maka url akan menghasilkan data, seperti berikut:

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-16.png" alt="Gambar 5.15 - Tampilan API Response Untuk Read API Keys" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.15</b> Tampilan API Response Untuk Read API Keys</p>

Setelah mendapatakan hasil response dari **API**, langkah berikutnya adalah membuat project flutter terlebih dahulu pada software android studio.

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-17.png" alt="Gambar 5.16 - Tampilan Awal Software Android Studio" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.16</b> Tampilan Awal Software Android Studio</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-18.png" alt="Gambar 5.17 - Proses Pembuatan Project Baru" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.17</b> Proses Pembuatan Project Baru</p>

Setelah file project berhasil terbentuk, pastikan kembali bahwa tampilan yang diberikan oleh android studio sudah berada pada menu **project**. Jika sudah, masuklah ke dalam file **pubspec.yaml** dan tambahkan package berikut ke dalam bagian **depedencies**.

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-19.png" alt="Gambar 5.18 - Package yang digunakan" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.18</b> Package yang digunakan</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-20.png" alt="Gambar 5.19 - Struktur Tree Project" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.19</b> Struktur Tree Project</p>

Jika sudah membuat struktur project, seperti pada Gambar 5.19, kembalilah ke API response yang telah dihasilkan dan salinlah data tersebut kemudian bukalah halaman website **https://quicktype.io/** untuk mengenerate API response yang diberikan secara otomatis.

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-21.png" alt="Gambar 5.20 - Tampilan Halaman Website Quicktype" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.20</b> Tampilan Halaman Website Quicktype</p>

Masukkanlah API response yang telah disalin sebelumnya ke bagian *field* sebelah kiri dan ubahlah nama field tersebut menjadi **Field1Model**. Pastikan bahasa pemrograman yang digunakan adalah dart dan opsi *null safety* dihidupkan.

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-22.png" alt="Gambar 5.21 - Hasil Generate Model API Response" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.21</b> Hasil Generate Model API Response</p>

Setelah quicktype memberikan model untuk response API keys, salinlah model tersebut dengan menekan tombol **Copy Code** dan masukkan ke dalam file **field1_model.dart**. Lakukanlah hal yang sama terhadap field 2 dan 3. Jika ketiga model field telah dibuat, masuklah ke dalam file **api_service.dart** dan masukkan kode program berikut:

{{< alert context="info" text="Code **api_service.dart** akan dipaparkan oleh **PJ Shift**." />}}

<span></span>

Pada praktikum ini, kita menggunakan package **DIO** untuk melakukan komunikasi dengan API dan mendapatkan response dari API tersebut yang nantinya akan disimpan ke dalam function yang telah disedikan. Fungsi **getField1()** akan menangkap data response untuk field temperature yang dipanggil melalui url dari variabel field1Url. Fungsi **getField2()** akan menangkap data response untuk field humidity yang dipanggil melalui url dari variabel field2Url. Fungsi **getField3()** akan menangkap data response untuk field soil moisture yang dipanggil melalui url dari variabel field3Url. Masing-masing fungsi akan memanggil endpoint yang sama, yakni readKey dan data dalam bentuk JSON tersebut nantinya akan melewati proses konversi terlebih dahulu menggunakan *property* **fromJson** yang ada di masing-masing class model.

Berikutnya tambahkan folder baru bernama **assets** pada root project dan tambahkan beberapa gambar ke dalam folder tersebut.

{{< alert context="info" text="Silahkan download gambar BAB 5 melalui [link ini](https://drive.google.com/drive/u/3/folders/1nRZpn_jf6hIT3IbuCarAHwRwkPfl2pid)." />}}

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-23.png" alt="Gambar 5.22 - Gambar pada Folder Assets" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.22</b> Gambar pada Folder Assets</p>

Setelah menambahkan gambar, bukalah kembali file pubspec.yaml dan carilah baris **assets** yang terbungkus dengan tanda *comment* (//). Hilangkan tanda tersebut, sehingga terlihat, seperti pada Gambar 5.23.

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-24.png" alt="Gambar 5.23 - Tampilan Baris Assets pada Pubspec.yaml" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.23</b> Tampilan Baris Assets pada Pubspec.yaml</p>

Jika sudah menghilangkan comment tersebut, lakukanlah **pub get** untuk memperbarui hasil konfigurasi. Jika sudah, bukalah file **app_provider.dart** dan masukkan kode program berikut:

```dart
import 'package:flutter/material.dart';
import 'package:google_fonts/google_fonts.dart';
import 'package:mcs_bab_5/models/field1_model.dart';
import 'package:mcs_bab_5/screens/home_page.dart';
import 'package:mcs_bab_5/services/api_service.dart';
import '../models/field2_model.dart';
import '../models/field3_model.dart';

class AppProvider extends ChangeNotifier {
  TextStyle roboto14Italic = GoogleFonts.roboto(
    fontSize: 14,
    fontWeight: FontWeight.w400,
  );
  TextStyle roboto14 = GoogleFonts.roboto(
    fontSize: 14,
    fontWeight: FontWeight.w500,
  );
  TextStyle roboto14SemiBold = GoogleFonts.roboto(
    fontSize: 14,
    fontWeight: FontWeight.w600,
  );
  TextStyle roboto14Bold = GoogleFonts.roboto(
    fontSize: 14,
    fontWeight: FontWeight.w700,
  );
  TextStyle roboto16Italic = GoogleFonts.roboto(
    fontSize: 16,
    fontWeight: FontWeight.w400,
  );
  TextStyle roboto16 = GoogleFonts.roboto(
    fontSize: 16,
    fontWeight: FontWeight.w500,
  );
  TextStyle roboto16SemiBold = GoogleFonts.roboto(
    fontSize: 16,
    fontWeight: FontWeight.w600,
  );
  TextStyle roboto16Bold = GoogleFonts.roboto(
    fontSize: 16,
    fontWeight: FontWeight.w700,
  );

  TextStyle whiteRoboto14Bold = GoogleFonts.roboto(
    fontSize: 14,
    fontWeight: FontWeight.w700,
    color: Colors.white,
  );

  Color mainColor = const Color(0xff36725D);
  String loremIpsum =
      "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.";
  String thermoMeterImage = "assets/thermometer.png";
  String humiditySensorImage = "assets/humidity_sensor.png";
  String soilAnalysisImage = "assets/soil_analysis.png";
  Field1Model? field1model;
  Field2Model? field2model;
  Field3Model? field3model;

  goToNextPage({required BuildContext context, required navigationPage}) {
    Navigator.push(
      context,
      MaterialPageRoute(builder: (context) => navigationPage),
    );
    notifyListeners();
  }

  Future getTemperature() async {
    notifyListeners();
    return field1model = await ApiService().getField1();
  }

  Future getHumidity() async {
    notifyListeners();
    return field2model = await ApiService().getField2();
  }

  Future getSoilMoisture() async {
    notifyListeners();
    return field3model = await ApiService().getField3();
  }
}
```

Kode program tersebut berisikan kumpulan deklarasi variabel dan fungsi yang nantinya dapat digunakan secara berulang. Variabel dengan tipe String yang bernama **thermoMeterImage, humiditySensorImage,** dan **soilAnalysisImage** adalah variabel untuk menyimpan path dimana gambar disimpan. Variabel dengan nama **field1model, field2model,** dan **field3model** adalah variabel yang nantinya menampung nilai return saat function yang berada di class ApiService() bernama getField1(), getField2() dan getField3() dipanggil. Fungsi tersebut akan dijalankan ketika fungsi getTemperature(), getHumidty() dan getSoilMoisture() dipanggil.

Kemudian bukalah file **main.dart** dan tuliskan kode program berikut:

{{< alert context="info" text="Code **main.dart** akan dipaparkan oleh **PJ Shift**." />}}

<span></span>

Pada file main.dart terlihat bahwa terdapat pemanggilan terhadap function getTemperature(), getHumidity() dan getSoilMoisture() yang bertujuan agar fungsi tersebut langsung dijalankan bersamaan pada saat aplikasi dijalankan. Hal tersebut juga dapat membuat data yang ingin diambil langsung disajikan tanpa menunggu untuk beberapa saat.

Berikutnya bukalah file **splash_screen.dart** dan masukkan kode program berikut:

{{< alert context="info" text="Code **splash_screen.dart** akan dipaparkan oleh **PJ Shift**." />}}

<span></span>

Kode tersebut merupakan kode yang digunakan untuk membangun halaman *splash screen* aplikasi yang muncul paling awal pada saat aplikasi dijalankan. Pada kode tersebut, terdapat fungsi void bernama initState() yang memanggil 3 fungsi lain yang telah didefinisikan pada provider, seperti **getTemperature(), getHumidity(),** dan **getSoilMoisture()** yang dipajnggila lagi untuk memastikan bahwa data yang ingin diambil benar-benar telah siap. Meskipun saat inisialisasi provider ketigatiga function tersebut sudah dipanggil, hal tersebut tidak dapat menjadi jaminan bahwa function yang dipanggil dapat berjalan.

Berikutnya masuklah ke dalam file **custom_read_file.dart** dan masukkan kode program berikut:

{{< alert context="info" text="Code **custom_read_file.dart** akan dipaparkan oleh **PJ Shift**." />}}

<span></span>

Kode program pada file tersebut digunakan untuk memberikan tampilan yang nantinya dapat digunakan pada halaman utama untuk menampilkan data yang diambil dari Thingspeak. Dengan adanya class CustomReadField() kita dapat memanggil widget dengan layout yang sama, karena kita hanya perlu memanggil class CustomReafField() saja yang nantinya class ini akan meminta constructor yang perlu diisi saat class tersebut dipanggil. Terdapat 3 bagian di dalam constructor yang harus diisi, **result** adalah untuk menampilkan data dari field channel Thingspeak, borderColor adalah warna yang digunakan untuk border widget yang dibangun dan image untuk menampilkan gambar pada widget tersebut.

Berikutnya masuklah ke dalam file **home_page.dart** dan masukkan kode program berikut:

{{< alert context="info" text="Code **home_page.dart** akan dipaparkan oleh **PJ Shift**." />}}

<span></span>

Kode program yang digunakan pada halaman ini akan mengenerate sebuah tampilan yang akan menampilkan data yang diambil pada Thingspeak melalui JSON. Widget yang digunakan untuk menampilkan data tersebut adalah CustomReadField() dan penggunaannya hanya perlu memanggil classnya saja. Ketika class CustomReadField() dipanggil, class tersebut akan meminta 3 constructor yang harus diisi, yakni result yang diisi dengan nilai field, borderColor yang diisi dengan warna, dan image yang diisi dengan gambar yang telah disiapkan. Seluruh data tersebut diambil melalui pendefinisian yang telah dilakukan pada provider.
