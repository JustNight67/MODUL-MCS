---
weight: 27
title: "Prosedur Praktikum"
description: "Proses pembuatan Card Bridge pada MCS"
icon: "Assignment"
date: "2025-09-13T16:48:46+07:00"
lastmod: "2025-09-13T16:48:46+07:00"
toc: true
---

## Prosedur Praktikum

Dalam membangun REST API pada praktikum ini, terdapat beberapa langkah yang harus dilalui terlebih dahulu, sebelum nantinya melakukan pembuatan kode untuk REST API. Berikut merupakan langkah-langkah yang harus dilalui:

1.  Memeriksa seluruh kebutuhan yang diperlukan
    <ul><li><b>Bahasa Pemrograman Golang</b> (Version 1.23 atau di atasnya)</li></ul>
    <ul><li><b>Visual Studio Code</b> (Extension Golang dan Code Runner)</li></ul>
    <ul><li><b>Postgre SQL</b></li></ul>
    <ul><li><b>Postman</b></li></ul>

    Untuk memastikan apakah bahasa pemrograman golang telah terinstall pada perangkat, bukalah command prompt dan ketikan perintah go version. Jika perangkat telah terinstall dengan bahasa golang, maka tampilan dari command prompt akan terlihat, seperti pada Gambar 6.4.

    <center>
      <img src="/images/babSix/Ba6-3.png" class="img-fluid mb-3 responsive-img">
    </center>

    <p style="text-align: center;"><b>Gambar 6.3</b> Proses Pengecekkan Golang </p>

    <center>
      <img src="/images/babSix/Ba6-4.png" class="img-fluid mb-3 responsive-img">
    </center>

    <p style="text-align: center;"><b>Gambar 6.4</b> Hasil Pengecekkan Versi Golang </p>

2.	Buatlah sebuah folder baru dengan nama bebas. Jika nama folder lebih dari 1 suku kata, pisahkan dengan menggunakan underscore (_).

    <center>
      <img src="/images/babSix/Ba6-5.png" class="img-fluid mb-3 responsive-img">
    </center>

    <p style="text-align: center;"><b>Gambar 6.5</b> Proses Pembuatan Folder Project </p>

3.	Masuklah ke dalam folder tersebut dan ketiklah perintah **cmd** pada bagian path folder agar langsung masuk ke dalam command prompt untuk melakukan konfigurasi lebih lanjut.

    <center>
      <img src="/images/babSix/Ba6-6.png" class="img-fluid mb-3 responsive-img">
    </center>

    <p style="text-align: center;"><b>Gambar 6.6</b> Proses Konfigurasi Project </p>

4.	Setelah masuk ke dalam command prompt, masukkan seluruh konfigurasi berikut secara satu per satu.

    ```
    god mod init [nama_project]

    go get -u "github.com/gin-gonic/gin"
    go get -u "github.com/lib/pq"
    go get -u "github.com/rubenv/sql-migrate"
    go get -u "github.com/joho/godotenv"
    ```

Berikut merupakan penjelasan singkat terkait kode konfigurasi yang telah dimasukkan:

1.	Perintah **go mod init [nama_project]** digunakan untuk menginisialisasi golang pada folder project. Hasil dari proses ini akan menghasilkan sebuah file bernama **go.mod** yang berisikan konfigurasi.
2.	Perintah go get -u "github.com/gin-gonic/gin" digunakan untuk instalasi package Gin framework. Gin framework memudahkan pengembangan API, karena package ini menyediakan berbagai fitur seperti routing, middleware dan handling JSON.
3.	Perintah **go get -u "github.com/lib/pq"** digunakan untuk mengunduh / instalasi driver untuk PostgreSQL. Package tersebut digunakan agar bahasa pemrograman Go berkomunikasi dengan PostgreSQL dan mengirim query.
4.	Perintah **go get -u "github.com/rubenv/sql-migrate"** digunakan untuk mengunduh / instalasi migrasi sql. Dengan adanya package ini pengembang dapat mengelola konfigurasi database.
5.	Perintah **go get -u "github.com/joho/godotenv"** digunakan untuk mengunduh / instalasi godotenv yang digunakan untuk membaca file .env yang berisikan berbagai konfigurasi.

Setelah melakukan konfigurasi pada project golang, bukalah folder tersebut pada software visual studio code dan bentuklah tree project, seperti yang terlihat pada Gambar 6.7.

<div class="d-flex justify-content-center w-60">
<img src="/images/babSix/Ba6-7.png" alt="Gambar 6.7 - Struktur Tree Project" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 6.7</b> Struktur Tree Project</p>

Setelah membentuk struktur tree project, bukalah file **card_bridge_entity.go** dan masukkanlah kode program berikut:

```
package entities

type Card struct {
    ID string `json:"id"`
}
```

Kode program tersebut berperan sebagai model yang mendefinisikan variabel serta tipe data yang digunakannya. Karena pada praktikum kali ini hanya digunakan untuk menyimpan data id dari RFID, maka variabel yang didefinisikan hanyalah 1 variabel saja dengan tipe string. Ketika data tersebut akan dikonversi ke dalam bentuk JSON, maka field tersebut akan tersimpan ke dalam key **id**.

Kemudian, bukalah file 1_initiate.sql yang tersimpan di dalam folder sql_migrations dan masukkanlah kode program berikut:

```
-- +migrate Up
-- +migrate StatementBegin

CREATE TABLE card(
    id varchar(20)
);

-- +migrate StatementEnd
```

Kode program di atas digunakan untuk membuat tabel database baru bernama **card**. Tabel yang dibuat pada praktikum kali ini hanya memiliki 1 field bernama **id** bertipe data varchar yang hanya dapat menampung karakter sepanjang 20 karakter. **Migrate up** merupakan instruksi yang akan menerapkan semua query SQL ke yang lebih baru. **Statement begin** merupakan instruksi yang menandakan awal dari proses pembuatan database, sedangkan **statement end** merupakan instruksi yang menandakan akhir dari pembuatan databse.

Berikutnya bukalah file **database.go** yang tersimpan pada folder database dan ketiklah kode program berikut:

{{< alert context="info" text="Code **database.go** akan dipaparkan oleh **PJ Shift**." />}}

Kode program di atas digunakan untuk proses migrasi golang ke database. Baris kode program //**go:embed sql_migrations/*.sql** bukanlah sebuah komentar, melainkan baris tersebut berfungsi sebagai kode yang akan menyematkan seluruh file yang berekstensi .sql yang ada pada folder sql_migrations ke dalam variabel dbMigrations. Oleh karena itu, perintah ini **wajib** dituliskan sebelum nantinya membangun fungsi migrasi database. Pada bagian awal kode program, terdapat 2 pendefinisian variabel, yakni **dbMigrations** yang akan menyimpan hasil embed yang telah dilakukan pada folder sql_migrations dan dbConnection yang akan menyimpan koneksi ke database.

Berikutnya terdapat function **DBMigrate()** yang di dalamnya terdapat parameter dbParam yang berfungsi dalam menerima status koneksi golang ke database. Ketika function tersebut dipanggil, maka sistem akan menjalankan proses migrasi database dengan root yang diambil dari folder sql_migrations. Berikutnya sistem akan menjalankan proses migrasi dengan pemanggilan terhadap fungsi **Exec()**. Proses tersebut akan menyimpan jumlah migrasi yang berhasil dilakukan dan mengembalikan kondisi error jika proses migrasi mengalami permasalahan. Jika terjadi error, maka sistem akan memanggil fungsi **panic()** yang akan langsung menghentikan jalannya program. Jika tidak terdeteksi error, maka sistem akan menampilkan pesan bahwa proses migrasi berhasil dilakukan.

Kemudian bukalah file **card_bridge_repo.go** dan masukkanlah kode program berikut:

{{< alert context="info" text="Code **card_bridge_repo.go** akan dipaparkan oleh **PJ Shift**." />}}

Kode di atas digunakan agar golang dapat melakukan interaksi dengan database. Terdapat 3 fungsi yang dibentuk pada file ini, antara lain **GetCards(), InsertCard() dan DeleteCard()** yang masing-masing function memiliki tujuan penggunaannya sendiri. Fungsi GetCards() digunakan untuk membaca seluruh data yang tersimpan dalam tabel card. Data tersebut dibaca dengan menggunakan perintah query **SELECT * FROM card**. Pada fungsi tersebut, sistem akan melakukan looping untuk mengisikan data ke dalam variabek result.

Fungsi InsertCard() digunakan untuk menginput data ke dalam table card dengan menggunakan perintah query **INSERT INTO card(id) values($1)**. Sedangkan, fungsi DeleteCard() merupakan fungsi untuk menghapus data dari tabel berdasarkan id yang terdeteksi. Perintah query yang digunakan untuk menghapus data tersebut adalah **DELETE FROM card WHERE id = $1**. 

Selanjutnya masuklah ke dalam file **card_bridge_controller.go** dan masukkanlah kode program berikut:

{{< alert context="info" text="Code **card_bridge_controller.go** akan dipaparkan oleh **PJ Shift**." />}}

Kode program yang digunakan pada file controller bertujuan untuk mengontrol apa yang akan dilakukan oleh sistem. Pada file ini, terdapat 3 fungsi yang dibentuk berdasarkan fungsi yang terbentuk pada file card_bridge_repo.go. Fungsi **GetCards()** berfungsi untuk mengambil seluruh data yang tersimpan pada database. Data yang diambil akan ditampung ke dalam forat JSON dengan key bernama result. Jika terjadi error, maka sistem akan menampilkan pesan error pada key tersebut.

Fungsi **InsertCard()** digunakan untuk menginput data ke dalam database. Data kartu dimasukkan menggunakan parameter di akhir url bernama id. Variabel idCard memiliki nilai yang diambil dari parameter id, lalu card.ID diinisialisasi dengan nilai dari idCard. Setelah itu memanggil InsertCard() dari package repositories agar data masuk ke database. Jika error maka response yang akan diberikan adalah error dengan StatusInternalServerError. Fungsi **DeleteCard()** digunakan untuk meenghapus data kartu yang telah disimpan pada database dengan memanggil fungsi DeleteCard() yang telah dibentuk pada package repositories. Jika terjadi error maka response yang diberikan adalah StatusInternalServerError.

Selanjutnya, bukalah file **card_bridge_router.go** dan masukkanlah kode program berikut:

{{< alert context="info" text="Code **card_bridge_router.go** akan dipaparkan oleh **PJ Shift**." />}}

Kode program yang dituliskan pada file tersebut merupakan kode yang akan mengatur endpoint dari masing-masing fungsi yang telah dibangun. Seluruh fungsi tersebut akan dijalankan dengan url yang sama. Namun, endpoint yang ingin digunakan akan disesuaikan berdasarkan kebutuhan. Endpoint yang dapat digunakan pada praktikum ini, antara lain:

1.	**/cards** = Digunakan untuk menampilkan seluruh data yang ada dengan method API yang digunakan adalah method **GET**.
2.	**/card/input/:id** = Digunakan untuk menginput data baru ke dalam database dengan method API yang digunakan adalah method **POST**. Untuk menginput data, variabel id pada endpoint diganti dengan data yang diinginkan.
3.	**/card/delete/:id** = Digunakan untuk menghapus data yang telah tersimpan dalam database dengan menggunakan method API **DELETE**. Sama halnya dengan pada saat input data, variabel id pada endpoint tersebut juga diganti dengan data yang ingin dihapus.

Setelah mendefinisikan router yang akan digunakan pada praktikum kali ini, langkah berikutnya sebelum membangun kode utama adalah membuat database terlebih dahulu. Database yang digunakan pada praktikum kali ini adalah postgre SQL yang dapat diakses dengan membuka software pgAdmin yang telah terinstall.

<div class="d-flex justify-content-center w-60">
<img src="/images/babSix/Ba6-8.png" alt="Gambar 6.8 - Proses Membuka Postgre SQL" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 6.8</b> Proses Membuka Postgre SQL</p>

Setelah pgAdmin terbuka pada perangkat, tekanlah menu **server** yang berada pada bagian sebelah kiri dan pilihlah server PostgreSQL yang tersedia **(Note: Versi server dapat berbeda-beda)**. Selanjutnya masukkanlah password yang telah dibuat ke dalam field yang telah disediakan dan tekanlah tombol OK untuk masuk ke dalam server tersebut.

<div class="d-flex justify-content-center w-60">
<img src="/images/babSix/Ba6-9.png" alt="Gambar 6.9 - Proses Mengakses Server Postgre SQL" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 6.9</b> Proses Mengakses Server Postgre SQL</p>

Setelah berhasil masuk ke dalam server, klik kanan pada menu **Databases > Create > Database…**

<div class="d-flex justify-content-center w-60">
<img src="/images/babSix/Ba6-10.png" alt="Gambar 6.10 - Proses Pembuatan Database" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 6.10</b> Proses Pembuatan Database</p>

PostgreSQL akan menampilkan halaman baru yang berisikan konfigurasi untuk pembuatan database. Pada menu tersebut, isilah kolom **database** dengan nama bebas. Jika nama folder lebih dari 1 suku kata, pisahkan dengan menggunakan underscore (_). Kemudian tekanlah tombol **save** untuk membuat database. Jika berhasil terbentuk, maka pada menu Databases yang ada di sebelah kiri, akan muncul file database dengan nama yang telah dibuat.

<div class="d-flex justify-content-center w-60">
<img src="/images/babSix/Ba6-11.png" alt="Gambar 6.11 - Konfigurasi Database" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 6.11</b> Konfigurasi Database</p>

Jika database telah terbentuk, kembalilah ke dalam software visual studio code dan masukkan kode berikut ke dalam file **main.go**:

{{< alert context="info" text="Code **main.go** akan dipaparkan oleh **PJ Shift**." />}}

Pada file tersebut, definisikan beberapa variabel yang bersifat konstanta, seperti **host, port, user, password,** dan **dbName**. Variabel tersebut ini nantinya akan digunakan untuk berkomunikasi dengan PostgreSQL. Selain itu, buatlah variabel global bernama **DB** dengan tipe *sql.DB dan err yang akan menangkap error. 

Pada file tersebut, buatlah satu fungsi bernama **main()** yang di dalamnya terdapat logika program utama yang akan dijalankan oleh sistem. Pada fungsi tersebut definisikanlah variabel PORT dengan nilai :8080. SQL akan dibuka dengan pemanggilan terhadap fungsi **Open()** yang di dalamnya terdapat parameter “**postgres”** dan **psqlInfo**. Jika terjadi error pada saat membuka database, maka aplikasi akan menampilkan pesan error pada terminal. Selanjutnya, untuk proses migrasi database, panggilah fungsi DBMigrate() yang telah didefinisikan pada file database untuk menjalankan migrasi konfigurasi SQL ke aplikasi PostgreSQL. Kemudian, koneksi ke database akan ditutup setelah fungsi main() dijalankan dengan pemanggilan terhadap fungsi **Close()** dengan menggunakan defer agar tidak terjai kebocoran koneksi. Kemudian, server akan mulai dijalankan dengan pemanggilan terhadap fungsi **StartServer()** yang telah didefinisikan pada file routers dan dijalankan pada port yang telah ditentukan.

Setelah kode pada main.go selesai dituliskan, bukalah terminal visual studio code dan ketikan perintah **go run main.go** untuk menjalankan kode yang telah dibangun. Jika kode berhasil dijalankan, maka tampilan dari terminal akan terlihat, seperti pada Gambar 6.12.

<div class="d-flex justify-content-center w-60">
<img src="/images/babSix/Ba6-12.png" alt="Gambar 6.12 - Tampilan Terminal Ketika Berhasil Menjalankan Backend" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 6.12</b> Tampilan Terminal Ketika Berhasil Menjalankan Backend</p>

Bukalah aplikasi postman pada perangkat dan lakukanlah uji coba terhadap beberapa endpoint yang telah dibangun.

<div class="d-flex justify-content-center w-60">
<img src="/images/babSix/Ba6-13.png" alt="Gambar 6.13 - Hasil Uji Coba Terhadap Method POST" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 6.13</b> Hasil Uji Coba Terhadap Method POST</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babSix/Ba6-14.png" alt="Gambar 6.14 - Hasil Uji Coba Terhadap Method GET" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 6.14</b> Hasil Uji Coba Terhadap Method GET</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babSix/Ba6-15.png" alt="Gambar 6.15 - Hasil Uji Coba Terhadap Method DELETE" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 6.15</b> Hasil Uji Coba Terhadap Method DELETE</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babSix/Ba6-16.png" alt="Gambar 6.16 - Tampilan Terminal Ketika Telah Menjalankan Beberapa Method" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 6.16</b> Tampilan Terminal Ketika Telah Menjalankan Beberapa Method</p>
