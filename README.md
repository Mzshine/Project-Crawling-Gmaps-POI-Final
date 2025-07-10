# **Project-Crawling-Gmaps-POI-Final**
Proyek ini berisi skrip Python untuk melakukan scraping data Point of Interest (POI) dari Google Maps. Skrip ini menggunakan Selenium untuk mengotomatisasi interaksi browser web dan mengambil detail seperti nama, kategori, alamat, koordinat, dan tautan Google Maps untuk lokasi yang ditentukan
# **Daftar Isi** 
- Fitur
- Library yang Digunakan
- Pengaturan dan Instalasi
- Cara Menjalankan
- Struktur File
- Gambaran Kode
# **Fitur**
- Scraping Otomatis: Memanfaatkan Selenium untuk mengotomatisasi proses pencarian dan ekstraksi data dari Google Maps.
- Pencarian yang Dapat Disesuaikan: Kemudahan dalam mengonfigurasi daftar point of interest dan kota untuk scraping yang lebih tertarget.
- Ekstraksi Data: Mengumpulkan informasi lengkap untuk setiap POI, termasuk:
  - Nama
  - Kategori
  - Alamat Lengkap
  - Kecamatan
  - Latitude dan Longitude
  - URL Google Maps

- Output yang Terorganisir: Menyimpan data yang di-scrape ke dalam file CSV yang bersih dan terstruktur.

- Pencatatan (Logging): Menyimpan log terperinci untuk proses crawling dan hasilnya, yang sangat membantu untuk proses debugging dan melacak kemajuan.

- Penanganan Kesalahan (Error Handling): Dilengkapi mekanisme untuk menangani potensi kesalahan selama scraping, memastikan skrip dapat terus berjalan dengan lancar.

# Library yang Digunakan
- **Python**: Bahasa pemrograman inti yang digunakan untuk skrip.
  
- **Selenium**: Alat yang andal untuk mengotomatisasi browser web, digunakan di sini untuk berinteraksi dengan Google Maps.
  
- **webdriver-manager**: Alat untuk mengelola driver browser untuk Selenium secara otomatis.
  
- **pandas**: Meskipun tidak secara eksplisit ada dalam skrip yang disediakan, ini adalah pustaka yang umum dan direkomendasikan untuk menangani data output CSV untuk analisis lebih lanjut.
# Pengaturan dan Instalasi
1. Clone Repositori ini
   ```
