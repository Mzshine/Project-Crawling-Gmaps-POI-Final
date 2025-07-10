# **Project-Crawling-Gmaps-POI-Final**
Proyek ini berisi skrip Python untuk melakukan scraping data Point of Interest (POI) dari Google Maps. Skrip ini menggunakan Selenium untuk mengotomatisasi interaksi browser web dan mengambil detail seperti nama, kategori, alamat, koordinat, dan tautan Google Maps untuk lokasi yang ditentukan
# **Daftar Isi** 
- Fitur
- Library yang Digunakan
- Pengaturan dan Instalasi
- Cara Menjalankan
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
   git clone https://github.com/Mzshine/Project-Crawling-Gmaps-POI-Final.git
   cd Project-Crawling-Gmaps-POI-Final
   ```
3. Install Library Python yang diperlukan
   Buat file ** _requirements.txt_** dengan konten berikut :
   ```
   selenium
   webdriver-manager
   ```
   Kemudian, jalankan perintah berikut untuk menginstallnya :
   ```
   pip install -r requirements.txt
   ```
4. Siapkan file input
   Pastikan anda memiliki file **_list_vity.csv_** di direktori utama. File ini harus berisi daftar kota yang ingin anda scrape, dengan satu kota satu baris
# Cara Menjalankan
1. Konfigurasi skrip:
  Buka notebook crawling.ipynb dan ubah variabel berikut di sel keenam sesuai kebutuhan:

  - **_find_poi_**: Daftar nama point of interest yang ingin Anda cari (misalnya, ['INFORMA', 'MR.DIY']).

  - **_f_city_ind_** dan _**l_city_ind**_: Indeks awal dan akhir dari kota yang akan diproses dari file list_city.csv Anda.

2. Jalankan Jupyter Notebook:
Jalankan sel-sel di dalam notebook crawling.ipynb secara berurutan. Skrip akan:

  - Membuka jendela browser Chrome baru.

  - Menavigasi ke Google Maps.

  - Melakukan iterasi melalui setiap POI dan kota yang telah Anda tentukan.

  - Mencari setiap POI di setiap kota.

  - Menggulir panel hasil pencarian untuk memuat semua data yang tersedia.

  - Mengekstrak detail untuk setiap lokasi.

  - Menyimpan data ke file .csv di direktori utama proyek dan file log di direktori result/ dan log/.

# Gambaran Kode
Skrip ini diatur ke dalam beberapa bagian utama:

  - Impor dan Pengaturan: Mengimpor pustaka yang diperlukan dan mengatur konfigurasi untuk logging.

  - Inisialisasi Browser: Mengonfigurasi dan menginisialisasi Selenium WebDriver untuk Chrome.

  - Konfigurasi: Mendefinisikan kueri pencarian (**find_poi**) dan rentang kota yang akan di-scrape dari file **list_city.csv.**

  - Loop Utama:

    - Skrip melakukan iterasi melalui setiap Point of Interest (fp) dan setiap city.

    - Untuk setiap kombinasi, skrip membuat kueri pencarian dan mengirimkannya ke Google Maps.

    - Kemudian, secara dinamis menggulir panel hasil untuk memuat semua entri.

  - Ekstraksi dan Penyimpanan Data:

    - Untuk setiap hasil pencarian, skrip akan mengklik entri untuk melihat detailnya.

    - Skrip mengekstrak nama, kategori, alamat, koordinat, dan tautan Google Maps.

    - Data yang diekstraksi kemudian ditulis ke dalam file CSV.

    - Kemajuan proses dan setiap kesalahan dicatat ke konsol dan ke file log.
