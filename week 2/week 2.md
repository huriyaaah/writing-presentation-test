# writing-presentation-week-2

## Javascript  Scope<br>
### Pengertian Scope
> Scope adalah konsep dalam flow data variabel.
### Blocks
> Blocks adalah code yang berada didalam curly braces {}.
### Global Scope
Global scope berarti variabel yang kita buat dapat diakses dimanapun dalam suatu file. Agar menjadi Global Scope, suatu variabel harus dideklarasikan diluar Blocks. <br>
Contoh Global Scope
  ```Javascript
  let MyName = 'Huriyah'
  function greeting(){
      return myName
  }
  
  console.log(myName) //Output: Huriyah
  ```
### Local Scope
Local scope berarti kita mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping. Variabel hanya bisa diakses didalam blocks saja. Tidak bisa diakses diluar blocks. <br>
Contoh Local Scope
  ```Javascript
  function greeting(){
      let MyName = 'Huriyah'
      return myName
  }
  
  console.log(greeting())
  greeting(myName)
  ```
  <br>
  
## Javascript - Function <br>
### Pengertian Function
> Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur.
### Membuat Function
  ```Javascript
  function greeting(){
      return 'Hello World'
  }
  ```
Penjelasan :
- function adalah function keyword.
- greeting adalah identifier.
- { return 'Hello World' } adalah function body
### Memanggil Function
```Javascript
    greeting()
    console.log(greeting())
```
### Parameter dan Argumen
- Parameter Function
  - Dengan parameter, function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan task/tugas.
  - Saat membuat function/fitur, kita harus tahu data-data yang dibutuhkan. Misalnya saat membuat function penambahan 2 buah nilai. Data yang dibutuhkan adalah 2 buah nilai tersebut.
  - Contoh Parameter Function
    ```Javascript
    function tambah(a, b){
        return a + b
    }
    ```
    Penjelasan :
    > a, b adalah parameter
- Argumen Function
  - Argumen adalah nilai yang digunakan saat memanggil function.
  - Jumlah argumen harus sama dengan jumlah parameternya
  - Jadi jika di function penambahan ada 2 parameter nilai saat membuat function. Saat memanggil function kita gunakan 2 buah nilai argumen.
  - Contoh Argumen Function
    ```Javascript
    function tambah(a, b){
        return a + b
    }
    
    console.log(tambah(10, 6)) //Output: 16
    ```
    penjelasan :
    > 10, 6 adalah argumen sebagai nilai
- Default Parameters
  - Default paramaters digunakan untuk memberikan nilai awal/default pada parameter function.
  - Default parameters bisa digunakan jika kita ingin menjaga function agar tidak error saat dipanggil tanpa argumen.
  - Contoh Default Parameter
    ```Javascript
    function sapa(nama = 'orang'){
        return 'Halo' + nama
    }
    
    console.log(sapa('Huriyah'))
    console.log(sapa())
    ```
- Function Helper
  - Kita bisa menggunakan function yang sudah dibuat pada function lain.
  - Contoh Function Helper
    ```Javascript
    function tambah(nomor){
        return nomor * 10
    }
    function bagi(number){
        return tambah(number) / 2
    }
    
    bagi(10) //Returns 50
- Arrow Function
  - Arrow function adalah cara lain menuliskan function. Ini adalah fitur terbaru yang ada pada ES6 (Javascript Version)
  - Contoh Arrow Function
    ```Javascript
    const sapa = () => {
        return 'Hello World'
    }
    
    const tambah = (a, b) = {
    return a + b
    }
    ```
- Short Syntax Function
  - Nol Parameter
    ```Javascript
    const functionName = () => {}
    ```
  - Satu Parameter
    ```Javascript
    const functionName = paramOne = {}
    ```
  - Dua atau lebih Parameter
    ```Javascript
    const functionName = (paramOne, paramTwo) => {}
    ```
  - Single Line Block
    ```Javascript
    const sumNumber = number => number +number
    ```
  - Multi-Line Block
    ```Javascript
    const sumNumber = number => {
        const sum = number + number;
        return sum;
    }
    ```
    <br>
## Errors dan Debugging<br>
### Error
- Error objek dilempar ketika kesalahan runtime terjadi. Objek Errorjuga dapat digunakan sebagai objek dasar untuk pengecualian yang ditentukan pengguna.
- Kesalahan runtime menghasilkan Errorobjek baru yang dibuat dan dibuang.
- Tipe - Tipe Error
  - EvalError
    <br>Membuat instance yang mewakili kesalahan yang terjadi terkait fungsi global eval().
  - RangeError
    <br>Membuat instance yang mewakili kesalahan yang terjadi saat variabel numerik atau parameter berada di luar rentang validnya.
  - ReferenceError
    <br>Membuat instance yang mewakili kesalahan yang terjadi saat mereferensikan referensi yang tidak valid.
  - SyntaxError
    <br>Membuat instance yang mewakili kesalahan sintaks.
  - TypeError
    <br>Membuat instance yang mewakili kesalahan yang terjadi saat variabel atau parameter bukan tipe yang valid.
  - URIError
    <br>Membuat instance yang mewakili kesalahan yang terjadi saat encodeURI()atau decodeURI()melewati parameter yang tidak valid.
  - AggregateError
    <br>Membuat instance yang mewakili beberapa kesalahan yang dibungkus dalam satu kesalahan ketika beberapa kesalahan perlu dilaporkan oleh suatu operasi, misalnya oleh Promise.any().
  - InternalError
    <br>embuat instance yang mewakili kesalahan yang terjadi saat kesalahan internal di mesin JavaScript dilemparkan. Misalnya "terlalu banyak rekursi".
- Constructor
  <br> Membuat Error objek baru.
- Metode Statis
  - Error.captureStackTrace()
  - Error.stackTraceLimit
  - Error.prepareStackTrace()
- Instance Properties
  - Error.prototype.message
  - Error.prototype.name
  - Error.prototype.cause
### Debugging
- Cara Debugging Javascript
  - Cara termudah dan mungkin yang paling umum adalah dengan console.log() variabel yang ingin Anda periksa
  - Menggunakan alat pengembang chrome, buka halaman Anda dengan kode JS Anda (tekan cmd+o di macOS atau Ctrl+o di Windows) dan pilih file Anda untuk di-debug, klik baris yang ingin Anda debug dan segarkan kembali halaman Anda (F5).
- Call Stack
  - Jalur yang telah diambil program Anda untuk mencapai titik saat Anda menetapkan titik putus atau Anda mengalami kesalahan.
  - Contoh Call Stack
    ```javascript
      (function testing(){
          var obj = {
          add
      }
      function add(a, b) {
          var result = a + b
          return result.split('')
      }
      var stringResult = obj.add("1", "2") // stringResult becomes "12"
      var numberResult = obj.add(1, 2) // numberResult is never set, an error is thrown
      })()
    ```
    Penjelasan :
    - testing dipanggil secara otomatis karena ini adalah IIFE (immediately Invoked Function Expression);
    - variabel obj dideklarasikan dengan function add (menggunakan ES6 shorthand untuk fungsi dalam objek, itu akan sama dengan memiliki var obj = { add: add };
    - function add dipanggil dari variabel obj dengan dua string memiliki parameter, ada yang ditambahkan yang menjadikannya "12" dalam skenario ini dan kemudian split dipanggil sebelum mengembalikan ["1", "2"];
    - function add dipanggil lagi, kali ini dengan angka, nilai ditambahkan sehingga menjadi 3 tetapi kemudian, split (yang tidak tersedia untuk variabel tipe angka ) dipanggil yang membuat error dilemparkan;
- Alat untuk menghindari runtime errors
  - quokka untuk mengevaluasi kode pada saat mengetik
  - eslint untuk memastikan panduan gaya konsisten dan itu akan membawa satu atau dua kesalahan di sepanjang mengoding
  - Bagi Anda yang ingin menjadikan JS pengalaman mengetik yang lebih kuat, Anda dapat melihat hal-hal seperti TypeScript (seperti yang saya katakan di artikel sebelumnya, ketika belajar saya lebih suka menghindari perpustakaan yang mengabstraksi bahasa inti jadi saya tidak akan merekomendasikan yang terakhir ini ketika mulai).

## JavaScript - Introduction to DOM 
 - Document Object Model adalah Jembatan supaya bahasa pemrograman dapat berinteraksi dengan dokumen HTML. Dengan DOM, kita dapat memanipulasi JS
 - DOM bukan bagian dari JavaScript, tapi merupakan web API. Jadi bisa digunakan dalam bahasa pemrograman lain.
 - Ketika file HTML di load, DOM dalam bentuk struktur seperti tree
 - 	Element vs node <br>
    Elemen: Html element ex : <span><div>
    Node : setiap bagian terkecil di html (text, comment, span)
 -	Cara mengkases DOM
    1.	getElementbyId : mengambil elemen html menggunakan id. Merupakan salah satu method yang sering digunakan
    2.	getElementsbyClassName : mengambil elemen html berdasarkan nama class. Output berupa html collection karena class name bisa berupa jamak dan dapat digunakan lebih dari satu class. Cara mengaksesnya sama dengan array berupa indeks
    3.	geteElementsbyTagName : sama seperti getElementsbyClassName, tapi mencari berdasarkan tag html yang digunakan. 
    4.	Children : mendapatkan elemen children dari parent
    5.	querySelector : mengambil elemen html setiap elemen html dengan tag berkelas 
    6.	parentElement : mengambil parent element berdasarkan childnya
    7.	closest : untuk mengakses parent
    8.	previousElementSibling : akses elemen yang sejajar sebelum element tersebut 
    9.	nextElementSibling : sama dengan previousElementSibling setelah elemen tersebut <br><br>
-	Manipulasi 
    1.	innerHTML berisi string dan dapat dispesifikkan output elemennya 
    2.	innerText menentukan dan mengembalikan nilai konten dari suatu element dalam bentuk text atau string
    3.	createElement membuat elemen HTML melalui DOM
    4.	append menyisipkan sebuah elemen tanpa menghapus elemen yang sebelumnya sudah ada didalamnya 
    5.	appendChild sama seperti append, tapi hanya bisa menerima tentang node
    6.	remove untuk menhapus/menghilangkan elemen/node dari DOM
    7.	p.attributes untuk mengecek sebuah elemen memiliki atribut apa saja 
    8.	p.getAttributes untuk melihat isi atributnya dan juga menambah attribute
    9.	p.setAttributes untuk menambahkan attribute pada tag html
    10.	p.style memberikan style css kepada elemen html melalui DOM <br><br>
-	Events 
    Interaksi yang terjadi pada website. Ada 3 cara untuk memberikan events, yaitu 
    1.	HTML attribute <br>
        ```javascript
        <h1 onclick=”alert”(‘Selamat Datang’)>Hello</h1>
        ```
    2.	Event property 
        ```javascript
        Let paragraf = document.getElementbyId(“id”) 
        Paragraf.onclick = fuction (){
        Alert(‘ini dari paragraf’)
        }
        ```
    3.	addEventListener()
        ```javascript 
        let button = document.getElementById(“button”)
        button.addEventListener(“click”, function(){
        alert(“ini dari button”)
        })
        ```
Macam2 event 
-	onclick terjadi ketiika user mengklik element html tersebut
-	onmousehover terjadi ketika mouse diarahkan diatas elemen html
-	submit Instruksi untuk menjalankan script ketika sebuah form dikirim (biasanya dengan mengklik tombol submit)
-	onblur Menginstruksikan sebuah peristiwa dimana sebuah elemen kehilangan fokus (kabur).
-	onchange Menginstruksikan sebuah peristiwa ketika value (nilai) atau bisa juga konten dari sebuah element berubah.
-	Onscroll Instruksi untuk menjalankan script ketika scrollbar pada sebuah element digulung (keatas dan kebawah)






