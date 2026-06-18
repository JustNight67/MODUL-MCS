---
weight: 20
title: "Application Programming Interface"
description: "Memahami konsep dari API pada MCS"
icon: "Api"
date: "2025-10-13T12:24:40+07:00"
lastmod: "2025-10-13T12:24:40+07:00"
toc: true
---

*Application Programming Interface* (API) adalah cara agar sebuah perangkat lunak atau lebih dapat berkomunikasi dengan server yang berisikan data. Data pada server diambil dan digunakan oleh pengembang aplikasi untuk diolah, API menjadi perantara bagi para developer untuk mengambil data pada server. Jika dianalogikan pada kegiatan di restoran, maka seperti pelanggan yang melihat daftar menu makanan dan memesan makanan kepada restoran tersebut lalu restoran memberikannya, pelanggan tidak tahu bagaimana caranya sebuah makanan disiapkan, begitu juga developer tidak tahu bagaimana data tersebut disiapkan tapi yang penting adalah data didapat oleh developer.

## Tujuan

{{< table "table-striped" >}}
| **TUJUAN** | **PENJELASAN** |
|---------|------|
| **Mengetahui dan memahami konsep dasar dari application programming interface** | <p style="text-align: justify;>">Pada bab ini, praktikan akan diharapkan dapat mengetahui dan memahami konsep dasar application programming interface (API).</p> |
| **Mampu memanggil data pada API ke dalam aplikasi** | <p style="text-align: justify;>">Pada bab ini, praktikan akan diajarkan bagaimana caranya mengambil data melalui API dan menampilkannya pada aplikasi.</p> |
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

## Materi Praktikum

*Application Programming Interface* (API) merupakan sebuah mekanisme yang memungkinkan dua komponen perangkat lunak atau lebih untuk saling berkomunikasi dengan menggunakan protokol yang ada. Dalam pengembangan aplikasi, API berperan sebagai jembatan yang menghubungkan *front end* dan *back end* dalam proses pengembangan aplikasi. Front end akan mengirimkan permintaan data kepada back end melalui API, kemudian back end akan merespon permintaan tersebut dan mengirimkan data yang diminta oleh front end untuk ditampilkan ke layar aplikasi.

<div class="d-flex justify-content-center w-60">
<img src="/images/babFour/Ba4-1.png" alt="Gambar 4.1 - Ilustrasi Application Programming Interface" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 4.1</b> Ilustrasi Application Programming Interface</p>

Jika dianalogikan dalam sebuah sistem restoran, **API** diibaratkan sebagai waiter / pelayan, **front end** diibaratkan sebagai customer / pelanggan, dan **back end** diibaratkan sebagai chef. Pelanggan (front end) akan membaca menu yang telah disediakan oleh restoran tersebut, kemudian pelanggan akan memesan menu yang diinginkan. Setelah menerima menu yang diinginkan oleh pelanggan, waiters / pelayan (API) akan memberitahu menu yang diminta oleh pelanggan kepada chef (back end), dimana setelah menerima menu tersebut chef akan mulai memasak (server akan mencari data yang diminta). Setelah makanan jadi (data yang diminta telah didapatkan) chef akan mengirimkannya kembali kepada waiters / pelayan untuk dikirimkan kembali ke pelanggan
