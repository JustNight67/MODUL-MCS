---
weight: 14
title: "Dinamis UI"
description: "Memahami konsep dan pembuatan tampilan aplikasi yang dinamis menggunakan ListView.builder"
icon: "Dynamic_Feed"
date: "2025-09-13T16:48:46+07:00"
lastmod: "2025-09-13T16:48:46+07:00"
toc: true
---

Pembelajaran yang akan dilakukan pada bab ini merupakan pembelajaran yang ditingkatkan lagi setelah praktikan mengetahui hal-hal mendasar terkait Flutter. Pada pembelajaran ini akan diajarkan terkait cara membuat tampilan aplikasi yang dinamis dengan menggunakan ListView.builder. UI pada aplikasi akan dibuat secara dinamis berdasarkan data yang tersedia. Gambarannya adalah jika ListView() pada bab 1 berisi widget-widget yang dibuat secara manual maka di bab ini akan mengisikan widget-widget di dalam ListView() dibentuk secara otomatis sesuai dengan data yang tersedia.

## Tujuan

{{< table "table-striped" >}}
| **TUJUAN** | **PENJELASAN** |
|---------|------|
| **Mengetahui dan memahami bagaimana caranya membuat aplikasi dapat digulir** | <p style="text-align: justify;>">Pada bab ini, praktikan akan diajarkan tentang widget baru pada Flutter yang dapat membuat halaman dapat digulir, yakni **ListView()** dan turunannya, yaitu **ListView.builder()**.</p> |
| **Membuat dan memanggil data dummy** | <p style="text-align: justify;>">Dalam bab ini, praktikan akan diajarkan bagaimana caranya membuat sebuah list yang berisikan data dummy dan cara memanggil data dummy tersebut ke tampilan aplikasi.</p> |
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

## DinamisUI

Pada praktikum MCS bab 2, praktikan akan diajarkan bagaimana caranya membuat sebuah aplikasi yang memiliki tampilan UI yang dinamis. Dinamis UI sendiri merupakan sebuah tampilan yang isi konten dari halaman tersebut dapat berubah-ubah secara otomatis, baik dari segi content, jumlah content yang ditampilkan, light mode atau dark mode, dan lain-lain. Pada praktikum kali ini, para praktikan akan membuat sebuah aplikasi daftar kucing, dimana jumlah data kucing yang ditampilkan bergantung pada data yang tersedia. Data tersebut dapat ditambahkan atau dikurangi sesuai dengan keinginan pengguna.

Pada flutter, untuk membuat aplikasi yang memiliki tampilan dinamis terdapat 1 widget yang dapat digunakan, yakni widget **ListView.builder()**. Widget ini sama seperti widget ListView() yang digunakan pada bab praktikum sebelumnya. Namun, pada widget ini terdapat 1 properti tambahan, yakni properti itemCount: yang akan merender content aplikasi berdasarkan banyaknya nilai yang diinput pada properti tersebut.
