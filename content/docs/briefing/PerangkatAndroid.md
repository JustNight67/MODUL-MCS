---
weight: 3
title: "Perangkat Android"
description: "Memahami jenis-jenis perangkat android"
icon: "Android"
date: "2026-05-15T11:44:30+07:00"
lastmod: "2026-05-15T11:44:30+07:00"
toc: true
---

Pada bab briefing, praktikan akan diperkenalkan mengenai hal-hal mendasar yang berkaitan dengan proses praktikum Mobile Computing System (MCS), seperti materi, bahasa pemrograman, framework, dan tools yang digunakan selama praktikum berlangsung. Selain itu, pada pertemuan ini, praktikan juga akan diajarkan bagaimana caranya menginstall berbagai keperluan yang dibutuhkan selama praktikum.

## Tujuan

{{< table "table-striped" >}}
| **TUJUAN** | **PENJELASAN** |
|---------|------|
| **Memahami sistem operasi android dan sejarah perkembangannya** | <p style="text-align: justify;>">Pada bab briefing, praktikan akan diberikan penjelasan singkat mengenai sistem operasi android, seperti apa itu android, asal mula android, dan perkembangan dari sistem operasi android.</p> |
| **Memahami dasar bahasa pemrograman dart dan framework flutter dalam mengembangkan aplikasi berbasis mobile** | <p style="text-align: justify;>">Pada bab briefing, praktikan akan diberikan penjelasan singkat mengenai bahasa pemrograman dart mulai dari apa itu dart, asal mula, kelebihan, kekurangan dan beberapa syntax yang ada pada dart. Selain itu, terdapat juga penjelasan mengenai framework Flutter.</p> |
| **Mengenalkan seluruh tools yang akan digunakan selama praktikum** | <p style="text-align: justify;>">Pada bab briefing, praktikan akan dikenalkan terhadap beberapa tools yang akan digunakan, seperti android studio dan visual studio code.</p> |
| **Memahami proses instalasi dart SDK, android studio, dan visual studio code** | <p style="text-align: justify;>">Pada bab briefing ini terdapat langkah demi langkah dalam melakukan instalasi terhadap dart SDK dan android studio, mulai dari proses download, setup pada hardware hingga konfigurasi pada software android studio dan visual studio code .</p> |
| **Memahami cara pembuatan Flutter project pada android studio** | <p style="text-align: justify;>">Pada bab briefing, praktikan akan diajarkan bagaimana caranya membuat project Flutter pada android studio.</p> |
| **Memahami beberapa widget dasar yang ada pada flutter** | <p style="text-align: justify;>">Pada bab briefing, praktikan akan diperkenalkan dengan beberapa widget dasar yang ada pada Flutter.</p> |
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

## Perangkat Android

<span class=""> </span>

Android merupakan salah satu jenis operating system mobile berbasis linux yang dikembangkan oleh Android Inc pada tahun 2003 di California, Amerika Serikat. Android Inc didirikan oleh 4 orang yang ahli dibidang IT, yakni Andy Rubin, Rich Minner, Nick Sears dan Chris White. Pada bulan Agustus 2005, perusahaan besar ternama, yakni Google melakukan proses akuisisi terhadap perusahaan Android Inc. Pada tanggal 23 September 2008, sistem operasi Android berhasil dirilis ke publik bersamaan dengan pembentukan sebuah konsorsium Open Handset Alliance (OHA) yang terdiri dari beberapa perusahaan hardware, software, dan telekomunikasi. Selain itu, beberapa perusahaan ternama seperti Google, HTC, Intel, Motorola, Qualcomm, T-Mobile, 21 dan Nvidia juga ikut tergabung ke dalam konsorsium tersebut. Sistem android bersifat open-source yang membuat seluruh vendor pengembang smartphone diberikan akses untuk melakukan custom terhadap android versi mereka sendiri.

Sejak perilisannya pada tahun 2008, sistem operasi Android telah mengalami perkembangan yang begitu pesan hingga sampai saat ini. Tercatat bahwa sudah ada sekitar 24 jenis sistem Android yang telah dikembangkan, antara lain:

<p style="text-align: center;"><b>Tabel B.1</b> Perkembangan Sistem operasi Android</p>

{{< table "table-striped" >}}
| <p style="text-align: center;"><b>NO</b></p> | <p style="text-align: Center;"><b>NAMA SISTEM</b></p> | <p style="text-align: center;"><b>TAHUN PERILISAN</b></p> |
|---------|------|-------------|----|
| <p style="text-align: center;"><b> 1 </b></p> | <p style="text-align: Center;"><b> Android 1.0 (Alpha) </b></p> | <p style="text-align: center;"><b> 23 September 2008 </b></p> |
| <p style="text-align: center;"><b> 2 </b></p> | <p style="text-align: Center;"><b> Andorid 1.1 (Beta) </b></p> | <p style="text-align: center;"><b> 9 Februari 2009 </b></p> |
| <p style="text-align: center;"><b> 3 </b></p> | <p style="text-align: Center;"><b> Android 1.5 (Cupcake) </b></p> | <p style="text-align: center;"><b> 27 April 2009 </b></p> |
| <p style="text-align: center;"><b> 4 </b></p> | <p style="text-align: Center;"><b> Android 1.6 (Donut) </b></p> | <p style="text-align: center;"><b> 15 September 2009 </b></p> |
| <p style="text-align: center;"><b> 5 </b></p> | <p style="text-align: Center;"><b> Android 2.0 (Eclair) </b></p> | <p style="text-align: center;"><b> 26 Oktober 2009 </b></p> |
| <p style="text-align: center;"><b> 6 </b></p> | <p style="text-align: Center;"><b> Android 2.2 (Froyo) </b></p> | <p style="text-align: center;"><b> 20 Mei 2010 </b></p> |
| <p style="text-align: center;"><b> 7 </b></p> | <p style="text-align: Center;"><b> Android 2.3 (Gingerbread) </b></p> | <p style="text-align: center;"><b> 6 Desember 2010 </b></p> |
| <p style="text-align: center;"><b> 8 </b></p> | <p style="text-align: Center;"><b> Android 3.0 (Honeycomb) </b></p> | <p style="text-align: center;"><b> 22 Februari 2011 </b></p> |
| <p style="text-align: center;"><b> 9 </b></p> | <p style="text-align: Center;"><b> Android 4.0 (Ice Cream Sandwich) </b></p> | <p style="text-align: center;"><b> 18 Oktober 2011 </b></p> |
| <p style="text-align: center;"><b> 10 </b></p> | <p style="text-align: Center;"><b> Android 4.1 (Jelly Bean) </b></p> | <p style="text-align: center;"><b> 9 Juli 2012 </b></p> |
| <p style="text-align: center;"><b> 11 </b></p> | <p style="text-align: Center;"><b> Android 4.4 (KitKat) </b></p> | <p style="text-align: center;"><b> 31 Oktober 2013 </b></p> |
| <p style="text-align: center;"><b> 12 </b></p> | <p style="text-align: Center;"><b> Android 5.0 </b></p> | <p style="text-align: center;"><b> Lollipop </b></p> |
| <p style="text-align: center;"><b> 13 </b></p> | <p style="text-align: Center;"><b> Android 6.0 (Marshmallow) </b></p> | <p style="text-align: center;"><b> 29 September 2015 </b></p> |
| <p style="text-align: center;"><b> 14 </b></p> | <p style="text-align: Center;"><b> Android 7.0 - 7.1 (Nougat) </b></p> | <p style="text-align: center;"><b> 22 Agustus 2016 </b></p> |
| <p style="text-align: center;"><b> 15 </b></p> | <p style="text-align: Center;"><b> Android 8.0 - 8.1 (Oreo) </b></p> | <p style="text-align: center;"><b> 21 Agustus 2017 </b></p> |
| <p style="text-align: center;"><b> 16 </b></p> | <p style="text-align: Center;"><b> Android 9 (Pie) </b></p> | <p style="text-align: center;"><b> 6 Agustus 2018 </b></p> |
| <p style="text-align: center;"><b> 17 </b></p> | <p style="text-align: Center;"><b> Android 10 (Android Q) </b></p> | <p style="text-align: center;"><b> 3 September 2019 </b></p> |
| <p style="text-align: center;"><b> 18 </b></p> | <p style="text-align: Center;"><b> Android 11 (Red Velvet Cake) </b></p> | <p style="text-align: center;"><b> 8 September 2020 </b></p> |
| <p style="text-align: center;"><b> 19 </b></p> | <p style="text-align: Center;"><b> Android 12 (Snow Cone) </b></p> | <p style="text-align: center;"><b> 4 Oktober 2021 </b></p> |
| <p style="text-align: center;"><b> 20 </b></p> | <p style="text-align: Center;"><b> Android 13 (Tiramisu) </b></p> | <p style="text-align: center;"><b> 15 Agustus 2022 </b></p> |
| <p style="text-align: center;"><b> 21 </b></p> | <p style="text-align: Center;"><b> Android 14 (Upside Down Cake) </b></p> | <p style="text-align: center;"><b> 4 Oktober 2023 </b></p> |
| <p style="text-align: center;"><b> 22 </b></p> | <p style="text-align: Center;"><b> Android 15 (Vanilla Ice Cream) </b></p> | <p style="text-align: center;"><b> 3 September 2024 </b></p> |
| <p style="text-align: center;"><b> 23 </b></p> | <p style="text-align: Center;"><b> Android 16 (Baklava) </b></p> | <p style="text-align: center;"><b> 10 Juni 2025 </b></p> |
| <p style="text-align: center;"><b> 24 </b></p> | <p style="text-align: Center;"><b> Android 17 (Cinnamon Bun) </b></p> | <p style="text-align: center;"><b> 13 Februari 2026 </b></p> |

{{< /table >}}
