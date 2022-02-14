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
        - [Harga Spesial](#harga-spesial)
1. [Saldo awal](#saldo-awal)
    1. [Saldo awal Kas & Bank](#saldo-awal-kas--bank)
    1. [Saldo awal Hutang](#saldo-awal-hutang)
    1. [Saldo awal Piutang](#saldo-awal-piutang)
    1. [Saldo awal Persediaan](#saldo-awal-persediaan)
    1. [Saldo awal Uang Muka Pembelian & Penjualan](#saldo-awal-uang-muka-pemnbelian--penjualan)
    1. [Saldo awal Giro Dibuka & Diterima](#saldo-awal-giro-dibuka--diterima)

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

### Gudang

Secara bawaan kami sudah membuat gudang yaitu Gudang Utama. Jika Anda memiliki lebih dari satu gudang, maka Anda dapat membuat gudang baru. Untuk mengisi data gudang sebagai berikut:

1. Klik menu `Master > Gudang`.
2. Di pojok kanan atas ada tombol `Tambah Data`.
3. Berikut penjelasan kolom data gudang:
    - Nama gudang (Wajib diisi) .
    - Catatan berisi informasi tambahan gudang tersebut, tidak akan muncul di menu lain, hanya di daftar Gudang saja.
4. Setelah selesai mengisi semua klik `Simpan`.

### Tenaga Penjual

Dalam menu penjualan mungkin Anda memiliki tenaga penjual dan ingin mencatat nama tenaga penjual tersebut dalam setiap transaksi penjualan. Di menu ini Anda dapat menambahkan tenaga penjual yang nantinya dapat dihubungkan ke suatu data pelanggan. Untuk mengisi data tenaga penjual sebagai berikut:

1. Klik menu `Master > Tenaga Penjual`.
2. Di pojok kanan atas ada tombol `Tambah Data`.
3. Berikut penjelasan kolom data tenaga penjual:
    - Nama tenaga penjual (Wajib diisi) .
    - Catatan berisi informasi tambahan tenaga penjual tersebut, tidak akan muncul di menu lain, hanya di daftar Tenaga Penjual saja.
4. Setelah selesai mengisi semua klik `Simpan`.

### Kategori Supplier

Anda dapat mengkategorikan supplier jika dibutuhkan. Di menu ini Anda dapat membuat master kategori supplier yang nantinya dapat Anda pilih ketika Anda membuat master supplier. Untuk input melalui menu utama caranya sebagai berikut:

1. Klik menu `Master > Supplier > Kategori Supplier`.
2. Di pojok kanan atas ada tombol `Tambah Data`.
3. Berikut penjelasan kolom data kategori supplier:
    - Nama (Wajib diisi) kategori supplier.
4. Setelah selesai mengisi semua klik `Simpan`. Setelah di simpan silahkan masuk ke data kategori supplier ini akan muncul pada kolom Kategori Supplier di Form Supplier.

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

### Kategori Pelanggan

Anda dapat mengkategorikan pelanggan jika dibutuhkan. Di menu ini Anda dapat membuat master kategori pelanggan yang nantinya dapat Anda pilih ketika Anda membuat master pelanggan. Untuk input melalui menu utama caranya sebagai berikut:

1. Klik menu `Master > Pelanggan > Kategori Pelanggan`.
2. Di pojok kanan atas ada tombol `Tambah Data`.
3. Berikut penjelasan kolom data kategori pelanggan:
    - Nama (Wajib diisi) kategori pelanggan.
4. Setelah selesai mengisi semua klik `Simpan`. Setelah di simpan silahkan masuk ke data kategori pelanggan ini akan muncul pada kolom Kategori Pelanggan di Form Pelanggan.

### Pelanggan

Data pelanggan umumnya digunakan di modul Penjualan dan Piutang. Cara input data Pelanggan ada 2 pilihan, pertama melalui menu tampilan utama atau import melalui excel. Untuk import melalui excel silahkan download [format excel pelanggan disini](#). Untuk input melalui menu utama caranya sebagai berikut:

1. Klik menu `Master > Pelanggan > Pelanggan`.
2. Di pojok kanan atas ada tombol `Tambah Data`.
3. Berikut penjelasan kolom data pelanggan:
    - Nama (Wajib diisi): akan muncul di modul pembelian & laporan.
    - Alamat (Wajib diisi): sebagai tambahan informasi akan muncul di modul pembelian & ketika cetak dokumen menu pembelian.
    - No. Telepon (Wajib diisi): sebagai tambahan informasi akan muncul di modul pembelian & ketika cetak dokumen.
    - Email, Website, Kelurahan, Provinsi, Kecamatan, Provinsi, Negara, Zip code: sebagai pelengkap informasi pelanggan
    - Kategori Pelanggan & Deskripsi: sebagai tambahan informasi.
    - PIC List: sebagai tambahan informasi data PIC dari perusahaan pelanggan.
    - Tenaga Penjual: Pilih tenaga penjual untuk pelanggan ini.
4. Setelah selesai mengisi semua klik `Simpan`.

**Catatan Penting!**

1. Pada pelanggan tidak ada kolom pilihan PKP atau NON PKP. Untuk pengaturan PPN & NON PPN pada penjualan silahkan melihat penjelasan di [modul penjualan](#).
2. 1 (Satu) pelanggan hanya bisa memiliki 1 (Satu) tenaga penjual. Perubahan tenaga penjual akan merubah informasi tenaga penjual di modul penjualan untuk **data selanjutnya**, sedangkan data lama tidak akan berubah.

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

### Metode Pembayaran

Dalam menu penjualan sering sekali melakukan pembayaran yang mempengaruhi harga jual. Salah satu contoh kasus adalah pembayaran menggunakan kartu kredit / kartu debit akan ada charge sebesar +5%. Di menu metode pembayaran ini Anda dapat membuat data metode pembayaran sendiri dengan penjelasan kolom sebagai berikut:

-   Nama metode pembayaran (Wajib diisi).
-   Rentang jatuh tempo tambahan: adalah tambahan durasi (hari) jatuh tempo di menu pesanan penjualan & penjualan.
-   Tipe: adalah jenis tambahan biaya. Ada 2 tipe yaitu % atau jumlah tetap.
-   Biaya tambahan: adalah nominal tambahan biaya atas metode pembayaran ini.
-   Tampilkan sebagai biaya tambahan: adalah pengaturan bagaimana menampilkan informasi biaya tambahan ini.

Setelah mengisi kolom-kolom tersebut klik `Simpan`. Metode pembayaran ini akan muncul pada menu faktur penjualan dan muncul juga sebagai salah satu parameter pada menu harga spesial produk.

## Saldo Awal

Setelah mengisi data master dengan benar, langkah selanjutnya adalah mengisi saldo awal. Saldo awal penting untuk menghitung nilai awal perusahaan Anda seperti: Hutang, Piutang, Persediaan, Saldo Kas & Bank, Dll.

Untuk itu sebelum mengisi data saldo awal, disarankan untuk opname data-data terlebih dahulu. Karena fungsinya untuk menghitung nilai awal, maka nilai awal efeknya sangat menentukan hasil akhir dari setiap laporan.

Untuk mengisi saldo awal ada 2 cara pertama melalui tampilan utama dan yang kedua melalui excel. Untuk file excel sudah kami sediakan bisa Anda unduh [disini]()

### Saldo Awal Kas & Bank

1. Mengisi saldo awal menggunakan tampilan utama
    1. Masuk ke menu `Instalasi`
    2. Pada step yang pertama ada pilihan Install menggunakan excel atau memasukkan data secara manual. Pilih manual dengan klik tombol `Mulai instalasi`
    3. Kemudian Skip / Save hingga pada step ke halaman 2. Pada halaman ini Anda akan melihat semua data kas & bank yang sudah Anda isi, kolom saldo awal & tanggal saldo awal tersebut.
    4. Isi kolom saldo awal dengan nilai saldo awal Anda. Untuk tanggal kami sarankan mengisi di tanggal terakhir sebelum bulan Anda memulai. Contoh Anda memulai input pada bulan September 2021, maka isi lah tanggalnya yaitu 31 Agustus 2021.
    5. Jika sudah klik `Simpan`
2. Mengisi saldo awal menggunakan excel
    1. Setelah mengunduh file excel kami, silahkan pilih sheet `KAS/BANK`.
    2. Penjelasan kolom:
        - `PERKIRAAN` dengan nomor COA dari Kas / Bank tersebut. Contoh untuk `KAS KECIL` coanya adalah 1111 maka isi kolom `PERKIRAAN` dengan 1111.
        - `NAMA KAS/BANK` adalah nama dari Kas / Bank tersebut (tidak harus diisi).
        - `JUMLAH` adalah nilai saldo awal dari Kas / Bank tersebut (harus diisi).
        - `PER TGL.` adalah tanggal dari saldo awal.

### Saldo Awal Hutang

1. Mengisi saldo awal menggunakan tampilan utama
    1. Masuk ke menu `Instalasi`
    2. Pada step yang pertama ada pilihan Install menggunakan excel atau memasukkan data secara manual. Pilih manual dengan klik tombol `Mulai instalasi`
    3. Kemudian Skip / Save hingga pada step ke halaman 3.
    4. Klik tombol `Tambah Supplier` untuk menambahkan data hutang ke supplier. Disini hanya akan mengisi nilai hutang bukan item yang Anda beli di Supplier.
    5. Penjelasan pengisian kolom sebagai berikut:
        - Kolom `Supplier` untuk memilih supplier (wajib diisi).
        - Kolom `No. Dokumen` umumnya diisi dengan nomor nota hutang. Nantinya akan dijadikan referensi di keuangan untuk pelunasan hutang tersebut.
        - Kolom `Saldo awal` adalah nilai dari nota / hutang Anda.
        - Kolom `tanggal` adalah tanggal terhitung hutang. Untuk tanggal kami sarankan mengisi di tanggal terakhir sebelum bulan Anda memulai. Contoh Anda memulai input pada bulan September 2021, maka isi lah tanggalnya yaitu 31 Agustus 2021.
    6. Jika sudah klik `Simpan & Lanjutkan`
2. Mengisi saldo awal menggunakan excel
    1. Setelah mengunduh file excel kami, silahkan pilih sheet `HUTANG`.
    2. Penjelasan kolom:
        - `TANGGAL INVOICE` adalah tanggal saldo hutang Anda.
        - `NO. INVOICE` adalah umumnya diisi dengan nomor nota hutang. Nantinya akan dijadikan referensi di keuangan untuk pelunasan hutang tersebut.
        - `KODE SUPPLIER` Anda dapat menemukan kode supplier di menu `Master > Supplier > Supplier`. Di daftar supplier akan muncul informasi ringkas & kode supplier di bawah nama supplier. Contoh: **SUPPLIER001**.
        - `JUMLAH (RP.)` adalah nilai saldo awal.

### Saldo Awal Piutang

1. Mengisi saldo awal menggunakan tampilan utama
    1. Masuk ke menu `Instalasi`
    2. Pada step yang pertama ada pilihan Install menggunakan excel atau memasukkan data secara manual. Pilih manual dengan klik tombol `Mulai instalasi`
    3. Kemudian Skip / Save hingga pada step ke halaman 4.
    4. Klik tombol `Tambah Customer` untuk menambahkan data hutang ke customer. Disini hanya akan mengisi nilai hutang bukan item yang Anda beli di Customer.
    5. Penjelasan pengisian kolom sebagai berikut:
        - Kolom `Customer` untuk memilih customer (wajib diisi).
        - Kolom `No. Dokumen` umumnya diisi dengan nomor nota piutang. Nantinya akan dijadikan referensi di keuangan untuk pelunasan piutang tersebut.
        - Kolom `Saldo awal` adalah nilai dari nota / piutang Anda.
        - Kolom `tanggal` adalah tanggal terhitung piutang. Untuk tanggal kami sarankan mengisi di tanggal terakhir sebelum bulan Anda memulai. Contoh Anda memulai input pada bulan September 2021, maka isi lah tanggalnya yaitu 31 Agustus 2021.
    6. Jika sudah klik `Simpan & Lanjutkan`
2. Mengisi saldo awal menggunakan excel
    1. Setelah mengunduh file excel kami, silahkan pilih sheet `PIUTANG`.
    2. Penjelasan kolom:
        - `TANGGAL INVOICE` adalah tanggal saldo piutang Anda.
        - `NO. INVOICE` adalah umumnya diisi dengan nomor nota piutang. Nantinya akan dijadikan referensi di keuangan untuk pelunasan piutang tersebut.
        - `KODE CUSTOMER` Anda dapat menemukan kode customer di menu `Master > Customer > Customer`. Di daftar customer akan muncul informasi ringkas & kode customer di bawah nama customer. Contoh: **CUSTOMER001**.
        - `JUMLAH (RP.)` adalah nilai saldo awal.

### Saldo Awal Persediaan

1. Mengisi saldo awal menggunakan tampilan utama
    1. Masuk ke menu `Instalasi`
    2. Pada step yang pertama ada pilihan Install menggunakan excel atau memasukkan data secara manual. Pilih manual dengan klik tombol `Mulai instalasi`
    3. Kemudian Skip / Save hingga pada step ke halaman 5.
    4. Klik tombol `Tambah Produk` untuk menambahkan data persediaan awal produk.
    5. Penjelasan pengisian kolom sebagai berikut:
        - Kolom `Produk` untuk memilih produk (wajib diisi).
        - Kolom `Saldo Awal (Qty)` nilai saldo awal persediaan secara Qty sesuai dengan satuan pada produk.
        - Kolom `Saldo Awal (Rp)` nilai saldo awal persediaan secara Rupiah sesuai dengan satuan pada produk.
        - Kolom `Gudang` untuk memilih lokasi gudang.
    6. Jika sudah klik `Simpan & Lanjutkan`
2. Mengisi saldo awal menggunakan excel
    1. Setelah mengunduh file excel kami, silahkan pilih sheet `PERSEDIAAN`.
    2. Penjelasan kolom:
        - `KODE BARANG` Anda bisa melihat kode barang (SKU) di menu `Master > Produk > Produk`, pada daftar produk Anda akan melihat kode barang di bawah nama produk.
        - `KUANTITAS AWAL` nilai saldo awal persediaan secara Qty sesuai dengan satuan pada produk.
        - `HARGA SATUAN` nilai saldo awal harga satuan persediaan (Rp).
        - `SALDO AWAL (Rp.)` adalah kuantitas awal \* harga satuan.
        - `Per Tgl.` adalah tanggal terhitung saldo awal persediaan. Untuk tanggal kami sarankan mengisi di tanggal terakhir sebelum bulan Anda memulai. Contoh Anda memulai input pada bulan September 2021, maka isi lah tanggalnya yaitu 31 Agustus 2021.
        - Kolom `Gudang` untuk memilih lokasi gudang.

### Saldo Awal Uang Muka Pembelian / Penjualan

Untuk menu saldo awal uang muka pembelian / penjualan saat ini hanya dapat diisi melalui excel.

1. Setelah mengunduh file excel kami, silahkan pilih sheet `UANG MUKA`.
2. Penjelasan kolom:
    - `JENIS` berisi `PEMBELIAN` untuk uang muka pembelian dan `PENJUALAN` untuk uang muka penjualan.
    - `KODE SUPPLIER/CUST` berisi kode supplier / customer yang bersangkutan. Anda dapat menemukan kode supplier / customer pada menu `Daftar Customer` atau `Daftar Supplier`.
    - `PERKIRAAN` adalah COA Kas / Bank yang menerima atau mengeluarkan uang muka.
    - `JUMLAH` adalah nilai uang muka yang sifatnya global bukan uang muka per transaksi.
    - `Per Tgl.` adalah tanggal terhitung saldo awal persediaan. Untuk tanggal kami sarankan mengisi di tanggal terakhir sebelum bulan Anda memulai. Contoh Anda memulai input pada bulan September 2021, maka isi lah tanggalnya yaitu 31 Agustus 2021.

### Saldo Awal Giro Dibuka / Diterima

Untuk menu saldo awal giro dibuka / diterima saat ini hanya dapat diisi melalui excel.

1. Setelah mengunduh file excel kami, silahkan pilih sheet `GIRO`.
2. Penjelasan kolom:
    - `JENIS GIRO` berisi `DIBUKA` untuk giro dibuka ke supplier dan `DITERIMA` untuk giro diterima dari customer.
    - `PERKIRAAN` adalah COA Kas / Bank yang menerima atau mengeluarkan giro.
    - `SUPPLIER/CUST` berisi kode supplier / customer yang bersangkutan. Anda dapat menemukan kode supplier / customer pada menu `Daftar Customer` atau `Daftar Supplier`.
    - `JUMLAH` adalah nilai uang muka yang sifatnya global bukan uang muka per transaksi.
    - `TGL. DITERIMA` adalah tanggal terhitung giro dibuka / diterima.
    - `TGL. JATUH TEMPO` adalah tanggal jatuh tempo giro.
