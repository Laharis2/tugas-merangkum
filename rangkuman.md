Nama : La Haris
NIM : 20.01.013.068
Tugas : Merangkum

# Pengenalaan django ([Play](https://youtu.be/Cj89fGNiMSk))

Django merupakan web framework yang membantu untuk membuat situs web yang bersifat mvt (Model,View, template)

# Alur Kerja Django ([Play](https://youtu.be/xN8sAeMPsEg))

Alur kerja django yaitu; client > urlconf > view > template

# Tools yang dibutuhkan ([Play](https://youtu.be/5OAN7FhO-lw))

Tools yang dibutuhkan dalam django; cmd/terminal, text editor (visual studio code,dll), web browser, python, django.

# Membuat project ([Play](https://youtu.be/pJxiLVaVvIg))

1. Kali ini kita akan menyimpan file aplikasinya di dektop komputer kita dengan nama perpus.
2. Buka cmd dan ketik "cd Desktop" Untuk menyimpan Project di Halaman Desktop
3. Ketik "Django-admin startproject perpus"Perintah ini untuk membuat Project baru Bernama Perpus
4. Didalam Folder Project Perpus terdapat :
   -Manage.py 
   -__init__.py
   - Setting.py
   - Urls.py
   - Wsgi.py
5. lalu ketik "Python manage.py runserver" Untuk menjalankan Project
6. Setelah itu akan muncu tampilannya dan cari kalimat yang berisi alamat seperti http://127.0.0.1/8000/ copy alamat tersebut lalu paste pada web browser.

# Mengenal Basic Routing ([Play](https://youtu.be/jvMQR9u3Rgg))

1. Basic routing merupakan alur kerja apps; Adapun cara kerjanya yaitu; client > urlconf > view > client
2. Client memberikan Request untuk mengakses Halaman yang diminta pada Server Django
3. Untuk dapat melayani Request dari Client, harus dibuatkan URL jika url belum ada maka akan muncul
   "PAGE NOT FOUND" Karena URL yang di Request/minta belum ada di Server.
4. ketika url sudah tersedia, maka akan muncul tampilan yang diinginkan.

# Membuat Apps ([Play](https://youtu.be/R-SZTFZQ8Sg))

1. Apps merupakan aplikasi
2. langkah awal membuat aplikasi yaitu; masuk pada file perpus yang telah kita buat menggunakan text editor,
3. cari file "setting.py" lalu cari bagian "installed_apps"
4. tambahkan nama aplikasi kita "perpustakaan"
5. pada file perpustakaan sudah otomatis berisi template yang dibutuhkan.

# Membuat Views ([Play](https://youtu.be/sPFigndffM8))

membuat view hampir sama dengan pembuatan view pada episode sebelumnya dengan alur kerja yang sama, namun pada pembuatan view kali ini akan di simpan pada folder perpustakaan difile view.py. intinya view ini akan menjadi tampilan yang diminta oleh client.

# Template ([Play](https://youtu.be/5UScV1i0MoM))

1. Pada tahap ini, Alur yang digunakan mulai berkembang. Dimulai dari Client, URLConf, View, dan Template.
2. untuk confignya kita buka file seting.py pada folder perpus,
3. Pada Line 58. 'DIRS' : ['template'] tambahkan
4. kemudian buat Folder templates setara dengan folder perpuss dan perpustakaan,
5. buat file buku.html pada folder templates lalu membuat html sederhana.

# django template language ([Play](https://youtu.be/amP6jUVhp2g))

1. Substitute variabel untuk menampilkan variabel ketemplate yang dilemparkan dari views
2. filter memodifikasi variabel yang akan di tampilkan
3. Tags untuk melakukan controlflow seperti looping (untuk mengambil file eksternal)

# Template Extending/memperluas template ([Play](https://youtu.be/fLOWCJYfGXQ))

1. kita akan membuat Base Template/Template dasar untuk semua Halaman.
2. Template utama yang isinya Base.html adalah file html utama yang akan menampung konten-konten dari Template Apps
3. Didalam Apps akan dibuat folder template yang isinya hanya bagian-bagian konten
4. Bagian Konten akan diextend/dimasukkan kedalam Base.html

# Static Fil ([Play](https://youtu.be/YnUOG6Oor04))

merupakan kumpulan File CSS, Java Script, dan gambar. Static File digunakan untuk mempercantik/memperindah tampilan Aplikasi yang dibuat dan memberikan kenyamanan saat Aplikasi dipakai.

# Setup Bootstrap ([Play](https://youtu.be/5JagJ4bQzBY))

1. Tahap ini kita akan memindahkan file-file CSS
   dan Java Script kedalam Folder static yang telah di Set Up.
2. jangan lupa Download Bootstrap dan JQuery yang akan digunakan.
3. selanjutnay kita pindahkan ke folder static
4. lalu kita panggil file-file tersebut di Base.html pada folder temlates

# Setup DataBase ([Play](https://youtu.be/VHe-SxvTPDk))

1. saat kita melakukan runserver django telah mengcreate sebuah file db.sqlite3
2. django secara default menggunakan Mysql dengan nama 'db.sqile3'. nama ini bisa kita ganti sesuai dengan keinginan kita seperti 'perpustakaan.sql'
3. lalu kita akan melakukan Migrasi dengan cara masuk pada cmd, lalu masuk di file kita "cd Desktop/perpus/" lalu ketik "python manage.py migrate" lalu enter
4. hal ini untuk menyebarkan/menginisialisasi tabel-tabel kedalam db.sqlite3.

# Setup Mysql ([Play](https://youtu.be/NE5oAwWPdVs))

1. kita akan melakukan Konfigurasi MySql sebagai DBMS untuk project Django yang akan kita buat.
2. pada Tahap ini bersifat Opsional,karena kita juga bisa menggunakan sqlite3 sebagai DBMS
3. Jika ingin menggunakan MySql sebagai DBMS, kita perlu menginstall MySql terlebih dahulu
4. setelah diinstall,lalu buka MySql Command Line dan create Database
5. lakukan Konfigurasi Database pada file settings.py

# Models ([Play](https://youtu.be/q7grGllxyxE))

merupakan definisi dari database. Dengan menggunakan models kita tidak perlu menggunakan Query SQL untuk membuat tabel di database.
Ketika melakukan Migrasi pada models buku, maka Django akan melakukan Create Tabel Buku secara otomatis sesuai dengan file-file yang ada pada model buku. Maka jadilah Tabel pada Database yaitu Tabel Buku.

# Models Foreign Key ([Play](https://youtu.be/Iv1VKt4RHmw))

1. Foreign Key digunakan untuk membuat Relasi antar tabel dalam database Relational.
2. Kelompok_id merupakan Foreign Key yang nanti nya akan diisi oleh id tabel kelompok

# Django Admin ([Play](https://youtu.be/7vNQESIkPf4))

merupakan salah satu fitur yang powerfull yang ada pada Django. Dikatakan Powerfull karena dapat melakukan CRUD sederhana untuk mengelola data pada model yang kita buat. Model-Model yang kita buat akan ditambahkan kedalam Django Admin. Django admin ini bersifat Private karena diperlukan Login terlebih dahulu untuk dapat mengakses nya. Django admin Sederhana namun sangat membantu. Pertanyaannya ada dua :

1.  Bagaimana cara kita log in django admin ini?
2.  Bagaimana model-model kita di daftarkan ke dalam django admin ini? Sebenarnya saat kita membuat projek ada URL yang sudah dibuatkan oleh djangonya yaitu admin, URL inilah untuk mengakses django admin, apabila ingin akses langsung /admin tampilannya langsung django admin log in. Lalu buat akun buka terminal buat username nya dengan nama admin, lalu email addres, dan password 2 kali. Jalankan kembali servernya jika sudah membuat akun. Akun tersebut di masukkan ke dalam log in. Apabila sudah masuk ke dalam akun selanjutnya kita menampilkan model yang sudah kita buat di dalam django admin. Lalu save, model-model yang kita sudah buat sudah masuk sudah terdaftar. Perpustakaan adalah nama X nya, Buku dan kelompok adalah model nya. Power fullnya terdapat di tombol add kalau di klik akan menampilkan ada sebuah form untuk menambahkan data dalam Buku, kita hanya membuat kelas model saja di datakan di dalam django admin. Mengisi judul,penulis,penerbit,jumlah,dan kelompok id dengan mengisi nama dan keterangan dan save. Ini udah termasuk ke database. Kita buka lagi di model kelompok yang sudah terdapat 3 kelompok seperti adaptif,normatif,dan produktif.

# django admin : Model Admin ([Play](https://youtu.be/V8hY2hzyJw4))

Pada tahap ini, kita akan melakukan custom sederhana terhadap tampilan data buku, fill-fill apa saja yang ditampilkan sebagai informasi seperti judul,penulis,penerbit dan lain-lain. Kita akan menampilkan kotak pencarian dan filter kelompok buku.

# ORM (Object Relational Mapping) ([Play](https://youtu.be/zoNk0dPikpg))

merupakan teknik yang digunakan dalam pemrograman untuk menggunakan basis data relasional sebagai penyimpanan data dengan bentuk objek. Perlu diketahui django menggunakan teknik ini untuk menggunakan database relasional. Kenapa? Agar kode python yang ditulis tidak campur aduk dengan query sql. Jadi, ORM ini bertugas sebagai penghubung aplikasi yang dibuat menggunakan database relasional.

# Model form ([Play](https://youtu.be/DXXneMxdGEU))

1. Form biasanya ditulis dengan HTML. Namun di Django tidak wajib menggunakan HTML, bisa saja menggunakan Models
2. Input Type harus disesuaikan dengan Type data pada tabel database.
3. Selanjutnya Membuat file baru di perpustakaan dengan nama form. Lalu membuat viewsnya untuk menghasilkan seperti gambar dibawah ini

# Form Widged ([Play](https://youtu.be/gHNEdANR4WQ))

1. Pada tahap ini, kita menambahkan atribut dengan menggunakan widged pada output yang telah dibuat sebelumnya.
2. Didalam forms.py ditambahkan widgets, text Input merupakan typenya.
3. Tambahkan atribut kelas didalamnya.

# CRUD (Menambah Data) ([Play](https://youtu.be/ZWELAOzJhUM))

1. Pada tahap ini, kita masuk ke dalam queryset. Disini kita menambah data, menampilkan, mengubah dan mengapus data Dari data yang sudah dibuat.
2. Selanjutnya kita akan menyimpannya ke dalam database. Prosesnya ada di views yang nantinya akan mengecek apakah data yang di submit oleh user sudah benar atau sudah valid.
3. Apabila sudah maka akan di simpan ke database.
4. Lalu buka text editor, buka file views. Fungsi dari csrf sendiri adalah untuk mngamankan form yang dibuat.

# CRUD (Menampilkan Data) ([Play](https://youtu.be/EYlFTIcnAXE))

1. Menampilkan data buku yang sudah dibuat, seperti menampilkan nilai 90/100 danmenampilkan kelompok seperti produktif maka hasilnya pasti error karena kelompok_id merupakan type integer.
2. Namun Apabila menambah \_\_nama, maka akan bisa mengeluarkan hasilnya.
3. Penggunaan queryset tidak sepanjang query. Untuk menampilkan limit pada queryset cukup ditambah diujungnya [:3], sedangkan dalam query limit 3.

# CRUD (Mengubah Data) ([Play](https://youtu.be/auZJ5GM5iTc))

1. Tahap Mengubah data ini perannya sangat penting karena saat kita salah dalam melakukan input data, maka kita harus mengubahnya atau mengeditnya dengan menggunakan fitur update atau fitur ubah data ini. Ini lebih efektif dibandingkan dengan hapus, lalu input ulang
2. Ubah data sebenarnya sama dengan form menambah data. Bedanya form ubah data sudah terisi oleh data yang ingin kita ubah, misalnya seperti ingin mengubah judul yang dari Bhs.Indonesia menjadi IPA, lalu klik simpan dan selesai.

# CRUD (Hapus Data) ([Play](https://youtu.be/EWLuwTeJjSA))

1. Hapus data juga penting dalam aplikasi, karena apabila data tersebut tidak lagi digunakan kita dapat menghapus nya. Karena Fungsi fitur ini sendiri adalah untuk menghapus data yang sudah tidak digunakan oleh user.
2. Sebelum menggunakan action/aksi hapus, terlebih dahulu membuat konfirmasi yang berisi apakah yakin ingin menghapus atau tidak untuk menghindari ketidaksengajaan user dalam menghapus data.

# Login / LogOut ([Play](https://youtu.be/3xyYrYXMB_8)/[Play](https://youtu.be/4SXPDNdTgV8))

merupakan proses verifikasi/validasi identitas user yang terdaftar sebelum mengakses system. Dengan ini kita jadi bisa membatasi user mana saja yang boleh manambah data, mengubah data, dan menghapus data. Jadi tidak sembarang user mengakses halaman-halaman tersebut . django ada system authentication yang akan kita gunakan yang bernama class LoginView untuk membuat namanya sama seperti membuat log in django admin. Berarti saat ingin membuat yang baru bisa mambuat di terminal.

# Sign Up ([Play](https://youtu.be/wStQuGwp5ZA))

Pada tahap ini kita akan membuat form sign up, agar user bisa login ke aplikasi perpustakaan yang dibuat. Tahap ini berhubungan dengan django admin karena di dalamnya terdapat username django adminnya. Jika lihat di dokumentasi resmi Django, ada sebuah user form yang bernama UserCreationForm untuk membuat user baru

# Upload & export File ([Play](https://youtu.be/BHUT6XGF4eE)/[Play](https://youtu.be/ICI6OXkr7Vk))

Pada tahap ini kita membuat tools upload file, seperti mengupload cover buku. Kita akan menambahkan file baru pada model buku yang bernama cover sehingga di dalam tambah buku nanti akan muncul yang baru seperti cover atau muncul di ubah buku. Di buku kita akan menambahkan kolom baru yaitu cover sebagai informasi buku yang kita masukkan.

Pada tahap ini akan membuat export file. Export file ini biasa digunakan untuk membuat report atau laporan ke dalam bentuk file excel, pdf, atau file lainnya. Dalam aplikasi biasanya terdapat fitur laporan yang harus di export data yang terdapat dalam database ke dalam file excel contohnya. Cara menggunakan export ini bisa menggunakan django-importexport.

# Virtual Environment ([Play](https://youtu.be/qGPSGuTqajo))

Pada tahap ini akan membahas tentang virtual environment atau lingkungan virtual, dalam kasus ini lingkungan virtual berguna untuk mengisolasi projek yang kita buat. Setiap kita membuat projek didalam lingkungan virtual ini, projek tersebut akan terisolasi dari direktori system dan memiliki paket python sendiri yang terinstal di lingkugan virtual tersebut. Lingkungan system operasi lebih besar yang didalam nya sudah ada django versi 2.2.12,pillow versi 7.1.2, dan django-import-export versi 2.2.0. kita juga sudah membuat aplikasi perspustakaan di lingkungan system tersebut dengan menggunakan django versi 2.2.12. apabila kita membuat projek di dalam lingkungan virtual environment 1 dan virtual environment 2. Di dalam virtual env 1 terdapat aplikasi perpustakaan yang dibangun dengan django 1.11 sedangkan di dalam virtual env 2 terdapat juga aplikasi yang dibangun dengan django 3.0.8 mysqlclient.

# Persiapan deployment ([Play](https://youtu.be/VZGwILOsVxU))

Deployment adalah kegiatann untuk menyebarkan aplikasi yang telah dikerjakan oleh developer (pengembang). Artinya kita mempublish projekk atau aplikasi yang kita buat untuk dilihat oleh ornang lain. Kita juga melewati siklus pembuatan aplikasi yaitu :
a. Development : mengerjakan projek aplikasi kita atau proses pembuatan, pengembangan . kita di awal-awal akan membuat form,model,view,tampilan itu adalah tahapan development atau pengembangan.
b. Testing : setelah dilakukan pembuatan otomatis kita akan melakukan uji coba agar mengetahui kekurangan dari kegiatan tersebut. Mengecek apakah sudah sesuai atau apakah ada bug. Testing ini juga dilakukan saat production.
c. Production : aplikasi kita yang sudah di buat sudah di deploy / sudah bisa di publish / sudah bisa digunakan oleh orang lain. Bisa juga user melakukan testing pada saat tahap ini.
Alur kerja nya dari client yang melakukan request langsung ditangani oleh web server lalu ke wsgi lalu terakhir ke django atau perputaran yang sudah kita buat yaitu aplikasi perpustakaan tersebut.
Yang perlu disiapkan adalah app (github,writelab,perpus), terminal, server, domain

# Deployment ([Play](https://youtu.be/Gz038-K6Jvk))

Pada tahap ini, kita akan mendeploymen aplikasi yang telah dibuat ke server. Dengan awalan mengcoding di local lalu mengupload ke github lalu di clon atau ditarik ke computer server untuk dideploy disana.
Saat aplikasi kita dalam mode production disetting dan debug masih nilainya masih dalam true jadi kalau misalkan salah menuju ke halaman pasti akan eror . Saat kita dalam mode production kita tidak boleh dibiasakan mengubah tampilan saat mode dalam production, apabila terjadi eror akan berakibat fatal maka itu kalau kita ingin mengambangkan aplikasi yang dalam production kita hanya perlu mengembangkannya di local dan kita masuk ke tahap development atau tahap pengembangan lagi seperti mengubah tampilan atau menambah fitur yang diinginkan.
