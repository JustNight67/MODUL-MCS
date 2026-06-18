---
weight: 9
title: "Instalasi dan Setup Software Praktikum"
description: "Melakukan penginstallan dan Setup Software untuk praktikum MCS"
icon: "Apk_Install"
date: "2026-05-15T11:44:25+07:00"
lastmod: "2026-05-15T11:44:25+07:00"
toc: true
---

## Instalasi dan Setup Flutter SDK

Langkah pertama yang harus dilakukan agar framework Flutter dapat digunakan untuk mengembangkan sebuah software adalah melakukan instalasi terhadap Flutter SDK. Berikut merupakan langkah-langkah dalam proses instalasi Flutter SDK:

1.  Bukalah link berikut untuk mendownload Flutter SDK: https://docs.flutter.dev/install/archive
2.  Carilah section **"Install the Flutter SDK"** dengan cara melakukan *scroll* kebawah.
3.  Pilihlah menu **download and install** yang ada pada *section* tersebut.
4.  Pilihlah **flutter_windows_3.35.4-stable.zip** untuk menginstall flutter SDK yang direkomendasikan (**Note: Versi dapat berubah-ubah**).

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-2.png" alt="Gambar B.2 - Halaman Website untuk Mendownload Flutter SDK" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.2</b> Halaman Website untuk Mendownload Flutter SDK</p>

5.  Tunggulah sampai proses *download* Flutter SDK selesai.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-3.png" alt="Gambar B.3 - File Flutter SDK yang telah didownload" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.3</b> File Flutter SDK yang telah didownload</p> 

6.  Setelah file Flutter SDK telah selesai didownload, lakukanlah proses extract pada file tersebut dengan cara menekan tombol kanan pada mouse dan pilihlah opsi **extract all**.
7.  Centanglah opsi **"Show extracted files when complete"**
8.  Pilihlah destinasi penyimpanan untuk menyimpan hasil extract dari file tersebut dengan menekan menu **browse** yang disediakan (**Note: Destination Storage untuk menyimpan file hasil ekstraksi dapat disimpan dimana saja**).
9.  Tekanlah tombol **extract** untuk melanjutkan proses ekstraksi file dan tunggulah hingga proses ekstraksi file selesai dilakukan.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-4.png" alt="Gambar B.4 - Proses Extract File Flutter SDK" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.4</b> Proses Extract File Flutter SDK</p>

10. Carilah *folder* bernama **Flutter** pada direktori tersebut. Kemudian carilah folder bernama bin di dalam folder tersebut **([Direktori_asal]:\flutter\bin)**
11. Salinlah *path* tersebut dan bukalah *environment variables* dengan cara **masuk ke dalam search windows atau dengan menekan logo windows pada keyboard**. Setelah muncul kolom search, ketiklah “env” pada bagian search dan pilihlah menu **“Edit the system environment variabels”**.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-5.png" alt="Gambar B.5 - Menu Search Pada Windows" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.5</b> Menu Search Pada Windows</p>

12. Masuklah ke dalam menu **environment variables** kemudian pilihlah menu **path** pada bagian atas dan klik menu **"Edit..."**

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-6.png" alt="Gambar B.6 - Menu System Properties" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.6</b> Menu System Properties</p>

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-7.png" alt="Gambar B.7 - Menu Environment Variables" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.7</b> Menu Environment Variables</p>

13. Pilihlah menu **new** pada menu *edit environment variable* dan lakukanlah *paste* terhadap *path* yang telah disalin.
14. Setelah *path* flutter SDK berhasil terpasang, tekanlah tombol **OK** untuk menyimpan konfigurasi *path*.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-8.png" alt="Gambar B.8 - Menu Edit Environment Variables" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.8</b> Menu Edit Environment Variables</p>

15. Bukalah **command prompt** pada perangkat dan ketik perintah **flutter --version**. Proses instalasi flutter SDK dinyatakan selesai, jika output pada *command prompt* terlihat, seperti pada gambar berikut (**Note: Versi dapat berbeda-beda**).

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-9.png" alt="Gambar B.9 - Output pada command prompt" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.9</b> Output pada Command Prompt</p>

## Instalasi dan Setup Android Studio

Setelah proses instalasi Flutter SDK berhasil dilakukan, langkah berikutnya yang harus dilakukan adalah menginstall software android studio yang nantinya akan digunakan selama proses praktikum. Berikut merupakan langkah-langkah dalam menginstall software android studio:

1.  Bukalah link berikut untuk mendownload software android studio: https://developer.android.com/studio
2.  Tekanlah tombol **Download Android Studio Narwhal 3 Feature Drop** (**Note: Versi Android Studio dapat berubah-ubah**).

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-10.png" alt="Gambar B.10 - Halaman Website untuk Mendownload Android Studio" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.10</b> Halaman Website untuk Mendownload Android Studio</p>

3.  Setelah menekan tombol tersebut, maka website akan menampilkan menu **“Terms and Conditions.”** Lakukanlah scroll hingga mencapai batas bawah dari menu tersebut dan centanglah bagian **“Saya telah membaca dan menyetujui persyaratan dan ketentuan di atas.”** Kemudian tekan kembali tombol download yang telah disediakan.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-11.png" alt="Gambar B.11 - Tampilan Menu Terms and Conditions" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.11</b> Tampilan Menu Terms and Conditions</p>

4.  Tunggulah sampai proses download android studio selesai.
5.  Bukalah file android studio yang telah selesai didownload.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-12.png" alt="Gambar B.12 - File Android Studio yang telah didownload" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.12</b> File Android Studio yang telah didownload</p>

6.  Setelah masuk ke dalam menu setup untuk android studio, pilihlah tombol **next** untuk melanjutkan ke langkah berikutnya.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-13.png" alt="Gambar B.13 - Menu Setup Android Studio" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.13</b> Menu Setup Android Studio</p>

7.  Centanglah opsi **Android Virtual Device** agar android studio menyediakan opsi virtual device pada saat proses running project. Kemudian tekanlah tombol next untuk melanjutkan ketahap berikutnya.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-14.png" alt="Gambar B.14 - Menu Install Components Android Studio" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.14</b> Menu Install Components Android Studio</p>

8.  Pilihlah lokasi direktori untuk menyimpan software android studio pada perangkat dan tekanlah tombol next untuk melanjutkan ketahap berikutnya.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-15.png" alt="Gambar B.15 - Menu Configuration Location Android Studio" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.15</b> Menu Configuration Location Android Studio</p>

9.  Pada menu *choose start menu folder*, pastikan untuk memilih **android studio** kemudian tekanlah tombol **install** untuk melakukan proses instalasi terhadap android studio.

   <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-16.png" alt="Gambar B.16 - Menu untuk Membuat Shortcut Aplikasi Android Studio" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.16</b> Menu untuk Membuat Shortcut Aplikasi Android Studio</p> 

10. Tunggulah sampai proses instalasi android studio selesai.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-17.png" alt="Gambar B.17 - Proses Instalasi Android Studio" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.17</b> Proses Instalasi Android Studio</p>

11. Setelah proses instalasi android studio selesai, bukalah aplikasi android studio yang telah terinstall.
12. Jika belum pernah membuat *project* dengan menggunakan *software android studio*, maka tampilan awalnya akan terlihat, seperti pada Gambar B.18 Bukalah menu **"More Actions** yang telah disediakan oleh aplikasi dan pilihlah option **SDK Manager**.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-18.png" alt="Gambar B.18 - Tampilan Aplikasi Android Studio" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.18</b> Tampilan Aplikasi Android Studio</p>

13. Pada menu SDK Manager, centanglah *option* **Hide Obsolete Packages** yang terletak di bagian bawah.
14. Selanjutnya, masuklah ke dalam menu **SDK Tools** kemudian pilihlah **"Android SDK Command-line Tools (latest)"**.
15. Tekanlah tombol **apply** yang berada pada bagian bawah.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-19.png" alt="Gambar B.19 - Menu SDK Tools pada Android Studio" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.19</b> Menu SDK Tools pada Android Studio</p>

16. Aplikasi android studio akan menampilkan jendela baru yang berisikan pesan konfirmasi, seperti pada Gambar B.20. Pada bagian ini tekanlah tombol **OK** untuk menlanjutkan ketahap berikutnya.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-20.png" alt="Gambar B.20 - Jendela Pesan Konfirmasi" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.20</b> Jendela Pesan Konfirmasi</p>

17. Tunggulah sampai proses download Android SDK CLT selesai.
18. Setelah selesai, bukalah **command prompt** pada perangkat dan ketik perintah **flutter doctor**. Jika output dihasilkan pada saat menjalankan perintah tersebut terlihat, seperti pada Gambar B.21, maka ketiklah perintah **flutter doctor --android-licenses** ketika proses analisa telah selesai. Namun, jika output yang ditampilkan terlihat seperti pada Gambar B.22 maka proses setup android studio telah selesai.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-21.png" alt="Gambar B.21 - Output ketika Android Licenses Belum diambil" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.21</b> Output Ketika Android Licenses Belum diambil</p>

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-22.png" alt="Gambar B.22 - Output ketika Android Licenses Telah diambil" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.22</b> Output Ketika Android Licenses Telah diambil</p>

## Instalasi dan Setup Visual Studio Code

Setelah proses instalasi Flutter SDK dan software android studio berhasil dilakukan, langkah berikutnya yang harus dilakukan adalah menginstall software visual studio code yang nantinya akan digunakan pada proses praktikum. Berikut merupakan langkah-langkah dalam menginstall software android studio:

1.  Bukalah link berikut untuk mendownload software visual studio code: https://code.visualstudio.com/download
2.  Tekanlah menu download yang telah disediakan (**Note: Harap menekan salah satu menu download yang disesuaikan dengan sistem operasi perangkat**).

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-23.png" alt="Gambar B.23 - Halaman Website untuk Mendownload Visual Studio Code" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.23</b> Halaman Website untuk Mendownload Visual Studio Code</p>

3.  Tunggulah sampai proses download visual studio code selesai.
4.  Bukalah file visual studio code yang setelah selesai didownload

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-24.png" alt="Gambar B.24 - FIle Visual Studio Code yang telah didownload" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.24</b> File Visual Studio Code yang telah didownload</p>

5.  Tekanlah opsi **"I accept the agreement"** dan tombol **next** untuk melanjutkan proses ke tahap berikutnya.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-25.png" alt="Gambar B.25 - Menu Setup Visual Studio Code" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.25</b> Menu Setup Visual Studio Code</p>

6.	Pilihlah lokasi direktori untuk menyimpan software visual studio code pada perangkat dan tekanlah tombol next untuk melanjutkan ketahap berikutnya.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-26.png" alt="Gambar B.26 - Menu Configuration Location Visual Studio Code" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.26</b> Menu Configuration Location Visual Studio Code</p>

7.  Pada menu **"Select Start Menu Folder"** pastikan nama pada *field* adalah "Visual Studio Code" kemudian tekanlah tombol **next**.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-27.png" alt="Gambar B.27 - Menu untuk Membuat Shortcut Aplikasi Visual Studio Code" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.27</b> Menu untuk Membuat Shortcut Aplikasi Visual Studio Code</p>

8.  Centanglah seluruh opsi yang ada pada menu **"Select Additional Tasks"** dan tekanlah tombol **next**.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-28.png" alt="Gambar B.28 - Menu Select Additional Task" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.28</b> Menu Select Additional Task</p>

9.  Tunggulah sampai proses instalasi visual studio code selesai.

    <div class="d-flex justify-content-center w-60">
    <img src="/images/briefing/Br-29.png" alt="Gambar B.29 - Proses Instalasi Visual Studio Code" class="img-fluid mb-3 responsive-img">
    </div>

    <p style="text-align: center;"><b>Gambar B.29</b> Proses Instalasi Visual Studio Code</p>

Setelah proses instalasi selesai, centanglah opsi **"Launch Visual Studio Code"** dan tekanlah tombol **finish** untuk langsung membuka aplikasi visual studio code.
