---
weight: 4
title: "Bahasa Pemrograman"
description: "Memahami Bahasa pemrograman yang digunakan pada praktikum MCS"
icon: "Language"
date: "2026-05-15T11:44:29+07:00"
lastmod: "2026-05-15T11:44:29+07:00"
toc: true
---

## Dart

Dart merupakan bahasa pemrograman open source berorientasi objek yang dikembangkan oleh Lars Bark dan Kasper Lund di Google pada tahun 2011 yang kemudian diresmikan pada November 2013. Bahasa pemrograman ini awalnya dirancang khusus untuk pengembangan aplikasi website. Namun, seiring dengan berkembangnya zaman bahasa pemrograman ini telah dapat digunakan untuk mengembangkan berbagai aplikasi, seperti perangkat mobile, Internet of Things (IoT), game, server, desktop, dan lain-lain.

Bahasa pemrograman ini mengikuti gaya penulisan C-style yang membuat sintaks dari bahasa ini mirip dengan sintaks yang ada pada beberapa bahasa pemrograman yang berorientasi objek lainnya, seperti Java, C#, JavaScript, Kotlin, dan lain-lain (Swathiga, 2022). Terdapat beberapa fitur yang disediakan oleh bahasa pemrograman ini, yang membuat bahasa pemrograman ini menjadi populer dan banyak digunakan, antara lain:

1.  Open Source

    Bahasa pemrograman ini bersifat open-source yang membuat bahasa ini dapat digunakan oleh siapa pun secara gratis.

2.  Object Oriented

    Bahasa pemrograman ini mendukung seluruh konsep dasar dari pemrograman objek, seperti class, inheritence, abstract, encaptulation, dan polymorprhism.

3.  Simple Syntax

    Bahasa pemrograman dart memiliki syntax yang sederhana dan mudah untuk dipelajari.

4.  Cross Platform

    Bahasa pemrograman ini dapat dijalankan diberbagai sistem operasi berbeda, seperti windows, Linux, Unix, MacOS, dan sistem operasi lainnya.

5.  Multiplatform

    Bahasa pemrograman ini mendukung pengembangan aplikasi multiplatform, sehingga programmer dapat membangun aplikasi untuk Android dan iOS secara bersamaan dengan menggunakan kode yang sama.

6.  Garbage Collection

    Dart menyediakan sebuah sistem yang dapat mengelola memori secara otomatis dan dapat digunakan untuk mencegah terjadinya kebocoran memori.

7.  Asynchronous

    Bahasa dart menyediakan konsep asynchronus dengan fitur async dan await yang dapat meningkatkan kinerja programmer. Hal ini memungkinkan dart untuk menjalankan berbagai tugas secara bersamaan.

8.  Extensive Libraries

    Dart menyediakan berbagai library bawaan yang dapat digunakan, seperti Software Development Kit (SDK), core, math, asynchronous, convert, html, input-output (IO), dan masih banyak lagi library yang dapat digunakan.

<span></span>

### Tipe Data

Sama seperti bahasa pemrograman pada umumnya, dart memiliki beberapa tipe data yang digunakan untuk menentukan jenis dari nilai yang tersimpan dalam sebuah variabel. Berikut merupakan beberapa tipe data yang dapat digunakan dalam bahasa pemrograman dart:

1.  **String**

    String merupakan tipe data yang paling umum digunakan disetiap bahasa pemrograman. Tipe data ini akan membaca value yang diterima sebagai sebuah kalimat. Tipe data ini ditandai dengan penggunaan keyword **string** atau value yang diapit dengan petik 2 (“…”).

2.  **Integer**

    Tipe data integer merupakan salah satu tipe data numerik yang akan merepresentasikan nilai bilangan bulat, seperti 1, 3, 10, -30, dan sebagainya. Tipe data ini ditandai dengan penggunaan keyword **int**.

3.  **Double**

    Double merupakan jenis lain dari tipe data numerik yang akan menerima nilai bilangan desmial atau float, seperti 3.14, 5.7, 11.8, dan sebagainya. Tipe ini ditandai dengan penggunaan keyword **double**.

4.  **Number**

    Tipe data number merupakan gabungan dari tipe data integer dan double. Tipe data ini dapat merepresentasikan bilangan bulat maupun bilangan desimal. Penggunaan tipe data ini ditandai dengan keyword **num** yang digunakan.

5.  **Boolean**

    Boolean merupakan tipe data yang hanya menyimpan nilai true atau false terhadap sebuah nilai. Tipe data ini dapat digunakan dengan memanggil keyword **bool**.

6.  **Dynamic**

    Dynamic merupakan tipe data yang fleksibel yang dimiliki oleh bahasa pemrograman dart. Tipe data ini dapat berupa string, integer, double, number dan lain sebagainya, yang dapat berubah-ubah sesuai dengan value yang ditentukan. Hal tersebut dapat terjadi, karena tipe data ini akan menentukan jenisnya ketika sudah ada nilai yang diterima. Tipe data ini ditandai dengan penggunaan keyword **dynamic**.

7.  **List**

    List merupakan tipe data yang dapat menampung berbagai data ke dalam suatu objek, seperti string, integer, double, number, dan boolean. Penggunaan tipe data ini ditandai dengan keyword list dan penggunaan kurung siku ([…]) yang mengapit data-data.

8.  **Map**

    Map merupakan tipe data yang akan menyimpan sekumpulan data dalam format key:value. Dalam tipe data ini, seluruh data akan disimpan ke dalam sebuah key dan untuk mengakses data tersebut, pengguna dapat mengakses key yang menyimpan datanya. Tipe data ini ditandai dengan penggunaan format key:value dalam menyimpan datanya dan data tersebut diapit oleh penggunaan kurung kurawal ({…}).

### Control Flow

Bahasa pemrograman dart memiliki 4 sistem percabangan yang dapat digunakan, antara lain:

1.  **If statement**

    Statement if merupakan salah satu sistem percabangan sederhana yang akan menjalankan sebuah blok kode program jika suatu kondisi terpenuhi atau saat kondisi tersebut bernilai true. Berikut merupakan syntax yang digunakan dalam if statement:

    {{< tabs >}}
    {{% tab %}}

    if (condition) {
    // body of if
    }

    {{% /tab %}}
    {{< /tab >}}

    Pada statement if, sistem akan memeriksa boolean expression yang dihasilkan dari kondisi yang diamati. Jika kondisi tersebut menghasilkan nilai true, maka sistem akan menjalankan kode program yang ada di dalam statement if tersebut. Namun, jika kondisi tersebut bernilai false maka sistem tidak akan menjalankan blok kode program apa pun.

2.  **If-else statement**

    Statement ini akan menjalankan 2 kondisi yang berbeda, bergantung kepada nilai boolean yang diterima. Berikut merupakan syntax yang digunakan dalam statement if-else:

    {{< tabs >}}
    {{% tab %}}

    if (condition) {
        // body of if
    } else {
        // body of else
    }


    {{% /tab %}}
    {{< /tab >}}

    Dalam statement ini sistem akan memeriksa terlebih dahulu boolean expression yang akan dihasilkan dari kondisi yang diamati. Jika kondisi tersebut menghasilkan nilai true, maka sistem akan menjalankan kode program di dalamnya. Namun, jika kondisi yang didapati adalah false, maka program tetap akan menjalankan sebuah kode yang berada pada statement else.

3.  **Else-if statement**

    Statement else-if merupakan perkembangan dari statement if-else. Dalam statement ini, programmer dapat memasukkan beberapa kondisi yang akan dicek oleh sistem, sehingga output yang dihasilkan lebih bervariasi. Berikut adalah potongan kode dari statement else-if:

    {{< tabs >}}
    {{% tab %}}

    if (condition1) {
        // body of if
    } else if (condition2) {
        // body of if
    } else {
        // statement 
    }

    {{% /tab %}}
    {{< /tab >}}

    Dalam kode program tersebut, sistem akan melakukan pengecekkan terlebih dahulu terhadap kondisi pada statement if. Jika kondisi tersebut terpenuhi, maka sistem akan menjalankan blok kode program yang ada di dalamnya. Namun, jika kondisi tersebut tidak terpenuhi maka sistem akan menjalankan perintah else if yang memiliki sebuah kondisi. Jika pada statement else if kondisi tersebut terpenuhi, maka sistem akan menjalankan kode program di dalamnya. Namun, jika kondisi tidak terpenuhi maka sistem akan memeriksa kondisi else if lainnya. Jika kondisi else if yang lain juga tidak terpenuhi, maka sistem akan menjalankan blok program yang ada pada statement else.

4. **Switch-case statement**

    Switch-case statement merupakan satu-satunya control flow yang dimiliki oleh dart dengan mekanisme yang berbeda. Dalam statement ini, seluruh case atau kondisi akan diperiksa secara bersamaan. Jika salah satu case terpenuhi, maka sistem akan menjalankan blok program tersebut tanpa menjalankan blok program yang lain. Namun, jika dari beberapa case yang telah didefinisikan tidak ada yang sesuai, maka sistem akan menjalankan blok program pada statement default. Berikut merupakan syntax pada statement switch-case:

    {{< tabs >}}
    {{% tab %}}

    switch(variable_expression) { 
        case constant_expr1:
            // statements; 
            break; 
        case constant_expr2: 
            //statements;
            break; 
        default:
            //statements;
            break; 
    }

    {{% /tab %}}
    {{< /tab >}}

## Golang

Golang atau Go merupakan bahasa pemrograman yang dikembangkan oleh Google pada tahun 2007 dan bersifat open source. Golang mulai dikeperkenalkan ke publik pada tahun 2009. Sama seperti bahasa pemrograman pada umumnya, Golang memiliki sebuah framework yang digunakan untuk membangun berbagai aplikasi, seperti Goji, Revel, Martini, Gocraft, Buffalo, Echo dan Gin. Golang dapat digunakan untuk mengembangkan website, cloud dan jaringan. Bahasa pemrograman ini memiliki beberapa keunggulan dan kekurangannya sendiri. Keunggulan yang ditawarkan oleh bahasa pemrograman ini, antara lain:

1.  **Kecepatan**

    Golang merupakan bahasa pemrograman yang dikompilasi artinya kode yang ditulis bisa langsung diterjemahkan dengan format yang dapat dimengerti oleh prosesor.

2.  **Mudah** dipelajari

    Golang termasuk ke dalam bahasa pemrograman yang mudah untuk dipelajari mulai dari proses instalasi hingga penggunaanya. Sehingga pengguna tidak membutuhkan waktu lama untuk mempelajari Golang.

3.  **Punya** banyak dukungan

    Golang dapat digunakan di berbagai OS dan juga terdapat beberapa Integrated Development Environment (IDE) dan text editor yang mendukung penulisan Go seperti VSCode, Atom, Eclipse, Sublime, InteliJ.

4.  **Banyak** digunakan industry

    Banyak industri menggunakan Golang untuk membangun environment perusahaan. Mempelajari Golang memungkinkan menunjang profesi sebagai programmer.

Meskipun bahasa ini menawarkan beberapa keunggulan yang menarik, nyatanya terdapat beberapa kekurangan yang dimiliki oleh bahasa pemrograman ini, antara lain:

1.  **Memerlukan banyak waktu untuk melakukan tugas**

    Kesederhanaan Golang justru membuat bahasa pemrograman ini kurang deskriptif dibandingkan dengan pemrograman yang lain. Jika developer menulis suatu perintah pada bahasa pemrograman lain mungkin developer akan lebih banyak menulis baris code yang dibutuhkan di bahasa Go.

2.  **Tergolong bahasa pemrograman yang baru**

    Sebagai bahasa pemrograman yang tergolong baru kelemahannya adalah sulit diimplementasikan ke platform yang tidak terintegrasi dengan Golang. Developer akan merasa sedikit kesulitan dengan library yang ada.

3.  **Tidak mendukung generic function**

    Bahasa pemrograman lain mendukung generic function sehingga developer dapat menggunakan kembali kode atau function yang sebelumnya sudah dibuat. Kurangnya dukungan Go terhadap generic function menjadikan pengembangan tidak efisien.

Bahasa pemrograman ini telah diimplementasikan ke dalam beberapa aplikasi besar, seperti:

1. **Uber**. Golang diimplementasikan ke dalam maps yang berfungsi sebagai penuntun dalam melakukan sebuah perjalanan yang lebih cepat.
2. **Slack**. Golang digunakan di beberapa fitur, seperti posting pesan, notifikasi, kalender dan lainnya.
3. **Dropbox**. Golang digunakan untuk mengelola layanan *cloud-storage sharing*.
4. **Riot Games**. Golang digunakan untuk membangun *environment* dan penulisan kode dengan cepat.