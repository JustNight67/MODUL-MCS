---
weight: 23
title: "Thingspeak"
description: "Memahami Definisi dari Thingspeak pada MCS"
icon: "Database_Upload"
date: "2025-10-13T12:31:10+07:00"
lastmod: "2025-10-20T18:05:10+07:00"
toc: true
---

Pada praktikum MCS bab 5, praktikan akan belajar membuat sebuah aplikasi yang terhubung dengan software yang umum digunakan untuk project *Internet of Things* (IoT), yakni **Thingspeak**. Thingspeak merupakan sebuah software opern source yang dapat digunakan untuk mengumpulkan, mengupdate, hingga memantau suatu data melalui Application Programming Interface (API). Aplikasi yang dikembangkan nantinya akan mengambil data API dalam bentuk JSON. JSON memiliki beberapa format data yang dapat digunakan, seperti **array of object, array with nested object dan object with array**.

## Tujuan

{{< table "table-striped" >}}
| **TUJUAN** | **PENJELASAN** |
|---------|------|
| **Memperkenalkan Thingspeak** | <p style="text-align: justify;>">Pada bab ini, praktikan akan diberikan gambaran singkat mengenai Thingspeak.</p> |
| **Mampu menghubungkan aplikasi yang dibangun dengan Thingspeak** | <p style="text-align: justify;>">Pada bab ini, praktikan akan membangun sebuah aplikasi yang nantinya akan dihubungkan dengan Thingspeak.</p> |
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

Interaksi dengan JSON memiliki dua metode yaitu **encode** dan **decode**. **Encode** adalah proses mengubah object dari suatu bahasa pemrograman menjadi format JSON, contohnya adalah ketika mengirim data (biasanya ke database sebelum diproses dengan query). Sedangkan **decode** adalah kebalikannya, yaitu mengubah format JSON menjadi object yang dapat dimengerti oleh bahasa pemrograman tertentu, contohnya adalah ketika aplikasi membaca data dari API.

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-1.png" alt="Gambar 5.1 - Array of Objects" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.1</b> Array of Objects</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-2.png" alt="Gambar 5.2 - Array with Nested Object" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.2</b> Array with Nested Object</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babFive/Ba5-3.png" alt="Gambar 5.3 - Object with Array" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 5.3</b> Object with Array</p>
