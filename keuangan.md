---
layout: post
title: Mengelola Keuangan
---

**Penjelasan Singkat**

Modul keuangan digunakan untuk mencatat seluruh arus kas dalam perusahaan. Ada beberapa fitur kunci dalam modul keuangan yang kami sediakan untuk memenuhi kebutuhan perusahaan Anda, fitur-fitur tersebut sebagai berikut:

1. [Transaksi Masuk](#transaksi-masuk)
    1. [Pelunasan Piutang](#pelunasan-piutang)
    1. [Pelunasan Uang Muka Penjualan](#pelunasan-uang-muka-penjualan)
    1. [Pendapatan Lain-Lain](#pendapatan-lain-lain)
1. [Transaksi Keluar](#transaksi-keluar)
    1. [Pelunasan Hutang](#pelunasan-hutang)
    1. [Pelunasan Uang Muka Pembelian](#pelunasan-uang-muka-pembelian)
    1. [Pembayaran Lain-Lain](#pembayaran-lain-lain)
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
    -   Jika pembayaran Giro, pada kolom `No. Giro` isi dengan nomor giro diterima dan `Tanggal Jatuh Tempo Giro` isi dengan estimasi tanggal jatuh tempo giro. Anda dapat melihat bagian `Daftar Giro Diterima` untuk pengelolaan Giro yang sudah dibuat.
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
    -   Jika pembayaran Giro, pada kolom `No. Giro` isi dengan nomor giro diterima dan `Tanggal Jatuh Tempo Giro` isi dengan estimasi tanggal jatuh tempo giro. Anda dapat melihat bagian `Daftar Giro Diterima` untuk pengelolaan Giro yang sudah dibuat.
2.  `COA Cash/Bank` pilih akun kas / bank penerima transaksi masuk.
3.  `Pelanggan` pelanggan yang melakukan pembayaran piutang.
4.  `Tanggal` adalah tanggal transaksi
5.  `Catatan` catatan untuk transaksi tersebut.
6.  klik tombol `Pembayaran Uang Muka Penjualan`, kemudian akan muncul popup daftar nota uang muka penjualan yang belum lunas.
7.  Kemudian klik simpan.
8.  Klik tombol `COA Lain-lain` jika di dalam pembayaran ini terdapat biaya-biaya yang menambah atau mengurangi nilai pembayaran pelunasan. Kemudian klik simpan.
9.  Pastikan pada kolom `Total` adalah nominal pembayaran yang Anda terima di rekening bank / kas Anda.

### Pendapatan Lain-Lain

1.  `Jenis Transaksi Masuk` pilih tipe transaksi masuk: Kas / Bank / Giro.
    -   Jika pembayaran Giro, pada kolom `No. Giro` isi dengan nomor giro diterima dan `Tanggal Jatuh Tempo Giro` isi dengan estimasi tanggal jatuh tempo giro. Anda dapat melihat bagian `Daftar Giro Diterima` untuk pengelolaan Giro yang sudah dibuat.
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
    -   Jika pembayaran Giro, pada kolom `No. Giro` isi dengan nomor giro dibuka dan `Tanggal Jatuh Tempo Giro` isi dengan estimasi tanggal jatuh tempo giro. Anda dapat melihat bagian `Daftar Giro Dibuka` untuk pengelolaan Giro yang sudah dibuat.
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
    -   Jika pembayaran Giro, pada kolom `No. Giro` isi dengan nomor giro diterima dan `Tanggal Jatuh Tempo Giro` isi dengan estimasi tanggal jatuh tempo giro. Anda dapat melihat bagian `Daftar Giro Dibuka` untuk pengelolaan Giro yang sudah dibuat.
2.  `COA Cash/Bank` pilih akun kas / bank penerima transaksi masuk.
3.  `Supplier` supplier yang melakukan pembayaran hutang.
4.  `Tanggal` adalah tanggal transaksi
5.  `Catatan` catatan untuk transaksi tersebut.
6.  klik tombol `Pembayaran Uang Muka Pembelian`, kemudian akan muncul popup daftar nota uang muka pembelian yang belum lunas.
7.  Kemudian klik simpan.
8.  Klik tombol `COA Lain-lain` jika di dalam pembayaran ini terdapat biaya-biaya yang menambah atau mengurangi nilai pembayaran pelunasan. Kemudian klik simpan.
9.  Pastikan pada kolom `Total` adalah nominal pembayaran yang Anda keluarkan dari rekening bank / kas Anda.

### Pembayaran Lain-Lain

1.  `Jenis Transaksi Masuk` pilih tipe transaksi masuk: Kas / Bank / Giro.
    -   Jika pembayaran Giro, pada kolom `No. Giro` isi dengan nomor giro diterima dan `Tanggal Jatuh Tempo Giro` isi dengan estimasi tanggal jatuh tempo giro. Anda dapat melihat bagian `Daftar Giro Dibuka` untuk pengelolaan Giro yang sudah dibuat.
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

## Giro Diterima

### Aktivitas Utama

1. Melihat daftar giro yang pernah dibuat.
2. Melakukan pencairan atau pembatalan giro

### Melihat Daftar Giro

1. Klik menu `Keuangan` kemudian pilih submenu `Giro Diterima` untuk melihat semua daftar giro yang pernah Anda terima.
2. Dalam daftar giro ini ada menu pencarian yang dapat Anda gunakan. Kolom pencarian yang ada sebagai berikut:
    - `No. Dokumen` untuk mencari berdasarkan nomor giro
    - `Pelanggan` untuk mencari berdasarkan pelanggan yang melakukan pembayaran giro
    - `Tanggal` untuk mencari berdasarkan tanggal giro diterima
    - `Tanggal Jatuh Tempo` untuk mencari berdasarkan tanggal giro jatuh tempo
3. Dalam daftar giro juga ada beberapa kolom informasi sebagai berikut:
    - `Tanggal Dibuat` adalah tanggal transaksi giro dibuat
    - `Tanggal Jatuh Tempo` adalah tanggal giro jatuh tempo
    - `No. Dokumen` adalah nomor dokumen giro yang dibuat otomatis oleh sistem
    - `Bank Tujuan` adalah bank penerima pencairan giro
    - `Informasi Pelanggan` berisi informasi pelanggan yang melakukan pembayaran giro
    - `Jumlah` adalah nilai giro
    - `Status` adalah status giro. Ada 3 jenis status yaitu `Menunggu`, `Cair` & `Dibatalkan`

### Melakukan Pencairan Giro atau Pembatalan Giro

1. Masuk ke menu Giro Diterima
2. Pada kolom aksi klik tombol `Ubah Status` kemudian akan muncul popup dengan tombol `Cairkan Giro` atau `Batalkan Giro`
3. Untuk mencairkan Giro, tanggal jatuh tempo harus kurang dari atau sama dengan (<=) tanggal hari ini.
4. Giro yang sudah dicairkan secara otomatis akan membuat transaksi bank masuk dengan nominal giro tersebut.

## Giro Dibuka

### Aktivitas Utama

1. Melihat daftar giro yang pernah dibuat.
2. Melakukan pencairan atau pembatalan giro

### Melihat Daftar Giro

1. Klik menu `Keuangan` kemudian pilih submenu `Giro Dibuka` untuk melihat semua daftar giro yang pernah Anda buka.
2. Dalam daftar giro ini ada menu pencarian yang dapat Anda gunakan. Kolom pencarian yang ada sebagai berikut:
    - `No. Dokumen` untuk mencari berdasarkan nomor giro
    - `Supplier` untuk mencari berdasarkan supplier
    - `Tanggal` untuk mencari berdasarkan tanggal giro dibuka
    - `Tanggal Jatuh Tempo` untuk mencari berdasarkan tanggal giro jatuh tempo
3. Dalam daftar giro juga ada beberapa kolom informasi sebagai berikut:
    - `Tanggal Dibuat` adalah tanggal transaksi giro dibuat
    - `Tanggal Jatuh Tempo` adalah tanggal giro jatuh tempo
    - `No. Dokumen` adalah nomor dokumen giro yang dibuat otomatis oleh sistem
    - `Bank Sumber` adalah bank sumber pembayaran giro
    - `Informasi Supplier` berisi informasi supplier yang melakukan pembayaran giro
    - `Jumlah` adalah nilai giro
    - `Status` adalah status giro. Ada 3 jenis status yaitu `Menunggu`, `Cair` & `Dibatalkan`

### Melakukan Pencairan Giro atau Pembatalan Giro

1. Masuk ke menu Giro Dibuka
2. Pada kolom aksi klik tombol `Ubah Status` kemudian akan muncul popup dengan tombol `Cairkan Giro` atau `Batalkan Giro`
3. Untuk mencairkan Giro, tanggal jatuh tempo harus kurang dari atau sama dengan (<=) tanggal hari ini.
4. Giro yang sudah dicairkan secara otomatis akan membuat transaksi bank keluar dengan nominal giro tersebut.

## Mutasi Kas

### Aktivitas Utama

1. Melihat daftar mutasi & saldo kas.
2. Merubah transaksi kas masuk atau keluar.
3. Menghapus transaksi kas masuk atau keluar.
4. Mencetak bukti kas masuk atau keluar.

### Melihat Daftar Mutasi Kas

1. Untuk melihat daftar mutasi kas klik menu `Keuangan` kemudian submenu `Mutasi Kas`
2. Kemudian akan tampil daftar transaksi kas yang pernah Anda buat.
3. Di bagian atas tabel daftar transaksi terdapat nilai saldo kas. Nilai saldo adalah total dari daftar transaksi yang muncul di tabel.
4. Pada menu pencarian ada beberapa kolom yang dapat Anda gunakan sebagai berikut:
    - `No Dokumen` untuk mencari berdasarkan nomor dokumen kas
    - `No COA` untuk mencari transaksi dengan nomor COA tersebut
    - `Kas` untuk mencari berdasarkan jenis kas yang Anda miliki
    - `Tanggal` untuk mencari berdasarkan tanggal kas dibuat.
    - `Catatan` untuk mencari berdasarkan catatan pada transaksi

### Merubah transaksi kas

1. Masuk ke halaman `Mutasi Kas`
2. Pada daftar transaksi, klik tombol `Ubah` yang ada pada kolom Aksi.

### Menghapus transaksi

1. Masuk ke halaman `Mutasi Kas`
2. Pada daftar transaksi, klik tombol `Hapus` yang ada pada kolom Aksi.

### Mencetak transaksi

1. Masuk ke halaman `Mutasi Kas`
2. Pada daftar transaksi, klik tombol `Cetak` yang ada pada kolom Aksi.

## Mutasi Bank

### Aktivitas Utama

1. Melihat daftar mutasi & saldo bank.
2. Merubah transaksi bank masuk atau keluar.
3. Menghapus transaksi bank masuk atau keluar.
4. Mencetak bukti bank masuk atau keluar.

### Melihat Daftar Mutasi Bank

1. Untuk melihat daftar mutasi bank klik menu `Keuangan` kemudian submenu `Mutasi Bank`
2. Kemudian akan tampil daftar transaksi bank yang pernah Anda buat.
3. Di bagian atas tabel daftar transaksi terdapat nilai saldo bank. Nilai saldo adalah total dari daftar transaksi yang muncul di tabel.
4. Pada menu pencarian ada beberapa kolom yang dapat Anda gunakan sebagai berikut:
    - `No Dokumen` untuk mencari berdasarkan nomor dokumen bank
    - `No COA` untuk mencari transaksi dengan nomor COA tersebut
    - `Bank` untuk mencari berdasarkan jenis bank yang Anda miliki
    - `Tanggal` untuk mencari berdasarkan tanggal bank dibuat.
    - `Catatan` untuk mencari berdasarkan catatan pada transaksi

### Merubah transaksi bank

1. Masuk ke halaman `Mutasi Bank`
2. Pada daftar transaksi, klik tombol `Ubah` yang ada pada kolom Aksi.

### Menghapus transaksi

1. Masuk ke halaman `Mutasi Bank`
2. Pada daftar transaksi, klik tombol `Hapus` yang ada pada kolom Aksi.

### Mencetak transaksi

1. Masuk ke halaman `Mutasi Bank`
2. Pada daftar transaksi, klik tombol `Cetak` yang ada pada kolom Aksi.
