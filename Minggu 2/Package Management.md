# Package Management  

Nama : Lifta Annisa Husaina  
NRP : 3121600045  
Kelas : 2 D4 IT B 
Mata Kuliah : Workshop Administrasi Jaringan  
Dosen Pengampu : Dr. Ferry Astika Saputra ST, M.Sc  

---

## Pengenalan Linux

Linux adalah sistem operasi yang gratis dan open source yang pertama kali dibuat oleh Linus Torvalds pada tahun 1991. Sistem operasi ini didasarkan pada kernel Linux yang merupakan inti dari sistem operasi tersebut. Linux dikenal sebagai sistem operasi yang sangat stabil dan aman, serta banyak digunakan oleh kalangan profesional dan pengembang.

Salah satu kelebihan Linux adalah fleksibilitas dan kemampuan untuk disesuaikan dengan kebutuhan pengguna. Selain itu, Linux juga mendukung berbagai jenis perangkat keras dan software, serta memiliki berbagai distribusi yang dapat dipilih sesuai dengan kebutuhan pengguna.

Linux juga digunakan secara luas di dunia server karena kemampuannya untuk menjalankan layanan web, database, dan aplikasi lainnya dengan sangat baik. Selain itu, Linux juga digunakan di berbagai perangkat seperti smartphone, TV pintar, router, dan lain-lain.

Untuk mengakses dan mengelola sistem operasi Linux, pengguna dapat menggunakan antarmuka baris perintah (command line interface) atau antarmuka grafis (graphical user interface). Selain itu, Linux juga memiliki banyak tools dan aplikasi yang gratis dan open source, yang dapat membantu pengguna untuk melakukan berbagai tugas seperti pengembangan web, pengolahan data, pengelolaan basis data, dan lain-lain.

Karena kelebihannya tersebut, Linux menjadi pilihan populer bagi para pengembang dan pengguna yang membutuhkan sistem operasi yang andal dan aman, serta bebas untuk diubah dan disesuaikan sesuai dengan kebutuhan mereka.

---
  
## Evolusi OS

Evolusi Linux dimulai pada tahun 1991 ketika Linus Torvalds mengembangkan kernel Linux sebagai alternatif sistem operasi yang dapat dijalankan pada komputer pribadi. Sejak itu, banyak pengembang di seluruh dunia berkontribusi pada pengembangan kernel Linux dan distribusi Linux.

Berikut adalah beberapa titik penting dalam evolusi OS Linux:

- Linux 0.01: Dirilis pada tahun 1991, merupakan versi awal dari kernel Linux. Kernel ini hanya dapat menjalankan beberapa perintah dasar dan belum memiliki antarmuka - pengguna.
- Linux 0.10: Dirilis pada tahun 1992, menambahkan dukungan untuk sistem file dan lebih banyak perintah.
- Linux 0.95: Dirilis pada tahun 1992, menambahkan dukungan untuk banyak perangkat keras baru, termasuk tampilan grafis.
- Linux 1.0: Dirilis pada tahun 1994, merupakan rilis pertama kernel Linux yang stabil. Kernel ini menambahkan dukungan untuk banyak perangkat keras baru, termasuk jaringan komputer.
- Linux 2.0: Dirilis pada tahun 1996, menambahkan dukungan untuk sistem multiprosesor dan lebih banyak perangkat keras.
- Linux 2.2: Dirilis pada tahun 1999, menambahkan dukungan untuk USB dan PCMCIA.
- Linux 2.4: Dirilis pada tahun 2001, menambahkan dukungan untuk banyak perangkat keras baru, termasuk teknologi virtualisasi.
- Linux 2.6: Dirilis pada tahun 2003, menambahkan dukungan untuk teknologi power management dan teknologi keamanan yang lebih baik.
- Linux 3.0: Dirilis pada tahun 2011, merupakan rilis pertama yang menggunakan nomor versi 3.x. Kernel ini menambahkan dukungan untuk banyak perangkat keras baru, - termasuk arsitektur sistem ARM.
- Linux 4.0: Dirilis pada tahun 2015, menambahkan dukungan untuk teknologi memori yang lebih cepat dan dukungan untuk banyak perangkat keras baru.

Selain pengembangan kernel Linux, evolusi OS Linux juga mencakup pengembangan distribusi Linux yang berbeda. Distribusi Linux seperti Debian dan Ubuntu telah berkembang dengan cara yang berbeda dan menawarkan fitur dan fungsionalitas yang berbeda. 

### Debian 
Evolusi distribusi Linux Debian dimulai pada tahun 1993 ketika Ian Murdock mengumumkan pengembangan distribusi Linux yang stabil dan bebas biaya. Debian awalnya didasarkan pada kernel Linux dan menyediakan kumpulan perangkat lunak open-source yang lengkap dan stabil. Debian juga menawarkan manajemen paket yang canggih dan sistem konfigurasi yang fleksibel, yang memungkinkan pengguna untuk mengatur sistem sesuai dengan kebutuhan mereka. Debian menjadi salah satu distribusi Linux paling populer dan banyak digunakan di server dan desktop.

### Ubuntu 
Evolusi distribusi Linux Ubuntu dimulai pada tahun 2004 ketika Canonical Ltd, perusahaan swasta yang didirikan oleh Mark Shuttleworth, mengumumkan pengembangan distribusi Linux yang berbasis pada Debian. Ubuntu didesain untuk menjadi distribusi Linux yang mudah digunakan dan dikembangkan, dengan tampilan antarmuka pengguna yang modern dan dukungan untuk perangkat keras yang luas. Selain itu, Ubuntu juga menawarkan manajemen paket yang mudah digunakan dan sistem konfigurasi yang terpusat. Ubuntu menjadi salah satu distribusi Linux paling populer dan banyak digunakan di desktop dan laptop.

Perbedaan utama antara Debian dan Ubuntu adalah dalam desain dan fokus pengembangan. Debian lebih fokus pada stabilitas dan fleksibilitas sistem, sedangkan Ubuntu lebih fokus pada kemudahan penggunaan dan pengembangan. Debian juga lebih cocok untuk pengguna yang sudah memiliki pengalaman dengan Linux dan ingin mengatur sistem mereka dengan lebih banyak pilihan, sedangkan Ubuntu lebih cocok untuk pengguna yang baru menggunakan Linux atau ingin menginstal dan menggunakan sistem dengan cepat dan mudah. Namun, keduanya memiliki dukungan komunitas yang besar dan terus berkembang, dan keduanya terus memperbarui dan meningkatkan fitur dan fungsionalitas mereka seiring waktu. Meskipun demikian, semua distribusi Linux didasarkan pada kernel Linux dan memungkinkan pengguna untuk menggunakan perangkat lunak open-source secara gratis.

---

## Perintah Su dan Sudo
Perintah su dan sudo adalah perintah dalam sistem operasi Linux yang digunakan untuk memperoleh hak akses superuser atau root untuk menjalankan perintah yang membutuhkan akses tersebut.

### Perintah Su
Perintah su adalah singkatan dari "switch user" atau "substitute user". Ketika perintah su dieksekusi, pengguna diminta untuk memasukkan kata sandi root untuk memperoleh hak akses superuser atau root. Setelah hak akses superuser didapatkan, pengguna dapat menjalankan perintah yang memerlukan hak akses tersebut. su biasanya digunakan untuk beralih dari pengguna yang sedang aktif ke pengguna root atau pengguna lain dengan hak akses superuser.

### Perintah Sudo
Perintah sudo adalah singkatan dari "superuser do". Ketika perintah sudo dieksekusi, pengguna diminta untuk memasukkan kata sandi pengguna yang memiliki akses ke sudoers, yaitu file konfigurasi yang mengatur hak akses sudo. Setelah otorisasi berhasil, pengguna dapat menjalankan perintah yang memerlukan hak akses superuser. sudo biasanya digunakan untuk memberikan hak akses superuser kepada pengguna tanpa harus beralih ke pengguna root, sehingga lebih aman dan lebih mudah untuk dilacak log aktivitas pengguna.

### Perbedaan perintah Su dan Sudo
Perbedaan utama antara su dan sudo adalah dalam cara memperoleh hak akses superuser. su membutuhkan kata sandi root untuk memperoleh hak akses superuser, sedangkan sudo membutuhkan kata sandi pengguna yang memiliki akses ke sudoers. Selain itu, pengguna yang menggunakan su akan masuk ke dalam lingkungan pengguna root, sedangkan pengguna yang menggunakan sudo akan tetap berada dalam lingkungan pengguna aktif. Ini berarti pengguna yang menggunakan sudo masih dapat mengakses dan menggunakan hak akses pengguna aktif, seperti direktori rumah dan variabel lingkungan pengguna. Hal ini dapat mengurangi risiko kesalahan pengguna yang dapat terjadi ketika menggunakan su. Namun, karena penggunaan sudo lebih kompleks dalam hal konfigurasi, penggunaan su masih sering digunakan oleh pengguna yang lebih berpengalaman dalam sistem operasi Linux.

---

## Package Maintenence
Package maintenance pada sistem operasi Linux adalah proses pengelolaan paket atau software pada sistem operasi Linux. Ini melibatkan menginstal, menghapus, memperbarui, dan mengelola perangkat lunak pada sistem operasi Linux.  

Pada sistem operasi Linux, paket atau software biasanya dikemas dalam format yang disebut sebagai package manager. Package manager ini memungkinkan pengguna untuk dengan mudah menginstal, menghapus, dan memperbarui paket atau software pada sistem operasi Linux.  

Package manager yang populer pada sistem operasi Linux adalah Advanced Packaging Tool (APT). APT adalah package manager pada sistem operasi Debian dan turunannya seperti Ubuntu. APT memungkinkan pengguna untuk dengan mudah menginstal, menghapus, dan memperbarui paket atau software pada sistem operasi Linux. APT juga memungkinkan pengguna untuk mengelola dependensi paket atau software pada sistem operasi Linux.  

Pada umumnya, package maintenance pada sistem operasi Linux dilakukan secara reguler untuk memastikan bahwa sistem operasi Linux tetap aman, stabil, dan up-to-date dengan patch keamanan terbaru. Pengguna juga dapat mengelola paket atau software secara manual dengan menggunakan package manager yang tersedia pada sistem operasi Linux.

### Arti dari Versi di Repository
Repository pada sistem operasi Linux Debian adalah tempat penyimpanan paket software yang telah dikompilasi untuk distribusi Debian. Setiap repository terdiri dari paket-paket software yang telah disediakan oleh pengembang atau komunitas Debian.

Setiap paket software pada repository Debian memiliki nomor versi. Nomor versi pada paket software di Debian terdiri dari tiga bagian: nomor utama (major), nomor minor (minor), dan revisi (patch). Misalnya, versi paket "apache2" pada Debian 10 adalah 2.4.38-3+deb10u5, dimana 2.4.38 adalah nomor versi utama, 3 adalah nomor versi minor, dan +deb10u5 adalah revisi.

Nomor versi pada paket software di Debian biasanya berisi informasi tentang pembaruan keamanan, perbaikan bug, atau penambahan fitur baru pada paket software tersebut. Setiap kali ada pembaruan pada paket software, nomor versi pada paket tersebut akan dinaikkan.

Setiap repository pada Debian juga memiliki distribusi tertentu yang dapat dipakai oleh pengguna Debian. Sebagai contoh, repository "main" pada Debian 10 memiliki distribusi "buster". Distribusi ini menunjukkan bahwa paket-paket pada repository tersebut disediakan untuk distribusi Debian 10 "buster". Pada setiap distribusi Debian, paket-paket software yang terdapat pada repository tersebut dapat disesuaikan dengan kebutuhan pengguna Debian.

### Setting Repository
Untuk melakukan setting repository pada sistem operasi Linux Debian, berikut ini adalah langkah-langkahnya:
1. Buka terminal pada sistem operasi Linux Debian.
2. Ketikkan perintah berikut untuk mengedit file sources.list: \ sudo nano /etc/apt/sources.list \ 
File sources.list akan terbuka pada text editor nano. Pada file ini, akan terlihat daftar repository yang telah diatur pada sistem operasi Linux Debian. Anda dapat menambahkan repository baru pada file ini.

Untuk menambahkan repository baru, Anda dapat menambahkan baris berikut pada file sources.list:

css
Copy code
deb [repository-url] [distribution-name] [components]
[repository-url]: URL dari repository yang ingin ditambahkan
[distribution-name]: Nama distribusi Linux Debian yang digunakan (seperti "buster" untuk Debian 10)
[components]: Komponen dari repository yang ingin ditambahkan, seperti "main", "contrib", atau "non-free"
Sebagai contoh, jika Anda ingin menambahkan repository Debian Multimedia pada Debian 10, Anda dapat menambahkan baris berikut pada file sources.list:

javascript
Copy code
deb http://www.deb-multimedia.org buster main non-free
Setelah menambahkan baris tersebut, simpan perubahan dengan menekan tombol Ctrl + X, kemudian pilih Y untuk menyimpan perubahan.

Setelah selesai menambahkan repository baru, jalankan perintah berikut untuk memperbarui daftar paket pada sistem operasi Linux Debian:

sql
Copy code
sudo apt update
Perintah ini akan mengambil daftar paket terbaru dari semua repository yang telah diatur pada sistem operasi Linux Debian.

Dengan demikian, repository baru sudah diatur pada sistem operasi Linux Debian. Anda dapat menginstal paket atau software baru dari repository tersebut dengan menggunakan package manager seperti APT.

### Arti dari Repository
### Cari Instalasi Package
#### MC
#### Net-tools
#### Htop
