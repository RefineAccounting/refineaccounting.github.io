---
layout: post
title: Mengelola Persediaan
---

**Penjelasan Singkat**

Di halaman ini kami akan memandu Anda untuk melihat data persediaan dan mengelola sado persediaan.

1. [Daftar Persediaan](#daftar-persediaan)
1. [Mutasi Persediaan](#mutasi-persediaan)
1. [Kartu Persediaan](#kartu-persediaan)
1. [Koreksi Persediaan](#koreksi-persediaan)
1. [Transfer Persediaan](#transfer-persediaan)

**Kumpulan Video**
Berikut ini kumpulan video untuk mengelola persediaan

1. [Alur Sistem Penjualan](https://youtu.be/eNGoXnzBtDo)
2. [Menu Pesanan Penjualan](https://youtu.be/wpgVBN1hA0E)
3. [Menu Penerimaan Barang](https://youtu.be/s6ieqLwrWv4)
4. [Menu Faktur Penjualan](https://youtu.be/8Wa8vJq-Ka8)

## Daftar Persediaan

Tujuan dari halaman ini adalah melihat nilai total kuantitas produk di gudang tertentu. Ada beberapa filter yang dapat Anda gunakan sebagai berikut:

-   `Gudang` untuk menampilkan hanya gudang tertentu
-   `Produk` untuk menampilkan hanya produk tertentu

## Mutasi Persediaan

Tujuan dari halaman ini adalah melihat mutasi persediaan dalam sebuah periode tertentu. Penjelasan kolom yang ada di halaman ini adalah sebagai berikut:

-   `Informasi Produk` berisi nama produk & SKU
-   `Saldo Awal` berisi nilai kuantitas & nilai rupiah di awal periode.
-   `Mutasi Masuk` berisi mutasi masuk dalam nilai kuantitas & nilai rupiah dalam suatu periode. Yang termasuk dalam mutasi masuk adalah pembelian, penerimaan barang retur penjualan, transfer persediaan, koreksi persediaan masuk.
-   `Mutasi Keluar` berisi mutasi keluar dalam nilai kuantitas & nilai rupiah dalam suatu periode. Yang termasuk dalam mutasi keluar adalah penjualan, surat jalan retur pembelian, transfer persediaan, koreksi persediaan keluar.
-   `Saldo Akhir` adalah total saldo awal + mutasi masuk - mutasi keluar

Ada beberapa filter yang dapat Anda gunakan sebagai berikut:

-   `Periode` untuk menampilkan mutasi persediaan dalam periode tertentu
-   `Produk` untuk menampilkan mutasi suatu produk

# Kartu Persediaan

Tujuan dari halaman ini adalah melihat daftar transaksi sebuah produk dalam periode tertentu. Untuk menampilkan kartu persedian Anda harus memilih terlebih dahulu produk, periode dan gudang.

Penjelasan kolom pada kartu persediaan:

-   `Tanggal` adalah tanggal transaksi
-   `Kode Transaksi` adalah nomor nota atau nomor transaksi
-   `Catatan` berisi jenis transaksi tersebut. Ada beberapa jenis sebagai berikut: Pembelian, Penjualan, Retur Pembelian, Retur Penjualan, Koreksi Persediaan, Transfer Persediaan
-   `Mutasi Masuk` dan `Mutasi Keluar` dalam nilai kuantitas
-   `Saldo Akhir` adalah total dari saldo awal + mutasi masuk - mutasi keluar

## Koreksi Persediaan

### Aktivitas Utama

1. **Buat koreksi persediaan:** Klik menu Persediaan > Koreksi Persediaan. Kemudian di ujung kanan atas terdapat tombol `Tambah Data`. Klik untuk menambah data baru.
2. **Hapus koreksi persediaan:** Aksi ini untuk menghapus koreksi persediaan.

**Note:**

-   Koreksi persediaan untuk metode FIFO akan mengeluarkan semua urutan HPP dan memasukkan satu nilai kuantitas koreksi beserta dengan nilai persediaan yang baru.
-   Koreksi persediaan tidak dapat diubah. Jika terjadi salah input, Anda dapat menghapus dan menambahkan kembali koreksi persediaan tersebut

### Penjelasan Kolom pada Form Koreksi Persediaan

1. `Gudang` adalah gudang sumber koreksi.
1. `No. Dokumen` adalah nomor dokumen koreksi persediaan. Terbuat otomatis dan reset setiap bulan.
1. `Tanggal` adalah tanggal koreksi persediaan. Jika merubah tanggal pesanan yang sudah dibuat dan tanggal berbeda bulan,
   maka sistem **secara otomatis merubah** nomor dokumen mengikuti urutan nomor pada bulan tersebut.
1. `Catatan` untuk menulis catatan-catatan pada koreksi persediaan
1. `Daftar Koreksi Persediaan` terdiri produk, kuantitas saat ini, kuantitas baru yang akan dikoreksi, koreksi (hitung otomatis oleh program), HPP adalah nilai hpp saat ini (hanya muncul ketika metode AVG), HPP Baru adalah nilai HPP yang baru.

## Transfer Persediaan

### Aktivitas Utama

1. **Buat koreksi persediaan:** Klik menu Persediaan > Transfer Persediaan.

### Penjelasan Kolom pada Form Transfer Persediaan

1. `Dari Gudang` adalah gudang yang akan mengeluarkan barang.
1. `Menuju Gudang` adalah gudang yang akan menerima barang.
1. `No. Dokumen` adalah nomor dokumen transfer persediaan. Terbuat otomatis dan reset setiap bulan.
1. `Tanggal` adalah tanggal transfer persediaan.
1. `Catatan` untuk menulis catatan-catatan pada transfer persediaan
1. `Daftar Transfer Persediaan` terdiri produk, kuantitas saat ini, kuantitas yang akan dipindahkan.
