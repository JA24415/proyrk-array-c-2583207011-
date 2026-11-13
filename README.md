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

<img width="868" height="903" alt="WhatsApp Image 2026-11-12 at 12 49 56 (1)" src="https://github.com/user-attachments/assets/3d0a2197-eb77-495d-bc08-2f8f99ae1b66" />


2. Skenario Transaksi Penjualan

<img width="972" height="832" alt="WhatsApp Image 2026-11-12 at 12 49 58 (2)" src="https://github.com/user-attachments/assets/3b4d1da9-7d9d-43e1-b499-7ef47d1aa37f" />
<img width="852" height="940" alt="WhatsApp Image 2026-11-12 at 12 49 58 (1)" src="https://github.com/user-attachments/assets/76a65693-8816-4204-b5b2-18270b5b3383" />



Bukti Tangkapan Layar:


3. Skenario Pembaruan Stok Otomatis

T<img width="868" height="903" alt="WhatsApp Image 2026-11-12 at 12 49 56 (1)" src="https://github.com/user-attachments/assets/17604023-708c-4a25-9c11-cede103fbe1e" />


4. Skenario Validasi Stok Tidak Cukup

![Uploading WhatsApp Image 2026-11-12 at 12.49.57 (2).jpeg…]()
![Uploading WhatsApp Image 2026-11-12 at 12.49.57 (2).jpeg…]()
<img width="849" height="730" alt="WhatsApp Image 2026-11-12 at 12 49 57 (3)" src="https://github.com/user-attachments/assets/fcda0e0d-fc89-4ead-b58b-45c5dea6359e" />




5. Skenario Laporan Penjualan

Tindakan / Input: Memilih menu 8. Laporan Penjualan.

<img width="972" height="832" alt="WhatsApp Image 2026-11-12 at 12 49 58 (2)" src="https://github.com/user-attachments/assets/ec973625-8487-405e-9737-2c68031d392d" />
<img width="1066" height="904" alt="WhatsApp Image 2026-11-12 at 12 49 57" src="https://github.com/user-attachments/assets/cd3d0c19-299b-4a15-9b86-9eb79742213e" />



6. Skenario Pengurutan Produk

<img width="1066" height="904" alt="WhatsApp Image 2026-11-12 at 12 49 57" src="https://github.com/user-attachments/assets/82414f3e-fceb-412d-8b1e-1bd46af4a2a3" />
<img width="1054" height="886" alt="WhatsApp Image 2026-11-12 at 12 49 57 (1)" src="https://github.com/user-attachments/assets/cc51a65c-04c7-4554-9a67-6dea5c3a13ff" />
<img width="1054" height="886" alt="WhatsApp Image 2026-11-12 at 12 49 57 (4)" src="https://github.com/user-attachments/assets/9a64c112-ba43-4535-8e4e-7d31faf0fc47" />




7. Skenario Pencarian Produk dan Cek Stok Menipis (< 5)

<img width="877" height="583" alt="WhatsApp Image 2026-11-12 at 13 03 37" src="https://github.com/user-attachments/assets/251898f9-383c-4887-8cb9-f67fd9a73d93" />
<img width="870" height="279" alt="WhatsApp Image 2026-11-12 at 13 03 50" src="https://github.com/user-attachments/assets/7f5333bd-d131-4679-a6b7-408078d43619" />
<img width="904" height="708" alt="WhatsApp Image 2026-11-12 at 12 49 58 (3)" src="https://github.com/user-attachments/assets/6cbe8d62-4f74-4564-bfea-249717745151" />
<img width="868" height="903" alt="WhatsApp Image 2026-11-12 at 12 49 56 (2)" src="https://github.com/user-attachments/assets/8bb3d6b4-1b7d-45db-b454-2cebf5de1c8c" />

