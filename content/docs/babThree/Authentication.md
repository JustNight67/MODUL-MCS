---
weight: 16
title: "Authentication"
description: "Memahami definisi dari Authentication pada MCS"
icon: "Fact_Check"
date: "2025-10-13T12:06:26+07:00"
lastmod: "2025-10-13T12:06:26+07:00"
toc: true
---

Pembelajaran yang akan dilakukan pada bab ini merupakan pembelajaran yang berkaitan dengan keamanan sebuah aplikasi. Praktikum kali ini akan memanfaatkan platform pihak ke-3, yakni firebase untuk mengimplementasikan sistem keamanan terhadap sebuah aplikasi. Selain itu, para praktikan juga akan diajarkan tentang bagaimana caranya mengatur struktur project menjadi lebih rapi dengan menggunakan salah satu state management yang disediakan oleh Flutter, yakni Provider. State management sendiri merupakan sebuah cara yang dapat digunakan untuk mengatur, mengelola, dan menangani sebuah state / tindakan secara efisien.

## Tujuan

{{< table "table-striped" >}}
| **TUJUAN** | **PENJELASAN** |
|---------|------|
| **Mengetahui dan memahami konsep authentication dalam keamanan sebuah aplikasi** | <p style="text-align: justify;>">Pada bab ini, praktikan diharapkan dapat mengetahui dan memahami konsep serta tujuan dari penggunaan authentication dalam sebuah aplikasi.</p> |
| **Mampu mengimplementasikan konsep authentication ke dalam aplikasi** | <p style="text-align: justify;>">Setelah mengetahui dan memahami konsep dan tujuan dari penggunaan authentication, praktikan diharapkan dapat menerapkan konsep tersebut ke dalam aplikasi yang telah dibangun pada pertemuan sebelumnya.</p> |
| **Mampu mengimplementasikan state management provider** | <p style="text-align: justify;>">Pada bab ini, praktikan akan dijelaskan terkait salah satu state management pada flutter, yakni provider. Praktikan akan dijelaskan mengenai provider, tujuan, hingga cara menggunakannya.</p> |
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

## Authentication

*Authentication* merupakan sebuah proses untuk memvalidasi atau memverifikasi identitas dari seseorang sebelum nantinya pengguna tersebut dapat menggunakan layanan dari sebuah aplikasi atau sistem. Authentication merupakan hal yang sangat penting dalam pengembangan sebuah aplikasi atau sistem, karena dengan adanya sistem authentication keamanan dari sebuah aplikasi atau sistem menjadi meningkat. Sistem ini akan memastikan bahwa hanya pengguna yang berwewenang saja yang dapat masuk dan menggunakan layanan dari sebuah aplikasi atau sistem. Pada aplikasi atau sistem dengan skala besar, authentication merupakan suatu layanan yang wajib digunakan untuk menjaga keamanan data, mencegah terjadinya penyalahgunaan akun, dan juga digunakan untuk melindungi informasi pribadi pengguna.

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-1.png" alt="Gambar 3.1 - Alur Kerja Sistem Authentication" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.1</b> Alur Kerja Sistem Authentication</p>

Cara kerja dari sistem authentication dapat dilihat pada ilustrasi gambar di atas. Pengguna akan memasukkan id (email atau username) dan password yang telah dibuat sebelumnya ke dalam field yang telah disediakan oleh aplikasi atau sistem. Selanjutnya sistem akan melakukan validasi atau verifikasi terhadap data tersebut menggunakan metode yang telah tersedia. Jika data yang diinput oleh pengguna sudah sesuai, maka pengguna dapat masuk dan menikmati layanan yang disediakan oleh aplikasi atau sistem. Namun, jika terdapat salah satu data yang tidak sesuai, maka sistem akan menolak pengguna tersebut dan pengguna diarahkan kembali ke halaman login.

Saat ini, sistem authentication telah berkembang pesat dan memiliki berbagai metode yang digunakan, antara lain **single factor authentication (SFA), double factor authentication (2FA), multi factor authentication (MFA), authentication token-based, authentication biometric-based, authentication dengan OTP** dan lain-lain.
