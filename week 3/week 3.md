# Writing Week 3

## JavaScript - Array 
### Apa itu Array ?
    Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya. Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya. <br>
    contoh :
    ```JavaScript 
    let hewan = ["anjing", 'kura - kura', 'kelinci', 'ayam', 'anjing', 'kucing']
    ```
    Array didefinisikan menggunakan square bracket [].

### Mengakses Array 
    Array pada JavaScript dimulai dari Index ke - 0. Jadi data pertama memiliki index-0
    ```JavaScript
        let hewan = ["anjing", 'kura - kura', 'kelinci', 'ayam', 'anjing', 'kucing']
    ```
    hewan anjing merupakan data pertama, maka memiliki index ke-0, kura-kura index ke-1 dan seterusnya 

### Update Array 
    Mengganti isi array dengan array baru 
    ```JavaScript 
        let makanan = ['nasi goreng', 'mie goreng', 'Sate Ayam']
        makanan[0] = 'nasi kuning'
        console.log(makanan)
        //output : ['nasi kuning','mie goreng','sate ayam']
    ```

### Const pada Array
    Jika menggunakan let, kita dapat mengubah array dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain. Const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable). Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const. <br>
    Contoh : 
    ```JavaScript
        const merekMotor = ['Yamaha','Honda','Kawasaki']
        merekMotor = ['Suzuki'] //Output : Error
    ```

### Array Properties 
    Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer. Salahsatunya yaitu length. length akan mengembalikan nilai dari jumlah panjang data suatu array.
    contoh :
    ```JavaScript 
    const merekMotor = ['Yamaha','Honda','Kawasaki']
    console.log(merekMotor.length) //Output : 3
    ```

### Array Method
    Array memiliki method atau biasa disebut built-in methods. Contoh Array Built-in Methods :
    - push : Method untuk menambahkan item array pada urutan yang paling akhir.
    - pop : Method yang menghapus item array index terakhir.
    - shift : Method untuk menghapus item Array pada index pertama
    - unshift : Method untuk menambahkan item Array pada index pertama
    - sort : Method untuk mengurutkan secara Ascending atau Descending Alphanumeric

### Array Looping 
    1. map -> Melakukan perulangan/looping dengan membuat array baru. Contoh :
    ```JavaScript 
    let angka = [1,2,3,4]
    let kaliDua = angka.map(num => {
    return num * 2
    })
    //Output : [2,4,6,8]
    ```
    2. for each -> method untuk melakukan looping pada setiap elemen array. Contoh :
    ```JavaScript
    const merekMotor = ['Yamaha','Honda','Kawasaki']
    const forEach(element =>{
    console.log(element)
    })
    //Output : 'Yamaha','Honda','Kawasaki'
    ```

### Array MultiDimensi
    Multidimensional Array bisa dianalogikan dengan array of array. Ada array di dalam array
    ```
    let inventory = [
    ['Celana',5],
    ['Baju', 10]
    ]

    console.log(inventory)

    ```
    Akses Index array multi dimensi 
    ```
    let inventory = [
    ['Celana',5],
    ['Baju', 10]
    ]

    console.log(inventory[1][0]) //Output : Celana
    ```

## JavaScript - Objek 
    Object adalah tipe data pada variabel yang menyimpan properti dan fungsi (method). Properti adalah data lengkap dari sebuah object. Method adalah action dari sebuah object. Cara membuat objek yaitu :
    ```
    let siswa = {
    nama : 'terra',
    umur : 17,
    hobi : 'memancing', 
    "nomor handphone" : 08256814086
    }
    console.log(siswa);
    ```
### Cara Akses 
    Dalam mengakses object terdapat 2 cara yaitu menggunakan dot notation dan bracket. Selain itu, bisanya dalam mengakses object yaitu menggunakan console.log(object). dot notation, misalnya console.log(siswa.nama); maka output yang dihasilkan yaitu terra bracket, misalnya console.log(siswa['nama']);

    - tambah properti kedalam objek
    ```JavaScript
    let buku = {
    Judul : "Mantan jadi manten",
    Penulis : "Hayati",
    "Jumlah halaman" : 250,
    };
    buku.tahun : 2022;
    buku.terjual : 3000;
    console.log(bukuu);
    //Output :
    Judul : Mantan jadi manten
    Penulis : Hayati
    Jumlah halaman : 250
    buku.tahun : 2022
    buku.terjual : 3000
    ```

    - Ganti properti 
    ```
    let hewan = {
    nama : 'kucing',
    kaki : 4,
    warna : 'putih',
    };
    hewan.nama : 'kelinci',
    hewan.warna : 'hitam',
    console.log(hewan);
    //Output 
    nama : kelinci
    kaki : 4
    warna : hitam
    ```

### Method
    Method adalah ketika ingin menambahkan sebuah function. Ada 2 method dalam object, yaitu :
    - const greeting 
    ```
    const greeting = { welcome : function(){ return "halo selamat datang"; }; afterpay:function(){ return "terimakasih sudah membeli produk kami"; } }; console.log(greeting.welcome()); //Output : halo selamat datang
    ```
    - nested object 
    ```
    let buku = {
    Judul : "Tips jago Javascript",
    Tahun : 2022;
    Penulis {
        Penulis1 : {
        Nama : "Reyhan",
        Umur : 28,
        Kota : "Jakarta"
        }
        Penulis2 : {
        Nama : "Fala",
        Umur : 25,
        Kota : "Madiun"
        }
        Penulis3 : {
        Nama : "Diana",
        Umur : 20,
        Kota : "Bandung"
        }
        }
    };
    console.log(buku.penulis.penulis1.nama);//Output : Reyhan
    ```

### Array of Objecct 
    array yang menyimpan banyak object sebagai nilainya.
    ```JavaScript 
    let users = {
    {
    Nama : "Reyhan",
    Umur : 28,
    Kota : "Jakarta",
    },
    {
    Nama : "Fala",
    Umur : 20,
    Kota : "Bandung",
    },
    {
    Nama : "Diana",
    Umur : 24,
    Kota : "Madiun",
    },
    };
    console.log(user);

    Dengan menggunakan Map, maka
    let data = users.map((el) => {
    console.log(el.nama);
    });
    //Output :
    Reyhan
    Fala
    Diana
    ```

### Rekursif dan Modules 
- Rekursif 
function atau algoritma yang memanggil dirinya sendiri sampai kondisi tertentu. Rekrusif ini mirip seperti looping. Misalnya pada gambar ada gambar di dalam gambar. Terdapat 2 kunci pada rekrusif,yaitu base case atau titik berhenti dan recrusion case atau titik memanggil function.
```
Menampilkan bilangan 1 2 3 4 5

function deretAngka(n){
  if (n == 1) {
  console.log(n)
} else {
  deretAngka(n-1)
  console.log(n);
  }
}
deretAngka(3)
```

- Modules
cara untuk memisahkan kode ke file yang berbeda. Keuntungan dari modules yaitu mudah untuk mengelola kode serta kode tidak menumpuk di dalam satu file. Terdapat 2 kata kunci pada modules yaitu export dan import.
```
// File Jepang.js
export let motor = ["suzuki", "yamaha", "honda", "kawasaki"]

let entertainment = ["anime", "manga", "wibu", "dorama"]
export default entertainment

export function sayHello() {
console.log("hallooo")
}

import {apple} from './amerika.js';
console.log(apple);

// File Indonesia.js
import {motor} from "./Jepang.js"
console.log(motor);

import Entertainment, { motor as motorJepang, sayHello  } from "./jepang.js"
console.log(Entertainment);

// File Amerika.js
let apple = ["iphone", "macbook", "imac"]
export {apple}
```

## Asynchronus 
Merupakan sebuah proses yang dilakukan secara tidak berurutan. Jika proses terlalu panjang, akan diselat oleh proses yang lebih singkat. Secara umum, bahasa pemrograman berjalan secara synchronous. JS memiliki kelebihan dapat menjalankan sebuah proses tanpa harus berurutan. <br>

3 Kunci Utama dalam Asynchronus 
    1. CallBack 
    merupakan sebuah function yang dijadikan argumen. Ketika sesuatu memerlukan waktu yang lama, maka dia akan masuk kedalam callback queue lalu menjalankan proses yang berada di belakangnya. Jika proses yg belakang sudah selesai, maka engine akan memeriksa yang ada didalam callback queue untuk dijalankan.
    ```
    Console.log(“A”)
    setTimeout( () => {
    Console.log(“B”) 
    }, 1000)
    Console.log(“C”)
    //Output :
    //A
    //C
    //B
    ```
    2. Promises
    Kejadian yang telah selesai atau gagal dalam operasi asynchronous yang menghasilkan nilai. Saat on progress progress dalam fase pending. Jika gagal maka status asynchronous menjadi rejected. Jika kejadian dari event asynchronous telah berhasil, maka status fulfilled. 
    ```
    Let nontonPromise = new Promise ((resolve, reject) => {
    resolve(“nonton terpenuhi”)
    reject(“gagal”)
    })
    console.log(“A”)
    nontonPromise
    .then(result =>{
    console.log(result)
    })
    .catch((err) => {
    console.log(err)
    })

    console.log(“C”)
    // output 
    // A
    // C
    // B
    ```
    3. Async Await

## JavaScript - Web Storage 
Ada beberapa cara untuk menyimpan data pengguna seperti pencarian, artikel berita, dan lain-lain ke lokal (browser) menggunakan web storage seperti cookies, local storage, dan session storage. Data ini dimanfaatkan oleh situs web tersebut untuk merekam kebiasaan pengguna agar dapat memberikan rekomendasi sesuai preferensi si pengguna tersebut.

### cookies 
Cookies adalah data kecil yang dikirim dari situs web dan disimpan di komputer kita oleh web browser saat kita menjelajah. Disebut data kecil karena maksimum data yang dapat disimpan dalam cookies adalah 4096 bytes (4 KB). Biasanya data yang disimpan di cookies adalah access token pengguna saat login atau data pencarian saat melakukan pencarian pada situs web tertentu. Hal ini yang biasanya dilakukan oleh situs pencarian untuk melacak pencarian kita dan menampilkan iklan yang berhubungan dengan pencarian kita sebelumnnya. Namun ada beberapa kekurangan yang perlu kita perhatikan mengenai cookies di antaranya:
1. Setiap kita mengakses situs web, cookies juga kembali dikirim sehingga memperlambat aplikasi web kamu dengan mengirimkan data yang sama.
2. Cookies disertakan pada setiap HTTP request, sehingga mengirimkan data yang tidak dienkripsi melalui internet, maka saat kita ingin menyimpan data dalam cookies kita harus mengenkripsinya terlebih dahulu.
3. Cookies hanya dapat menyimpan data sebanyak 4KB.
4. Lalu cookies juga memiliki tanggal kadaluarsa. Tanggal ini telah ditentukan sehingga web browser bisa menghapus cookies jika tanggal sudah kadaluarsa atau tidak dibutuhkan.
Kita dapat memanfaatkan jenis web storage yang lain untuk mengatasi kekurangan yang dimiliki cookies.

### Local Storage 
Berbeda dengan local storage, walaupun masuk ke dalam web storage, data yang tersimpan pada session storage akan hilang ketika session dari sebuah laman berakhir. <br>
Karakteristik Local Storage:
- Menyimpan data tanpa tanggal kadaluarsa.
- Data tidak akan dihapus ketika web browser ditutup dan akan tersedia seterusnya selama kita tidak menghapus data local storage pada web browser.
- Dapat menyimpan data hingga 5MB.
- Hanya dapat menyimpan data string. <br>

Sedangkan Karakteristik Session Storage:
- Data yang disimpan pada session storage akan terus tersimpan selama browser terbuka dan tidak hilang jika laman di-reload.
- Membuka banyak tab/window dengan URL yang sama, akan menciptakan session storage yang berbeda di masing-masing tab/window.
- Menutup tab/window akan mengakhiri session dan menghapus data yang tersimpan di session storage pada tab/window tersebut.
- Data yang tersimpan dalam session storage harus berbentuk string.
- Hanya dapat menyimpan data sebanyak 5MB.

### Akses Local Storage & Session Storage
1. Local Storage
- Menyimpan Data
Untuk menyimpan data pada local storage, kita menggunakan method setItem() yang membutuhkan 2 parameter. Parameter pertama adalah key yang ingin kita simpan dan parameter kedua adalah data (value) dari key yang akan disimpan.
`localStorage.setItem('key', value);`
- Mengambil Data 
Untuk mengambil data yang telah tersimpan pada local storage, kita dapat menggunakan method getItem() yang membutuhkan 1 parameter. Parameter tersebut adalah key dari data yang kita inginkan.
`localStorage.getItem('key');`
- Menghapus Data 
```
Menghapus Data
Untuk menghapus data yang telah tersimpan pada local storage, kita dapat menggunakan method removeItem() yang membutuhkan 1 parameter. Parameter tersebut adalah key dari data yang ingin kita hapus.
// menghapus key tertentu
localStorage.removeItem("key");

// menghapus semua key
localStorage.clear();
```
2. Session Storage 
- Menyimpan Data 
Sama dengan local storage, sintaks untuk menyimpan data pada session storage adalah sebagai berikut:
```
// menambah session storage
sessionStorage.setItem('key', value);
```
- Mengambil Data 
Sama seperti local storage, cara mendapatkan data dari session storage juga menggunakan getItem(), seperti berikut ini:
```
// mendapatkan session storage
sessionStorage.getItem('key');
```
- Menghapus Data Syntax 
untuk menghapus data dari session storage ada 2, yaitu:
```
// menghapus session storage satu persatu berdasarkan key
sessionStorage.removeItem('key');

// menghapus seluruh session storage sekaligus
sessionStorage.clear();
```