# Pemrograman Berbasis Platform (CSGE602022) - diselenggarakan oleh Fakultas Ilmu Komputer Universitas Indonesia, Semester Ganjil 2022/2023

Pemrograman Berbasis Platform (CSGE602022) - diselenggarakan oleh Fakultas Ilmu Komputer Universitas Indonesia, Semester Ganjil 2022/2023

**Nama**	: Syahrul Apriansyah

**NPM** 	: 2106708311

**Kelas**	: F

## Tugas 7: Elemen Dasar Flutter

### Jelaskan apa yang dimaksud dengan *stateless widget* dan *stateful widget* dan jelaskan perbedaan dari keduanya.This project is a starting point for a Flutter application.

* Stateless Widget merupakan widget yang tidak dapat mengubah state-nya selama runtime aplikasi Flutter. Oleh karena itu, tampilan dan properti tetap tidak berubah sepanjang lifetime widget tersebut.
* Stateful widget merupakan widget yang dapat mengubah state-nya selama runtime aplikasi Flutter. Widget ini memungkinkan objek state yang dapat berubah seiring waktu dan memicu UI rebuild dari widget, seperti tampilan dan properti.

Perbedaan dari stateless widget dan stateful widget:* Stateless widget dapat berguna ketika state tidak bergantung pada widget lain, sedangkan stateful widget berguna ketika state perlu berubah secara dinamis.

* Stateless widget tidak dapat di-update selama runtime aplikasi, sehingga external events diperlukan sebagai trigger. Stateful widget dapat di-update selama runtime.
* Contoh stateless widget adalah teks, icons, icon buttons, dan raised buttons, sedangkan contoh dari stateful widget adalah slider, radio button, form, dan text field.

### Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya.

* `Scaffold`, sebagai landasan halaman
* `AppBar()`, biasanya menjadi judul (dari sebuah aplikasi atau halaman)
* `Center()`, semua Widget yang ada didalam Widget ini akan diletakkan di bagian tengah
* `Column()`, semua widget yang ada didalam widget ini akan ditampilkan secara vertical
* `Row()`, semua widget yang ada didalam widget ini akan ditampilkan secara horizontal
* `Text()`, menampilkan teks dan memberikan style pada teks
* `FloatingActionButton()`, menampilkan button floating
* dll

### Apa fungsi dari `setState()`? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.

`setState()` berfungsi untuk menandakan *framework* bahwa internal *state* dari sebuah objek telah diubah yang dapat mempengaruhi tampilan untuk  *user* . `setState()` perlu digunakan untuk meng-*update* *state* dari sebuah objek. Variabel yang terdampak dari `setState()` adalah `_counter`.

### Jelaskan perbedaan antara `const` dengan `final`.

Seperti pada bahasa pemrograman umumnya dart juga mendukung variabel yang bersifat immutable atau nilainya tidak bisa dirubah, pada bahasa dart sendiri terdapat 2 kata kunci berbeda yang dapat digunakan untuk membuat variabel immutable yaitu final dan const. -Final dapat digunakan untuk deklarasi variabel immutable yang nilainya sudah ataupun belum diketahui pada saat waktu kompilasi berjalan. -Const dapat digunakan untuk deklarasi variabel immutable yang nilainya bersifat konstan dan harus sudah diketahui pada saat waktu kompilasi berjalan, artinya adalah nilai dari variabel tersebut harus sudah di berikan secara langsung.

### Jelaskan bagaimana cara kamu mengimplementasikan *checklist* di atas.

1. Membuat sebuah program Flutter baru dengan nama counter_7 dengan menjalankan perintah `flutter create counter_7`
2. Mengubah text title dari aplikasi menjadi Program Counter dengan menuliskan kode `home: const MyHomePage(title: 'Program Counter'),` dalam fungsi build.
3. Membuat fungsi untuk melakukan decrement pada counter.
4. Menambahkan kode di bawah ini (sebagai children dari Column) untuk mengubah text beserta stylingnya jika nilai counter adalah ganjil atau genap.
5. Menambahkan kode untuk membuat FloatingActionButton yang memicu increment dan decrement dari counter.


## Tugas 8: Flutter Form

### Jelaskan perbedaan `Navigator.push` dan `Navigator.pushReplacement`.

`Navigator.pushReplacement` merupakan metode push yang membuang rute sebelumnya sehingga jika berpindah halaman tidak dapat kembali ke halaman sebelumnya. `Navigator.push` merupakan metode push untuk menambahkan rute lain ke atas tumpukan, jadi menampilkan halaman baru dan tetap dapat mengakses halaman sebelumnya.

### Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya.

* `Drawer` berfungsi sebagai menu drawer untuk pindah ke tampilan atau page lain
* `TextFormField` berfungsi untuk ask input text
* `Form` -> Membuat sebuah container untuk dijadikan parent dari input input yang dideklarasikan
* `ListTile` -> component yang didalamnya juga bisa digunakan widget
* `Padding` berfungsi untuk menampilkan child-nya dengan padding tertentu. 
* `Row` berfungsi untuk  menampilkan child-nya ke tata letak yang horizontal. 
* `Column` berfungsi untuk  menampilkan child-nya ke tata letak yang vertikal. 
* `DropdownButtonTextField` berfungsi untuk membuat form field untuk user memilih input
* `Text` berfungsi untuk menampilkan text
* `TextStyle` berfungsi untuk melakukan styling terhadap text
* `Container` berfungsi sebagai tempat untuk menampung komponen
* `TextButton` berfungsi untuk membuat tombol dengan text tertentu

### Sebutkan jenis-jenis event yang ada pada Flutter (contoh: `onPressed`).

* `onChanged` adalah untuk mengeksekusi jika sebuah widget diubah. 
* `onFocusChanged` adalah untuk mengeksekusi jika fokus berubah. 
* `onSaved` adalah untuk mengeksekusi jika sebuah widget disiimpan. onHover adalah untuk mengeksekusi jika pointer bergerak dalam sebuah widget. 
* `onPressed` adalah untuk mengeksekusi jika sebuah widget diklik.

### Jelaskan bagaimana cara kerja Navigator dalam "mengganti" halaman dari aplikasi Flutter.

Navigator pada flutter serupa dengan implementasi stack. Sehingga jika melakukan "push" akan menuju suatu halaman dan untuk mengembalikannya menggunakan "pop". "push" menambahkan halaman pada antrian teratas stack dan "pop" mengurangi halaman pada antrian stack.

### Jelaskan bagaimana cara kamu mengimplementasikan _checklist_ di atas.

1. Menambahkan file `form.dart` untuk page Form Budget dan file `show.dart` untuk page Data Budget
2. Menambahkan drawer dalam build pada `main.dart`, `form.dart`, dan `show.dart`, yang berfungsi untuk navigasi ke page lainnya.
3. Membuat class Budget yang berisi dengan atribut-atribut dari form budget tersebut dan constructornya.
4. Membuat validator untuk memeriksa apakah text field numerik untuk input nominal budget.
5. Membuat form dalam halaman Form Budget dengan menambahkan widget-widget seperti seperti `TextFormField`, `DropdownButtonFormField`, `TextButton`, dan lain-lain seperti yang sudah dijelaskan pada soal nomor 2.
6. Menambahkan data-data dari budget melalui `ListView` Builder

## Tugas 9: Integrasi Web Service pada Flutter

### Apakah bisa kita melakukan pengambilan data JSON tanpa membuat model terlebih dahulu? Jika iya, apakah hal tersebut lebih baik daripada membuat model sebelum melakukan pengambilan data JSON?

Pengambilan data **JSON** tanpa membuat model dapat dilakukan. Secara behavioral, **JSON** sendiri merupakan suatu object dalam **notasi Javascirpt** di mana pada bahasa Dart, hal tersebut **ekuivalen** dengan **Map** di mana object yang terdiri dari *key* dengan *value pair*. Namun, pengambilan data JSON tanpa melakukan konversi ke dalam suatu model ***bukan merupakan best practice*** dalam pengimplementasiannya. Konversi data JSON ke dalam suatu model bertujuan untuk **meminimalisir kesalahan** pengambilan atau pengiriman data melalui http request yang akan ditampilkan pada sisi UI aplikasi.

###  Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya.

1. FutureBuilder() = widget yang membangun dirinya sendiri berdasarkan interaksi snapshot terakhir dengan `Future`.
2. MyWatchDetail() = widget yang digunakan untuk menampilkan detail dari mywatch
3. RichText() = widget yang dapat menampilkan text dengan menggunakan beberapa *style* yang berbeda.
4. GestureDetector() = widget yang dapat mendeteksi gestur pengguna.
5. ListTile() = Widget yang merepresentasikan satu baris dengan tinggi tetap.
6. CheckboxListTile() = `ListTile` dengan `Checkbox`.

###  Jelaskan mekanisme pengambilan data dari json hingga dapat ditampilkan pada Flutter.

1. Membuat sebuah function **http request** dengan method `GET` secara *async* untuk mengambil data ke pihak eksternal
2. Pada function tersebut lakukan parsing dengan `jsonDecode()` untuk mengubah response **String** menjadi **JSON**
3. Konversi object  **JSON** ke dalam suatu **Model object**
4. Gunakan widget `FutrueBuilder` untuk menampilkan widget-widget dengan snapshot data terbaru yang telah dikonversi menjadi sebuah object

###  Jelaskan bagaimana cara kamu mengimplementasikan _checklist_ di atas.

1. Menambahkan tombol navigasi pada drawer/hamburger untuk ke halaman mywatchlist.<br>
2. Membuat satu file dart yang berisi model mywatchlist<br>
3. Menambahkan halaman mywatchlist yang berisi semua watch list yang ada pada endpoint JSON di Django pada [Tugas 3](https://tugas-pbp-syahrul.herokuapp.com/mywatchlist/json/)<br>
4. Membuat navigasi dari setiap judul watch list ke halaman detail<br>
5. Menambahkan halaman detail untuk setiap mywatchlist<br>
6. Menambahkan tombol untuk kembali ke daftar mywatchlist<br>





