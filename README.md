# ⚡ Digital Voltmeter

Sebuah perangkat alat ukur tegangan (Voltmeter) DC yang dirancang murni menggunakan arsitektur perangkat keras (tanpa mikrokontroler) untuk membaca dan menampilkan nilai tegangan secara *real-time*.

## 🛠️ Fitur Utama
* **Konversi Analog ke Digital:** Membaca input tegangan DC menggunakan IC ADC 8-bit.
* **Display 7-Segment:** Menampilkan hasil ukur secara langsung melalui 7-segment yang didorong oleh *decoder/driver* *hardware*.
* **Custom Enclosure:** Dirakit ke dalam *box* mekanik pelindung yang solid agar portabel dan aman digunakan.

## 🧰 Komponen Utama
* **ADC0804LCN:** 8-Bit Analog-to-Digital Converter
* **74LS47:** BCD to 7-Segment Decoder/Driver
* **L7805:** IC Voltage Regulator (sebagai penurun tegangan untuk daya IC)
* Komponen Pasif: Resistor, Kapasitor, *Header/Connector*.

## 📸 Dokumentasi Visual

**1. Desain Rangkaian (PCB Routing)**
Desain jalur PCB (*routing*) dirancang secara presisi.
![Desain PCB](images/pcb-wit.jpeg)

**2. Skematik Rangkaian (Schematic)**
*File skematik lengkap sistem Voltmeter dapat dilihat pada folder `schematics/`.*

**3. Hasil Akhir (Final Assembly)**
Perangkat dirakit ke dalam *box* hitam pelindung mekanik.
![Final Box](images/voltmeter-3-box.jpg)

## ⚙️ Cara Kerja Singkat
Tegangan analog yang diukur masuk ke pin input ADC0804. ADC melakukan konversi sinyal tersebut menjadi data biner 8-bit. Data biner ini kemudian diterjemahkan oleh IC 74LS47 menjadi format yang dapat ditampilkan sebagai angka desimal yang mudah dibaca pada layar 7-segment.
