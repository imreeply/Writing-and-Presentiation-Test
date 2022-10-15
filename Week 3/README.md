# Writing and Presentation Test Week 3

## DAY 1 : Array

- Array adalah tipe data yang digunakan untuk mendeskripsikan kumpulan elemen (nilai/variable) yang tiap tiap elemennya memiliki index
- Contoh Array

```
let hari = ['senin','selasa',rabu']
```

> Cara menulis array menggunakan kurung siku [], dengan array kita dapat menampung lebih dari 1 nilai

- Kenapa Array ?
  - Key adalah index pada array dengan tipe integer yang dimulai dari 0
  - Array pada javscript bertipe Object
  - Array memiliki fungsi / method lenght untuk menghitung jumlah elemen didalamnya
  - Array boleh memiliki tipe data yang berbeda
- Cara memanggil nilai pada Array

```
let angka = ['satu','dua','tiga'];
```

- Satu adalah index 0, dua index 1, dan tiga index 2
- Memanggil dua `console.log(angka[1]`
- Menghitung jumlah nilai pada array `console.log(angka.lenght);`

### Manipulasi Array dengan Method

- .pop()

```
let buah = ["pisang", "anggur", "apel"];
buah.pop();

console.log(buah);
```

> Menghapus index terakhir pada array

- .push()

```
let buah = ["pisang", "anggur", "apel"];
buah.push("mangga");

console.log(buah);
```

> Menambah index terakhir pada array

- shift()

```
let buah = ["pisang", "anggur", "apel"];
buah.shift();

console.log(buah);

```

- .unshift()
  > Untuk menghapus index pertama pada array

```
let buah = ["pisang", "anggur", "apel"];
buah.unshift("mangga");

console.log(buah);

```

> Untuk menambahkan index pertama pada array

- .sort()

```
let buah = ["pisang", "anggur", "apel"];
buah.sort();

console.log(buah);

```

> Method untuk mengurutkan secara Ascending atau Descending Alphanumeric

### Array Looping

- foreach()
  > foreach digunakan jika tidak ingin memanipulsai data asli atau keluaran dari array tersebut.
- .map()
  > Gunakan .map() untuk membuat array baru yang diisi dengan hasil panggilan fungsi yang disediakan pada setiap elemen kembali pada array.

### Array Multidimensional

> Array Multidimensi adalah sebuah Array yang memiliki lebih dari satu subskrip atau Array didalam Array

```
let mobil = [["Avanza"], ["Volvo"]];
console.log(mobil);
```

- Method Built-in Array
  > Sama seperti Array satu dimensi, multidimensional array juga dapat menggunakan property dan Method built-in array

```
let mobil = [["Avanza"], ["Volvo"]];

mobil.push(["Tesla"]);

```

## DAY 2 : Javascript Object

### Object

> Object adalah kumpulan nilai berupa nama

- Cara membuat sebuah Object
  > Obeject dapat diassign kedalam sebuah variable

```
let mahasiswa = {
  name: "Reza",
  age: 21,
};
```

- Mengakses Object

```
let mahasiswa = {
  name: "Reza",
  age: 21,
};

console.log(mahasiswa);
```

- Mengakses Property Object

```
let mahasiswa = {
  name: "Reza",
  age: 21,
};

console.log(mahasiswa.age);
```

- Mengupdate Object

```
let mahasiswa = {
  name: "Reza",
  age: 21,
};

mahasiswa.age = 25;

mahasiswa.address = "Pontianak";

console.log(mahasiswa);
```

- Menghapus Property Object

```
let mahasiswa = {
  name: "Reza",
  age: 21,
  address: "Pontianak",
};

delete mahasiswa.address;

console.log(mahasiswa);
```

### Method

> Jika value yang kita masukkan pada property berupa function maka disebut method

```
const greeting = {
    welcome: function() {
        return 'Halo Selamat Datang';
    },
    afterTransaction: function() {
        return 'Terima Kasih Sudah Berbelanja'
    },
};

console.log(greeting.welcome());
```

### Looping Object

 - For In

  ```
  let mahasiswa = {
    nama: "Reza",
    umur: 22,
  };

  console.log(siswa);

  for (let i in mahasiswa) {
    console.log(siswa[i]);
  }
  ```

 - For of

  ```
  let mahasiswa = {
    nama: "Reza",
    umur: 22,
  };
  for (let i of Object.keys(mahasiswa)) {
    console.log(i)
  }
  ```

 - map

  ```
  let mahasiswa = {
  nama: "Reza",
  umur: 22,
  };
  let mahasiswa2 = Object.keys(mahasiswa).map((i) => {
  return i;
  });
  console.log(mahasiswa2);

  ```

## DAY 3 : Javascript Recursive

> Recursive adalah function yang memanggil dirinya sendiri hingga kondisi tertentu

- Struktur Recursive

```
function recursive() {
    recursive();
}
```

```
function recursive() {
    if(condition)
} else {
    recursive();
}
```

> Recursive akan berhenti memanggil dirinya jika kondisi terpenuhi

### JS Modules

> Dengan JS Modules memungkinkan memisahkan kode menjadi file yang berbeda, Keuntungan dari modules yaitu mudah untuk mengelola kode serta kode tidak menumpuk di dalam satu file.

```
 // file 1.js
let person = {
    firstName: 'Reza',
    lastName: 'Saputra',
  };

  function getFirstName() {
    return person.firstName;
  }
```

```
// file 2.js
console.log(getFirstName());

```

> Saat kita menyematkan kode `<script src="./file-1.js"></script>`, kita harus memastikan bahwa kita tidak menambahkan atribut async karena akan membuat urutan muat menjadi tidak bisa diprediksi. Sementara pada kasus kode di atas, file-1.js haru dimuat terlebih dahulu sebelum kita bisa menggunakan di file-2.js.

## DAY 4 : Asynchronous

### Asynchronous Introduction

- Asynchronous
  > Kode yang dieksekusi tanpa menunggu urutan dinamakan Asynchronous, Sebuah kode yang dijalankan secara Asynchronous akan membiarkan kode di bawahnya juga berjalan sehingga kode bisa berjalan bersamaan.
- Synchronous
  > Kode yang dieksekusi secara berurutan dinamakan dengan Synchronous code execution. Pada contoh pada artikel sebelumnya kita menggunakan Synchronous.
- Callback
  > function yg dijadikan sebagai argumen Ketika sesuatu memerlukan waktu yang lama, maka dia akan masuk kedalam callback queue lalu menjalankan proses yang berada di belakangnya. Jika proses yg belakang sudah selesai, maka engine akan memeriksa yang ada didalam callback queue untuk dijalankan.

```
console.log("Reza");
setTimeout(() => {
  console.log("Reza 1");
}, 1000);
console.log("Reza 3");
```

### Promise

> promise adalah Sebuah mekanisme baru pada fitur javascript / ES6 yang merepresentasikan sebuah object request pengolahan data yang dilakukan secara asynchronous, dan promise ini mewakili sebuah operasi yang belum selesai, tetapi diharapkan di masa mendatang.

- Ada 3 kemungkinan pada Promise
  - Pending ( Tertunda )
  - Fullfied ( Terpenuhi )
  - Rejected ( Dibatalkan )
- Contoh Promise

```
let nontonOnePiece = new Promise((resolve, rejcet) => {
  if (promise) {
    resolve("Jadi Nonton");
  } else {
    reject("Gak jadi nonton");
  }
});

```

## DAY 5 : Web Storage

### Local Storage

> LocalStorage merupakan salah satu cara yang dapat digunakan untuk menyimpan data di web browser. Pada localStorage penyimpanan data tidak memiliki kadaluarsa, artinya data yang disimpan tetap ada meskipun browser telah ditutup.

### Session Storage

> SessionStorage menyimpan data secara sementara, data akan menghilang saat tab ditutup atau browser ditutup. Metode dalam sessionStorage sama halnya dengan localStorage.

- 4 Metode yang digunakan untuk menggunakan Local Storage dan Session Storage
  - setItem()
    > Metode ini digunakan untuk menyimpan data kedalam localStorage.
  - getItem()
    > Metode ini memungkinkan kalian untuk mengakses data yang disimpan pada localStorage.
  - removeItem()
    > Metode ini digunakan untuk menghapus data tertentu pada penyimpanan localStorage kalian bedasarkan key.
  - clear()
    > Metode ini digunakan untuk menghapus seluruh data yang telah tersimpan di localStorage. Penggunaannya kalian tidak perlu menuliskan key ataupun value
