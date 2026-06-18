---
weight: 11
title: "Materi Widget Dasar Flutter"
description: "Memahami Widget-Widget dasar yang digunakan pada praktikum MCS"
icon: "Apps"
date: "2025-08-24T18:41:23+07:00"
lastmod: "2025-08-24T18:41:23+07:00"
toc: true
---

Pembelajaran yang akan dilakukan pada bab ini adalah pembelajaran mendasar mengenai framework Flutter yang merupakan salah satu jenis framework yang digunakan untuk mengembangkan suatu aplikasi perangkat mobile. Selain pemberian materi, praktikan juga akan melakukan praktek secara langsung untuk mengimplementasikan materi yang telah disampaikan.

## Tujuan

{{< table "table-striped" >}}
| **TUJUAN** | **PENJELASAN** |
|---------|------|
| **Mengetahui dan memahami widget-widget dasar yang ada pada Flutter** | <p style="text-align: justify;>">Pada bab ini, praktikan diharapkan dapat mengetahui dan memahami widget-widget dasar dalam membangun aplikasi mobile dengan Flutter.</p> |
| **Mengetahui cara membuat project baru pada Flutter dan memahami struktur project Flutter** | <p style="text-align: justify;>">Praktikan diharapkan dapat mengetahui dan memahami cara membuat project Flutter untuk pertama kali dan mengetahui struktur folder yang ada pada Flutter.</p> |
{{< /table >}}

## Persyaratan

<span class=""> </span>

Disarankan praktikan menggunakan hardware dan software sesuai pada dokumentasi ini. Apabila terdapat versi hardware atau software yang cukup lama dari versi yang direkomendasikan maka sebaiknya bertanya kepada Asisten Mengajar Shift.

{{< table "table-striped" >}}
| **HARDWARE YANG DIBUTUHKAN PRAKTIKUM** | **JENIS** |
|--|--|
| **PC / Laptop CPU** | **≥ 4 Cores** |
| **PC / Laptop RAM** | **≥ 8 GB** |
| **PC / Laptop Storage** | **≥ 10GB** |
{{< /table >}}

{{< table "table-striped" >}}
| **SOFTWARE YANG DIBUTUHKAN PRAKTIKUM** |
|--|--|
| **Android Studio / Visual Studio Code**|
{{< /table >}}

{{< alert context="info" text="Diusahakan untuk memakai **Versi** dan **Aplikasi** yang sama agar tidak terjadinya kesalahan yang tidak diinginkan!." />}}

<span></span>

Pada praktikum MCS bab 1, praktikan akan diajarkan mengenai widget-widget dasar yang ada pada flutter yang digunakan untuk membentuk suatu halaman aplikasi. Selain itu, praktikan juga akan langsung mengimplementasikan widget-widget tersebut dalam membentuk sebuah aplikasi. Pada pemrograman flutter, terdapat beberapa widget dasar yang harus dipahami terlebih dahulu sebelum programmer memulai pengembangan sebuah aplikasi menggunaakan flutter.  Berikut beberapa widget dasar yang harus dikuasai:

## MaterialApp()

MaterialApp() merupakan widget paling dasar yang berfungsi sebagai fondasi yang berisikan konfigurasi umum dari aplikasi yang akan dibangun. Untuk menggunakan widget ini, pengguna harus melakukan import terhadap **'package:flutter/material.dart'**. Berikut merupakan struktur dari widget MaterialApp():

```dart 
MaterialApp(
    title: ...,
    debugShowCheckedModeBanner: ...,
    theme: ...,
    home: ....
    routes: {...}
    //dan lain lain
);
```

MaterialApp() berisikan beberapa properti yang digunakan, seperti:

1.  title:

    memberikan label pada aplikasi.

2.  debugShowCheckedModeBanner:

    menerima nilai boolean true or false untuk mengatur kehadiran dari *banner debug* yang berada pada pojok kanan atas.

3.  theme:

    konfigurasi tema aplikasi.

4.  home:

    mengatur navigasi halaman pada saat aplikasi dijalankan sekaligus menetapkan halaman pertama yang akan ditampilkan oleh aplikasi.

## Scaffold()

Scaffold() merupakan widget umum yang digunakan untuk membentuk halaman pada sebuah aplikasi. Widget ini memiliki berbagai macam properti, seperti **appBar:, body:, drawer:, floatingActionButton:, bottomNavigationBar:** dan lain-lain. Berikut merupakan struktur dari widget scaffold():

```dart
Scaffold(
    appBar: ...,
    body: ...,
    floatingActionButton: ...,
    drawer: ...,
    bottomNavigationBar: ...,
)
```

Untuk menggunakan berbagai jenis widget yang tersedia pada flutter, programmer perlu melakukan extends terhadap class yang dibentuk dengan menggunakan **StatelessWidget()** atau **StatefulWidget()**. Kedua widget tersebut memiliki perbedaan dan kegunaannya masing-masing. Berikut beberapa perbedaan antara **StatelessWidget()** dengan **StatefulWidget()**:

{{< table "table-striped" >}}

| <p style="text-align: center;"><b>StatelessWidget()</b></p> | <p style="text-align: Center;"><b>StatefulWidget()</b></p> |
|---------|------|-------------|
| <p style="text-align: Center;"><b> Hanya fokus pada tampilan </b></p> | <p style="text-align: Center;"><b> Dapat menangani perubahan tampilan, Misal terdapat angka 1 pada halaman kemudian ingin dilakukakn perubahan tertentu dengan aktivitas tertentu pada angka tersebut, dengan StatefulWdget hal tersebut bisa dilakukan. </b></p> | 
| <p style="text-align: Center;"><b> Tidak dapat menangani perubahan tampilan. Misal terdapat angka 1 pada halaman kemudian ingin dilakukakn perubahan tertentu dengan aktivitas tertentu pada angka tersebut, dengan StatelessWdget hal tersebut tidak bisa dilakukan. </b></p> | <p style="text-align: Center;"><b> Dibuat dengan extends dari StatefulWidget. </b></p> | 
| <p style="text-align: Center;"><b> Dibuat dengan extend dari StatelessWidget. </b></p> | <p style="text-align: Center;"><b> Menggunakan 2 class berbeda. yakni widget dan state </b></p> | 

{{< /table >}}

