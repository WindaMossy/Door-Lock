# Sistem Pintu Otomatis Berbasis Fingerprint

Proyek ini merupakan sistem kontrol akses pintu otomatis berbasis sensor fingerprint dengan dukungan **relay** sebagai pengendali kunci. Sistem ini dapat melakukan **pendaftaran sidik jari (enrollment)** dan **verifikasi pengguna secara real-time**, serta membuka pintu otomatis jika sidik jari dikenali.

## 🔧 Fitur
- Mode **enroll** untuk mendaftarkan sidik jari baru
- Mode **verifikasi** untuk mencocokkan sidik jari dengan database
- Aktivasi relay untuk membuka pintu selama 3 detik jika sidik jari valid
- Komunikasi serial melalui **SoftwareSerial** atau **HardwareSerial**
- Kompatibel dengan Arduino UNO dan ESP8266

## 🧰 Komponen dan Library
- **Arduino UNO
- **Sensor Fingerprint** AS608)
- **Relay 1 channel**
- **Kabel jumper, breadboard**
- Library Arduino:
  - [`Adafruit_Fingerprint`](https://github.com/adafruit/Adafruit-Fingerprint-Sensor-Library)
  - `SoftwareSerial`

## ⚙️ Pinout Koneksi (Untuk Arduino UNO)
| Komponen        | Arduino UNO |
|----------------|-------------|
| Sensor TX (Putih) | Pin 3       |
| Sensor RX (Hijau) | Pin 2       |
| Relay IN         | Pin 4       |
| VCC & GND        | 5V & GND    |

## 🚀 Cara Menggunakan
1. **Unggah kode** ke Arduino melalui Arduino IDE.
2. Buka **Serial Monitor** pada baudrate `9600`.
3. Tekan `E` untuk masuk ke mode **enrollment**, lalu ikuti petunjuk untuk mendaftarkan sidik jari.
4. Sistem akan otomatis berpindah ke mode **verifikasi** setelah proses selesai.
5. Ketika sidik jari terdaftar dikenali, **relay akan aktif selama 3 detik** untuk membuka pintu.


## Skema Rangkaian

![Gambar Proyek Anda Disini](https://github.com/WindaMossy/Door-Lock/blob/9600ea29b86f2c630758f484593247ba73ce0fd8/WhatsApp%20Image%202025-07-29%20at%2015.10.43_f6e96083.jpg)

---

## 📂 Struktur File

- `dorlock.ino` — Source code utama Arduino untuk sistem pintu.

--
