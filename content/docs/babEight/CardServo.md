---
weight: 32
title: "Card Reader & Servo Controller"
description: "Memahami konsep Card Reader & Servo Controller pada MCS"
icon: "Smart_Card_Reader"
date: "2025-09-13T16:48:46+07:00"
lastmod: "2025-09-13T16:48:46+07:00"
toc: true
---

Pada praktikum MCS bab 8, praktikan akan membangun sebuah aplikasi yang dapat mengontrol servo dan melihat data id kartu yang masuk ke database melalui sensor Radio Frequency Identification (RFID). Agar dapat mengontrol servo dan membaca id kartu yang masuk, kita akan mengonsumsi data API yang telah dibuat pada pertemuan praktikum bab 6 dan bab 7.

## Tujuan

{{< table "table-striped" >}}
| **TUJUAN** | **PENJELASAN** |
|---------|------|
| **Mengetahui cara mengontrol servo menggunakan kartu RFID** | <p style="text-align: justify;>">Pada bab ini, praktikan akan dijelaskan mengenai bagaimana cara untuk menggerakan servo menggunakan kartu RFID.</p> |
| **Memahami cara memasangkan id kartu dengan database** | <p style="text-align: justify;>">Bab ini akan menggunakan kartu RFID yang di daftarkan ke database untuk memantau perubahan kondisi servo.</p> |
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
| **Arduino IDE**|
| **Postman**|
{{< /table >}}

<span></span>

## Materi Praktikum

Pada pertemuan sebelumnya, kita telah membuat 2 database dengan beberapa route endpoint. Database dan endpoint yang dibuat pada bab 6 merupakan endpoint untuk menangani proses pembacaan data kartu yang masuk ke database melalui RFID. Sedangkan, database dan endpoint pada bab 7 digunakan untuk mengontrol servo.

<ul><li>Endpoint yang dibangun pada bab 6:</li><ul>

<span></span>

1.  **/cards** (Route untuk membaca kartu dengan metode GET)
2.  **/card/input/:id** (Route untuk menginput id kartu ke database melalui parameter :id dengan menggunakan metode POST)
3.  **/card/delete/:id** (Route untuk menghapus id kartu dari database melalui parameter :id dengan menggunakan metode DELETE)

<span></span>

<ul><li>Endpoint yang dibangun pada bab 7:</li><ul>

<span></span>

1.  **/servo/init-proj** (Route untuk menginisialisasi nilai id menjadi 1 dan nilai status servo menjadi 0 dengan menggunakan metode POST)
2.  **/servo/status** (Route untuk membaca status servo dengan menggunakan metode GET)
3.  **/servo/update/:srv_status** (Route untuk mengubah status servo dengan parameter :srv_status dengan menggunakan metode PUT)
