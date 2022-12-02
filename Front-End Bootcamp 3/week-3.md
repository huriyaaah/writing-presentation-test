# Front-End Bootcamp Week 3

## React Context 
Context menyediakan cara untuk oper data melalui diagram komponen tanpa harus oper props secara manual di setiap tingkat.

Dalam aplikasi React yang khusus, data dioper dari atas ke bawah (parent ke child) melalui props, tetapi ini bisa menjadi rumit untuk tipe props tertentu (mis. preferensi locale, tema UI) yang dibutuhkan oleh banyak komponen di dalam sebuah aplikasi. Context menyediakan cara untuk berbagi nilai seperti ini di antara komponen tanpa harus oper prop secara explisit melalui setiap tingkatan diagram.

### Kapan penggunaan react context?
Context dirancang untuk berbagi data yang dapat dianggap “global” untuk diagram komponen React, seperti pengguna terotentikasi saat ini, tema, atau bahasa yang disukai. 

Context terutama digunakan ketika beberapa data harus dapat diakses oleh banyak komponen pada tingkat bersarang yang berbeda. Gunakan dengan hemat karena membuat penggunaan kembali komponen menjadi lebih sulit.

## React Testing 

### apa itu unit testing?
Unit testing adalah sebuah pekerjaan dimana kita melakukan pengujian pada suatu bagian pada aplikasi yang kita buat. Tujuan dari unit testing sendiri yaitu untuk melakukan validasi setiap unit pada kode aplikasi agar berfungsi seperti yang diharapkan. Unit yang dimaksud bisa berupa kode, fungsi, metode, prosedur, modul, atau objek tersendiri.

### Kenapa unit testing penting?
1. Membantu memperbaiki bug di awal pada siklus software development dan menghemat biaya
2. Membantu developer untuk memahami basis kode dan memungkinkan mereka membuat perubahan dengan cepat
3. Berfungsi sebagai dokumentasi proyek
4. Membantu reusability code pada projek baru

### Jenis - jenis Testing 
1. Black box testing adalah sebuah pengujian yang tidak perlu melihat dan memahami suatu software lebih dalam, pengujiannya melalui user interface, input dan output
2. White box testing bersifat transparan jadi kita bisa melihat suatu sistem dari awal sampai akhir untuk dilakukan testing. Untuk testingnya dilakukan untuk menguji struktur internal, desain, fungsi dan detail implementasi dari sebuah aplikasi
3. Grey box testing ini merupakan sebuah perpaduan antara black box testing dan white box testing. Pengujiannya ini digunakan untuk eksekusi test, resiko dan metode penilaian

### Kelebihan Unit Testing 
1. Membantu menulis kode lebih baik
2. Membantu menemukan sebuah bug sebelumnya
3. Membantu mendeteksi bug regression (bug yang menyebabkan fitur menjadi berhenti)
4. Membuat kode lebih mudah di refactor
5. Membuat penulisan kode lebih efisien

### Apa itu Jest?
Jest adalah framework pengujian JavaScript yang menyenangkan dengan fokus pada kesederhanaan. Ia bekerja dengan projek yang menggunakan: Babel, TypeScript, Node, React, Angular, Vue, dan lainnya