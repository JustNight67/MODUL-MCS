---
weight: 33
title: "Prosedur Praktikum"
description: "Proses pembuatan aplikasi Flutter Servo dan Cards Control pada MCS"
icon: "Assignment"
date: "2025-09-13T16:48:46+07:00"
lastmod: "2025-09-13T16:48:46+07:00"
toc: true
---

## Tampilan Aplikasi

<div class="d-flex justify-content-center w-60">
<img src="/images/babEight/Ba8-1.png" alt="Gambar 8.1 - Tampilan Halaman Aplikasi yang Akan diimplementasikan" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 8.1</b> Tampilan Halaman Aplikasi yang Akan diimplementasikan</p>

**Penjelasan terkait bagaimana cara aplikasi bekerja akan diterangkan oleh asisten yang mengajar.**

## Implementasi Aplikasi

Implementasi aplikasi dilakukan dalam 2 lingkup berbeda, yakni lingkup pembangunan tampilan aplikasi menggunakan Flutter dan lingkup konfigurasi terhadap sensor yang digunakan. Sensor yang digunakan pada praktikum ini, antara lain servo dan RFID.

### Pembuatan Aplikasi

Dalam mengimplementasikan tampilan dari desain aplikasi di atas, terdapat beberapa langkah yang harus dilewati terlebih dahulu agar proses praktikum dapat berjalan dengan lancar dan terselesaikan sesuai dengan apa yang dituju. Langkah-langlah dalam pembuatan project baru sama seperti yang telah dilakukan pada praktikum pertemuan sebelumnya.

<div class="d-flex justify-content-center w-60">
<img src="/images/babEight/Ba8-2.png" alt="Gambar 8.2 - Tampilan Awal Software Android Studio" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 8.2</b> Tampilan Awal Software Android Studio</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babEight/Ba8-3.png" alt="Gambar 8.3 - Proses Pembuatan Project Baru" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 8.3</b> Proses Pembuatan Project Baru</p>

Setelah project berhasil terbentuk masuklah ke dalam file pubspec.yaml dan tambahkan package provider dan dio. Ketika sudah menambahkan kedua package tersebut jangan lupa untuk di pub get agar package yang ditambahkan dapat digunakan.

<div class="d-flex justify-content-center w-60">
<img src="/images/babEight/Ba8-4.png" alt="Gambar 8.4 - Package yang digunakan" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 8.4</b> Package yang digunakan</p>

Setelah melakukan pub get, buatlah struktur tree project, seperti yang terlihat pada Gambar 8.5.

<div class="d-flex justify-content-center w-60">
<img src="/images/babEight/Ba8-5.png" alt="Gambar 8.5 - Struktur Tree Project" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 8.5</b> Struktur Tree Project</p>

Berikutnya ketika struktur tree project sudah tersusun seperti pada gambar, masuklah ke dalam file **card_bridge_model.dart** dan isikan kode program berikut:

{{< alert context="info" text="Code **card_bridge_model.dart** akan dipaparkan oleh **PJ Shift**." />}}

Setelah file tersebut terisikan dengan kode program yang membangun model untuk mendapatkan data API yang dikirimkan melalui RFID, langkah berikutnya adalah membangun model yang akan digunakan untuk mengambil data yang dikirimkan oleh servo. Kode program tersebut dibentuk pada file **servo_status_model.dart**.

{{< alert context="info" text="Code **servo_status_model.dart** akan dipaparkan oleh **PJ Shift**." />}}

Setelah membuat kedua model object dart berdasarkan response API yang diberikan, langkah berikutnya adalah melakukan penulisan kode untuk file **card_api_service.dart** dan **servo_status_service.dart**. Berikut merupakan kode yang digunakan untuk membangun service API dari **card_bridge_model.dart**.

{{< alert context="info" text="Code **card_api_service.dart** akan dipaparkan oleh **PJ Shift**." />}}

Kode program tersebut digunakan untuk menghandle bagian RFID. Pada bagian awal class tersebut, didefinisikan variabel **cardBridgeUrl** yang berisikan url yang tersusun dari **ip address** dan **port** yang telah ditentukan. Kemudian, terdapat 2 fungsi yang didefinisikan, yakni fungsi **getUid()** yang digunakan untuk membaca data id kartu yang tersimpan di dalam database dan fungsi **deleteCard()** yang digunakan untuk menghapus data id kartu dari database.

Selanjutnya masuklah ke dalam file **servo_api_status.dart** dan tuliskan kode program berikut:

{{< alert context="info" text="Code **servo_api_status.dart** akan dipaparkan oleh **PJ Shift**." />}}

Kode program tersebut digunakan untuk menghandle bagian servo. Pada bagian awal class tersebut, didefinisikan variabel **servoControllerUrl** yang berisikan url yang tersusun dari **ip address** dan **port** yang telah ditentukan
Kemudian, terdapat 2 fungsi yang didefinisikan, yakni fungsi **getServoStatus()** yang digunakan untuk membaca status dari servo dan fungsi **writeServoStatus()** yang digunakan untuk menggerakan servo.

Kemudian masuklah ke dalam file **app_provider.dart** dan tuliskan kode program berikut ke file tersebut:

{{< alert context="info" text="Code **app_provider.dart** akan dipaparkan oleh **PJ Shift**." />}}

Kode program tersebut akan menginisialisasi seluruh atribut, seperti variabel dan fungs yang diperlukan ke dlaam 1 file. Sehingga, kita dapat menggunakannya secara berulang tanpa harus mendefinisikan dari awal. Berikutnya masuklah ke dalam file **main.dart** dan isikan dengan kode program berikut:

{{< alert context="info" text="Code **main.dart** akan dipaparkan oleh **PJ Shift**." />}}

Pada file main.dart terlihat bahwa terdapat pemanggilan terhadap class AppProvider() yang bertujuan agar seluruh variabel dan fungsi yang telah didefinisikan pada provider dapat langsung dijalankan bersamaan pada saat aplikasi dijalankan. Selanjutnya, kita akan membuat sebuah class yang di dalamnya berisikan kode program yang akan membangun suatu tombol yang akan digunakan untuk mengontrol servo. Masuklah ke dlaam file **custom_servo_button.dart** dan masukkan kode program berikut:

{{< alert context="info" text="Code **custom_servo_button.dart** akan dipaparkan oleh **PJ Shift**." />}}

Class CustomServoButton() merupakan sebuah class yang akan membentuk tampilan button yang akan mengotrol servo. Di dalam class tersebut terdapat constructor untuk kebutuhan tampilan buttonnya ataupun proses bisnisnya. Constructor ini akan diisi ketika class ServoButton() dipanggil.

Setelah proses pembuatan button selesai dilakukan, bukalah file **home_page.dart** dan masukkan kode program berikut:

{{< alert context="info" text="Code **home_page.dart** akan dipaparkan oleh **PJ Shift**." />}}

Pada kode program tersebut, terdapat widget StreamBuilder() yang digunakan. Widget tersebut umumnya digunakan ketika kita ingin membuat sebuah aplikasi yang menampilkan data secara real time. Penggunaan StreamBuilder() digunakan dalam 2 kondisi, yakni kondisi untuk menghandle status servo dan kondisi untuk menghandle data id kartu.

{{< alert context="info" text="Code **home_page.dart untuk StreamBuilder()** akan dipaparkan oleh **PJ Shift**." />}}

Kode di atas merupakan kode yang akan menghandle status dari servo. Widget StreamBuilder() pada kode tersebut akan melakukan stream atau pemantauan secara langsung terhadap fungsi getStatusServo() yang telah didefinisikan pada provider. Terdapat beberapa kondisi yang akan ditampilkan, bergantung kepada proses apa yang sedang dijalankan. Jika proses pengambilan data masih berlangsung, maka aplikasi akan menampilkan text “-”. Jika setelah pengambilan data ditemukan error, maka aplikasi akan menampilkan pesan error. Namun, jika aplikasi berhasil mengambil data, maka aplikasi akan menampilkan data berupa status dari servo tersebut.

{{< alert context="info" text="Code **Consumer AppProvider** akan dipaparkan oleh **PJ Shift**." />}}

Kode di atas merupakan kode yang akan menghandle data id kartu.  Sama seperti kode program sebelumnya, kode program ini akan melakukan stream terhadap fungsi getUid() yang telah didefinisikan dan akan menghasilkan tampilan yang berbeda-beda berdasarkan kondisi yang sedang dilewati. Jika proses pengambilan data masih berlangsung, maka aplikasi akan animasi loading yang berada di bagian tengah. Jika setelah pengambilan data ditemukan error, maka aplikasi akan menampilkan pesan error. Jika, data tersebut beesifat null atau data response kosong, maka aplikasi akan menampilkan pesan bahwa data id tidak tersedia. Namun, jika aplikasi berhasil mengambil data, maka aplikasi akan menampilkan seluruh id card yang terdaftar.

### Konfigurasi Alat

Setelah proses pembangunan aplikasi selesai dilakukan, maka kita dapat berpindah pada proses konfigurasi sensor-sensornya. Praktikum memanfaatkan ESP32, RFID-RC522, dan Servo Motor untuk membaca tag RFID dan mengontrol servo berdasarkan instruksi dari server melalui HTTP request. Dengan memanfaatkan koneksi Wi-Fi, sistem ini memungkinkan komunikasi realtime dengan server, yang dapat digunakan untuk aplikasi seperti kontrol akses atau otomatisasi berbasis RFID.

<div class="d-flex justify-content-center w-60">
<img src="/images/babEight/Ba8-6.png" alt="Gambar 8.6 - Ilustrasi Arsitektur Internet of Things" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 8.6</b> Ilustrasi Arsitektur Internet of Things</p>

Bukalah software Arduino IDE yang telah terinstall pada platform anda dan lakukanlah instalasi terhadap package ESP-32 dengan mengikut langkah-langkah berikut.

<div class="d-flex justify-content-center w-60">
<img src="/images/babEight/Ba8-7.png" alt="Gambar 8.7 - Proses Instalasi Package ESP-32" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 8.7</b> Proses Instalasi Package ESP-32</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babEight/Ba8-8.png" alt="Gambar 8.8 - Proses Instalasi Package ESP-32" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 8.8</b> Proses Instalasi Package ESP-32</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babEight/Ba8-9.png" alt="Gambar 8.9 - Proses Instalasi Modul ESP-32" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 8.9</b> Proses Instalasi Modul ESP-32</p>

<span></span>

<div class="d-flex justify-content-center w-60">
<img src="/images/babEight/Ba8-10.png" alt="Gambar 8.10 - Skematik Rangkaian" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 8.10</b> Skematik Rangkaian</p>

<div class="d-flex justify-content-center w-60">
<img src="/images/babEight/Ba8-11.png" alt="Gambar 8.11 - Pin Servo dan ESP-32" class="img-fluid mb-3 responsive-img">
</div>

<p style="text-align: center;"><b>Gambar 8.11</b> Pin Servo dan ESP-32</p>

<span></span>

Setelah proses *wiring* selesai dilakukan, kembalilah ke *software* Arduino IDE dan masukkan kode program berikut:

```
#include <WiFi.h>
#include <HTTPClient.h>
#include <SPI.h>
#include <MFRC522.h>
#include <ESP32Servo.h>

#define SS_PIN  5    // ESP32 pin GPIO5 
#define RST_PIN 27   // ESP32 pin GPIO27 

const char* ssid = "...";       // SESUAIKAN DENGAN SSID Wi-Fi YANG TERHUBUNG
const char* password = "titiktitiktitik"; // SESUAIKAN DENGAN PASSWORD Wi-Fi YANG TERHUBUNG
// const int* ipv4 = 192.168.0.109

const char* serverURL = "http://10.224.45.181:50001/servo/status";

MFRC522 rfid(SS_PIN, RST_PIN);
Servo myServo;

void setup() {
  Serial.begin(115200);
  myServo.attach(12); //pin servo

  WiFi.begin(ssid, password); // CONNECT TO Wi-Fi
  Serial.print("Connecting to WiFi");
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.print(".");
  }
  Serial.println("Connected to WiFi");

  SPI.begin();           // INITIALIZE SPI BUD
  rfid.PCD_Init();       // INITIALIZE MFRC522

  Serial.println("Tap an RFID/NFC tag on the RFID-RC522 reader");
}

void loop() {
  // Check for RFID tag
  if (rfid.PICC_IsNewCardPresent()) {
    if (rfid.PICC_ReadCardSerial()) {
      MFRC522::PICC_Type piccType = rfid.PICC_GetType(rfid.uid.sak);
      Serial.print("RFID/NFC Tag Type: ");
      Serial.println(rfid.PICC_GetTypeName(piccType));

      // PRINT UID IN SERIAL MONITOR IN HEX FORMAT
      String uidStr = "";
      Serial.print("UID:");
      for (int i = 0; i < rfid.uid.size; i++) {
        Serial.print(rfid.uid.uidByte[i] < 0x10 ? " 0" : " ");
        Serial.print(rfid.uid.uidByte[i], HEX);
        uidStr += String(rfid.uid.uidByte[i], HEX);
      }
      Serial.println();

      // SEND UID TO SERVER
      sendUIDToServer(uidStr);

      rfid.PICC_HaltA();        // HALT PICC
      rfid.PCD_StopCrypto1();   // STOP ENCRYPTION ON PCD
    }
  }
  checkServoStatus();
  delay(5000);
}

void sendUIDToServer(String uid) {
  if (WiFi.status() == WL_CONNECTED) {
    HTTPClient http;
    String url = "http://10.224.45.181:50000/card/input/" + uid;  // SESUAIKAN DENGAN IP DAN PORT
    http.begin(url);

    int httpResponseCode = http.POST("");

    if (httpResponseCode > 0) {
      String response = http.getString();
      Serial.println("Server Response: " + response);
    } else {
      Serial.println("Error on sending POST: " + String(httpResponseCode));
    }

    http.end();
  } else {
    Serial.println("WiFi not connected");
  }
}

// FUNCTION UNTUK STATUS SERVO
void checkServoStatus() {
  if (WiFi.status() == WL_CONNECTED) {
    HTTPClient http;
    http.begin(serverURL);
    
    int httpResponseCode = http.GET();
    
    if (httpResponseCode > 0) {
      String payload = http.getString();
      Serial.println("HTTP Response: " + payload);
      
     // Parse JSON response
      if (payload.indexOf("\"srv_status\":1") != -1) {
        // JIKA srv_status BERNILAI 1, SERVO AKAN BERGERAK KE CCW
        Serial.println("Servo moving to CCW");
        myServo.write(0);
      } else if (payload.indexOf("\"srv_status\":0") != -1) {
        // JIKA srv_status BERNILAI 0, SERVO AKAN BERGERAK KE CW
        Serial.println("Servo moving to CW");
        myServo.write(180);
      } else {
        Serial.println("Unknown status received");
      }
    } else {
      Serial.println("Error on HTTP request");
    }
    http.end();
  } else {
    Serial.println("WiFi Disconnected");
  }
}
```
