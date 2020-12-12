---
title: Kompresi Data Pada Teks, Citra, Audio/Video
description: Membahas pengertian serta contoh aplikasi dari kompresi data
tags: [algoritma]
createdAt: 2020-12-11
author: Alvin Maulana
---

## Pengertian Kompresi Data
Secara kalimat, kompresi itu adalah memampatkan atau memperkecil ukuran. Sedangkan jika digabungkan makan kompresi data adalah teknik dalam ilmu komputer untuk mengecilkan data sehingga dapat memperoleh sebuah file yang lebih kecil daripada ukuran aslinya. Atau bisa dibilang kompresi data adalah sebuah cara untuk memadatkan data sehingga hanya memerlukan sebuah ruangan yang lebih kecil dan dapat menjadi lebih efisien dalam penyimpanan serta mempersingkat waktu pertukaran data tersebut.

## Jenis-jenis Kompresi Data
Untuk jenis-jenis kompresi data terdapat berdasarkan mode pengiriman data yang diterima serta berdasarkan output.
Berdasarkan mode pengiriman data yang diterima adalah :
1. **Retrieval Mode**
Retrieval Mode adalah proses penerimaan data yang tidak dilakukan secara real-time (langsung). Mode ini dapat melakukan fast forward dan fast rewind pada sisi client dan dapat dilakukan random access terhadap data dan dapat bersifat interaktif

2. **Dialoque Mode**
Dialoque Mode adalah proses penerimaan data yang dimana pengirim dan penerima seakan-akan berdialog secara langsung (real time) seperti contohnya pada video conference. Waktu tunda atau delay tidak boleh dari 150 ms, yang dimana 50 ms untuk proses kompresi dan dekompresi dan 100 ms adalah untuk mentransmisikan data dalam jaringan

Berdasarkan outputnya adalah : 
1. Lossy Compression
<p>Lossy Compression adalah jenis kompresi yang dimana hasil dari kompresi tidak sama dengan data sebelum dikompresi tetapi sudah “cukup” untuk bisa digunakan. Kelebihan dari jenis kompresi ini adalah ukuran file yang dihasilkan lebih kecil dibandingkan dengan lossless compression namun masih tetap bisa untuk digunakan.</p>
<p>Kompresi jenis ini memiliki teknik dengan membuang bagian-bagian data yang tidak begitu berguna, tidak begitu dirasakan, tidak begitu dilihat oleh manusia sehingga manusia masih beranggapan bahwa data tersebut masih bisa digunakan walaupun sudah dikompresi.</p>
<p>Misalnya saja terdapat file gambar dengan ukuran 30,249 bytes yang kemudian dilakukan kompresi dengan JPEG kualitas 30 dan menjadi berukuran 4,537 bytes berarti file gambar tersebut 85% lebih kecil dan rasio kompresi adalah 15% Contoh file yang menggunakan jenis kompresi ini adalah seperti MP3, Media Streaming, JPEG, MPEG, dan WMA.</p>

2. Lossless Compression
<p>Jenis kompresi ini adalah dimana data hasil kompresi dapat dilakukan dekompresi lagi dan hasilnya tetap sama seperti data sebelum proses kompresi. Kompresi ini digunakan jika dibutuhkannya data setelah proses kompresi harus dapat melakukan dekompresi lagi dengan hasil yang sama seperti sebelum kompresi. Namun terkadang ada data-data yang setelah dikompresi dengan jenis ini malah ukurannya menjadi lebih besar ataupun sama.</p>
Contoh aplikasi aplikasi yang dapat digunakan untuk lossless compression adalah ZIP, RAR, GZIP, dan 7-Zip

## Kompresi Pada Teks
<p>Untuk kompresi data pada teks dilakukan dengan metode lossless compression. Karena jika menghilangkan salah satu atau beberapa karakter, maka makna dari teks tersebut akan hilang dan berbeda artinya.</p>
<p>Kompresi data pada teks terdapat 2 macam cara, diantaranya adalah dengan Character-based Frequency counting dan Word-based Frequency counting. Yang dimana 2 macam cara tersebut menggunakan algoritma yang berbeda pula. </p>
- Character-based Frequency counting </br>
Menggunakan algoritma Huffman Encoding serta Arithmetic Encoding </br>
- Word-based Frequency counting </br>
Menggunakan algoritma Lempel-Ziv (LZ) algorithm
<p>Salah satu contoh kompresi data pada teks akan dijelaskan dengan metode Huffman Encoding.</p>

### 1. Huffman Encoding
<p>Merupakan sebuah algoritma kompresi data yang dapat digunakan dalam data teks yang dibuat oleh mahasiswa MIT yang bernama David Huffman. Huffman Encoding adalah algoritma paling lama serta yang paling terkenal dalam kompresi teks. Metode ini bekerja dengan cara mereduksi / memotong panjang kode rata-rata dan menghasilkan kode prefiks (awalan) yang digunakan untuk merepresentasikan simbol-simbol dari suatu jenis huruf.
</p>
<p>Huffman Encoding dalam prosesnya menggunakan struktur pohon. Struktur pohon dikenal dengan terminologi parent (orang tua) dan child (anak). Parent (orang tua) adalah sebuah simpul yang memiliki lintasan ke simpul lain dengan level dibawahnya. Sedangkan child (anak) adalah sebuah simpul yang memiliki lintasan ke simpul lain dengan level di atasnya.</p>
<p>Berdasarkan jumlah anak pohon huffman encoding dikategorikan sebagai berikut : 
<br>- Uner : Pohon dengan orang tua (parent) yang hanya memiliki satu anak (child)
<br>- Biner : Pohon dengan orang tua (parent) yang memiliki dua anak (child)
<br>Proses pengkodean dengan huffman encoding menggunakan panjang bit yang bervariasi dalam pengkodean sebuah karakter. Karakter dengan frekuensi kemunculan yang lebih besar memiliki panjang bit yang lebih pendek.
</p>

Untuk cara kerja dari Huffman Encoding adalah sebagai berikut :
- Menghitung banyaknya jenis karakter dan jumlah dari masing-masing karakter yang terdapat dalam sebuah file.
- Menyusun  setiap  jenis  karakter dengan  urutan jenis  karakter  yang  jumlahnya  paling  sedikit  ke yang jumlahnya paling banyak.
- Membuat    pohon    biner    berdasarkan    urutan karakter  dari  yang  jumlahnya  terkecil  ke  yang terbesar, dan memberi kode untuk tiap karakter.
- Mengganti   data   yang   ada   dengan   kode   bit berdasarkan pohon biner.
- Menyimpan   jumlah   bit   untuk   kode   bit   yang terbesar,   jenis   karakter   yang   diurutkan   dari frekuensi  keluarnya  terbesar  ke  terkecil  beserta data   yang   sudah   berubah   menjadi   kode   bit sebagai data hasil kompresi.

Contoh kompresi dengan metode Huffman Encoding pada teks “CONTOH”. Teks ini memiliki ukuran 6 byte atau satu karakter sama dengan 1 byte. Berdasarkan cara kerja yang sudah diuraikan diatas, maka dapat dilakukan sebagai berikut :

1. Mencatat yang ada dan jumlah tiap karakter. C = 1, O = 2, N = 1, T = 1, H = 1
2. Mengurutkan dari kecil ke besar
<table>
    <thead>
        <th>Karakter</th>
        <th>Frekuensi</th>
    </thead>
    <tbody>
        <tr>
            <td>C<td>
            <td>1<td>
        </tr>
        <tr>
            <td>N<td>
            <td>1<td>
        </tr>
        <tr>
            <td>T<td>
            <td>1<td>
        </tr>
        <tr>
            <td>H<td>
            <td>1<td>
        </tr>
        <tr>
            <td>O<td>
            <td>2<td>
        </tr>
    </tbody>
</table>

3. Membuat pohon biner dari tiap karakter
<table>
    <thead>
        <th>Karakter</th>
        <th>Code Word</th>
    </thead>
    <tbody>
        <tr>
            <td>C<td>
            <td>00000<td>
        </tr>
        <tr>
            <td>N<td>
            <td>10000<td>
        </tr>
        <tr>
            <td>T<td>
            <td>1000<td>
        </tr>
        <tr>
            <td>H<td>
            <td>100<td>
        </tr>
        <tr>
            <td>O<td>
            <td>10<td>
        </tr>
    </tbody>
</table>

4. Semua karakter dalam string dapat diganti dengan kode binernya yaitu 
000001010000100010100
Karena angka 0 dan 1 mewakili 1 bit sehingga data bit diatas terdiri dari 21 bit yang sama seperti kira kira 2,625 byte dari yang awalnya adalah 6 byte.

## Kompresi Data Pada Citra(Gambar)
<p>Pada kompresi data untuk citra (gambar) yaitu bertujuan untuk mengurangi redudansi yang ada pada file citra (gambar) untuk menyimpan / mengirimkan data dalam bentuk yang paling efisien.</p>
<p>Kompresi data pada citra (gambar) dapat menggunakan jenis kompresi lossless compression maupun lossy compression. Dalam lossless compression, file citra (gambar) tidak akan mengalami penurunan kualitas dari file citra (gambar) yang hendak dikompres nantinya. Biasanya kompresi pada citra dengan lossless compression ini digunakan pada keperluan arsip, pencitraan medis, gambar teknis, dan sebagainya. Untuk jenis lossless algoritma yang digunakan antara lain : Run Length Encoding, Entropy Encoding (Huffman, Aritmatik), dan Adaptive Dictionary Based (LZW). Contoh kompresi pada data citra (gambar) dengan jenis kompresi lossless adalah untuk pada format gambar yang menggunakan format RAW, BMP, dan PNG yang sangat cocok digunakan dalam format gambar dengan dominan teks gambar dengan background yang transparan
</p>
<p>Untuk jenis kompresi pada data citra (gambar) lossy compression adalah dengan mengecilkan ukuran resolusi suatu citra (gambar) sehingga kualitas gambar akan ikut menjadi turun dan membuat size gambar menjadi lebih kecil. Teknik ini mengubah detail dan warna pada file citra (gambar) menjadi lebih sederhana tanpa terlihat perbedaannya yang mencolok dalam pandangan manusia, sehingga ukurannya menjadi lebih kecil. Untuk teknik dalam lossy compression pada file citra (gambar) adalah : Color Reduction dan Chroma Subsampling</p>

![](https://pemrogramanmatlab.files.wordpress.com/2018/11/contoh-program-kompresi-citra.jpg)

## Kompresi Pada Data Video/Audio 
<p>Kompresi pada data audio/video adalah bentuk kompresi data yang bertujuan untuk mengecilkan ukuran dari suatu file audio/video. Dalam file audio/video terdapat 2 hal yang dapat dilakukan kompresi, yaitu frame (gambar) dan audionya. Kompresi pada file video/audio menyebabkan kualitas dari file tersebut mengalami penurunan kualitas di berbagai frame ataupun terdapat noise pada audio. Hal itu dikarenakan proses kompresi yang menghilangkan beberapa data yang ada untuk mengecilkan ukuran dari file tersebut.</p>

<p>Video memiliki 3 dimensi yaitu adalah 2 dimensi spasial (horizontal dan vertikal) dan 1 dimensi waktu. Data dalam video redundancy spatial (warna dalam still image), redundancy temporal (perubahan antar frame). Penghilangan pada redundancy spatial dilakukan dengan mengambil fakta bahwa mata manusia tidak terlalu dapat membedakan warna dibandingkan dengan brightness, sehingga gambar / frame dalam video bisa dikompresi.
</p>

<p>Pada kompresi data audio / video dapat juga digunakan metode lossless dan lossy compression. Pada lossless format yang akan dihasilkan adalah FLAC dan pada lossy adalah formanya Vorbis, MP3, MPEG-I.</p>

<p>Berikut ini saya lampirkan beberapa contoh aplikasi dalam kompresi data pada data audio/video yang bernama HandBrake 
</p>

![](https://cdn.keepo.me/images/post/lists/2019/12/20/main-list-image-c59dd146-10f8-4a82-afb7-95a68ad33a84-2.jpg)