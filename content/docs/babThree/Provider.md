---
weight: 17
title: "Provider"
description: "Memahami definisi dari Provider pada MCS"
icon: "Folder"
date: "2025-10-13T12:06:26+07:00"
lastmod: "2025-10-13T12:06:26+07:00"
toc: true
---

## Provider

Flutter menyediakan banyak package yang dapat digunakan untuk mengimplementasikan state management, antara lain **setstate, provider, bloc, getX,** dan **riverpod**. Provider merupakan salah satu package state management yang menawarkan efisiensi, kesederhanaan dan fleksibilitas dalam hal mengelola state yang melibatkan beberapa widget tanpa harus melewati widget secara manual.

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-2.png" alt="Gambar 3.2 - Alur Kerja Aplikasi Tanpa Provider" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.2</b> Alur Kerja Aplikasi Tanpa Provider</p>

<span></span>

Tanpa menggunakan provider proses flow atau alur state menjadi lebih panjang karena bussines logic tergabung dengan UI. Penggabungan tersebut akan membuat state harus diturunkan secara manual menggunakan constructor atau widget parameter dari widget induk ke widget anaknya (metode ini disebut prop drilling). Semakin kompleks dan dalam susunan hirarki widget pada suatu aplikasi maka semakin banyak level yang harus di lewati state tersebut meskipun diantaranya tidak membutuhkan state tersebut. Hal tersebut akan membuat kode menjadi lebih rumit dan sulit untuk di maintenance. Flow di dalamnya pun menjadi tidak efisien.

<div class="d-flex justify-content-center w-60">
<img src="/images/babThree/Ba3-3.png" alt="Gambar 3.3 - Alur Kerja Aplikasi dengan Provider" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 3.3</b> Alur Kerja Aplikasi dengan Provider</p>

Sedangkan jika menggunakan provider, maka bussines logic akan dibuat terpisah dari UI. State akan dikelola secara terpusat sehingga dapat diakses oleh widget manapun tanpa harus melewati widget induk terlebih dahulu. Provider memungkinkan widget untuk mendengar (listen) state yang ada tanpa harus meneruskan data melalui constructor atau parameter.