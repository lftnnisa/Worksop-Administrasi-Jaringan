# LAPORAN RESMI WORSKHOP ADMINISTRASI JARINGAN

## Domain Name Service (DNS)

### Dosen Pengampu
Dr. Ferry Astika Saputra ST, M.Sc

### Disusun Oleh
Akbar Pratama Bimantoro - 3121600053<br>
Lifta Annisa Husaina - 3121600045<br>
Aditya Bagus Ferryanto - 31216000448<br>
2 D4 IT B

### Domain Name Service (DNS)
Domain Name Service (DNS) adalah layanan Internet yang memetakan alamat IP dan nama domain yang memenuhi syarat (FQDN) satu sama lain. Dengan cara ini, DNS mengurangi kebutuhan untuk mengingat alamat IP. Komputer yang menjalankan DNS disebut name servers. Ubuntu dilengkapi dengan BIND (Berkley Internet Naming Daemon), program yang paling umum digunakan untuk mengelola name servers di Linux.

## Overview

File konfigurasi DNS disimpan di direktori `/etc/bind`. File konfigurasi utama adalah `/etc/ bind/named.conf`, yang dalam tata letak yang disediakan oleh paket menyertakan berkas-berkas berikut:

- ```/etc/bind/named.conf.options```: opsi DNS global
- ```/etc/bind/named.conf.local```: untuk zona User
- ```/etc/bind/named.conf.default-zones```: zona default seperti localhost.

## Atur Penamaan Hosts

jika pada VM penamaan host belum sesaui bisa mengatur dengan perintah ```sudo hostnamectl set-hostname server10kelompok1.takehome.com```

kemudian edit file ```/etc/hosts``` tambahkan hostsnamenya

## Instalasi

buat terlebih dahulu server di VM sesuaikan ip dengan jaringan yang terhubung dan jangan lupa untuk megubah network pada VM menjadi Bridge

<img src="assets/1.png" width="" height="350" />

untuk mengaktifkan konfigurasi baru, mulai ulang server DNS. dari terminat dengan perintah berikut ```sudo apt install bind9 bind9utils bind9-doc dnsutils```

<img src="assets/5.png" width="" height="350"/>

jalankan perintah ``` sudo systemctl1 restart named``` untuk memulai ulang layanan Bind dan perintah ```sudo systemctl status named``` untuk periksa dan verifikasi layanan Bind

<img src="assets/7.png" width="" height="350"/>

kemudian jalankan perintah ```sudo nano /etc/bind/named.conf.options``` ubah pada bagain forwarders

<img src="assets/8.png" width="" height="350"/>

## Menyiapkan Zona
edit file named.local dengan perintah ```sudo nano /etc/bind/named.conf.local```

<img src="assets/9.png"/>

kemudian pindahkan file db.local ke db.kampus-01.takehome.com

<img src="assets/10.png"/>

jika sudah ubah isi dari file db.kampus-01.takehome.com

<img src="assets/11.png"/><br>

<img src="assets/12.png"/>

kemudian pada file konfigurasi reverse zone akan memeindahkan isi dari file dengan perintah 

<img src="assets/13.png"/><br>
<img src="assets/14.png"/><br>
<img src="assets/15.png"/>

## Testing

Langkah pertama dalam menguji BIND9 adalah menambahkan Alamat IP nameserver ke host resolver. Nameserver utama harus dikonfigurasi seperti halnya host lain untuk memeriksa ulang berbagai hal. Buka DNS client untuk mengetahui detail tentang cara menambahkan alamat nameserver ke network client. Edit nameserver dan parameter untuk domain pada file ```/etc/resolv.conf```

<img src="assets/16.png" width="" height="350"/>

Terdapat banyak cara untuk melakukan testing, pada kali ini kelompok kami menggunakan metode ping untuk mengetahui apakah konfigurasi sudah berhasil atau belum. Command yang diperlukan:

```ping www.example.com```<br>

screnshoot test di server VM<br>
<img src="assets/17.png"/>

Testing di PC Clint<br>
<img src="assets/18.png"/>

## Problem Solving
jika terdapat ```wired unmanaged``` pada jaringan di VM lakukan konfigurasi pada file ```/etc/NetworkManager/NetworkManager. conf``` dan ubah pada bagian manage menjadi true, setalah itu lakukan restart dengan perintah ```systemctl restart NetworkManager```




