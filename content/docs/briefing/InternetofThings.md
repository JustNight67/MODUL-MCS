---
weight: 8
title: "Internet of Things"
description: "Memahami konsep Internet of Things dalam MCS"
icon: "Device_Hub"
date: "2026-05-15T11:44:25+07:00"
lastmod: "2026-05-15T11:44:25+07:00"
toc: true
---

## Internet of Things

Internet of Things (IoT) merupakan sebuah konsep yang memungkinkan terhubungnya perangkat dengan lainnya melalui internet untuk melakukan aktivitas tertentu. Cara kerja IoT pada dasarnya membutuhkan 3 komponen, yaitu sensor, gateway dan cloud sehingga melibatkan pencarian, pengolahan dan pengiriman Awalnya sensor mengambil dan mengumpulkan data yang kemudian akan ditransmisikan ke cloud menggunakan gateway. Gateway dari arah lain juga dapat menjadi trigger bagi output perangkat IoT itu sendiri, seperti menghidupkan atau mematikan. Contoh implementasi dari cara kerja IoT dapat dilihat pada Gambar B.1

<div class="d-flex justify-content-center w-60">
<img src="/images/briefing/Br-1.png" alt="Gambar B.1 - Ilustrasi Internet of Things" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar B.1</b> Ilustrasi Internet of Things</p>

Dari arah microcontroller dan sensor terdapat ESP32, sensor DHT11 dan juga lampu, Sensor DHT11 akan menangkap suhu dan dibuat kondisi tertentu apabila suhu di bawah 19°C maka lampu akan menyala otomatis. Keadaan ini yang akan dikirimkan ke cloud. Di dalam cloud berisi database terhadap perangkat IoT dan dari pihak user akan membaca informasi dari cloud. Cloud yang digunakan bisa berupa service firebase, thingspeak atau bahkan cloud yang dibangun sendiri (back end). Hal ini juga berlaku dari pihak user melakukan trigger terhadap IoT dengan memanipulasi database.
