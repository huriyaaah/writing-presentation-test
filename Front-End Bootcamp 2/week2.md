# Front End Bootcamp Week 2

## PropTypes 
### Apa itu proptypes?
Sangat penting ketika develop aplikasi. Digunakan untuk mengecek tipe data yang dikirim melalui props

### Apa fungsinya?
Untuk mencegah kesalahan dari tipe data yang dikirim dari parent ke child. Tidak bersifat wajib, hanya untuk tindakan pencegahan 

## React Router
Digunakan untuk berpindah halaman ketika menggunakan react. Router mengarahkan alamat/lokasi lain.

### Kenapa harus memakai React Router?
Dengan menggunakan router, kita dapat berpindah halaman tanpa mereload. Jadi dari segi kecepatan lebih cepat mengguakan react router 

## React Redux 
### Props Drilling 
Melempar data props dari grandparent, parent, child, grandchild dst. Hal ini dapat menimbulkan masalah ketika pemberian propsnya diubah (missal : nama props diganti). Maka, harus mengganti satu-satu. </br>
Lalu bagaimana cara mengatasinya? Dengan data terpusat, tidak perlu pelemparan data. Data langsung diakses dari sumber. Hal ini disebut dengan state management </br>
State management : 
-	Redux 
-	Context 
-	Jotai 
-	Zustand 

### Apa itu redux? 
Salah satu cara management agar tidak terjadi props drilling. Metode untuk membuat penampungan data agar dapat diakses oleh seluruh komponen. Third party untuk memanipulasi state management. 
