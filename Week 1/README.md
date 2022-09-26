# Writing and Presentation Test Week 1
## Day 1 : Apa itu CLI ?
### Unix Command Line 
  - **Shell** adalah sebuah program utama untuk berinteraksi dengan Sistem Operasi.
  - **Command Line Interface** adalah tampilan sebuah terminal yang digunakan untuk menjalankan program, mengelola file, dan berinteraksi dengan komputer. 
    - SH 
    - Bash
    - Zsh
    - CMD
  - Cara membuka CLI 
    -  Buka menu pada Windows Logo 
    -  Ketik “Command Prompt” 
    -  Pilih Command Prompt.
### Navigasi Menggunakan CLI
  - File System berfungsi untuk mengatur bagaimana data disimpan didalam sebuah sistem
    - pwd digunakan untuk melihat current working direktori
    - ls digunakan untuk melihat isi file yang ada pada sebuah direktori
    - cd <direktori> digunakan untuk berpindah direktori
### Manupulasi File dan Directory
  - head untuk melihat isi awal file
  - tail untuk melihat isi akhir file
  - cat untuk melihat isi keseluruhan file
  - touch berfungsi untuk membuat sebuah file
  - mkdir berfungsi untuk membuat suatu direktori
  - cp digunakan untuk menyalin file dan cp -R direktori
  - mv digunakan untuk memindahkan suatu file atau direktori, bisa juga
  digunakan untuk rename
  - rm digunakan untuk menghapus suatu file atau direktori
  
### Git & Github
  - GIT berfungsi untuk dapat mengatur versi dari source code program dengan memberikan tanda baris serta code mana yang perlu untuk ditambah atau diganti
  - GIT hanya alat version control
  - sedangkan Github merupakan alat version control dan penyimpanan cloud
#### Konfigurasi GIT
       $ git config --global user.name "Reza Saputra"
       $ git config --global user.email reza@gmail.com
       $ git config --list (untuk memeriksa konfigurasi)
#### Membuat Repository
  ##### git init
      $ git init .
  >  **"git init ."** digunakan untuk membuat repository di file lokal
  ##### git status   
      $ git status 
  >  **"git status"** digunakan untuk mengetahui sebuah status dari sebuah repository lokal
  ##### git add
      $ git add index.html
      $ git add .
  > - **"git add index.html"** digunakan untuk menambahkan file baru pada repository yang dipilih
  > - **"git add ."** digunakan untuk menambahkan semua file yang ada di direktori pada repository yang dipilih
  ##### git commit
      $ git commit -m "first commit"
  >  **"git commit"** untuk menyimpan perubahan yang dilakukan, tetapi tidak ada perubahan pada remote repository
  ##### git branch
      $ git branch -m main
  >  **"git branch"** untuk menggunakan branch main di repository
  ##### git remote
      $ git remote add origin https://github.com/username/testing.git
  >  **"git remote"** untuk menghubungkan remote repository dengan project lokal yang telah kita buat direktorinya
  ##### git push
      $ git push -u origin main
  >  **"git push"** untuk mengirimkan perubahan file setelah di commit ke remote repository
  - **git checkout** untuk menukar branch yang aktif dengan branchyang dipilih
  - **git clone** untuk membuat salinan repository lokal
  - **git log** untuk melihat catatan log perubahan pada respositori
  - **git pull** mengambil commit terbaru lalu otomatis menggabungkan (merge) dengan branch yang aktif
  
  ## Day 2 : HTML
  - HTML adalah singkatan dari Hypertext Markup Language
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
    <title>Website Reza</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>Ini adalah website saya</p>
    <ul>
      <li>Instagram</li>
      <li>Facebook</li>
      <li>Twitter</li>
    </ul>
  </body>
</html>

```
  > - Code diatas terdiri dari Opening dan Closing tag
  > - Contoh : Opening Tag ``<h1>`` dan Closing Tag ``</h1>``
 - HTML Attributes : properties dari sebuah element HTML
  > Contohnya yaitu : id,class,name
 - HTML Single Tag
   > Contoh : ``</br>``
 - HTML Double 
   > Contoh : ``<p>``  ``</p>``
 - HTML Comment digunakan untuk memberikan informasi tambahan pada kode HTML dan kadang juga digunakan untuk menon-aktifkan beberapa kode HTML
   > ``<!-- -->``
 - Membuat Table
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
  
## DAY 3 : CSS
  - CSS dapat digunakan untuk mengubah warna, menggunakan font custom, editing text format, mengatur tata letak, dan lainnya
  - Ada 3 cara untuk menambahkan CSS ke dalam dokumen HTML : 
  > - Inline – menggunakan atribut style dalam elemen HTML
  > - Internal – menggunakan elemen ``<style>`` di dalam elemen ``<head>``
  > - Eksternal – menggunakan elemen ``<link>`` di dalam elemen ``<head>``, ex ``<link rel="stylesheet" type="text/css" href="style.css">``
  - CSS Tag Name 
  ```
  h1 {
       color: green;
     }
  ```
  > Jika menggunakan Tag Element, maka ini bersifat global, Global artinya akan mempengaruhi seluruh Tag Elemen HTML yang ada pada file tersebut
  
  - CSS Class Name
  ```
  .title {
           color: green;
         }
  ```
  > Atribut class berfungsi untuk menentukan nama class dari suatu elemen
  - Nested Element yaitu setiap element yang terdiri atas parent dan child
  - !important CSS yaitu styling CSS yang memiliki tingkat paling atas dari ID dan Class
  
  ### Flexbox
  - Flexbox atau Flexible Box  merupakan sebuah mode pengaturan atau konsep layout pada CSS yang digunakan untuk mengatur elemen atau container beserta item didalamnya pada halaman web
  - Flexbox memiliki kemampuan untuk menyesuaikan layout secara otomatis.
  - Flexbox memiliki 1 parent/container dan bisa beberapa child/item.
  - **flex-direction** digunakan untuk mengatur letak item child. 
  - **flex-wrap**  secara default akan membuat tata letak item children dalam 1 line saja. flex akan menyesuaikan space yang ada.
  - **flex-flow** digunakan sebagai shortcut untuk set up flex-direction dan flex-wrap bersamaan.
  - **order** yaitu berfungsi untuk ordering item mana yang ingin kita atur posisinya berdasarkan urutan order.
  - **align** content digunakan untuk mengatur tata letak antar item child secara vertikal atau cross axis.
  - **flex-grow** digunakan untuk mengatur size suatu item child pada flexbox.
  - **flex-shrink** digunakan untuk memperkecil size suatu item child secara relatif terhadap item child lainnya.
  - **flex-basis** digunakan untuk mengatur width setiap item child.
  
  ## Day 4 : Algoritma dan Data Struktur
  ### Algortima
  - Algoritma adalah sederetan langkah-langkah logis yang disusun secara sistematis untuk memecahkan suatu masalah.
  
  - Manfaat Algoritma
    - Membantu menyederhanakan suatu program yang rumit dan juga besar.
    - Mempermudah pembuatan program yang dapat menyelesaikan masalah tertentu.
  
  - Ciri - ciri Algortima
    - Input "Memiliki 0 atau lebih inputan"
    - Output "Memiliki 1 buah Output"
    - Definiteness "Intruksi jelas, tidak ambigu"
    - Finiteness "Memiliki titik berhenti"
    - Effectiveness  "Sebisa mungkin tepat sasaran"
  
  - Cara penyajian Algoritma ada 3 :
    - Deskriptif
    > Penulisan algoritma dengan cara deskriptif seperti kita menulis tutorial (tata cara) dengan bahasa sehari-hari
    - Flow Chart
    > Flow chart atau diagram alir, penyajian algoritmanya lebih mudah dibaca karena memiliki tampilan visual.
    - Pseudo Code
    > Penulisan algoritma yg hampir menyerupai penulisan pada kode pemrograman disebut dengan pseudo code.
  
  - Contoh Algoritma sederhana menggunakan javascript
  
   ```
  var nama = "Reza";
console.log("Nama Saya :" + nama);
  
  Output : 
  Nama Saya :Reza
  ```
  - Pseudocode adalah menuliskan algoritma dengan umumnya bahasa inggris sebelum kita implementasikan ke bahasa pemograman tertentu.
  - Procedural adalah cara berpikir secara runtun. Artinya serangkaian perintah yang berurutan.
  - Conditional digunakan saat dibutuhkan percabangan kasus. Komputer akan melakukan suatu tindakan jika suatu kondisi terpenuhi. 
  - Komputer dapat melakukan sebuah proses yang sama berulang-ulang.
  - Big O Notation adalah sebuah cara atau metode untuk melakukan analisa terhadap sebuah algoritma pemrograman terhadap waktu eksekusi.
  - Contoh Struktur Data menggunakan Javascript
  ```
  let buah = {
    nama: 'apel',
    warna: ['merah', 'hijau'],
}
 console.log(buah)
  
  Output : 
  { nama: 'apel', warna: [ 'merah', 'hijau' ] }
  ```
## Day 5 : JS Dasar Conditional & Looping
  - Looping adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi stop/berhenti tercapai.
  ```
  for(let i = 0; i < 100; i++){
  console.log(i)
}
  ```
                         
  > - Hitungan akan dimulai dari ``0 (i = 0);``
  > - Hitungannya sampai berapa? Sampai ``i < 10;``
  > - Lalu di setiap perulangan ``i`` akan bertambah ``+1 (i++).``
  ```
  for(counter = 0; counter < 10; counter+=2){
    console.log(counter);
}
  ```
  > Melakukan perulangan menggunakan For Loop dimulai dari nol ``0``, Lalu di setiap perulangan nilai variabel couter akan ditambah ``2``  ``(counter+=2)``.
  ```
  let x = 1;
 
while( x <=10 ) {
 console.log(x);
 x++;
}
  ```
  > While Loop akan melakukan perulangan kalau kondisi (syarat) terpenuhi.
  
  ```
  let x = 1;
 
do
{
 console.log(x);
 x++;
}
while (x <= 7);
  ```
  > Do While melakukan perulangan dulu, kemudian memeriksa kondisinya atau sayaratnya.
  
  - Nested Loop yaitu jika kita membuat looping didalam looping.
