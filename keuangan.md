---
layout: post
title: Mengelola Keuangan
---

**Penjelasan Singkat**

Modul keuangan digunakan untuk mencatat seluruh arus kas dalam perusahaan. Ada beberapa fitur kunci dalam modul keuangan yang kami sediakan untuk memenuhi kebutuhan perusahaan Anda, fitur-fitur tersebut sebagai berikut:

1. [Transaksi Masuk](#transaksi-masuk)
1. [Transaksi Keluar](#transaksi-keluar)
1. [Pemindahbukuan](#pemindahbukuan)
1. [Giro Diterima](#giro-diterima)
1. [Giro Dibuka](#giro-dibuka)
1. [Mutasi Kas](#mutasi-kas)
1. [Mutasi Bank](#mutasi-bank)

**Kumpulan Video**
Berikut ini kumpulan video untuk mengelola keuangan

## Transaksi Masuk

Tujuan dari fitur ini adalah mencatat transaksi masuk, ada beberapa jenis transaksi masuk: Kas / Bank / Giro. Dalam transaksi masuk dapat dibagi menjadi beberapa kategori transaksi.

-   `Pelunasan Piutang` jenis penerimaan ini secara otomatis mengambil data faktur penjualan yang belum lunas
-   `Pelunasan Uang Muka Penjualan` jenis penerimaan ini secara otomatis mengambil data faktur uang muka penjualan yang belum lunas.
-   `Lain-lain` ada kalanya Anda menerima transaksi masuk dari transaksi lainnya. Dimana Anda harus menentukan COA lawan transaksi ini.

Kategori transaksi ini semua dapat Anda input di form transaksi masuk. Untuk cara input tiap-tiap kategori transaksi tersebut akan kami jelaskan di bagian selanjutnya.

### Pelunasan Piutang

1.  `Jenis Transaksi Masuk` pilih tipe transaksi masuk: Kas / Bank / Giro.
    -   Jika pembayaran Giro, pada kolom `No. Giro` isi dengan nomor giro diterima dan `Tanggal Jatuh Tempo Giro` isi dengan estimasi tanggal jatuh tempo giro.
2.  `COA Cash/Bank` pilih akun kas / bank penerima transaksi masuk.
3.  `Pelanggan` pelanggan yang melakukan pembayaran piutang.
4.  `Tanggal` adalah tanggal transaksi
5.  `Catatan` catatan untuk transaksi tersebut.
6.  klik tombol `Pembayaran Piutang`, kemudian akan muncul popup daftar faktur penjualan dan retur penjualan yang belum lunas. Pilih faktur penjualan dan isi nominal pembayaran (default adalah pembayaran penuh). Anda juga dapat memilih retur penjualan jika dalam pembayaran faktur ini dikurangi dengan nilai returnya.
7.  Kemudian klik simpan.
8.  Klik tombol `COA Lain-lain` jika di dalam pembayaran ini terdapat biaya-biaya yang menambah atau mengurangi nilai pembayaran pelunasan. Kemudian klik simpan.
9.  Pastikan pada kolom `Total` adalah nominal pembayaran yang Anda terima di rekening bank / kas Anda.

### Pelunasan Uang Muka Penjualan

1.  `Jenis Transaksi Masuk` pilih tipe transaksi masuk: Kas / Bank / Giro.
    -   Jika pembayaran Giro, pada kolom `No. Giro` isi dengan nomor giro diterima dan `Tanggal Jatuh Tempo Giro` isi dengan estimasi tanggal jatuh tempo giro.
2.  `COA Cash/Bank` pilih akun kas / bank penerima transaksi masuk.
3.  `Pelanggan` pelanggan yang melakukan pembayaran piutang.
4.  `Tanggal` adalah tanggal transaksi
5.  `Catatan` catatan untuk transaksi tersebut.
6.  klik tombol `Pembayaran Uang Muka Penjualan`, kemudian akan muncul popup daftar nota uang muka penjualan yang belum lunas.
7.  Kemudian klik simpan.
8.  Klik tombol `COA Lain-lain` jika di dalam pembayaran ini terdapat biaya-biaya yang menambah atau mengurangi nilai pembayaran pelunasan. Kemudian klik simpan.
9.  Pastikan pada kolom `Total` adalah nominal pembayaran yang Anda terima di rekening bank / kas Anda.

### Penerimaan Uang dari Transaksi Lainnya

1.  `Jenis Transaksi Masuk` pilih tipe transaksi masuk: Kas / Bank / Giro.
    -   Jika pembayaran Giro, pada kolom `No. Giro` isi dengan nomor giro diterima dan `Tanggal Jatuh Tempo Giro` isi dengan estimasi tanggal jatuh tempo giro.
2.  `COA Cash/Bank` pilih akun kas / bank penerima transaksi masuk.
3.  `Tanggal` adalah tanggal transaksi
4.  `Catatan` catatan untuk transaksi tersebut.
5.  Klik tombol `COA Lain-lain` dan pilih akun COA sebagai lawan transaksi ini. Kemudian klik simpan.
6.  Pastikan pada kolom `Total` adalah nominal pembayaran yang Anda terima di rekening bank / kas Anda.

## Transaksi Keluar

Tujuan dari fitur ini adalah mencatat transaksi keluar, ada beberapa jenis transaksi keluar: Kas / Bank / Giro. Dalam transaksi keluar dapat dibagi menjadi beberapa kategori transaksi.

-   `Pelunasan Hutang` jenis penerimaan ini secara otomatis mengambil data faktur pembelian & retur pembelian yang belum lunas
-   `Pelunasan Uang Muka Pembelian` jenis penerimaan ini secara otomatis mengambil data faktur uang muka pembelian yang belum lunas.
-   `Lain-lain` ada kalanya Anda melakukan pembayaran untuk transaksi lainnya. Dimana Anda harus menentukan COA lawan transaksi ini.

Kategori transaksi ini semua dapat Anda input di form transaksi keluar. Untuk cara input tiap-tiap kategori transaksi tersebut akan kami jelaskan di bagian selanjutnya.

### Pelunasan Hutang

1.  `Jenis Transaksi Keluar` pilih tipe transaksi masuk: Kas / Bank / Giro.
    -   Jika pembayaran Giro, pada kolom `No. Giro` isi dengan nomor giro diterima dan `Tanggal Jatuh Tempo Giro` isi dengan estimasi tanggal jatuh tempo giro.
2.  `COA Cash/Bank` pilih akun kas / bank transaksi keluar.
3.  `Supplier` supplier yang melakukan pembayaran hutang.
4.  `Tanggal` adalah tanggal transaksi
5.  `Catatan` catatan untuk transaksi tersebut.
6.  klik tombol `Pembayaran Hutang`, kemudian akan muncul popup daftar faktur pembelian dan retur pembelian yang belum lunas. Pilih faktur pembelian dan isi nominal pembayaran (default adalah pembayaran penuh). Anda juga dapat memilih retur pembelian jika dalam pembayaran faktur ini dikurangi dengan nilai returnya.
7.  Kemudian klik simpan.
8.  Klik tombol `COA Lain-lain` jika di dalam pembayaran ini terdapat biaya-biaya yang menambah atau mengurangi nilai pembayaran pelunasan. Kemudian klik simpan.
9.  Pastikan pada kolom `Total` adalah nominal pembayaran yang Anda keluarkan dari rekening bank / kas Anda.

### Pelunasan Uang Muka Pembelian

1.  `Jenis Transaksi Masuk` pilih tipe transaksi masuk: Kas / Bank / Giro.
    -   Jika pembayaran Giro, pada kolom `No. Giro` isi dengan nomor giro diterima dan `Tanggal Jatuh Tempo Giro` isi dengan estimasi tanggal jatuh tempo giro.
2.  `COA Cash/Bank` pilih akun kas / bank penerima transaksi masuk.
3.  `Supplier` supplier yang melakukan pembayaran hutang.
4.  `Tanggal` adalah tanggal transaksi
5.  `Catatan` catatan untuk transaksi tersebut.
6.  klik tombol `Pembayaran Uang Muka Pembelian`, kemudian akan muncul popup daftar nota uang muka pembelian yang belum lunas.
7.  Kemudian klik simpan.
8.  Klik tombol `COA Lain-lain` jika di dalam pembayaran ini terdapat biaya-biaya yang menambah atau mengurangi nilai pembayaran pelunasan. Kemudian klik simpan.
9.  Pastikan pada kolom `Total` adalah nominal pembayaran yang Anda keluarkan dari rekening bank / kas Anda.

### Pengeluaran Uang untuk Transaksi Lainnya

1.  `Jenis Transaksi Masuk` pilih tipe transaksi masuk: Kas / Bank / Giro.
    -   Jika pembayaran Giro, pada kolom `No. Giro` isi dengan nomor giro diterima dan `Tanggal Jatuh Tempo Giro` isi dengan estimasi tanggal jatuh tempo giro.
2.  `COA Cash/Bank` pilih akun kas / bank penerima transaksi masuk.
3.  `Tanggal` adalah tanggal transaksi
4.  `Catatan` catatan untuk transaksi tersebut.
5.  Klik tombol `COA Lain-lain` dan pilih akun COA sebagai lawan transaksi ini. Kemudian klik simpan.
6.  Pastikan pada kolom `Total` adalah nominal pembayaran yang Anda keluarkan dari rekening bank / kas Anda.

## Pemindahbukuan

Pemindahbukuan atau transfer dapat diinput secara manual melalui transaksi masuk dan keluar dimana lawan transaksinya adalah COA ayat silang yang sudah Anda buat. Akan tetapi disini kami membuat form khusus untuk memudahkan Anda input transaksi pemindahbukuan. Penjelasan kolom pada form sebagai berikut:

-   `Akun Sumber` adalah kas / bank sumber pengirim dana.
-   `Akun Penerima` adalah kas / bank penerima dana.
-   `Jumlah` adalah nilai dana yang dipindahbukukan.
-   `Tanggal` adalah tanggal transaksi pindah buku.
-   `Catatan` untuk menambahkan catatan transaksi.
