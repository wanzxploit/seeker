
<p align="center"><img src="https://i.imgur.com/DIpuNTI.jpg"></p>

<p align="center">
  <b>Seeker</b> adalah hasil **forked** untuk menjaga akses jika repository asli dihapus.  
</p>

<p align="center">
  <br>
  <b>Hasil Forked oleh Wanz Xploit</b>
  <br>
</p>

---

## Deskripsi  

Seeker adalah alat berbasis phishing yang memanfaatkan HTML API untuk meminta izin lokasi dari perangkat target. Jika pengguna memberikan izin, alat ini dapat mengambil:  
- **Informasi Lokasi**: Longitude, Latitude, Accuracy, Altitude (tidak selalu tersedia), Speed (jika perangkat bergerak), dll.  
- **Informasi Perangkat**: ID unik, Model perangkat, OS, Browser, GPU, IP, RAM (perkiraan), dll.  

**Tujuan Utama**: Memberikan edukasi kepada pengguna tentang bahaya mengklik link acak dan memberikan izin penting seperti lokasi.  

## Fitur Utama  
- Akurasi lokasi menggunakan GPS (hingga 30 meter).  
- Bekerja lebih baik pada perangkat dengan GPS, seperti smartphone.  
- **Fallback** ke geolokasi IP jika perangkat tidak memiliki GPS.  

---

## Instalasi  

### Untuk Semua OS  
```bash
git clone https://github.com/wanzxploit/seeker.git
cd seeker/
chmod +x install.sh
./install.sh
```

### Docker  
```bash
docker pull wanzxploit/seeker
```

---

## Penggunaan  

### Jalankan Seeker  
```bash
python3 seeker.py
```

### Gunakan Tunnel  
Di terminal lain, jalankan tunnel seperti ngrok:  
```bash
./ngrok http 8080
```

### Opsi Tambahan  
- **Output KML File untuk Google Earth**:  
  ```bash
  python3 seeker.py -k <filename>
  ```
- **Pilih Port Khusus**:  
  ```bash
  python3 seeker.py -p 1337
  ./ngrok http 1337
  ```
- **Pilih Template Secara Otomatis**:  
  ```bash
  python3 seeker.py -t 1
  ```

### Cara Alternatif (Tanpa ngrok)  
Gunakan layanan lain seperti `localhost.run`:  
```bash
ssh -R 80:localhost:8080 nokey@localhost.run
```

---

## Templat yang Tersedia  

- **NearYou**  
- **WhatsApp**  
- **Telegram**  
- **Zoom**  

> Kamu juga bisa membuat templat sendiri. Lihat panduannya di file `createTemplate.md`.  

---

## Tested On  

- Kali Linux  
- BlackArch Linux  
- Ubuntu  
- Fedora  
- Termux  
- Parrot OS  
- macOS  

---
