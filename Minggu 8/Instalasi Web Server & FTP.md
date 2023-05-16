# Instalasi Web Service & FTP
### Dosen Pengampu
Dr. Ferry Astika Saputra ST, M.Sc
### Disusun Oleh
Akbar Pratama Bimantoro - 3121600053<br>
Lifta Annisa Husaina - 3121600045<br>
Aditya Bagus Ferryanto - 31216000448<br>
2 D4 IT B

---

## Instalasi Web Server Apache
#### Install Apache
Berikut adalah langkah-langkah instal Apache
- Memperbarui paket yang tersedia ke versi terbaru untuk mencerminkan perubahan upstream terbaru:
    ```
    sudo apt update
    ```
- Install paket Apache2
    ```
    sudo apt install apache2
    ```
    <img src="./images/install apache.png">
#### Menyesuaikan Firewall
Selama penginstalan, Apache mendaftarkan dirinya ke UFW untuk menyediakan beberapa profil aplikasi yang dapat digunakan untuk mengaktifkan atau menonaktifkan akses ke Apache melalui firewall. Setelah instalasi Apache, penting untuk memodifikasi pengaturan firewall untuk memungkinkan akses luar ke port web default. Berikut adalah langkah-langkahnya:
- Apabila belum terinstall ufw, terlebih dahulu install paket ufw
    ```
    sudo apt install ufw
    ```
    <img src="./images/install ufw.png">
- Setelah itu, lihat list dari ufw application yang tersedia
    ```
    sudo ufw app list
    ```
    <img src="./images/ufw app list.png">
- Untuk mengizinkan apache diakses dari jaringan public yakni port 80 untuk HTTP, menjalankan perintah:
    ```
    sudo ufw allow 'WWW'
    ```
    <img src="./images/allow www.png">
-  memverifikasi perubahan dengan memeriksa status
    ```
    sudo ufw status
    ```
- Outputnya akan memberikan daftar lalu lintas HTTP yang diizinkan:
    <img src="./images/status ufw.png">
#### Memeriksa Web Server

- Setelah instalasi apache dan konfigurasi firewall pada langkah sebelumnya, selanjutnya mengecek status dari apache dengan perintah dibawah ini.
    ```
    sudo systemctl status apache2
    ```
    
    <img src="./images/status apache.png">

- Untuk memastikan berjalan dengan cara mengakses alamat IP dari server atau komputer yang terinstal Apache
    <img src="./images/periksa apache.png">

## Instalasi Database
Setelah memiliki server web yang aktif dan berjalan, perlu menginstal sistem basis data untuk dapat menyimpan dan mengelola data untuk situs. Di Debian, metapackage mysql-server, yang secara tradisional digunakan untuk menginstal server MySQL, digantikan oleh default-mysql-server. Metapackage ini merujuk MariaDB, garpu komunitas dari server MySQL asli oleh Oracle, dan saat ini merupakan server basis data default yang kompatibel dengan MySQL yang tersedia di repositori manajer paket berbasis Debian.

- Melakukan instalasi MariaDB dengan perintah:
    ```
    sudo apt install mariadb-server
    ```
    <img src="./images/install database.png">
- Setelah proses instalasi selesai, kemudian cek status apakah MySQL sudah berjalan dengan perintah:
    ```
    sudo systemctl status mysql
    ```
    <img src="./images/status database.png">
- Untuk melihat versi MySQL :
    ```
    mysqladmin -u root -p version
    ```
    <img src="./images/versi database.png">

## Instalasi PHP
PHP adalah komponen pengaturan Anda yang akan memproses kode untuk menampilkan konten dinamis kepada pengguna akhir. Itu dapat menjalankan skrip, terhubung ke basis data MariaDB Anda untuk mendapatkan informasi, dan menyerahkan konten yang diproses ke server web Anda untuk ditampilkan.
- Menginstal PHP, modul Apache PHP serta menggunakan MySQL dengan PHP menjalankan perintah:
    ```
    sudo apt install php libapache2-mod-php php-mysql
    ```
    <img src="./images/install php.png">
- Setelah instalasi selesai, jalankan perintah berikut untuk mengecek versi PHP
    ```
    php -v
    ```
    <img src="./images/cek versi php.png">

## Instalasi FTP Server (VSFTPD)
FTP, kependekan dari File Transfer Protocol, adalah protokol populer untuk mentransfer file ke dan dari server FTP. Namun, itu penuh dengan risiko keamanan karena mengirimkan data dan informasi sensitif seperti nama pengguna dan kata sandi dalam teks biasa. VSFTPD (Daemon FTP Sangat Aman) adalah server FTP yang cepat, aman, dan stabil yang menggunakan enkripsi untuk mengamankan data yang dipertukarkan dengan server.
- Install paket vsftpd
    ```
    sudo apt install vsftpd
    ```
    <img src="./images/install vsftpd.png">
 -  Setelah diinstal, vsftpd dimulai secara otomatis. Anda dapat mengonfirmasi atau mengecek statusnya dengan menjalankan perintah:
    ```
    sudo systemctl status vsftpd
    ```
    <img src="./images/status vsftpd.png">
- Jika layanan vsftpd tidak berjalan, masukkan perintah
    ```
    sudo systemctl start vsftpd
    ```
- Kemudian aktifkan layanan untuk memulai saat boot.
    ```
    sudo systemctl enable vsftpd
    ```
- cek kembali dengan perintah berikut 
     ```
    sudo systemctl status vsftpd
    ```
    <img src="./images/status vsftpd.png">
