---
weight: 26
title: "Card Bridge"
description: "Memahami penjelasan database menggunakan bahasa Golang"
icon: "Id_Card"
date: "2025-09-13T16:48:46+07:00"
lastmod: "2025-09-13T16:48:46+07:00"
toc: true
---

Pada praktikum MCS bab 6, praktikan akan belajar tentang bagaimana caranya membangun RESTFUL API sebuah aplikasi backend yang menjadi penghubung antara end user dengan Internet of Things (IoT). Server menjadi connector antara aplikasi android mobile dan IOT yang dibangun berbasis Uniform Resource Locator (URL). Pada praktikum kali ini, server akan berperan sebagai database untuk menyimpan nilai id yang dihasilkan dari RFID.

## Tujuan

{{< table "table-striped" >}}
| **TUJUAN** | **PENJELASAN** |
|---------|------|
| **Memberikan penjelasan tentang bagaimana pengguna terhubung ke server** | <p style="text-align: justify;>">Memberikan gambaran umum mengenai alur saat user melakukan koneksi ke dalam server.</p> |
| **Membangun database dengan bahasa pemrograman Golang** | <p style="text-align: justify;>">Dalam bab ini, praktikan akan diajarkan cara membuat sebuah database dengan menggunakan bahasa pemrograman Golang.</p> |
| **Melakukan migrasi database dengan Golang** | <p style="text-align: justify;>">Dalam bab ini, praktikan akan diajarkan bagaimana caranya melakukan migrasi ke Postgre SQL database menggunakan bahasa Golang.</p> |
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

Pada bab ini aplikasi backend yang akan dibangun menggunakan bahasa pemrograman Go dengan framework yang bernama Gin. Adapun dari sisi IoT menggunakan microcontroller ESP32 dan sensor Radio Frequency Identification (RFID). Setiap kartu yang dibaca oleh RFID akan masuk ke server kemudian data kartu yang ada di server akan dibaca oleh aplikasi Android. Untuk berkomunikasi dengan backend berbasis URL (RESTFUL API) diperlukan beberapa method, beberapa method yang digunakan adalah **GET, POST, PUT, DELETE**.

<div class="d-flex justify-content-center w-60">
<img src="/images/babSix/Ba6-1.png" alt="Gambar 6.1 - Hubungan User dan Server" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 6.1</b> Hubungan User dan Server</p>

User mengirim request dengan beberapa method yang digunakan untuk berkomunikasi dengan server kemudian server mengirim kembali data berupa response.

<div class="d-flex justify-content-center w-60">
<img src="/images/babSix/Ba6-2.png" alt="Gambar 6.2 - Request dan Response" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 6.2</b> Request dan Response</p>

**Di praktikum ini hanya akan membangun dari sisi server saja dan praktikum akan berlanjut di bab 7 dan 8**
