Nama Lengkap : Jana abdullah

NIM :C 2583207011

Kelas: Pti A 

Mata Kuliah : Algoritma dan Pemrograman Lanjutan

Dosen Pengampu : Taofik Muhammad, M.Kom

Deskripsi Proyek

Pengelolaan kantin kampus yang dilakukan secara manual sering kali menyulitkan pengelola dalam memantau sisa stok barang, menghitung total transaksi multi-produk dengan cepat, serta mengetahui produk mana yang paling diminati.

Aplikasi ini hadir sebagai solusi berbasis Command Line Interface (CLI) yang menyimpan dan mengolah data secara dinamis selama program berjalan (in-memory), dengan menerapkan struktur data Array sebagai fondasi utama penyimpanan data.

Fitur Utama Program

Lihat Daftar Produk: Menampilkan seluruh daftar produk yang tersedia beserta harga, sisa stok, dan jumlah yang telah terjual.

Tambah Produk Baru: Menambahkan item produk baru ke dalam daftar (hingga kapasitas maksimal 50 produk).

Ubah Data Produk: Memperbarui harga dan jumlah stok dari produk yang sudah terdaftar.

Transaksi Penjualan Multi-Produk: Memproses pembelian beberapa jenis produk sekaligus dalam satu transaksi, menghitung subtotal serta total pembayaran, dan otomatis mengurangi stok serta menambah catatan penjualan.

Tambah Stok: Menambahkan jumlah stok pada produk tertentu.

Cari Produk: Mencari produk berdasarkan kata kunci nama produk.

Urutkan Produk: Mengurutkan daftar produk berdasarkan harga termurah atau berdasarkan jumlah penjualan terbanyak (menggunakan algoritma Bubble Sort).

Laporan Penjualan: Menampilkan rincian pendapatan per produk, total unit terjual keseluruhan, total pendapatan kantin, dan produk paling laris.

Cek Stok Menipis: Memberikan peringatan dini dengan menampilkan daftar produk yang memiliki sisa stok kurang dari 5 unit.

Penerapan Struktur Data Array

Sesuai dengan ketentuan proyek, program ini menggunakan struktur data Array (tanpa database atau file eksternal) dengan kapasitas maksimal MAX_PRODUK = 50 dan 5 data produk awal:

Array Karakter Dua Dimensi (char namaProduk[50][50]): Digunakan untuk menyimpan daftar nama-nama produk (maksimal 50 produk, dengan masing-masing panjang nama hingga 49 karakter).

Array Satu Dimensi (int hargaProduk[50]): Digunakan untuk menyimpan harga satuan dari setiap produk sesuai indeksnya.

Array Satu Dimensi (int stokProduk[50]): Digunakan untuk mencatat jumlah ketersediaan stok terkini dari masing-masing produk.

Array Satu Dimensi (int terjualProduk[50]): Digunakan untuk mengakumulasi total unit yang berhasil terjual pada setiap transaksi untuk masing-masing produk.

Petunjuk Kompilasi dan Menjalankan Program

1. Menggunakan Compiler GCC (Terminal / VS Code / Code::Blocks)

Buka terminal pada direktori tempat file main.c disimpan, lalu jalankan perintah berikut untuk mengompilasi:

gcc main.c -o program_kantin


Setelah berhasil dikompilasi tanpa error, jalankan program dengan perintah:

Windows:

.\program_kantin.exe


Linux / macOS:

./program_kantin


2. Menggunakan kode block

Pastikan file kode sudah ditulis menggunakan magic command %%writefile main.c dan dijalankan pada sel pertama.

Kompilasi program pada sel baru:

!gcc main.c -o program_kantin


Jalankan program pada sel berikutnya:

!./program_kantin


Dokumentasi Skenario Pengujian

Berikut adalah hasil pengujian program berdasarkan 7 skenario wajib yang telah ditentukan:

1. Skenario Tambah Produk

Tindakan / Input: Memilih menu 2. Tambah Produk dan memasukkan data produk baru (misalnya:es teh tawar, Harga: 8000, Stok: 15).

Hasil yang Diharapkan: Produk baru berhasil disimpan ke dalam array dan muncul saat menampilkan daftar produk.

Bukti Tangkapan Layar:


2. Skenario Transaksi Penjualan

Tindakan / Input: Memilih menu 4. Transaksi Penjualan dan membeli lebih dari satu jenis produk dalam satu sesi transaksi.

Hasil yang Diharapkan: Program menampilkan rincian belanja, menghitung subtotal setiap item, dan menjumlahkan total pembayaran dengan akurat.

Bukti Tangkapan Layar:


3. Skenario Pembaruan Stok Otomatis

Tindakan / Input: Menyelesaikan transaksi pada skenario 2, lalu memeriksa menu 1. Lihat Daftar Produk.

Hasil yang Diharapkan: Stok produk yang dibeli berkurang sesuai jumlah pembelian, dan kolom terjual bertambah.

Bukti Tangkapan Layar:


4. Skenario Validasi Stok Tidak Cukup

Tindakan / Input: Melakukan transaksi dengan jumlah pembelian yang melebihi sisa stok yang tersedia.

Hasil yang Diharapkan: Program menolak transaksi, menampilkan pesan peringatan bahwa stok tidak mencukupi, dan sisa stok tidak berubah.

Bukti Tangkapan Layar:


5. Skenario Laporan Penjualan

Tindakan / Input: Memilih menu 8. Laporan Penjualan.

Hasil yang Diharapkan: Menampilkan rincian pendapatan tiap produk, akumulasi total unit terjual, total pendapatan keseluruhan, serta menampilkan produk paling laris.

Bukti Tangkapan Layar:


6. Skenario Pengurutan Produk

Tindakan / Input: Memilih menu 7. Urutkan Produk untuk mengurutkan berdasarkan harga termurah (opsi 1) dan penjualan terbanyak (opsi 2).

Hasil yang Diharapkan: Data produk ditampilkan secara terurut sesuai kriteria yang dipilih tanpa merusak indeks data asli.

Bukti Tangkapan Layar:


7. Skenario Pencarian Produk dan Cek Stok Menipis (< 5)

Tindakan / Input: Memilih menu 6. Cari Produk dengan memasukkan kata kunci nama produk, serta memilih menu 9. Cek Stok Menipis.

Hasil yang Diharapkan: Pencarian menampilkan produk yang cocok dengan kata kunci, dan fitur cek stok menipis menampilkan produk yang stoknya berada di bawah 5 unit (seperti Bakso Kuah dengan stok awal 4).
