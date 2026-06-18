---
weight: 29
title: "Servo Controller"
description: "Memahami definisi dari Servo pada MCS"
icon: "Controller_Gen"
date: "2025-09-13T16:48:46+07:00"
lastmod: "2025-09-13T16:48:46+07:00"
toc: true
---

Pada praktikum MCS bab 7, praktikan akan membangun RESTFUL API yang digunakan untuk menggerakan servo. RESTFUL API akan melakukan pemantauan terhadap data yang tersimpan pada database. Jika terdapat perubahan data, maka microcontroller akan menghasilkan output untuk menggerakkan servo.

## Tujuan

{{< table "table-striped" >}}
| **TUJUAN** | **PENJELASAN** |
|---------|------|
| **Membangun database dengan bahasa pemrograman Golang** | <p style="text-align: justify;>">Dalam bab ini, praktikan akan diajarkan cara membuat sebuah database dengan menggunakan bahasa pemrograman Golang.</p> |
| **Memahami cara memantau database dari perubahan kondisi servo** | <p style="text-align: justify;>">Pada bab ini, database digunakan sebagai media untuk memantau perubahan kondisi servo.</p> |
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
| **Visual Studio Code**|
| **Postgre SQL**|
| **Postman**|
{{< /table >}}

<span></span>

## Materi Praktikum

Pada bab ini aplikasi backend yang akan dibangun menggunakan bahasa pemrograman Go dengan framework yang bernama Gin. Adapun dari sisi IoT menggunakan microcontroller ESP32 dan servo. Servo akan bergerak sesuai dengan id yang tersimpan dalam database. Pada bagian database, field id akan bernilai 1 dan tidak ada data id lain yang terbentuk, Sedangkan, untuk servo status akan berisi angka 0 atau 1 dimana angka tersebut akan digunakan pada pengkondisian untuk membuat servo dapat bergerak.
