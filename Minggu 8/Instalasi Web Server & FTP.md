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
    <img src="./gambar/install_apache.JPG">
#### Menyesuaikan Firewall
Selama penginstalan, Apache mendaftarkan dirinya ke UFW untuk menyediakan beberapa profil aplikasi yang dapat digunakan untuk mengaktifkan atau menonaktifkan akses ke Apache melalui firewall. Setelah instalasi Apache, penting untuk memodifikasi pengaturan firewall untuk memungkinkan akses luar ke port web default. Berikut adalah langkah-langkahnya:
- Apabila belum terinstall ufw, terlebih dahulu install paket ufw
    ```
    sudo apt install ufw
    ```
- Setelah itu, lihat list dari ufw application yang tersedia
    ```
    sudo ufw app list
    ```
    <img src="./gambar/ufw_app_list.JPG">
- Untuk mengizinkan apache diakses dari jaringan public yakni port 80 untuk HTTP, menjalankan perintah:
    ```
    sudo ufw allow 'WWW'
    ```
-  memverifikasi perubahan dengan memeriksa status
    ```
    sudo ufw status
    ```
- Outputnya akan memberikan daftar lalu lintas HTTP yang diizinkan:
    <img src="./gambar/ufw_app_list.JPG">
#### Memeriksa Web Server

- Setelah instalasi apache dan konfigurasi firewall pada langkah sebelumnya, selanjutnya mengecek status dari apache dengan perintah dibawah ini.
    ```
    sudo systemctl status apache2
    ```
    
    <img src="./gambar/check_apache_installation.JPG">

- Untuk memastikan berjalan dengan cara mengakses alamat IP dari server atau komputer yang terinstal Apache
    
    <img src="./gambar/test_apache.JPG">



## Instalasi Database
Setelah memiliki server web yang aktif dan berjalan, perlu menginstal sistem basis data untuk dapat menyimpan dan mengelola data untuk situs. Di Debian, metapackage mysql-server, yang secara tradisional digunakan untuk menginstal server MySQL, digantikan oleh default-mysql-server. Metapackage ini merujuk MariaDB, garpu komunitas dari server MySQL asli oleh Oracle, dan saat ini merupakan server basis data default yang kompatibel dengan MySQL yang tersedia di repositori manajer paket berbasis Debian.

- Melakukan instalasi MariaDB dengan perintah:
    ```
    sudo apt install mariadb-server
    ```
    <img src="./gambar/install_MySQL_server.JPG">

- Setelah proses instalasi selesai, kemudian cek status apakah MySQL sudah berjalan dengan perintah:

    ```
    sudo service mysql status
    ```

    <img src="./gambar/mySQL_status.JPG">

- Untuk melihat versi MySQL :

    ```
    mysqladmin -u root -p version
    ```

    <img src="./gambar/mysql_version.JPG">

## Instalasi PHP
PHP adalah komponen pengaturan Anda yang akan memproses kode untuk menampilkan konten dinamis kepada pengguna akhir. Itu dapat menjalankan skrip, terhubung ke basis data MariaDB Anda untuk mendapatkan informasi, dan menyerahkan konten yang diproses ke server web Anda untuk ditampilkan.
- Menginstal PHP, modul Apache PHP serta menggunakan MySQL dengan PHP menjalankan perintah:
    ```
    sudo apt install php libapache2-mod-php php-mysql
    ```
    <img src="./gambar/install_PHP.JPG">
- Setelah instalasi selesai, jalankan perintah berikut untuk mengecek versi PHP
    ```
    php -v
    ```
    <img src="./gambar/php_version.JPG">

## Instalasi FTP Server (PROFTPD)
- Melakukan instalasi PROFTPD:

    ```
    sudo apt install proftpd -y
    ```

    <img src="./gambar/install_ProFTPD.JPG">

- Memulai layanan dan mengaktifkan proftpd dengan perintah:

    ```
    sudo systemctl start proftpd
    sudo systemctl enable proftpd
    ```

- Cek status apakah sudah berjalan:

    ```
    sudo systemctl status proftpd
    ```

    <img src="./gambar/install _ProFTPD_2.JPG">
