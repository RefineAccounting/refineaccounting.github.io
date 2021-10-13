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

## Alur Sistem Penjualan

**Penjelasan**

Alur sistem penjualan pada Refine Accounting ada 2 garis besar. Pertama menggunakan sistem pemesanan dimana setiap surat jalan / faktur penjualan harus didasarkan pada sebuah dokumen pesanan. Kedua tanpa menggunakan sistem pemesanan.

Untuk sistem pertama sebagai berikut:

1. Admin penjualan mengirimkan penawaran harga atas beberapa barang.
2. Admin penjualan menyetujui harga dan **input pesanan penjualan (SO)** kepada customer X dan barang-barang yang akan dipesan.
3. SO ini dikirimkan ke customer untuk diproses.
4. Pengiriman barang ke customer oleh bagian gudang, secara otomatis sistem akan **membuat faktur penjualan (INVOICE)** dan **mutasi masuk pada persediaan**.

Sedangkan, untuk sistem kedua sebagai berikut:

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

1. Buat pesanan penjualan. Klik menu Penjualan > Pesanan Penjualan. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. Lakukan pengecekan apakah pesanan penjualan sudah benar.
3. Jika ada kesalahan untuk merubah data. Cari data yang ingin di ubah dalam `Daftar Pesanan Penjualan` setelah itu klik aksi `Ubah` yang terdapat pada ujung kanan data tersebut.
4. Jika hanya merubah status Anda bisa klik aksi `Disetujui`.
5. Jika ada kebutuhan untuk menutup Pesanan Penjualan padahal belum dikirim full, Anda bisa klik aksi `Tutup`

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

### Penjelaan Status

1. PENDING / MENUNGGU adalah SO baru dibuat dan menunggu verifikasi
2. APPROVED / DISETUJUI adalah SO sudah disetujui dan terhubung dengan menu Surat Jalan
3. RECEIVED / DITERIMA adalah seluruh item dalam SO sudah diterima
4. CLOSED / DITUTUP adalah SO ditutup secara sengaja, bisa sebagian / tidak ada item yang diterima dan memutus hubungan dengan menu Surat Jalan.

## Surat Jalan

### Aktivitas Utama

1. Buat laporan surat jalan. Klik menu Penjualan > Surat Jalan. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. Jika ada kesalahan untuk merubah data. Cari data yang ingin di ubah dalam `Daftar Surat Jalan` setelah itu klik aksi `Ubah` yang terdapat pada ujung kanan data tersebut.

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

1. Jika menggunakan sistem pesanan, maka Faktur Penjualan otomatis terbuat jika membuat Surat Jalan.
2. Jika tidak menggunakan sistem pesanan, Anda dapat membuat faktur penjualan. Klik menu Penjualan > Faktur Penjualan. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
3. Jika ada kesalahan untuk merubah data (baik itu menggunakan sistem pesanan atau tanpa pesanan). Cari data yang ingin di ubah dalam `Daftar Faktur Penjualan` setelah itu klik aksi `Ubah` yang terdapat pada ujung kanan data tersebut.

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

1. Buat penerimaan barang retur. Klik menu Penjualan > Penerimaan Barang Retur. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. Lakukan pengecekan apakah penerimaan barang retur penjualan sudah benar.
3. Jika ada kesalahan untuk merubah data. Cari data yang ingin di ubah dalam `Daftar Penerimaan Barang Retur` setelah itu klik aksi `Ubah` yang terdapat pada ujung kanan data tersebut.

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

1. Buat retur penjualan. Klik menu Penjualan > Retur Penjualan. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. Lakukan pengecekan apakah retur penjualan sudah benar.
3. Jika ada kesalahan untuk merubah data. Cari data yang ingin di ubah dalam `Daftar Retur Penjualan` setelah itu klik aksi `Ubah` yang terdapat pada ujung kanan data tersebut.

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

## Uang Muka Penjualan

### Aktivitas Utama

1. Buat uang muka penjualan. Klik menu Penjualan > Uang Muka Penjualan. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. Lakukan pengecekan apakah retur penjualan sudah benar.
3. Jika ada kesalahan untuk merubah data. Cari data yang ingin di ubah dalam `Daftar Retur Penjualan` setelah itu klik aksi `Ubah` yang terdapat pada ujung kanan data tersebut.
4. Nilai pada uang muka penjualan dapat digunakan sebagai pembayaran `Faktur Penjualan`. Tekan tombol `gunakan` di kolom aksi untuk melihat daftar faktur penjualan dari Uang Muka tersebut, kemudian pilih faktur penjualan yang ingin dibayarkan.

### Penjelasan Kolom pada Form Uang Muka Penjualan

1. `Customer` adalah customer yang akan melakukan transaksi Uang Muka Penjualan.
1. `Daftar Pesanan Penjualan` adalah pesanan penjualan dari customer tersebut.
1. `No. Dokumen` adalah nomor dokumen uang muka penjualan. Terbuat otomatis dan reset setiap bulan.
1. `Tanggal` adalah tanggal uang muka penjualan. Jika merubah tanggal pesanan yang sudah dibuat dan tanggal berbeda bulan,
   maka sistem **secara otomatis merubah** nomor dokumen mengikuti urutan nomor pada bulan tersebut.
1. `Catatan` untuk menulis catatan-catatan pada uang muka penjualan
1. `Jumlah Uang Muka %` nominal uang muka dalam persentase %.
1. `Jumlah Uang Muka` nominal uang muka dalam rupiah.

### Penjelaan Status

1. PENDING / MENUNGGU adalah Uang Muka Penjualan baru dibuat dan menunggu pelunasan
2. PAID / LUNAS adalah Uang Muka Penjualan telah lunas dibayar
