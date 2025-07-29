# 🔐 DorLock - IoT Smart Door Lock System

DorLock adalah sistem kunci pintu pintar berbasis IoT menggunakan **ESP8266**, yang memungkinkan pengguna membuka kunci pintu menggunakan **PIN** dan memonitor status kunci melalui LCD serta Web Interface.

---

## 📦 Fitur Utama

- ✅ Buka dan kunci pintu menggunakan kode PIN
- 🌐 Terhubung ke WiFi dan dikendalikan via Web Server
- 📟 Menampilkan status di LCD 16x2 I2C
- 🔒 Penguncian otomatis jika kode salah beberapa kali
- 🔄 Reset sistem lewat tombol fisik
- 🔔 Buzzer sebagai indikator

---

## 🧰 Hardware yang Digunakan

- ESP8266 (NodeMCU atau sejenis)
- Keypad 4x4
- Servo Motor (sebagai pengunci)
- LCD 16x2 dengan I2C
- Buzzer
- Tombol reset
- Breadboard dan kabel jumper

---

## 📂 Struktur File

- `dorlock.ino` — Source code utama Arduino untuk sistem pintu.

---

## ⚙️ Cara Instalasi

1. **Persiapkan Library Arduino berikut**:
    - `ESP8266WiFi`
    - `ESP8266WebServer`
    - `Servo.h`
    - `Wire.h`
    - `LiquidCrystal_I2C`
    - `Keypad`

2. **Upload kode `dorlock.ino` ke ESP8266** menggunakan Arduino IDE.

3. **Hubungkan perangkat keras** sesuai dengan pin yang ditentukan dalam kode:
    - LCD I2C
    - Keypad 4x4
    - Servo di pin `D4` (GPIO2)
    - Buzzer dan tombol reset di pin yang sesuai

4. **Atur WiFi**:
    - Ganti nama SSID dan password di dalam kode:
      ```cpp
      const char* ssid = "Nama_WiFi";
      const char* password = "Password_WiFi";
      ```

5. **Akses Web Server**:
    - Setelah ESP8266 terkoneksi ke WiFi, buka browser dan akses alamat IP yang dicetak di Serial Monitor.

---

## 📖 Cara Menggunakan

1. **Nyalakan sistem** dan tunggu sampai LCD menampilkan "Enter PIN".
2. **Masukkan PIN melalui keypad**.
3. Jika PIN benar, servo akan terbuka dan LCD menampilkan "Access Granted".
4. Jika PIN salah beberapa kali, sistem akan terkunci sementara.
5. Gunakan Web Interface untuk monitoring status atau membuka pintu secara manual (jika diaktifkan di kode).

---

## 📌 Catatan Tambahan

- Sistem ini dapat dikembangkan lebih lanjut dengan fitur:
    - Penyimpanan PIN di EEPROM
    - Logging akses via server
    - Integrasi RFID atau sidik jari

---

## 📜 Lisensi

Proyek ini bebas digunakan untuk keperluan pembelajaran dan pengembangan pribadi. Jika digunakan untuk komersial, mohon mencantumkan kredit kepada pengembang asli.

---

## 👨‍💻 Kontribusi

Silakan kirim pull request atau laporkan issue jika Anda menemukan bug atau ingin menambahkan fitur baru!

