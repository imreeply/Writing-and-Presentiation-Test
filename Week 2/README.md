# Writing and Presentation Test Week 2

## DAY 1 : Javascript Dasar
### Scope
 - Scope adalah konsep dalam flow data variable.
 - Scope dapat mengatur sampai batas mana suatu variable masih dapat dilihat atau maasih dapat digunakan.
 
 ### Global Scope
  - Variabel global dapat diakses dan dimodifikasi hampir dimana saja di dalam kode program yang kita buat. 
  
  ```
 let namaSaya = "Reza";

function greeting() {
    return namaSaya;
}

console.log(namaSaya);
  ```
  > Contoh Global Scope
  
 ### Local Scope
  - Variabel yang dideklarasikan dalam local scope hanya bisa di akses dalam scope tersebut dan tidak dapat diakses secara global atau local scope yang lain.
  
  
### Function
 - Function adalah fasilitas untuk membuat suatu program yang dapat kita gunakan berulang ulang tanpa ada batasan selama halaman masih terhubung dengan function tersebut.
 - Kenapa harus membuat function
   - Reusability atau penggunaan kembali dari kode yang sudah kita buat.
   - Untuk menyembunyikan kompleksitas dari prorgram yang kita buat.
   - Dengan adanya function kita dapat dengan mudah mencari letak kesalahan program.
   
 ### Parameter dan Argument
  - Parameter
    - Parameter adalah variabel yang di tulis didalam kurung pada saat function dibuat.
    - Parameter digunakan untuk menampung nilai yang dikirimkan saat function dipanggil
  - Argument
    - Nilai yang dikirimkan ke parameter saat fungsi dipanggil
 ```
 function tambah(a, b) {
  return a + b; // Parameter
}
console.log(tambah(2, 3)); // Argument
 ```
  > Contoh Penggunaan Parameter & Argument
  - Arrow Function
    - Cara lain penulisan dengan menggunakan arrow(panah) "=>" tanpa menggunakan kata kunci "function" dalam syntax.
  ```
let tampilPesan = (nama) => {
  console.log("Halo" + nama);
};
tampilPesan("Reza");
  ```
  > Contoh Penggunaan Arrow Function
  
## DAY 2 : Data Type Built in Prototype & Method
## Tipe Data
  - Tipe data yaitu berfungsi untuk membedakan tipe nilai satu dengan yang lainnya
  - Tipe Data Primitive
    
    - String : Berguna untuk menyimpan data yang dapat direpresentasikan dalam bentuk teks.
 ```
const x = "Ini adalah string";
const y = "Ini adalah string dengan kutip tunggal";
 ```
    - Number : 
 
