---
layout: post
title: Memulai Refine Accounting
---

**Penjelasan Singkat**

Di halaman ini kami akan memandu Anda untuk **mempersiapkan master data, menjelaskan saldo awal
dan bagaimana mengisi saldo awal, dan melakukan beberapa pengaturan**. Berikut daftar isi
penjelasan memulai Refine Accounting.

1. [Mempersiapkan master data](#mempersiapkan-master-data)
    1. [COA](#coa)
    1. [Kas & Bank](#kas-&-bank)
    1. [Supplier](#supplier)
    1. [Customer](#customer)
    1. [Gudang](#gudang)
    1. [Produk](#produk)
        - [Satuan Produk](#satuan-produk)
        - [Kategori Produk](#kategori-produk)
        - [Kelola Produk](#kelola-produk)
        - [Konversi Satuan Produk](#konversi-satuan-produk)
        - [Grup Produk / Parcel](#grup-produk--parcel)
        - Harga Spesial
1. Saldo awal
    1. Saldo awal Kas & Bank
    1. Saldo awal Hutang
    1. Saldo awal Piutang
    1. Saldo awal Persediaan
    1. Saldo awal Uang Muka Pembelian
    1. Saldo awal Uang Muka Penjualan
    1. Saldo awal Giro Dibuka & Diterima

## Mempersiapkan Master Data

### COA

**Penjelasan**

COA adalah Chart Of Account atau dalam bahasa indonesia adalah kode akun.
Kode akun ini sangat erat penggunaannya oleh divisi Akuntansi. Dimana COA akan membantu
Anda dan sistem mengontrol pencatatan dan mempermudah penyusunan laporan keuangan [PSAK 45](http://dit-keuangan.upi.edu/uploads/PSAK45ttgPelaporan-Keuangan-Organisasi-Nirlaba.pdf)

Untuk mempermudah Anda dalam memulai, kami sudah membuat default COA sehingga bagi Anda yang kurang memahami
COA dan teknis Akuntansi, Anda tidak perlu bingung dan bisa lewati ke penjelasan selanjutnya.

[//]: <> TODO: Link / print daftar coa default
[Lihat Daftar Coa Default](#)

### Kas & Bank

Kas & Bank menyimpan semua kas & bank yang Anda miliki. Data kas & bank digunakan ketika input transaksi masuk / keluar.
Untuk mengisi data kas & bank sebagai berikut:

1. Klik menu `Master > Kas` untuk mengisi kas atau `Master > Bank` untuk mengisi bank
1. Di pojok kanan atas ada tombol "Tambah Data". Klik untuk menambah data atau mengubah yang sudah ada.
    1. Pada **Kas** yang harus diisi adalah sebagai berikut:
        - COA (Harus diisi). Jika COA yang Anda inginkan belum ada silahkan untuk menambah COA terlebih dahulu
        - Nama (Harus diisi). Sebagai identifikasi nama kas, akan muncul di setiap pilihan transaksi
        - Deskripsi. Sebagai tambahan penjelasan penggunaan kas, tidak akan muncul di menu lain.
    1. Pada **Bank** yang harus diisi adalah sebagai berikut:
        - COA (Harus diisi). Jika COA yang Anda inginkan belum ada silahkan untuk menambah COA terlebih dahulu
        - Nama Bank (Harus diisi). Sebagai identifikasi nama kas, akan muncul di setiap pilihan transaksi
        - Informasi Rekening (Harus diisi). Sebagai tambahan informasi bank, tidak akan muncul di menu lain.
        - Nomor Rekening (Harus diisi). Sebagai tambahan informasi bank, akan muncul di setiap pilihan transaksi.
        - Deskripsi. Sebagai tambahan penjelasan penggunaan kas, tidak akan muncul di menu lain.
1. Setelah mengisi semua data dengan benar. Klik simpan

Pengisian saldo awal kas & bank akan dijelaskan pada bagian [Saldo Awal](#saldo-awal)

### Supplier

Data supplier umumnya digunakan di modul Pembelian dan Hutang. Cara input data Supplier ada 2 pilihan, pertama melalui menu tampilan utama atau import melalui excel. Untuk import melalui excel silahkan download [format excel supplier disini](#). Untuk input melalui menu utama caranya sebagai berikut:

1. Klik menu `Master > Supplier > Supplier`.
2. Di pojok kanan atas ada tombol `Tambah Data`.
3. Berikut penjelasan kolom data supplier:
    - Nama (Wajib diisi), akan muncul di modul pembelian & laporan.
    - Alamat (Wajib diisi), sebagai tambahan informasi akan muncul di modul pembelian & ketika cetak dokumen menu pembelian.
    - No. Telepon (Wajib diisi), sebagai tambahan informasi akan muncul di modul pembelian & ketika cetak dokumen.
    - Email, Website, Kelurahan, Provinsi, Kecamatan, Provinsi, Negara, Zip code, sebagai pelengkap informasi supplier
    - Kategori Supplier & Deskripsi, sebagai tambahan informasi.
    - Status Supplier: PKP atau NON PKP. Jika dipilih PKP, maka secara otomatis pada modul pembelian akan terisi kolom PPN. Secara default sistem akan membuat status supplier adalah NON PKP.
    - PIC List, sebagai tambahan informasi data PIC dari perusahaan supplier.
4. Setelah selesai mengisi semua klik `Simpan`.

**Video Tutorial**

-   [Video tutorial menambahkan supplier melalui excel](https://youtu.be/WiGOYNRph5E)
-   [Video tutorial menambahkan supplier melalui tampilan utama](https://youtu.be/WiGOYNRph5E)

### Pelanggan

Data pelanggan umumnya digunakan di modul Penjualan dan Piutang. Cara input data Pelanggan ada 2 pilihan, pertama melalui menu tampilan utama atau import melalui excel. Untuk import melalui excel silahkan download [format excel pelanggan disini](#). Untuk input melalui menu utama caranya sebagai berikut:

1. Klik menu `Master > Pelanggan > Pelanggan`.
2. Di pojok kanan atas ada tombol `Tambah Data`.
3. Berikut penjelasan kolom data pelanggan:
    - Nama (Wajib diisi): akan muncul di modul pembelian & laporan.
    - Alamat (Wajib diisi): sebagai tambahan informasi akan muncul di modul pembelian & ketika cetak dokumen menu pembelian.
    - No. Telepon (Wajib diisi): sebagai tambahan informasi akan muncul di modul pembelian & ketika cetak dokumen.
    - Email, Website, Kelurahan, Provinsi, Kecamatan, Provinsi, Negara, Zip code: sebagai pelengkap informasi pelanggan
    - Kategori Supplier & Deskripsi: sebagai tambahan informasi.
    - PIC List: sebagai tambahan informasi data PIC dari perusahaan pelanggan.
4. Setelah selesai mengisi semua klik `Simpan`.

**Catatan Penting!**

Pada pelanggan tidak ada kolom pilihan PKP atau NON PKP. Untuk pengaturan PPN & NON PPN pada penjualan silahkan melihat penjelasan di [modul penjualan](#).

**Video Tutorial**

-   [Video tutorial menambahkan pelanggan melalui excel](https://youtu.be/8_UIiCIt_38)
-   [Video tutorial menambahkan pelanggan melalui tampilan utama](https://youtu.be/8_UIiCIt_38)

## Produk

### Satuan Produk

Satuan produk digunakan untuk beberapa hal:

-   Satuan utama produk
-   Konversi satuan
-   Pilihan satuan pada modul pembelian & penjualan

Cara mengisi satuan sebagai berikut:

1. Klik menu `Master > Produk > Satuan Produk`.
2. Di pojok kanan atas ada tombol `Tambah Data`.
3. Isi nama satuan

### Kategori Produk

Kategori produk digunakan untuk sebagai berikut:

-   Tambahan informasi produk
-   Penggolongan data di potongan harga spesial

Cara mengisi kategori produk sebagai berikut:

1. Klik menu `Master > Produk > Kategori Produk`.
2. Di pojok kanan atas ada tombol `Tambah Data`.
3. Isi nama kategori (wajib diisi) & deskripsi (tidak wajib).

### Kelola Produk

Produk umumnya akan muncul di menu pembelian dan penjualan. Sebelum mengisi sebuah produk pastikan Anda sudah membuat [kategori produk](#kategori-produk) dan [satuan produk](#satuan-produk). Cara input data produk ada 2 pilihan, pertama melalui menu tampilan utama atau import melalui excel. Untuk import melalui excel silahkan download [format excel produk disini](#). Untuk input melalui menu utama caranya sebagai berikut:

1. Klik menu `Master > Produk > Produk`.
2. Di pojok kanan atas ada tombol `Tambah Data`.
3. Berikut penjelasan kolom data produk:
    - Nama (Wajib diisi): akan muncul di modul penjualan, pembelian & laporan.
    - Satuan (Wajib diisi): sebagai satuan utama produk ini, satuan utama harus satuan terkecil.
    - SKU (Wajib diisi): sebagai kode produk dan harus unik tidak boleh kembar.
    - Price: sebagai acuan / informasi harga satuan di menu penjualan.
    - Tipe produk (Stock / Non Stock): Jika Anda memiliki produk yang sifatnya jasa pilih tipe Non Stock.
    - Default Warehouse: sebagai default gudang produk tersebut
    - Kategori & deskripsi: sebagai pelengkap informasi.
4. Setelah selesai mengisi semua klik `Simpan`.

**Catatan Penting!**

Setelah ada transaksi pembelian / penjualan, produk tidak dapat dihapus. Harap berhati-hati ketika merubah produk yang sudah ada transaksi pembelian / penjualan karena perubahan akan mengubah semua data yang lama.

### Konversi Satuan Produk

Konversi satuan produk digunakan untuk mencatat tiap konversi satuan. Contoh: Produk Sabun Batang Merk A 1 Dus = 12 Pcs. Maka disini yang harus dilakukan adalah:

-   Input satuan Pcs & Dus di [satuan produk](#satuan-produk)
-   Input konversi satuan untuk mendefinisikan 1 Dus = 12 Pcs.

Cara input konversi satuan sebagai berikut:

1. Klik menu `Master > Produk > Konversi Satuan Produk`.
2. Di pojok kanan atas ada tombol `Tambah Data`.
3. Di form tambah data yang harus dilakukan adalah:
    - Pilih produk yang diinginkan. Jika belum ada, Anda harus membuat produk terlebih dahulu.
    - Pilih satuan konversi, dalam contoh kasus ini pilih Dus.
    - Isi konversi satuan, dalam contoh kasus ini adalah 12.
4. Setelah memeriksa dan sesuai semua silahkan klik `Simpan`.

**Catatan Penting!**

Perubahan konversi satuan di kemudian hari tidak dapat dilakukan. Saran kami silahkan buat produk baru dan isi konversi satuan yang baru. Hal ini juga akan membantu Anda untuk mencocokan persediaan di gudang antara produk yang lama dan yang baru.

### Grup Produk / Parcel

Grup produk adalah produk yang terdiri dari beberapa produk. Grup produk sendiri tidak memiliki persediaan, karena persediaannya mengacu pada anggota produk tersebut. Contoh: 1 Pcs Parsel Lebaran yang berisi 1 Botol Sirup A, 1 Kaleng Biskuit A dan 1 Box Biskuit B.

Jika salah satu dari anggota grup produk habis, maka grup produk tidak dapat dijual.

Cara input produk grup sebagai berikut:

1. Klik menu `Master > Produk > Produk`.
2. Di pojok kanan disebelah tombol `Tambah Data` klik anak panah kebawah, maka akan muncul `Produk Grup Baru`.
3. Berikut penjelasan kolom data produk grup:
    - Secara garis besar sama dengan produk. Isi nama, satuan, SKU, harga, gudang default, kategori & deskripsi.
    - Di bagian bawah Anda dapat mengisi anggota grup produk tersebut. Klik `Tambah Produk` untuk menambahkan anggota produk.
    - Setiap anggota produk Anda dapat mengisi satuan grup produk, qty & rasio COGS. Rasio COGS digunakan sebagai perbandingan jika Anda membeli ke supplier sebuah parsel. Total Rasio COGS harus = 100%
4. Setelah selesai mengisi semua klik `Simpan`.

### Harga Spesial

Menu ini sangat membantu jika perusahan Anda adalah retail / supermarket. Menu ini menjaga potongan produk Anda lebih konsisten. Contoh kasus: Diskon potongan Rp 1.000 jika pembelian di atas 12 Pcs. Kemudian ada Diskon potongan Rp 1.500 jika pembelian di atas 36 Pcs.

Cara input harga spesial produk sebagai berikut:

1. Klik menu `Master > Produk > Harga Spesial Produk`.
2. Di pojok kanan disebelah tombol `Tambah Data`.
3. Penjelasan kolom pada Harga Spesial Produk:
    - Nama (wajib diisi): adalah nama harga spesial produk
    - Produk: Pilih jika harga spesial ini berlaku untuk produk tersebut
    - Kategori Produk: Pilih jika harga spesial ini berlaku untuk kategori produk tersebut
    - Kategori Pelanggan: Pilih jika harga spesial ini berlaku untuk kategori pelanggan tertentu
    - Minimum Qty (Wajib diisi): Isi minimum pemesanan qty dalam kasus ini 12 pcs.
    - Tipe Diskon (Wajib diisi): Pilih rupiah untuk potongan nominal yang sudah fix, atau % untuk % dari harga yang sudah di input di master Produk.
    - Jumlah Diskon (Wajib diisi): Rupiah / % discount

Anda bisa input beberapa kali harga spesial, secara otomatis pada menu penjualan akan menghitung harga spesial jika memenuhi semua kriteria yang sudah Anda terapkan.
