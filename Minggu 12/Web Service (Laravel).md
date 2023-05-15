# Instalasi Laravel
### Dosen Pengampu
Dr. Ferry Astika Saputra ST, M.Sc
### Disusun Oleh
Akbar Pratama Bimantoro - 3121600053<br>
Lifta Annisa Husaina - 3121600045<br>
Aditya Bagus Ferryanto - 31216000448<br>
2 D4 IT B

---

## Instalasi Laravel di Linux
Berikut adalah step-step instalasi Laravel
#### Instalasi Composer
- Untuk melakukan instalasi composer dapat dilakukan dengan menggunakan perintha:
    ```
    sudo apt install composer
    ```
    <img src="./image/install composer.jpeg">
#### Install Laravel
- Install Laravel dapat dilakukan dengan perintah
    ```
    composer global require "laravel/installer"
    ```
    <img src="./image/install laravel.jpeg">
### Mengglobalkan Direktori
Pastikan direktori ~/.composer/vendor/bin/ menjadi global di sistem. Jika belum, maka bisa lakukan step berikut:
- Buka file ~/.bashrc
    ```
    nano ~/.bashrc
    ```
    <img src="./image/install laravel.jpeg">
- Lalu pada baris terakhir, tambahkan dua baris berikut:
    ```
    PATH=$PATH:$HOME/.config/composer/vendor/bin
    export PATH
    ```
    <img src="./images/mengglobalkan direktori.jpeg">
### Membuat Project Laravel
- Untuk membuat project baru pada laravel dapat dilakukan dengan menggunakan composer dengan perintah 
    ```
    composer create-project --prefer-dist laravel/laravel blog
    ```
- Untuk membuat project baru pada laravel dapat dilakukan dengan menggunkan command
    ```
    laravel new namaproject
    ```
    <img src="./image/create project.jpeg">
- Apabila pada saat pembuatan project laravel disini terdapat 1 problem yaitu phpunit. Oleh karena itu terlebih dahulu install phpunit dengan perintah
    ```
    sudo apt install phpunit
    ```
    <img src="./image/install phpunit.jpeg">
    
### Testing Laravel
Jika proses di atas lancar tanpa error. Maka laravel sudah terinstall dengan baik. Berikutnya adalah melakukan testing pada project laravel yang telah dibuat
- Masuk ke direktori project.
    ```
    cd Kelompok1/
    ```
- Lalu jalankan perintah berikut:
    ```
    php artisan serve
    ```
    <img src="./image/test laravel 1.jpeg">
- Apabila terdapat eror dan warning seperti gambar diatas maka update composer dengan perintah:
    ```
    composer update
    ```
    <img src="./image/update composer.jpeg">
- Lalu jalankan perintah berikut:
    ```
    php artisan serve
    ```
    <img src="./image/test laravel 2.jpeg">
- Maka laravel akan berjalan menggunakan default server php, pada port 8000. Sehingga ketika kita membuka http://localhost:8000, kita akan mendapati halaman seperti berikut~
  <img src="./image/test web.jpeg">

