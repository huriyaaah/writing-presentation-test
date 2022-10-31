# Front-End Bootcamp week 1

## Apa itu Node JS?
Sebuah teknologi yang memungkinkan JS agar dapat dijalankan diluar browser. Digunakan untuk menginstall react dan beberapa library 

## Apa itu React JS
Dikembangkan oleh tim engineer facebook karena kesulitan dengan penggunaan DOM. React merupakan view library js untuk membuat tampilan (user inteface) pada website. 

## Kenapa harus mengguanakan react?
-	Membuat aplikasi front end menjadi lebih cepat walaupun harus menghandle berbagai data. 
-	React js membagi 1 tampilan pada web menjadi komponen2 kecil 
-	Dapat digunakan pada aplikasi berskala kecil hingga besar dan kompleks 
-	Komunitas react sangat luas 

## Cara instal Node.js
1.	download pada laman nodejs.org <br>
2.	install lts version 
3.	lalu instal seperti biasa 
4.	Jika sudah terinstal, kita bisa cek melalui git bash 

## Cara install project react baru menggunakan node 
    ```
    npx create-react-app belajar-react
    cd belajar-react 
    npm start
    ```

- Library tampilan web ini menggunakan teknologi SPA (Single Page Application). File HTML yang digunakan hanya 1. jika ingin pindah dalam page lain, isinya yang akan diganti tanpa perlu mengganti halaman HTML (tanpa refresh). Teknologi ini digunakan untuk web yang sangat sering berganti data (ex :  e-comerce). 

- Jika ingin berinteraksi dengan DOM, harus menggunakan perantara virtual DOM (replica dalam DOM yang asli). Dengan penggunaan virtual DOM, proses perubahan data jadi lebih cepat (performa web lebih cepat). 
React memungkinkan kita untuk menuliskan script html dalam file javascript. Dengan menggunakan react, kita tidak perlu menggunakan innerHTML, getDocument dll
App.js hanya dapat mereturn satu elemen, jadi harus dibungkus dalam satu div atau tag kosong 

## React Component
Cara membagi UI kedalam komponen – komponen kecil. Bertujuan agar daapt digunakan kembali di tempat yang lain (reusable).

## Stateless & Stateful component 
-	Stateless berarti tidak memiliki state, hanya memiliki props 
-	Stateful berarti memiliki state dan mengirim state tersebut kedalam komponen 

## Apa itu props & state?
Props (properties) digunakan untuk komunikasi antara komponen parent dan komponen child untuk pengiriman data. 
State merupakan sebuah objek untuk menyimpan data di react lalu akan dirender/dimuat ketika melakukan perubahan data. State adalah data local


## React JS Hooks
Apa itu hooks?
Berfungsi untuk memudahkan penggunaan functional components agar bisa menggunakan state dan lifecycle lainnya 
Dengan pengguanan hooks, state (setState) dan lifecycle (componentDidMount, componentDidUpdate) dapat digunakan pada functional component 
Functional component akan melakukan  hooks terhadap hal hal yang hanya ada di class agar dapat digunakan oleh functional component dengan mudah. 

## Kelebihan penggunaan hooks
Dengan penggunaan hooks, code terlihat lebih clean, pendek, dan mudah dimengerti 

## Apa itu useState?
useState di panggil dalam function component untuk menambahkan suatu state lokal. React akan menyimpan state antar render. useState memberikan dua hal: nilai state saat ini dan fungsi untuk memperbarui nilai tersebut.
Update State 
State dapat diubah menggunakan variable kedua dari state hooks

## Array dalam useState
Kita dapat menggunakan array untuk menyimpan data dalam state, kita tinggal memasukkan tanda [] dalam useState untuk menandakan state tersebut berupa array 

## Apa itu useEffect hooks?
Digunakan untuk lifecycle pada functional component agar lebih mudah 

## Apa itu lifecycle
-	Analoginya, seperti lingkaran kehidupan selama 24 jam mulai dari bangun sampai tidur lagi 
-	setiap component di react js ternyata juga memiliki siklus hidup.
