### Kelompok 1
1. Lifta Annisa Husaina (3121600045)
2. Akbar Pratama Bimantoro (3121600053)
3. Aditya Bagus Ferryanto (31216000448)

Kelas : 2 D4 IT B  

## Instalasi Wine dan Winbox
### Wine
Berikut adalah langkah-langkah untuk instalasi wine :  
1. Masuk sebagai root dengan menggunakan perintah `su -` 
2. Pastikan sudah terhubung dengan koneksi internet karena pada saat install membutuhkan koneksi internet
3. Lalu ketikkan command `apt-get install wine` atau bisa dengan menggunakan perintah `sudo apt-get install wine` apabila tidak memasuki root.
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/5c3c9535c086e525bab353e8248e873480c1a04f/Minggu%203/images/4.InstallWine.jpeg"/>
3. Maka wine telah terinstall.
---

### Winbox
Berikut adalah langkah-langkah menginstall winbox
1. Akses web “https://mikrotik.com/download/“
2. Download apk winbox dengan format .exe sesuai spesifikasi PC anda
3. Setelah terinstall, buka "winbox.exe" dengan menggunakan command `wine winbox.exe` pada terminal linux
4. Apabila terdapat eror "it looks like wine32 is missing, you should install it. as root, please execute `apt-get install wine32`", maka ketikkan perintah tersebut pada terminal sebagai root untuk mendownload paket yang hilang. Lalu ketikkan perintah `apt-get update`
5. Setelah itu, jalankan kembali pada terminal dengan menggunakan perintah `wine winbox.exe`
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/5c3c9535c086e525bab353e8248e873480c1a04f/Minggu%203/images/5.OpenWinbox.jpeg" />
6. Maka tampilan winbox akan seperti gambar di bawah ini :
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/5c3c9535c086e525bab353e8248e873480c1a04f/Minggu%203/images/6.WinboxOpened.jpeg"/>
7. Pilih fitur routing untuk melakukan routing sehingga bisa mengakses dan melakukan seluruh subnet pada router lain
---

## Konfigurasi Routing di Winbox

1. Pastikan semua PC di meja anda mendapatkan IP address sesuai dengan menyetting ip dan interface dan catat IP address yang ada pada router RB 3011
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/8ae8f535ca9ecc418ff60523d06b89d206bf7419/Minggu%205/images/1.png">
2. Akses router RB 3011 menggunakan “winbox.exe" via wine yang telah terinstall dengan menggunakan perintah `wine winbox.exe` pada terminal. Maka tampilan akan seperti dibawah ini:
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/5c3c9535c086e525bab353e8248e873480c1a04f/Minggu%203/images/6.WinboxOpened.jpeg" />
3. Untuk melakukan konfigurasi, terlebih dahulu masuk pada Legacy Mode 
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/92039e746234319ac33fcdf124d199a6af49cb62/Minggu%203/images/routing1.jpeg" />
4. Lalu klik "Neighbors", lalu pilih Mac Address anda dan klik connect. Maka tampilan akan seperti di bawah ini:
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/92039e746234319ac33fcdf124d199a6af49cb62/Minggu%203/images/routing2.jpeg" />
5. Routing default gateway dari Ip route ke gateway sesuai topologi. Pilih routing, untuk konfigurasi agar bisa melakukan routing atau mengakses subnet pada router lain. Maka tampilan akan seperti gambar dibawah ini
- ip `0.0.0.0 dst 10.252.108.212` merupakan ip dari internet PENS
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/92039e746234319ac33fcdf124d199a6af49cb62/Minggu%203/images/routing3.jpeg" />
7. Klik tombol + untuk menambahkan address dari router lain.
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/4c167efd9c17f92395364b9ca03d364879666478/Minggu%203/images/routing4.png" />

Pada Dst address masukkan network address dari router. Untuk Gateway masukkan gateway dari network tersebut. Setelah itu masukkan seluruh network yang ada.

Kelompok 1
- Network Address : 10.252.108.20
- Gateway : 192.168.10.1  

Kelompok 2  
- Network Address : 10.252.108.12  
- Gateway : 192.168.2.1  

Kelompok 3  
- Network Address : 10.252.108.13
- Gateway : 192.168.3.1

Kelompok 4  
- Network Address : 10.252.108.14
- Gateway : 192.168.4.1

Kelompok 5
- Network Address : 10.252.108.15
- Gateway : 192.168.5.1

Kelompok 6
- Network Address : 10.252.108.16
- Gateway : 192.168.6.1

Kelompok 7
- Network Address : 10.252.108.17
- Gateway : 192.168.7.1

Kelompok 8
- Network Address : 10.252.108.18
- Gateway : 192.168.8.1

Kelompok 9
- Network Address : 10.252.108.19
- Gateway : 192.168.9.1

8.	Setting dhcp server via dhcp setup -> rangenya dari 192.168.X.100- 192.168.X.254
9. 	Sambungkan pc/laptop ke jaringan anda, Cek ip address pastikan ip address dari pc mendapatkan ip address dari router dari dhcp server

10. Lalu cek hasil routing apakah sudah bisa mengakses router tersebut dengan menggunakan perintah `ping`
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/5c0c2776a11a0065586cd5709df9a9598a22f87a/Minggu%203/images/routing5.jpeg"/>

11. Berikut adalah tabel routingnya:
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/bcdbd387fd72d3488033fef63c2a9ee0c5272935/Minggu%203/images/routing6.jpeg"/>

---

## Instalasi Virtual Box
1. Mendownload installasi virtualbox di https://www.virtualbox.org/wiki/Downloads kemudian memilih Linux Distribution dan memilih versi dari debian kita.
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/2c1c32ebc4f70cf46003530de23ebc0f6da5b9e8/Minggu%203/images/download%20VB.png" height="250" /> 
2. Sebelum melakukan installasi VirtualBox kita perlu untuk mengupdate package list dari debian dengan menjalankan perintah `sudo apt update` diterminal juga menjalankan perintah `sudo apt install build-essential dkms` untuk menginstal essentials linux kernels
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/2c1c32ebc4f70cf46003530de23ebc0f6da5b9e8/Minggu%203/images/vb1.jpeg" width="" height="500" />
3. Ketika terdapat error, masuk ke akun root dan menjalankan perintah `apt --fix-broken isntall` untuk menanganinya.
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/2c1c32ebc4f70cf46003530de23ebc0f6da5b9e8/Minggu%203/images/vb2.jpeg" width="" height="150" />
4. Pergi ke direktori download dengan perintah `cd Download`. Setelah itu menggunakan perintah ls untuk melihat isi direktori dan memeriksa paket tersebut tersedia. Kemudian untuk menginstall paket Virtualbox.deb menjalankan perintah `sudo dpkg -i virtualbox-6.1_6.1.34-150636.1~Debian~bullseye_amd64.deb` di terminal.
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/b4fba8a2e2890146caca07cf15c53d3a3b6e250d/Minggu%203/images/vb3.jpeg" width="" height="500" />
5. Karena terdapat pesan error, jalankan perintah `sudo apt install -f` di terminal untuk memaksa pememasangan paket tersebut.
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/b4fba8a2e2890146caca07cf15c53d3a3b6e250d/Minggu%203/images/vb4.jpeg" width="" height="500" />
6. VirtualBox berhasil diinstall.

---
## Instalasi Ubuntu
Ketika sudah menginstall virtualbox, kita perlu men-setting virtual machine untuk menginstall ubuntu

- Beri nama virtual machine dan OS yang akan diinstall
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/d2f603871ffea6cadf45c0e035eac08c2bac66cb/Minggu%203/images/VirtualMachine1.png"/>

- Tentukan jumlah memori dan yang digunakan untuk virtual OS
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/02251bed6f81d99416bf9aca7376588bd22d6aa1/Minggu%203/images/VirtualMachine2.png"/>

- Tentukan jumlah storage dan yang digunakan untuk virtual OS
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/02251bed6f81d99416bf9aca7376588bd22d6aa1/Minggu%203/images/VirtualMachine3.png"/>

- Berikut adalah summary dari setting yang sudah dilakukan sebelumnya
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/02251bed6f81d99416bf9aca7376588bd22d6aa1/Minggu%203/images/VirtualMachine4.png"/> 

Setelah setting virtual machine, install OS ubuntu pada virtual machine yang sudah dibuat. Berikut tampilan awal OS Ubuntu setelah diinstall.

<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/02251bed6f81d99416bf9aca7376588bd22d6aa1/Minggu%203/images/InstallUbuntu.png">

---
## Setting IP Static pada Virtual Machine & Konfigurasi NTP
1. Power up/nyalakan virtual machine anda pastikan konfigurasi jaringan ke bridge. Pastikan mendapatkan ip address dari dhcp server
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/174c33f3747732a21b1894cce17327162818b2cc/Minggu%205/images/7.png">
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/174c33f3747732a21b1894cce17327162818b2cc/Minggu%205/images/8.png">
2.	Setelah mendapat ip address dan terconnect jaringan. Konfigurasi server ip add VM menjadi static dengan menggunakan perintah `nano /etc/network/interfaces` pada terminal
3.	Lalu setting ip mulai dari 192.168.1.10
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/174c33f3747732a21b1894cce17327162818b2cc/Minggu%205/images/9.png">
4. Konfigurasi NTP ke 0.id.pool.htp.org , 1, 2, dst
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/174c33f3747732a21b1894cce17327162818b2cc/Minggu%205/images/10.png">
5. Jika sudah, lakukan konfigurasi sudo
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/174c33f3747732a21b1894cce17327162818b2cc/Minggu%205/images/11.png">
 <img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/174c33f3747732a21b1894cce17327162818b2cc/Minggu%205/images/12.png">
6. Setelah itu, ganti hostname VM menjadi Servers10/kelompok1.takehome.com dengan menggunakan perintah `nano /etc/hostname server`
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/174c33f3747732a21b1894cce17327162818b2cc/Minggu%205/images/13.png">
 
 

       
 



