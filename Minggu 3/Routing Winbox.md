### Kelompok 6
1. Lifta Annisa Husaina (3121600045)
2. Andriana Wahyu (3121600040)
3. Adhika Syafrina (312160005?)

Kelas : 2 D4 IT B  

## Instalasi Wine dan Winbox
### Wine
Berikut adalah langkah-langkah untuk instalasi wine :  
1. Masuk sebagai root dengan menggunakan perintah `su -` 
2. Lalu ketikkan command `apt-get install wine` atau bisa dengan menggunakan perintah `sudo apt-get install wine` apabila tidak memasuki root.
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/5c3c9535c086e525bab353e8248e873480c1a04f/Minggu%203/images/4.InstallWine.jpeg"/>
3. Maka wine telah terinstall.

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
1. Pastikan semua PC di meja anda mendapatkan IP address sesuai dengan gambar dengan menggunakan perintah `#dhclient -v`
2. Catat IP address yang ada pada router RB 3011 atau Dapat dengan mengecek di terminal dengan command ‘ip addr’ atau ‘ifconfig’dan ambil screenshootnya 
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/3fba2a180ea5927d8d6aecdebe04b3e3c667fd65/Minggu%203/images/1.catatIP.jpeg" width="" height="250" /> 
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/3fba2a180ea5927d8d6aecdebe04b3e3c667fd65/Minggu%203/images/Ether1.jpeg" width="" height="150" /><img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/5c3c9535c086e525bab353e8248e873480c1a04f/Minggu%203/images/Ether2.jpeg" width="" height="150" /> 
3. Akses router RB 3011 menggunakan “winbox.exe" via wine yang telah terinstall dengan menggunakan perintah `wine winbox.exe`. Maka tampilan akan seperti dibawah ini:
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/5c3c9535c086e525bab353e8248e873480c1a04f/Minggu%203/images/6.WinboxOpened.jpeg" />
4. Untuk melakukan konfigurasi, terlebih dahulu masuk pada Legacy Mode 
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/92039e746234319ac33fcdf124d199a6af49cb62/Minggu%203/images/routing1.jpeg" />
5. Lalu klik "Neighbors", lalu pilih Mac Address anda dan klik connect. Maka tampilan akan seperti di bawah ini:
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/92039e746234319ac33fcdf124d199a6af49cb62/Minggu%203/images/routing2.jpeg" />
6. Pilih routing, untuk konfigurasi agar bisa melakukan routing atau mengaksws subnet pada router lain. Maka tampilan akan seperti gambar dibawah ini
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

Kelompok 7
- Network Address : 10.252.108.17
- Gateway : 192.168.7.1

8. Lalu cek hasil routing apakah sudah bisa mengakses router tersebut dengan menggunakan perintah `ping`
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/5c0c2776a11a0065586cd5709df9a9598a22f87a/Minggu%203/images/routing5.jpeg"/>

9. Berikut adalah tabel routingnya:
<img src="https://github.com/lftnnisa/Worksop-Administrasi-Jaringan/blob/bcdbd387fd72d3488033fef63c2a9ee0c5272935/Minggu%203/images/routing6.jpeg"/>

## Instalasi Virtual Box 
5) Install Virtul box
denzan menyaunatan petrijut deri
behate virtual box. (Instalas aght tricky , perly sedket exploie te.
lupendener , tentarne le packag
