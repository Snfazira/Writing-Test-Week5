# __Wriring Test Week 5__
## __Web Server & RESTful API__

- Web server terdiri dari 2 komponen penting, yaitu :
    - Hardware
    - Software

- Di sisi hardware , web server adalah komputer yang menyimpan perangkat lunak server web dan file komponen situs web. (misalnya, dokumen HTML, gambar, CSS stylesheet, dan file JavaScript) Server web terhubung ke Internet dan mendukung pertukaran data fisik dengan perangkat lain yang terhubung ke web.

- Di sisi software,web server mencakup beberapa bagian yang mengontrol cara pengguna web mengakses file yang dihosting. Minimal, ini adalah server HTTP. Server HTTP adalah perangkat lunak yang memahami URL (alamat web) dan HTTP (protokol yang digunakan browser Anda untuk melihat halaman web). Server HTTP dapat diakses melalui nama domain situs web yang disimpannya, dan mengirimkan konten situs web yang dihosting ini ke perangkat pengguna akhir.

- Static Web Server
: terdiri dari komputer (perangkat keras) dengan server HTTP (perangkat lunak). atau sering disebut "statis" karena server mengirimkan file yang dihosting apa adanya ke browser Anda.

- Dynamic Web Server
 : terdiri dari server web statis ditambah perangkat lunak tambahan, paling sering server aplikasi dan database. sering di sebut dengan"dinamis" karena server aplikasi memperbarui file yang dihosting sebelum mengirim konten ke browser Anda melalui server HTTP.

 - Pemrograman Sisi Server
 : Server web menunggu pesan permintaan klien, memprosesnya saat tiba, dan membalas browser web dengan pesan respons HTTP. Respons berisi baris status yang menunjukkan apakah permintaan berhasil atau tidak (e.g.. "HTTP/1.1 200 OK" untuk berhasil).

 - Situs statis adalah situs yang mengembalikan konten hard-coded yang sama dari server setiap kali sumber daya tertentu diminta). Saat pengguna ingin menavigasi ke halaman, browser mengirimkan permintaan "GET" HTTP yang menentukan URL-nya.

 - Situs web dinamis adalah situs di mana beberapa konten respons dihasilkan secara dinamis, hanya bila diperlukan.

 - Perbedaan Situs Statis dan Dinamis, yaitu :
    - Mereka memiliki tujuan dan perhatian yang berbeda.

    - Mereka umumnya tidak menggunakan bahasa pemrograman yang sama (pengecualiannya adalah JavaScript, yang dapat digunakan di sisi server dan klien).

    - Mereka berjalan di dalam lingkungan sistem operasi yang berbeda.

- Yang dapat Anda lakukan di sisi server?

    - Penyimpanan dan pengiriman informasi yang efisien

    - Pengalaman pengguna yang disesuaikan

    - Akses terkontrol ke konten

    - Simpan informasi sesi/status

    - Pemberitahuan dan komunikasi

    - Analisis data

- REST adalah gaya arsitektur untuk menyediakan standar antara sistem komputer di web, sehingga memudahkan sistem untuk berkomunikasi satu sama lain.

- Komunikasi antara Klien dan Server :

    - Membuat permintaan

        REST mengharuskan klien membuat permintaan ke server untuk mengambil atau mengubah data di server. Permintaan umumnya terdiri dari:

    - kata kerja HTTP, yang mendefinisikan jenis operasi apa yang harus dilakukan

    - header, yang memungkinkan klien untuk menyampaikan informasi tentang permintaan

    - jalan menuju sumber daya

    - pesan opsional yang berisi data

- Ada 4 kata kerja HTTP dasar yang digunakan dalam permintaan untuk berinteraksi dengan sumber daya dalam sistem REST:

    - GET — mengambil sumber daya tertentu (berdasarkan id) atau kumpulan sumber daya

    - POST — buat sumber daya baru

    - PUT — perbarui sumber daya tertentu (berdasarkan id)

    - DELETE — menghapus sumber daya tertentu dengan id

    - Header dan Terima Parameter : Di header permintaan, klien mengirimkan jenis konten yang dapat diterimanya dari server.
    
- Paths : Permintaan harus berisi jalur ke sumber daya tempat operasi harus dilakukan. Dalam RESTful API, jalur harus dirancang untuk membantu klien mengetahui apa yang sedang terjadi.

- Sending Responses

    - Response Codes :  berisi kode status untuk memperingatkan klien tentang informasi tentang keberhasilan operasi. 

- Kode status
    - 200 (Oke) : permintaan HTTP yang berhasil.

    - 201 (DIBUAT) : permintaan HTTP yang menghasilkan item yang berhasil dibuat.

    - 204 (TIDAK ADA ISI) : permintaan HTTP yang berhasil, di mana tidak ada yang dikembalikan di badan respons.

    - 400 (PERMINTAAN BURUK) : Permintaan tidak dapat diproses karena sintaks permintaan yang buruk, ukuran yang berlebihan, atau kesalahan klien lainnya.

    - 403 (DILARANG) : Klien tidak memiliki izin untuk mengakses sumber daya ini.

    - 404 
    (TIDAK DITEMUKAN) : Sumber daya tidak dapat ditemukan saat ini. Mungkin sudah dihapus, atau belum ada.

    - 500 (INTERNAL SERVER ERROR) :  kegagalan tak terduga jika tidak ada informasi lebih spesifik yang tersedia.

<hr>

## __Intro Node JS__

- Node.js merupakan platform JavaScript yang dapat berjalan di backend atau server-side, di komputer kita secara langsung.

- Node REPL membuat kita bisa langsung menggunakan dan mengeksekusi kode Javascript dengan menjalankan node di terminal.

- Node memiliki beberapa variabel global yang dapat diakses dan dimodifikasi, seperti global, process

- Biasanya variabel process.env sering digunakan untuk menyimpan configuration ataupun credentials yang sifatnya rahasia, yang bisa digunakan di dalam aplikasi.

- NodeJS punya beberapa Module Built-in yang bisa langsung kita pakai sesuai kebutuhan aplikasi NodeJS kita.

- Kita juga bisa mengimport module built-in tersebut, ataupun Package module yang yang kita buat sendiri nantinya.

- NPM atau (Node Package Manager) adalah package dan dependency manager utama pada NodeJS dan merangkap sebagai website, registry, platform dan ekosistem Node.

- Dependency adalah suatu unsur metode untuk memisahkan dan mengintegrasikan berbagai program berbeda menjadi program yang utuh.

## __Express JS__

- kerangka aplikasi web back end untuk Node.js, dirilis sebagai perangkat lunak sumber terbuka dan gratis di bawah Lisensi MIT. Ini dirancang untuk membangun aplikasi web dan API. Ini telah disebut sebagai kerangka kerja server standar de facto untuk Node.js.

- Back end app adalah aplikasi yang berjalan di server-side yang bekerja untuk memberikan informasi berupa data sesuai request dari client / browser / front end app. Umumnya server-side app membuat REST API

- RESTful API / REST API merupakan penerapan dari API (Application Programming Interface). 

- Sedangkan REST (Representional State Transfer) adalah sebuah arsitektur metode komunikasi yang menggunakan protokol HTTP untuk pertukaran data dimana metode ini sering diterapkan dalam pengembangan aplikasi. Dengan tujuannya untuk menjadikan sistem memiliki performa yang baik, cepat dan mudah untuk di kembangkan (scale) terutama dalam pertukaran dan komunikasi data.

- RESTFUL API memiliki 4 komponen penting yaitu:

    - URL Design
    - HTTP Verbs
    - HTTP Response Code
    - Format Response

- Express Middleware adalah sebuah fungsi yang memiliki akses ke object request (req), object response (res), dan sebuah fungsi next didalam request-response cycle.

- Yang Bisa Dilakukan Oleh Function Middleware :
    - Menjalankan kode apapun.
    - Memodifikasi Object Request dan Object Response.
    - Menghentikan request-response cycle.
    - Melanjutkan ke middleware function selanjutnya atau ke handler function dalam suatu request response cycle.

- Express Middleware dapat dikelompokkan berdasarkan dari dimana middleware function itu digunakan :

    - Application Level Middleware
    - Router Level Middleware
    - Error Handling Middleware

- Express Middleware dapat juga dikelompokkan berdasarkan dari dimana middleware function itu didapatkan :

    - Express Build-in Middleware
    - Third Party (custom) Middleware

- Express JS sudah menyediakan 3 buah build-in middleware function yang bisa digunakan :

    - express.static()
    - express.json()
    - express.urlEncoded()

## __Design Database With MySQL__

- langkah - langkah membuat design database :

1. Menentukan Entity
    - mengidentifikasi entity dalam database.

    - Beberapa kandidat yang paling sering menjadi sebuah entity : peoples, things, events, locations

    -  Mulai list entity yang ada.

    - Berikut adalah kandidat yang bisa dijadikan enitity dalam database :
    User,Singer,Track,Album,Playlist

2. Menentukan Atribbutes dari Entity

   -  menentukanattributes apa saja yang akan datanya kita simpan di dalam sebuah entity.

   - Attributes yang di perlukan didalam entity kemungkinan sudah ada di dalam requirements document, atau mungkin juga diperlukan penafsiran kita sendiri sebagai database developer.

3. Menentukan Relasi Antar Entity

4. Membuat SQL Table dari Entity

    Setelah punya ERD, maka kita akan lanjut dengan create table berdasarkan dengan data yang kita punya.

<hr>











