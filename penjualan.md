---
layout: post
title: Mengelola Data Penjualan
---

**Penjelasan Singkat**

Di halaman ini kami akan memandu Anda untuk mengelola data-data penjualan. Berikut daftar isi
mengelola data penjualan dengan Refine Accounting

1. [Alur Sistem Penjualan](#alur-sistem-penjualan)
1. [Alur Sistem Uang Muka Penjualan](#alur-sistem-uang-muka-penjualan)
1. [Pesanan Penjualan](#pesanan-penjualan)
1. [Surat Jalan](#surat-jalan)
1. [Faktur Penjualan](#faktur-penjualan)
1. [Penerimaan Barang Retur](#penerimaan-barang-retur)
1. [Retur Penjualan](#retur-penjualan)
1. [Piutang Usaha](#piutang-usaha)
1. [Uang Muka Penjualan](#uang-muka-penjualan)
1. [Deposit Customer](#deposit-customer)

**Kumpulan Video**

1. [Alur Sistem Penjualan](https://youtu.be/eNGoXnzBtDo)
2. [Menu Pesanan Penjualan](https://youtu.be/wpgVBN1hA0E)
3. [Menu Penerimaan Barang](https://youtu.be/s6ieqLwrWv4)
4. [Menu Faktur Penjualan](https://youtu.be/8Wa8vJq-Ka8)

# Alur Sistem

Sebelum masuk ke teknis cara input, di bagian ini kami akan menjelaskan beberapa alur sistem untuk memudahkan Anda memahami bagaimana memulai input di modul penjualan.

Ada 2 penjelasan alur sistem yaitu alur sistem penjualan dan alur sistem uang muka penjualan.

## Alur Sistem Penjualan

**Penjelasan**

Alur sistem penjualan pada Refine Accounting ada 2 garis besar. Pertama menggunakan sistem pemesanan dimana setiap surat jalan / faktur penjualan harus didasarkan pada sebuah dokumen pesanan. Kedua tanpa menggunakan sistem pemesanan.

Untuk sistem pertama **dengan sistem pesanan penjualan dari customer** sebagai berikut:

1. Admin penjualan mengirimkan penawaran harga atas beberapa barang.
2. Admin penjualan menyetujui harga dan **input pesanan penjualan (SO)** kepada customer X dan barang-barang yang akan dipesan.
3. SO ini dikirimkan ke customer untuk diproses.
4. Pengiriman barang ke customer oleh bagian gudang, secara otomatis sistem akan **membuat faktur penjualan (INVOICE)** dan **mutasi masuk pada persediaan**.

Sedangkan, untuk sistem kedua **tanpa sistem pesanan dari customer** sebagai berikut:

1. Admin penjualan melakukan **input faktur penjualan** ke customer X dan barang-barang yang akan dijual, secara otomatis sistem akan membuat **mutasi masuk pada persediaan**. Disini perbedaannya sistem tidak dapat melakukan pengecekan kebenaran qty dipesan dan dikirim jadi ada resiko qty dikirim berbeda dengan yang dipesan.

## Alur Sistem Uang Muka Penjualan

**Penjelasan**

Alur sistem uang muka penjualan pada Refine Accounting adalah sebagai berikut:

1. Admin penjualan **input pesanan penjualan (SO)** kepada customer X dan barang-barang yang akan dipesan.
1. Pesanan penjualan kemudian harus **disetujui**
1. Admin penjualan membuat nota **Uang Muka Penjualan** pada menu [uang muka penjualan](#uang-muka-penjualan)
1. Pihak keuangan melakukan pelunasan **Uang Muka Penjualan**.
1. Selanjutnya setelah faktur penjualan terbuat, Anda dapat menggunakan uang muka penjualan sebagai pembayaran.

## Pesanan Penjualan

### Aktivitas Utama

1. **Buat pesanan penjualan:** Cara membuat pesanan penjualan yaitu klik menu Penjualan > Pesanan Penjualan. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. **Ubah pesanan penjualan:** Jika ada kesalahan untuk merubah data. Cari data yang ingin di ubah dalam `Daftar Pesanan Penjualan` setelah itu klik aksi `Ubah` yang terdapat pada ujung kanan data tersebut.
3. **Menyetujui pesanan penjualan:** Aksi ini digunakan untuk menyetujui pesanan penjualan yang sudah dibuat.
4. **Menutup pesanan penjualan:** Aksi ini digunakan untuk menutup pesanan penjualan meskipun barang belum diterima secara keseluruhan. Untuk menutup pesanan penjualan klik menu Penjualan > Pesanan Penjualan. Pada daftar pesanan penjualan, di bagian kanan terdapat kolom `Aksi` dan tombol `Tutup`. Klik tombol `Tutup` untuk menutup pesanan penjualan tersebut.
5. **Hapus pesanan penjualan:** Pesanan penjualan hanya bisa dihapus jika status `Pending`.

### Penjelasan Kolom pada Form Pesanan Penjualan

1. `Customer` adalah customer pesanan penjualan. Customer Pesanan Penjualan & Penerimaan Barang harus sama.
2. `No. Dokumen` adalah nomor dokumen pesanan penjualan. Terbuat otomatis dan reset setiap bulan.
3. `Tanggal` adalah tanggal pesanan penjualan. Jika merubah tanggal pesanan yang sudah dibuat dan tanggal berbeda bulan,
   maka sistem **secara otomatis merubah** nomor dokumen mengikuti urutan nomor pada bulan tersebut.
4. `Catatan` untuk menulis catatan-catatan pada pesanan penjualan
5. `Status` ada 3 macam: _PENDING_, _APPROVED_, _RECEIVED_, _CLOSED_. Daftar pesanan penjualan tersambung pada menu Surat Jalan **hanya jika** status _APPROVED_.
6. `Daftar Barang` terdiri dari nama produk, kuantitas, satuan, harga satuan, disc (%), disc (Rp) dan subtotal
7. `Diskon`
8. `PPN` kolom ini terisi otomatis jika status perusahaan adalah PKP.

### Penjelasan Status

1. PENDING / MENUNGGU adalah SO baru dibuat dan menunggu verifikasi
2. APPROVED / DISETUJUI adalah SO sudah disetujui dan terhubung dengan menu Surat Jalan
3. RECEIVED / DITERIMA adalah seluruh item dalam SO sudah diterima
4. CLOSED / DITUTUP adalah SO ditutup secara sengaja, bisa sebagian / tidak ada item yang diterima dan memutus hubungan dengan menu Surat Jalan.

## Surat Jalan

### Aktivitas Utama

1. **Buat surat jalan:** Cara membuat surat jalan yaitu klik menu Pembelian > Laporan Penerimaan Barang. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. **Ubah surat jalan:** Aksi ini untuk merubah informasi surat jalan.
    - Penerimaan barang hanya bisa diubah jika status pembayaran atas faktur penjualan adalah menunggu pembayaran (`Pending`).
    - Untuk merubah surat jalan, cari data yang ingin diubah di daftar laporan surat jalan setelah itu klik tombol `Ubah` yang terdapat pada kolom aksi.
3. **Hapus surat jalan:** Penerimaan barang dapat dihapus jika status pembayaran terhadap faktur penjualan adalah menunggu pembayaran (`Pending`).

### Penjelasan Kolom pada Form Surat Jalan

1. `Customer` ketika memilih customer, secara otomatis sistem akan mengambil seluruh Pesanan Penjualan dengan customer tersebut dan status Pesanan Penjualan adalah _APPROVED_.
1. `Gudang` adalah gudang barang keluar. Sistem akan mencatat mutasi persediaan keluar pada gudang tersebut.
1. `No. Dokumen` adalah nomor dokumen surat jalan. Terbuat otomatis dan reset setiap bulan.
1. `Tanggal` adalah tanggal surat jalan. Jika merubah tanggal yang sudah dibuat dan tanggal berbeda bulan,
   maka sistem **secara otomatis merubah** nomor dokumen mengikuti urutan nomor pada bulan tersebut.
1. `Catatan` untuk menulis catatan-catatan pada pesanan penjualan
1. `Daftar Barang` terdiri dari tanggal pesanan penjualan, nomor pesanan penjualan, info produk, kuantitas dipesan, kuantitas terpenuhi, kuantitas diterima.

## Faktur Penjualan

### Aktivitas Utama

1. **Buat faktur penjualan:**
    - Jika menggunakan sistem pesanan, maka Faktur Pembelian otomatis terbuat jika membuat Laporan Penerimaan Barang.
    - Jika tidak menggunakan sistem pesanan, Anda dapat membuat faktur penjualan. Klik menu Pembelian > Faktur Pembelian. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. **Ubah faktur penjualan:** Aksi ini untuk merubah informasi faktur penjualan.
    - Faktur penjualan dapat dihapus jika status pembayaran adalah belum dibayar (`Pending`).
    - Untuk merubah faktur penjualan, cari data yang ingin diubah di daftar faktur penjualan setelah itu klik tombol `Ubah` yang terdapat pada kolom aksi.
3. **Hapus faktur penjualan:** Aksi ini untuk menghapus faktur penjualan. Faktur penjualan dapat dihapus jika status pembayaran adalah belum dibayar (`Pending`).

### Penjelasan Kolom pada Form Faktur Penjualan

1. `Customer` adalah customer untuk faktur penjualan tersebut.
1. `Gudang` adalah gudang lokasi barang keluar. Sistem akan mencatat mutasi persediaan keluar pada gudang tersebut.
1. `No. Dokumen` adalah nomor dokumen faktur penjualan. Terbuat otomatis dan reset setiap bulan.
1. `Tanggal` adalah tanggal faktur penjualan. Jika merubah tanggal yang sudah dibuat dan tanggal berbeda bulan,
   maka sistem **secara otomatis merubah** nomor dokumen mengikuti urutan nomor pada bulan tersebut.
1. `Catatan` untuk menulis catatan-catatan pada pesanan penjualan
1. `Daftar Barang` terdiri dari nama produk, kuantitas, satuan, harga satuan, disc (%), disc (Rp), subtotal.
1. `Diskon`
1. `PPN` kolom ini terisi otomatis jika status customer adalah PKP. (Mohon melihat bagian master data untuk penjelasan lebih detail)
1. `Informasi Lainnya` terdiri dari No. Faktur Customer, No. Faktur Pajak, Tgl Faktur Customer dan Tgl Jatuh Tempo.

### Penjelaan Status

1. PENDING / MENUNGGU adalah Faktur Penjualan baru dibuat dan menunggu pembayaran ke customer
2. PAID / LUNAS adalah Faktur Penjualan telah lunas dibayar ke customer

## Penerimaan Barang Retur Penjualan

### Aktivitas Utama

1. **Buat penerimaan barang retur:** Klik menu Penjualan > Surat Jalan Retur. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. **Ubah penerimaan barang retur:** Aksi ini untuk merubah informasi penerimaan barang retur.
    - Surat jalan retur hanya bisa diubah jika status pembayaran atas nota retur pembelian adalah menunggu pembayaran (`Pending`).
    - Untuk merubah penerimaan barang retur, cari data yang ingin diubah di daftar penerimaan barang retur setelah itu klik tombol `Ubah` yang terdapat pada kolom aksi.
3. **Hapus penerimaan barang retur:** Aksi ini untuk menghapus penerimaan barang retur. Surat jalan retur hanya bisa dihapus jika status pembayaran atas nota retur pembelian adalah menunggu pembayaran (`Pending`).

### Penjelasan Kolom pada Form Penerimaan Barang Retur Penjualan

1. `Customer` adalah customer retur penjualan.
1. `Gudang` adalah gudang barang retur diterima.
1. `No. Dokumen` adalah nomor dokumen penerimaan barang retur. Terbuat otomatis dan reset setiap bulan.
1. `Tanggal` adalah tanggal penerimaan barang retur. Jika merubah tanggal pesanan yang sudah dibuat dan tanggal berbeda bulan,
   maka sistem **secara otomatis merubah** nomor dokumen mengikuti urutan nomor pada bulan tersebut.
1. `Catatan` untuk menulis catatan-catatan pada pesanan penjualan
1. `Daftar Penerimaan Barang` terdiri nomor surat jalan, informasi barang diterima, kuantitas surat jalan, kuantitas telah diretur, kuantitas yang akan diretur saat ini dan satuan.
1. Tombol `Tambah No. Penerimaan Barang` untuk menambahkan barang yang akan diretur.

## Retur Penjualan

### Aktivitas Utama

1. **Buat retur penjualan:** Klik menu Penjualan > Retur Penjualan. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. **Ubah retur penjualan:** Aksi ini untuk merubah informasi retur penjualan.
    - Retur penjualan hanya bisa diubah jika status pembayaran adalah menunggu pembayaran (`Pending`).
    - Untuk merubah retur penjualan, cari data yang ingin diubah di daftar retur penjualan setelah itu klik tombol `Ubah` yang terdapat pada kolom aksi.
3. **Hapus retur penjualan:** Aksi ini untuk menghapus retur penjualan. Retur pembelian hanya bisa dihapus jika status pembayaran adalah menunggu pembayaran (`Pending`).

### Penjelasan Kolom pada Form Retur Penjualan

1. `Customer` adalah customer retur penjualan.
1. `Gudang` adalah gudang barang retur diterima.
1. `No. Dokumen` adalah nomor dokumen retur penjualan. Terbuat otomatis dan reset setiap bulan.
1. `Tanggal` adalah tanggal retur penjualan. Jika merubah tanggal pesanan yang sudah dibuat dan tanggal berbeda bulan,
   maka sistem **secara otomatis merubah** nomor dokumen mengikuti urutan nomor pada bulan tersebut.
1. `Catatan` untuk menulis catatan-catatan pada retur penjualan
1. `Daftar Retur Penjualan` terdiri nomor surat jalan, informasi barang diterima, kuantitas surat jalan, kuantitas telah diretur, kuantitas yang akan diretur saat ini, satuan dan harga satuan.
1. Tombol `Pilih Surat Jalan` untuk menambahkan barang yang akan diretur.

### Penjelaan Status

1. PENDING / MENUNGGU adalah Retur Penjualan baru dibuat dan menunggu pelunasan
2. PAID / LUNAS adalah Retur Penjualan telah lunas dibayar

**Note**
Sistem retur yang kami gunakan adalah pengurangan nilai Piutang.

## Piutang Usaha

**Penjelasan**
Menu ini digunakan untuk memantau daftar piutang usaha yang masih menunggu pembayaran. Menu ini secara otomatis akan 2 sumber piutang usaha yaitu `Faktur Penjualan` dan `Retur Penjualan`, Anda **tidak dapat menambahkan piutang usaha** di menu ini.

Penjelasan kolom di daftar piutang usaha:

-   `Tanggal` adalah tanggal faktur penjualan / retur penjualan
-   `Kode Transaksi` adalah nomor nota penjualan / nota retur penjualan
-   `Faktur Penjualan` adalah nilai faktur penjualan
-   `Hutang` adalah nilai sisa piutang
-   `Tanggal Jatuh Tempo` adalah tanggal jatuh tempo piutang usaha

Ada beberapa filter yang dapat Anda gunakan untuk memudahkan pencarian sebagai berikut:

-   `Supplier` saring untuk melihat daftar piutang berdasarkan supplier
-   `Tanggal` saring untuk melihat daftar piutang dalam periode tertentu

## Uang Muka Penjualan

### Aktivitas Utama

1. **Buat uang muka penjualan:** Klik menu Penjualan > Uang Muka Penjualan. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. **Ubah uang muka penjualan:** Aksi ini untuk merubah informasi uang muka penjualan.
    - Uang muka penjualan hanya bisa diubah jika status pembayaran adalah menunggu pembayaran (`Pending`).
    - Untuk merubah uang muka penjualan, cari data yang ingin diubah di daftar uang muka penjualan setelah itu klik tombol `Ubah` yang terdapat pada kolom aksi.
3. **Hapus uang muka penjualan:** Aksi ini untuk menghapus uang muka penjualan. Uang muka penjualan hanya bisa dihapus jika status pembayaran adalah menunggu pembayaran (`Pending`).
4. **Gunakan uang muka penjualan:** Aksi ini untuk menggunakan uang muka sebagai pembayaran Faktur Penjualan. Tekan tombol `gunakan` di kolom aksi untuk melihat daftar faktur penjualan dari Uang Muka tersebut, kemudian pilih faktur penjualan yang ingin dibayarkan.

### Penjelasan Kolom pada Form Uang Muka Penjualan

1. `Customer` adalah customer yang akan melakukan transaksi Uang Muka Penjualan.
1. `Daftar Pesanan Penjualan` adalah pesanan penjualan dari customer tersebut.
1. `No. Dokumen` adalah nomor dokumen uang muka penjualan. Terbuat otomatis dan reset setiap bulan.
1. `Tanggal` adalah tanggal uang muka penjualan. Jika merubah tanggal pesanan yang sudah dibuat dan tanggal berbeda bulan,
   maka sistem **secara otomatis merubah** nomor dokumen mengikuti urutan nomor pada bulan tersebut.
1. `Catatan` untuk menulis catatan-catatan pada uang muka penjualan
1. `Jumlah Uang Muka %` nominal uang muka dalam persentase %.
1. `Jumlah Uang Muka` nominal uang muka dalam rupiah.

### Penjelasan Status

1. PENDING / MENUNGGU adalah Uang Muka Penjualan baru dibuat dan menunggu pelunasan
2. PAID / LUNAS adalah Uang Muka Penjualan telah lunas dibayar
