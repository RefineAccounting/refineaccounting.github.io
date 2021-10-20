---
layout: post
title: Mengelola Data Pembelian
---

**Penjelasan Singkat**

Di halaman ini kami akan memandu Anda untuk mengelola data-data pembelian. Berikut daftar isi
mengelola data pembelian dengan Refine Accounting

1. [Pesanan Pembelian](#pesanan-pembelian)
1. [Laporan Penerimaan Barang](#penerimaan-barang)
1. [Faktur Pembelian](#faktur-pembelian)
1. [Surat Jalan Retur](#surat-jalan-retur)
1. [Retur Pembelian](#retur-pembelian)
1. [Hutang Usaha](#hutang-usaha)
1. [Uang Muka Pembelian](#uang-muka-pembelian)
1. [Deposit Supplier](#deposit-supplier)

**Kumpulan Video**

1. [Alur Sistem Pembelian](https://youtu.be/eNGoXnzBtDo)
2. [Menu Pesanan Pembelian](https://youtu.be/wpgVBN1hA0E)
3. [Menu Penerimaan Barang](https://youtu.be/s6ieqLwrWv4)
4. [Menu Faktur Pembelian](https://youtu.be/8Wa8vJq-Ka8)

# Alur Sistem

Sebelum masuk ke teknis cara input, di bagian ini kami akan menjelaskan beberapa alur sistem untuk memudahkan Anda memahami bagaimana memulai input di modul pembelian.

Ada 2 penjelasan alur sistem yaitu alur sistem pembelian dan alur sistem uang muka pembelian.

## Alur Sistem Pembelian

**Penjelasan**

Alur sistem pembelian pada Refine Accounting ada 2 garis besar. Pertama menggunakan sistem pemesanan dimana setiap penerimaan barang / faktur pembelian harus didasarkan pada sebuah dokumen pesanan. Kedua tanpa menggunakan sistem pemesanan.

Untuk sistem pertama **dengan sistem pesanan pembelian ke supplier** sebagai berikut:

1. Admin pembelian mengirimkan permintaan harga atas beberapa barang.
2. Admin pembelian menyetujui harga dan **input pesanan pembelian (PO)** kepada supplier X dan barang-barang yang akan dipesan.
3. PO ini dikirimkan ke supplier untuk diproses.
4. Pengiriman barang dari supplier masuk ke bagian Gudang. Gudang menerima barang beserta dengan surat jalan dari supplier.
5. Pihak Gudang melakukan pencocokan data antara SJ & PO. Jika sudah cocok, pihak Gudang melakukan **input laporan penerimaan barang (LPB)** dan secara otomatis sistem akan **membuat faktur pembelian (FB)** dan **mutasi masuk pada persediaan**.

Sedangkan, untuk sistem kedua **tanpa sistem pesanan ke supplier** sebagai berikut:

1. Admin pembelian melakukan **input faktur pembelian** ke supplier X dan barang-barang yang akan dibeli, secara otomatis sistem akan membuat **mutasi masuk pada persediaan**. Disini perbedaannya sistem tidak dapat melakukan pengecekan kebenaran qty dipesan dan diterima jadi ada resiko qty diterima berbeda dengan yang dipesan.

## Alur Sistem Uang Muka Pembelian

**Penjelasan**

Alur sistem uang muka pembelian pada Refine Accounting adalah sebagai berikut:

1. Admin pembelian **input pesanan pembelian (PO)** kepada supplier X dan barang-barang yang akan dipesan.
1. Pesanan pembelian kemudian harus **disetujui**
1. Admin pembelian membuat nota **Uang Muka Pembelian** pada menu [uang muka pembelian](#uang-muka-pembelian)
1. Pihak keuangan melakukan pelunasan **Uang Muka Pembelian**.
1. Selanjutnya setelah faktur pembelian terbuat, Anda dapat menggunakan uang muka pembelian sebagai pembayaran.

## Pesanan Pembelian

### Aktivitas Utama

1. **Buat pesanan pembelian:** Cara membuat pesanan pembelian yaitu klik menu Pembelian > Pesanan Pembelian. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. **Ubah pesanan pembelian:** Jika ada kesalahan untuk merubah data. Cari data yang ingin di ubah dalam `Daftar Pesanan Pembelian` setelah itu klik aksi `Ubah` yang terdapat pada ujung kanan data tersebut.
3. **Menyetujui pesanan pembelian:** Aksi ini digunakan untuk menyetujui pesanan pembelian yang sudah dibuat.
4. **Menutup pesanan pembelian:** Aksi ini digunakan untuk menutup pesanan pembelian meskipun barang belum diterima secara keseluruhan. Untuk menutup pesanan pembelian klik menu Pembelian > Pesanan Pembelian. Pada daftar pesanan pembelian, di bagian kanan terdapat kolom `Aksi` dan tombol `Tutup`. Klik tombol `Tutup` untuk menutup pesanan pembelian tersebut.
5. **Hapus pesanan pembelian:** Pesanan pembelian hanya bisa dihapus jika status `Pending`.

### Penjelasan Kolom pada Form Pesanan Pembelian

1. `Supplier` adalah supplier pesanan pembelian. Supplier Pesanan Pembelian & Penerimaan Barang harus sama.
2. `No. Dokumen` adalah nomor dokumen pesanan pembelian. Terbuat otomatis dan reset setiap bulan.
3. `Tanggal` adalah tanggal pesanan pembelian. Jika merubah tanggal pesanan yang sudah dibuat dan tanggal berbeda bulan,
   maka sistem **secara otomatis merubah** nomor dokumen mengikuti urutan nomor pada bulan tersebut.
4. `Catatan` untuk menulis catatan-catatan pada pesanan pembelian
5. `Status` ada 3 macam: _PENDING_, _APPROVED_, _RECEIVED_, _CLOSED_. Daftar pesanan pembelian tersambung pada menu Laporan Penerimaan Barang **hanya jika** status _APPROVED_.
6. `Daftar Barang` terdiri dari nama produk, kuantitas, satuan, harga satuan, disc (%), disc (Rp) dan subtotal
7. `Diskon`
8. `PPN` kolom ini terisi otomatis jika status supplier adalah PKP. (Mohon melihat bagian master data untuk penjelasan lebih detail)
9. `Biaya Pengiriman`

### Penjelaan Status

1. PENDING / MENUNGGU adalah PO baru dibuat dan menunggu verifikasi
2. APPROVED / DISETUJUI adalah PO sudah disetujui dan terhubung dengan menu Laporan Penerimaan Barang
3. RECEIVED / DITERIMA adalah seluruh item dalam PO sudah diterima
4. CLOSED / DITUTUP adalah PO ditutup secara sengaja, bisa sebagian / tidak ada item yang diterima dan memutus hubungan dengan menu Laporan Penerimaan Barang.

## Laporan Penerimaan Barang

### Aktivitas Utama

1. **Buat penerimaan barang:** Cara membuat penerimaan barang yaitu klik menu Pembelian > Laporan Penerimaan Barang. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. **Ubah penerimaan barang:** Aksi ini untuk merubah informasi penerimaan barang.
    - Penerimaan barang hanya bisa diubah jika status pembayaran atas faktur pembelian adalah menunggu pembayaran (`Pending`).
    - Untuk merubah penerimaan barang, cari data yang ingin diubah di daftar laporan penerimaan barang setelah itu klik tombol `Ubah` yang terdapat pada kolom aksi.
3. **Hapus penerimaan barang:** Penerimaan barang dapat dihapus jika status pembayaran terhadap faktur pembelian adalah menunggu pembayaran (`Pending`).

### Penjelasan Kolom pada Form Laporan Penerimaan Barang

1. `Supplier` ketika memilih supplier, secara otomatis sistem akan mengambil seluruh Pesanan Pembelian dengan supplier tersebut dan status Pesanan Pembelian adalah _APPROVED_.
1. `Gudang` adalah gudang penerima barang. Sistem akan mencatat mutasi persediaan masuk pada gudang tersebut.
1. `No. Dokumen` adalah nomor dokumen penerimaan barang. Terbuat otomatis dan reset setiap bulan.
1. `Tanggal` adalah tanggal penerimaan barang. Jika merubah tanggal yang sudah dibuat dan tanggal berbeda bulan,
   maka sistem **secara otomatis merubah** nomor dokumen mengikuti urutan nomor pada bulan tersebut.
1. `Catatan` untuk menulis catatan-catatan pada pesanan pembelian
1. `Daftar Barang` terdiri dari tanggal pesanan pembelian, nomor pesanan pembelian, info produk, kuantitas dipesan, kuantitas terpenuhi, kuantitas diterima.

## Faktur Pembelian

### Aktivitas Utama

1. **Buat faktur pembelian:**
    - Jika menggunakan sistem pesanan, maka Faktur Pembelian otomatis terbuat jika membuat Laporan Penerimaan Barang.
    - Jika tidak menggunakan sistem pesanan, Anda dapat membuat faktur pembelian. Klik menu Pembelian > Faktur Pembelian. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. **Ubah faktur pembelian:** Aksi ini untuk merubah informasi faktur pembelian.
    - Faktur pembelian dapat dihapus jika status pembayaran adalah belum dibayar (`Pending`).
    - Untuk merubah faktur pembelian, cari data yang ingin diubah di daftar faktur pembelian setelah itu klik tombol `Ubah` yang terdapat pada kolom aksi.
3. **Hapus faktur pembelian:** Aksi ini untuk menghapus faktur pembelian. Faktur pembelian dapat dihapus jika status pembayaran adalah belum dibayar (`Pending`).

### Penjelasan Kolom pada Form Faktur Pembelian

1. `Supplier` adalah supplier untuk faktur pembelian tersebut.
1. `Gudang` adalah gudang penerima barang. Sistem akan mencatat mutasi persediaan masuk pada gudang tersebut.
1. `No. Dokumen` adalah nomor dokumen faktur pembelian. Terbuat otomatis dan reset setiap bulan.
1. `Tanggal` adalah tanggal faktur pembelian. Jika merubah tanggal yang sudah dibuat dan tanggal berbeda bulan,
   maka sistem **secara otomatis merubah** nomor dokumen mengikuti urutan nomor pada bulan tersebut.
1. `Catatan` untuk menulis catatan-catatan pada pesanan pembelian
1. `Daftar Barang` terdiri dari nama produk, kuantitas, satuan, harga satuan, disc (%), disc (Rp), subtotal.
1. `Diskon`
1. `PPN` kolom ini terisi otomatis jika status supplier adalah PKP. (Mohon melihat bagian master data untuk penjelasan lebih detail)
1. `Biaya Pengiriman`. Biaya pengiriman disini akan menambahkan HPP persediaan yang masuk.
1. `Informasi Lainnya` terdiri dari No. Faktur Supplier, No. Faktur Pajak, Tgl Faktur Supplier dan Tgl Jatuh Tempo.

### Penjelaan Status

1. PENDING / MENUNGGU adalah Faktur Pembelian baru dibuat dan menunggu pembayaran ke supplier
2. PAID / LUNAS adalah Faktur Pembelian telah lunas dibayar ke supplier

## Surat Jalan Retur Pembelian

### Aktivitas Utama

1. **Buat surat jalan retur:** Klik menu Pembelian > Surat Jalan Retur. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. **Ubah surat jalan retur:** Aksi ini untuk merubah informasi surat jalan retur.
    - Surat jalan retur hanya bisa diubah jika status pembayaran atas nota retur pembelian adalah menunggu pembayaran (`Pending`).
    - Untuk merubah surat jalan retur, cari data yang ingin diubah di daftar surat jalan retur setelah itu klik tombol `Ubah` yang terdapat pada kolom aksi.
3. **Hapus surat jalan retur:** Aksi ini untuk menghapus surat jalan retur. Surat jalan retur hanya bisa dihapus jika status pembayaran atas nota retur pembelian adalah menunggu pembayaran (`Pending`).

### Penjelasan Kolom pada Form Surat Jalan Retur Pembelian

1. `Supplier` adalah supplier retur pembelian.
1. `Gudang` adalah gudang sumber barang keluar.
1. `No. Dokumen` adalah nomor dokumen surat jalan retur. Terbuat otomatis dan reset setiap bulan.
1. `Tanggal` adalah tanggal surat jalan retur. Jika merubah tanggal pesanan yang sudah dibuat dan tanggal berbeda bulan,
   maka sistem **secara otomatis merubah** nomor dokumen mengikuti urutan nomor pada bulan tersebut.
1. `Catatan` untuk menulis catatan-catatan pada pesanan pembelian
1. `Daftar Penerimaan Barang` terdiri nomor penerimaan barang, informasi barang diterima, kuantitas penerimaan barang, kuantitas telah diretur, kuantitas yang akan diretur saat ini dan satuan.
1. Tombol `Tambah No. Penerimaan Barang` untuk menambahkan barang yang akan diretur.

## Retur Pembelian

### Aktivitas Utama

1. **Buat retur pembelian:** Klik menu Pembelian > Retur Pembelian. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. **Ubah retur pembelian:** Aksi ini untuk merubah informasi retur pembelian.
    - Retur pembelian hanya bisa diubah jika status pembayaran adalah menunggu pembayaran (`Pending`).
    - Untuk merubah retur pembelian, cari data yang ingin diubah di daftar retur penjualan setelah itu klik tombol `Ubah` yang terdapat pada kolom aksi.
3. **Hapus retur pembelian:** Aksi ini untuk menghapus retur pembelian. Retur pembelian hanya bisa dihapus jika status pembayaran adalah menunggu pembayaran (`Pending`).

### Penjelasan Kolom pada Form Retur Pembelian

1. `Supplier` adalah supplier retur pembelian.
1. `Gudang` adalah gudang sumber barang keluar.
1. `No. Dokumen` adalah nomor dokumen surat jalan retur. Terbuat otomatis dan reset setiap bulan.
1. `Tanggal` adalah tanggal surat jalan retur. Jika merubah tanggal pesanan yang sudah dibuat dan tanggal berbeda bulan,
   maka sistem **secara otomatis merubah** nomor dokumen mengikuti urutan nomor pada bulan tersebut.
1. `Catatan` untuk menulis catatan-catatan pada retur pembelian
1. `Daftar Penerimaan Barang` terdiri nomor penerimaan barang, informasi barang diterima, kuantitas penerimaan barang, kuantitas telah diretur, kuantitas yang akan diretur saat ini, satuan dan harga satuan.
1. Tombol `Tambah No. Penerimaan Barang` untuk menambahkan barang yang akan diretur.

### Penjelaan Status

1. PENDING / MENUNGGU adalah Retur Pembelian baru dibuat dan menunggu pelunasan
2. PAID / LUNAS adalah Retur Pembelian telah lunas dibayar

**Note**
Sistem retur yang kami gunakan adalah pengurangan nilai Hutang.

## Hutang Usaha

**Penjelasan**
Menu ini digunakan untuk memantau daftar hutang usaha yang masih menunggu pembayaran. Menu ini secara otomatis akan 2 sumber hutang usaha yaitu `Faktur Pembelian` dan `Retur Pembelian`, Anda **tidak dapat menambahkan hutang usaha** di menu ini.

Penjelasan kolom di daftar hutang usaha:

-   `Tanggal` adalah tanggal faktur pembelian / retur pembelian
-   `Kode Transaksi` adalah nomor nota pembelian / nota retur pembelian
-   `Faktur Pembelian` adalah nilai faktur pembelian
-   `Hutang` adalah nilai sisa hutang
-   `Tanggal Jatuh Tempo` adalah tanggal jatuh tempo hutang usaha

Ada beberapa filter yang dapat Anda gunakan untuk memudahkan pencarian sebagai berikut:

-   `Supplier` saring untuk melihat daftar hutang berdasarkan supplier
-   `Tanggal` saring untuk melihat daftar hutang dalam periode tertentu

## Uang Muka Pembelian

### Aktivitas Utama

1. **Buat uang muka pembelian:** Klik menu Pembelian > Uang Muka Pembelian. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. **Ubah uang muka pembelian:** Aksi ini untuk merubah informasi uang muka pembelian.
    - Uang muka pembelian hanya bisa diubah jika status pembayaran adalah menunggu pembayaran (`Pending`).
    - Untuk merubah uang muka pembelian, cari data yang ingin diubah di daftar uang muka pembelian setelah itu klik tombol `Ubah` yang terdapat pada kolom aksi.
3. **Hapus uang muka pembelian:** Aksi ini untuk menghapus uang muka pembelian. Uang muka pembelian hanya bisa dihapus jika status pembayaran adalah menunggu pembayaran (`Pending`).
4. **Gunakan uang muka pembelian:** Aksi ini untuk menggunakan uang muka sebagai pembayaran Faktur Pembelian. Tekan tombol `gunakan` di kolom aksi untuk melihat daftar faktur pembelian dari Uang Muka tersebut, kemudian pilih faktur pembelian yang ingin dibayarkan.

### Penjelasan Kolom pada Form Uang Muka Pembelian

1. `Supplier` adalah supplier yang akan melakukan transaksi uang muka pembelian.
1. `Daftar Pesanan Pembelian` adalah pesanan pembelian dari supplier tersebut.
1. `No. Dokumen` adalah nomor dokumen surat jalan retur. Terbuat otomatis dan reset setiap bulan.
1. `Tanggal` adalah tanggal surat jalan retur. Jika merubah tanggal pesanan yang sudah dibuat dan tanggal berbeda bulan,
   maka sistem **secara otomatis merubah** nomor dokumen mengikuti urutan nomor pada bulan tersebut.
1. `Catatan` untuk menulis catatan-catatan pada uang muka pembelian
1. `Jumlah Uang Muka %` nominal uang muka dalam persentase %.
1. `Jumlah Uang Muka` nominal uang muka dalam rupiah.

### Penjelasan Status

1. PENDING / MENUNGGU adalah Uang Muka Pembelian baru dibuat dan menunggu pelunasan
2. PAID / LUNAS adalah Uang Muka Pembelian telah lunas dibayar
