# Format HTML \(Tidak Dilanjutkan\)

{% hint style="danger" %}
Pengisian [Database](../ketentuan-umum/definisi-kata/#database-pangkalan-data) dengan menggunakan format berkas [HTML](../ketentuan-umum/definisi-kata/definisi-format-berkas.md#html) akan tidak dilanjutkan pengembangannya. Akan tetapi, Ryuuganime akan menggunakan JavaScript yang dapat mengambil data database dari [JSON](../ketentuan-umum/definisi-kata/definisi-format-berkas.md#json).
{% endhint %}

{% hint style="warning" %}
Pastikan Anda dapat mengakses website yang telah didaftar di [sini](../informasi-sumber/situs-tracking-yang-digunakan.md).  
Disarankan untuk memiliki ekstensi SIMKL Search untuk mempermudah dalam input data. Lihat di [sini](../informasi-sumber/mencari-entri-web-lain-di-simkl.md).  
Anda juga disarankan untuk telah meng-_fork_ [repo](../ketentuan-umum/definisi-kata/#repositori-kendali-versi) Ryuuganime, memasang aplikasi [Git](../ketentuan-umum/definisi-kata/#git) dan Visual Studio Code \(atau aplikasi teks editor yang mendukung Git\) versi terbaru.
{% endhint %}

Berikut tata cara menginput data:

1. Buka salah satu entri yang ingin diisi di `../lib/anime-db/`.
2. Buka SIMKL, cari anime yang dituju, dan lakukan pencarian ke situs.
3. Pada baris pertama, yaitu pada `<img src="" width="640" />`, isilah link gambar _backdrop_ dari situs The Movie DB ataupun TVDB di antara tanda kutip di `src=""`. Petunjuk lebih lanjut dapat dilihat di [sini](../ketentuan-database/pengambilan-tautan-gambar-backdrop-dan-visual-key.md).
4. Kemudian, isilah sinopsis yang terdapat di Otak Otaku dengan cara menyalin dan tempelkan di samping kanan setelah `<p>&emsp;&emsp;` dan sebelum `</p>`
5. Selanjutnya, cantumkan nama situs yang dipakai untuk sinopsis di `<i>Sumber:` 
6. Untuk Judul alternatif dan sinonim, dapat dilihat di sini.
7. Pada `<li>Tipe: <a href="https://ryuuganime.blogspot.com/search/label/"></a></li>` isilah jenis tayangan berdasarkan informasi di Otak Otaku setelah `/label/` dan  sebelum `</a>` \(dua kali\). Contoh: 

   `<li>Tipe: <a href="https://ryuuganime.blogspot.com/search/label/TV">TV</a></li>`

8. Lalu, pada informasi episode, isi sesuai yang tertera di MyAnimeList ataupun SIMKL.
9. Untuk informasi status, memiliki beberapa kasus. Anda dapat melihat rinciannya di [sini](../ketentuan-database/status-penayangan.md).
10. Pengisian informasi _genre_ dan _tag_ dapat dilihat di [sini](../ketentuan-database/genre-dan-tags.md) mengingat bedanya penggolongan _genre anime_ di MyAnimeList, dst dengan Ryuuganime.
11. Pada saat isi informasi musim, Anda hanya perlu mengisi di bagian `title="Dirilis pada"` di tag `div` dan  `<a href="https://ryuuganime.blogspot.com/search/label/></a>` saja. Tata cara pengisian dapat dilihat di [sini](../ketentuan-database/musim.md).
12. Isi durasi per episode dalam satuan menit.
13. Petunjuk pengisian studio dapat dilihat di [sini](../ketentuan-database/studio.md), mengingat beberapa nama studio menggunakan aksara Latin lanjutan.
14. Isilah informasi rating sesuai dengan yang tercantum di MAL, AniList, IMDb, atau TVDB.
15. Sumber Adaptasi dapat dilihat dari MAL.
16. Asal Negara dapat dikosongkan.

