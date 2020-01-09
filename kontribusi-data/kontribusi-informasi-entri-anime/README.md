# Kontribusi Informasi Entri Anime

> Sebelum melanjutkan, pastikan Anda dapat mengakses website yang telah didaftar di [sini](../../informasi-sumber/situs-tracking-yang-digunakan.md).  
> Disarankan untuk memiliki akun SIMKL untuk mempermudah dalam input data. Lihat di [sini](mencari-entri-web-lain-di-simkl.md).  
> Anda juga disarankan untuk telah meng-fork repo Ryuuganime, memasang aplikasi Git dan Visual Studio Code versi terbaru

Berikut tata cara menginput data:

1. Buka salah satu entri yang ingin diisi di `../lib/anime-db/`.
2. Buka SIMKL, cari anime yang dituju, dan lakukan pencarian ke situs.
3. Pada baris pertama, yaitu pada `<img src="" width="640" />`, isilah link gambar _backdrop_ dari situs The Movie DB ataupun TVDB di antara tanda kutip di `src=""`. Petunjuk lebih lanjut dapat dilihat di [sini](mengisi-tautan-gambar-dari-tmdb-dan-tvdb.md).
4. Kemudian, isilah sinopsis yang terdapat di Otak Otaku dengan cara menyalin dan tempelkan di samping kanan setelah `<p>&emsp;&emsp;` dan sebelum `</p>`
5. Selanjutnya, cantumkan nama situs yang dipakai untuk sinopsis di `<i>Sumber:` 
6. Untuk Judul alternatif dan sinonim, dapat dilihat di sini.
7. Pada `<li>Tipe: <a href="https://ryuuganime.blogspot.com/search/label/"></a></li>` isilah jenis tayangan berdasarkan informasi di Otak Otaku setelah `/label/` dan  sebelum `</a>` \(dua kali\). Contoh: 

   `<li>Tipe: <a href="https://ryuuganime.blogspot.com/search/label/TV">TV</a></li>`

8. Lalu, pada informasi episode, isi sesuai yang tertera di MyAnimeList ataupun SIMKL.
9. Untuk informasi status, memiliki beberapa kasus. Anda dapat melihat rinciannya di [sini](status-penayangan.md).
10. Pengisian informasi _genre_ dan _tag_ dapat dilihat di [sini ](genre-dan-tag.md)mengingat bedanya penggolongan _genre anime_ di MyAnimeList, dst dengan Ryuuganime.
11. Pada saat isi informasi musim, Anda hanya perlu mengisi di bagian `title="Dirilis pada"` di tag `div` dan  &lt;a href="https://ryuuganime.blogspot.com/search/label/&gt;&lt;/a&gt; saja. Tata cara pengisian dapat dilihat di [sini](musim.md).
12. Isi durasi per episode dalam satuan menit.
13. 
