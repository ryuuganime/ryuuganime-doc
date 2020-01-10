# Mencari Entri Web Lain Melalui SIMKL Search

> Sebelum melanjutkan, pastikan Anda telah memasang ekstensi SIMKL Search di peramban anda. Ekstensi tersedia di [Chrome Web Store](https://chrome.google.com/webstore/detail/simkl-search-select-and-s/mdofghopgfobjkgepojjmcfljnocaaff).

Untuk pengaturan awal, lakukan hal berikut ini:

1. Klik kanan pada logo SIMKL Search di ekstensi. Pilih Opsi \(Options\).
2. Lalu, buka menu `Import/Export Config` yang terletak di sebelah kiri.
3. Salin dan tempelkan kode berikut ke dalam kotak yang tertera di menu import tersebut.

```javascript
{
   "newTab":true,
   "newTabSelected":true,
   "newTabPosition":"Last",
   "trackGA":true,
   "searchEverywhere":true,
   "searchEverywhereGroups":false,
   "searchEngines":[
      {
         "name":"AniList",
         "url":"https://anilist.co/search/anime?sort=SEARCH_MATCH&search=%s",
         "incognito":false,
         "group":"",
         "$$hashKey":"object:154"
      },
      {
         "name":"Anime-Planet",
         "url":"https://www.anime-planet.com/anime/all?name=%s",
         "incognito":false,
         "group":""
      },
      {
         "name":"aniSearch",
         "url":"https://www.anisearch.com/anime/index?text=%s&char=all&q=true",
         "incognito":false,
         "group":"",
         "plus":true
      },
      {
         "name":"Annict",
         "url":"https://annict.com/search?q=%s",
         "incognito":false
      },
      {
         "name":"Kitsu",
         "url":"https://kitsu.io/anime?text=%s",
         "incognito":false
      },
      {
         "name":"LiveChart",
         "url":"https://www.livechart.me/search?q=%s",
         "incognito":false
      },
      {
         "name":"Metacritic",
         "url":"https://www.metacritic.com/search/tv/%s/results",
         "incognito":false
      },
      {
         "name":"Notify",
         "url":"https://notify.moe/search/%s",
         "incognito":false
      },
      {
         "name":"Onnada",
         "url":"http://onnada.com/search/?q=%s&x=0&y=0",
         "incognito":false
      },
      {
         "name":"Rotten Tomatoes",
         "url":"https://www.rottentomatoes.com/search/?search=%s",
         "incognito":false
      },
      {
         "name":"Shikimori",
         "url":"https://shikimori.org/animes?search=%s",
         "incognito":false
      },
      {
         "name":"Trakt",
         "url":"https://trakt.tv/search?query=%s",
         "incognito":false
      },
      {
         "name":"Nautiljon",
         "url":"https://www.nautiljon.com/animes/?q=%s&annee_min_jj=&annee_min_mm=&annee_min_aaaa=&annee_max_jj=&annee_max_mm=&annee_max_aaaa=&annee_vf_min_jj=&annee_vf_min_mm=&annee_vf_min_aaaa=&annee_vf_max_jj=&annee_vf_max_mm=&annee_vf_max_aaaa=&licencie=&nb_ep_min=&nb_ep_max=&public_averti=&editeur=&societe=&pays=&titre_alternatif=1&titre_alternatif_suite=1&titre_original_latin=1&titre_original=1&has=&tri=0",
         "incognito":false,
         "plus":true
      },
      {
         "name":"SIMKL",
         "url":"https://simkl.com/search/?type=anime&q=%s",
         "incognito":false
      }
   ]
}
```

4. Tekan Import.  
5. Apabila muncul pesan, tekan YES.

