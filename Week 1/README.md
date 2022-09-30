# Writing and Presentation Test Week 1

## Day 1 : Unix CommandLine

### CLI / CommandLine Interface
  - CLI adalah sebuah program dimana user dapat mengetikan sebuah perintah dalam bentuk teks untuk memberikan intruksi pada komputer untuk melakukan tugas tertentu.
  
### Shell
  - Merupakan *User Interface* yang mengelola sebuah perintah yang diketik di CLI.
  - Shell membaca dan mengartikan sebuah perintah yang diberikan oleh user.
  - Lalu mengintruksikan sistem operasi untuk menjalankan task sesuai perintah.
    
  - Fungsi Shell
    - Menangani File dan Direktori.
    - Membuka dan menutup program.
    - Mengelola proses komputer.
    - Menjalan task berulang.

  - Contoh dari Shell yaitu WindowsShell atau CMD *Command Prompt* 

### File System
  - Sebuah proses yang mengatur dimana dan bagaimana sebuah data disimpan dan diakses dalam *Disk Penyimpanan*.
  - Mengatur pengoperasian didalam sebuah *disk* yang terhubung ke komputer.
  - Prosesnya tidak bisa dilihat oleh user yang menggunakan komputer tersebut.

### Command / Perintah
  - ``pwd`` digunakan untuk melihat current working direktori.
  - ``ls`` digunakan untuk melihat isi file yang ada pada sebuah direktori.
  - ``cd`` <direktori> digunakan untuk berpindah direktori.
  - ``head`` melihat isi awal file.
  - ``tail`` melihat isi akhir file.
  - ``cat`` melihat isi keseluruhan file.
  - ``touch`` membuat file baru.
  - ``mkdir`` membuat direktori baru.
  - ``cp`` mengcopy File, ``cp -R`` mengcopy direktori
  - ``mv`` memindahkan file/direktori, bia juga untuk mengganti nama file/direktori.
  - ``rm`` menghapus file, ``rm -R`` menghapus direktori
  
### Git & Github
  - *GIT* sebuah version control yang berfungsi sebagai control system untuk menjalankan proyek pengembangan software.
  - *Github* sebuah platform atau layanan web host yang memungkinkan tim developer untuk bekerja bersama secara online, di github juga kita bisa menyimpan code yang kita buat secara cloud.

### Penggunaan GIT
  - ``$ git config --global user.name`` untuk melakukan konfigurasi username.
  - ``$ git config --global user.email`` untuk melakukan konfigurasi email.
  - ``$ git config --list`` untuk memastikan proses login berhasil.
  - ``$ git init`` digunakan untuk membuat repository di file lokal.
  - ``$ git status`` digunakan untuk mengetahui sebuah status dari sebuah repository.
  - ``$ git add`` menambahkan file baru pada repository yang dipilih.
  - ``$ git commit -m "first commit"`` untuk menyimpan perubahan yang dilakukan, tetapi tidak ada perubahan pada remote repository
  - ``$ git branch -m main`` untuk menggunakan branch main di repository
  - ``$ git remote add origin`` untuk menghubungkan remote repository dengan project lokal yang telah kita buat direktorinya
  - ``$ git push -u origin main`` untuk mengirimkan perubahan file setelah di commit ke remote repository
  - ``git checkout`` untuk menukar branch yang aktif dengan branchyang dipilih
  - ``git clone`` untuk membuat salinan repository lokal
  - ``git log`` untuk melihat catatan log perubahan pada respositori
  - ``git pull`` mengambil commit terbaru lalu otomatis menggabungkan (merge) dengan branch yang aktif
  
### Membuat Repository di Github
  - Login atau Register ke https://github.com/
  - Create New Repository
  - Isikan seperti nama Repository dan Deskripsi lalu Create Repository
  - Repository berhasil dibuat!

## Day 2 : HTML Dasar
### HTML : Hypertext Markup Language
  - HTML berfungsi untuk menampilkan konten pada browser
  - Tools yang digunakan untuk membuat HTML
    - Browser (Chrome)
    - Code Editor (Visual Studio Code)
  - HTML Structure

  ``` 
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>_</title>
  </head>
  <body></body>
</html>
```
  > Dokumen HTML harus memiliki struktur dasar yang terdiri dari 4 bagian utama yaitu: tag ``<!DOCTYPE>``, tag ``<html>``, tag ``<head>``, dan tag ``<body>``. Keempat bagian tersebut adalah syarat minimal yang menjadi standar pada struktur global dokumen HTML
  
  - Tag dasar pada HTML : 
    - Single Tag
      > Contoh : ``<br />``
    - Double Tag
      > Contoh : ``<p>``  ``</p>``
    - Comment Tag 
      > - digunakan untuk memberikan informasi tambahan pada kode HTML dan kadang juga digunakan untuk menon-aktifkan beberapa kode HTML
      > - ``<!-- -->``

  - Contoh membuat tabel menggunakan *HTML*
 ``` 
<table border="1">
        <thead>
            <tr>
                <td>Nama</td>
                <td>Umur</td>
                <td>Jurusan</td>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Reza Saputra</td>
                <td>21 Tahun</td>
                <td>Sistem Informasi</td></tf>
            </tr>
        </tbody>
    </table>
</html>
```

  - Output
  <table border="1">
        <thead>
            <tr>
                <td>Nama</td>
                <td>Umur</td>
                <td>Jurusan</td>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Reza Saputra</td>
                <td>21 Tahun</td>
                <td>Sistem Informasi</td></tf>
            </tr>
        </tbody>
    </table>
 
  > - ``<thead>`` digunakan untuk membungkus konten bagian judul atau kepala tabel
  > - ``<tr>`` berfungsi untuk membuat baris pada tabel
  > - ``<td>`` digunakan untuk membuat kolom atau sel di setiap baris pada tabel
  > - ``<tbody>`` digunakan untuk membungkus konten bagian isi atau tubuh dari tabel
  
  - **Semantic Tag**
    > - Semantic Tag atau Semantic Markup, adalah sebutan untuk tag-tag HTML yang memiliki 'arti' atau 'makna'.
       > - Contoh : ``<nav>Ini Adalah Navbar</nav>``
  - HTML Attributes : properties dari sebuah element HTML
    > Contohnya yaitu : id,class,name | ``<div id="nama">``

## DAY 3 : CSS

### CSS : Cascading Style Sheet
  - CSS dapat digunakan untuk mengubah warna, menggunakan font custom, editing text format, mengatur tata letak, dan lainnya
  - Ada 3 cara untuk menambahkan CSS ke dalam dokumen HTML : 
  > - Inline – menggunakan atribut style dalam elemen HTML ``<h1 style="background-color: aqua">Hai.. I'm <span>Reza</span></h1>``
  > - Internal – menggunakan elemen ``<style>`` di dalam elemen ``<head>``
  ```
  <head>
  <style type="text/css">
    p {color:white; font-size: 10px;}
    .center {display: block; margin: 0 auto;}
    #button-go, #button-back {border: solid 1px black;}
  </style>
</head>
  ```
  > - Eksternal – menggunakan elemen ``<link>`` di dalam elemen ``<head>``, ex ``<link rel="stylesheet" type="text/css" href="style.css">``
### Sintaks Dasar CSS 
  ```
  h1 {
    color: red;
}
  ```
  > - ``Selector`` untuk memilih elemen HTML yang akan kita beri style.

  ```
  properti: "nilai";
  ```
  > - ``Property`` yaitu aturan yang akan diberikan kepada elemen yang dipilih.

  ```
  h1{ 
   background-color: green
} 
  ```
  > - ``Declaration Block`` tempat kita menuliskan atribut atau properti CSS yang akan diberikan ke pada elemen yang telah diseleksi.
  
### Flexbox
  - Flexbox digunakan untuk mengatur jarak antar item pada sebuah container.
  > - ``flex-direction`` : digunakan untuk mengatur arah item didalam container.
  > - ``flex-wrap`` : memungkinkan kita memindahkan item ke baris bawah, apabila baris atas tidak cukup.
  > - ``justyfy-content`` : untuk mengatur rata dari sebuah elemen, seperti rata kiri atau kanan.
  > - ``align-items`` : untuk mengatur kesejajaran item secara vertikal.
  > - ``align-content`` : untuk mengatur jarak antar item terhadap cross-axis.
  > - ``order`` : untuk mengatur urutan dari items.
  > - ``flex-grow`` : untuk mengatur ukuran dari items.
  > - ``align-self`` : untuk mengatur urutan item yang dipilih secara spesifik.

## Day 4 : Algoritma dan Data Struktur | Intro to Javascript

### Algortima
  - Algoritma adalah sederetan langkah-langkah logis yang disusun secara sistematis untuk memecahkan suatu masalah.
  - Manfaat Algoritma
    - Membantu menyederhanakan suatu program yang rumit dan juga besar.
    - Mempermudah pembuatan program yang dapat menyelesaikan masalah tertentu.
  
  - Jenis - jenis Algoritma :
    - **Deskriptif** : Seperti kita menulis tutorial (tata cara) dengan bahasa sehari-hari
    - **Flow Chart** : Metode *Flow Chart* lebih mudah dibaca karena menggunakan gambar visual.
    - **Pseudo Code** :  Penulisan metode ini hampir sama seperti kode pemrograman.
  
  - Contoh Algoritma *Pseudo Code* sederhana menggunakan javascript
  
   ```
  const nama = "Reza";
console.log("Nama Saya " + nama);
  
  Output : 
  Nama Saya Reza
  ```
### Javascript 
  > Javacript adalah bahasa pemograman yang sangat powerful yang digunakan untuk logic pada sebuah website.
  - Syntax dan Statement
     - Syntax bisa dianalogikan seperti kosa kata (vocabulary) dan tata cara (grammar) pada bahasa pemograman.
     - Kita menggunakan syntax tertentu untuk membuat statement program, instruksi untuk djalankan/dieksekusi oleh web browser, compiler, ataupun intrepreter
  - Console log adalah tempat kita untuk cek logic pemograman web yang kita kembangkan.
  - Tipe data adalah klasifikasi yang kita berikan untuk berbagai macam data yang digunakan dalam programming.
    - number 
      > "Tipe data number adalah tipe data yang mengandung semua angka termasuk angka desimal."
    - string 
      > "Tipe data string adalah grup karakter yang ada pada keyboard laptop/PC kita yaitu letters (huruf), number (angka), spaces (spasi), symbol, dan lainnya."
    - boolean 
      > "Tipe data boolean adalah tipe data yang hanya mempunyai 2 buah nilai."
    - null 
      > "Tipe data null adalah tipe data yang diartikan bahwa sebuah variable/data tidak memiliki nilai."
    - undefined 
      > "Tipe data undefined adalah tipe data yang merepresentasikan varibel/data yang tidak memiliki nilai."
    - object 
      > "Tipe data object adalah koleksi data yang saling berhubungan (related). Tipe data pbject dapat menyimpan data dengan tipe data apapun (number, string, boolean, dan lainnya)."
  
### Variable 
  > Variable adalah tempat untuk menyimpan sebuah nilai.
  - Ada 3 cara mendefinisikan sebuah variabel.
    > - var
    > - let
    > - const
    
### Operator
  > Operator yaitu sebuah intruksi yang digunakan untuk melakukan suatu proses
  - Operator Artimatika

| Operator | Deskripsi      |
| ----------- | :---------: | 
| +  | Penjumlahan          | 
| -  | Pengurangan          | 
| *  | Perkalian            |
| /  | Pembagian            | 
| %  | Modulus              | 
| ++ | Increment            |
| -- | Decrement            |

  - Operator Perbandingan

| Operator | Deskripsi                    |
| ----------- | :---------:               | 
| ==  | Equal                             | 
| !=  | Non Equal                         | 
| === | Identical                         |
| !== | Not Identical                     | 
| >   | Lebih Besar                       | 
| <   | Lebih Kecil                       |
| >=  | Lebih besar sama dengan           |
| <=  | Lebih kecil sama dengan           |

  - Operator Logika

| Operator | Deskripsi                    |
| ----------- | :---------:               | 
| && | and  | 
| I I | or   | 
| !  | not  |
  
## Day 5 : JS Dasar Conditional & Looping
### Conditional
  - Conditional merupakan statement percabangan yang menggambarkan suatu kondisi.
   > - Conditional statement akan mengecek kondisi spesifik dan menjalankan perintah berdasarkan kondisi tersebut
   > - Yang dicek adalah apakah kondisi tersebut TRUE (benar). Jika TRUE maka code didalam kondisi tersebut dijalankan.

  ```
let haus = true;
if (haus) {
    console.log(haus);
}
```
  > Contoh IF Statement
  
   ```
let ngantuk = false;
if (ngantuk) {
  console.log("Ayo Tidur");
} else {
  console.log("Tidak Tidur");
}
```
  > IF ELSE : mengeksekusi sebuah statement/code jika suatu kondisi bernilai FALSE
  
  ```
let lampuJalan = "kuning";

if (lampuJalan === "merah") {
  console.log("berhenti!");
} else if (lampuJalan === "kuning") {
  console.log("pelan pelan");
} else if (lampuJalan === "hijau") {
  console.log("jalan");
} else {
  console.log("Tidak diketahui");
}
  ```
  > Else … If statement dapat kita gunakan jika kita mempunyai berbagai kondisi.


### Looping
  - Looping adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi stop/berhenti tercapai.
  ```
for (let i = 0; i < 100; i++) {
  console.log(i);
}


  ```
                         
  > - Hitungan akan dimulai dari ``0 (i = 0);``
  > - Hitungannya sampai berapa? Sampai ``i < 100;``
  > - Lalu di setiap perulangan ``i`` akan bertambah ``+1 (i++).``
