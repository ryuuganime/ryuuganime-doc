---
description: >-
  Dalam laman ini akan menjelaskan secara detail tata pengisian data entri yang
  benar berdasarkan JSON Schema Entri Database Ryuuganime.
---

# Format JSON

{% hint style="warning" %}
Sebelum melanjutkan, Anda perlu mengetahui struktur [JSON](../ketentuan-umum/definisi-kata/definisi-format-berkas.md#json) dan cara pengisian datanya. Anda dapat mempelajari lebih lanjut mengenai JSON di [sini \(Petani Kode, Struktur JSON\)](https://www.petanikode.com/json-pemula/), [sini \(Codepolitan, Struktur JSON, Rinci\)](https://www.codepolitan.com/mengenal-format-json-59e8152dd0e51), dan [sini \(w3school, Data JSON, Inggris, Rinci\)](https://www.w3schools.com/js/js_json_datatypes.asp).
{% endhint %}

{% hint style="warning" %}
Pastikan Anda dapat mengakses website yang telah didaftar di [sini](../informasi-sumber/situs-tracking-yang-digunakan.md).  
Disarankan untuk memiliki ekstensi SIMKL Search untuk mempermudah dalam input data. Lihat di [sini](../informasi-sumber/mencari-entri-web-lain-di-simkl.md).  
Anda juga disarankan untuk telah meng-_fork_ [repositori](../ketentuan-umum/definisi-kata/#repositori-kendali-versi) [database](../ketentuan-umum/definisi-kata/#database-pangkalan-data) Ryuuganime, memasang aplikasi [Git](../ketentuan-umum/definisi-kata/#git) dan Visual Studio Code \(atau aplikasi teks editor yang mendukung Git\) versi terbaru.
{% endhint %}

Sebagai informasi tambahan, sebelum anda mengisi entri database dalam bentuk format JSON, Anda perlu memperhatikan beberapa syarat tambahan sebagai berikut:

* Indentifikasi \(pelekukan\) baris: Spasi: 4
* JSON Schema: ada. Lihat [sini](https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/schema.json).

{% hint style="success" %}
Versi HJSON telah tersedia untuk kemudahan pengisian format data. Lihat di [sini](format-hjson.md).
{% endhint %}

Skema JSON adalah sebagai berikut:

{% code title="schema.json" %}
```javascript
{
    "$schema": "http://json-schema.org/draft-07/schema#",
    "title": "Ryuuganime JSON Schema for Anime Database, v.2-b",
    "description": "Anime JSON Entry Validator in JSON Schema of Ryuuganime.\nPerformance issues or else may occurs on this Schema while it's on Beta version.",
    "type": "object",
    "additionalProperties": false,
    "required": [
        "title",
        "backdrop",
        "visualKey",
        "synopsis",
        "information",
        "scores",
        "updatedDate",
        "fansub",
        "fanshare",
        "fanstream",
        "library"
    ]
}
```
{% endcode %}

## title

Judul serial dalam berbagai bahasa. Berdasarkan lokasi ICU. Untuk informasi mengenai ICU lebih lanjut, silakan kunjungi [laman berikut](http://www.localeplanet.com/icu/).  
Skema value objek adalah sebagai berikut:

{% code title="schema.json > properties > title" %}
```javascript
{
    "type": "object",
    "required": [
        "native",
        "en_Latn",
        "ar_001",
        "hu_HU",
        "he_IL",
        "id_ID",
        "en_US",
        "ja_JP",
        "de_DE",
        "ko_KR",
        "fr_FR",
        "pt_PT",
        "ru_RU",
        "es_ES",
        "zh_Hans",
        "zh_Hant",
        "vi_VN"
    ],
    "additionalProperties": true
}
```
{% endcode %}

### native

Merupakan judul dalam bahasa asli serial dari negara asal, contoh "アサティール 未来の昔ばなし" dalam bahasa Jepang untuk anime Asatir: Mirai no Mukashi Banashi yang ditayang di Jepang.

Skema `native` dapat dikatakan "tidak _restrictive_"_,_ mengingat objek menggunakan string dari berbagai bahasa.

{% code title="schema.json > properties > title > properties > native" %}
```javascript
{
    "type": "string"
}
```
{% endcode %}

Untuk pengisian data, lihat AniDB, MyAnimeList, Kitsu, AniList, The TVDB, The Movie DB, Trakt.

Contoh entri:

{% code title="json/1.json" %}
```javascript
        "native": "富豪刑事 Balance:UNLIMITED",
```
{% endcode %}

### en\_Latn

Judul dalam bentuk Romaji \(untuk Jepang\), Romaja \(Korea\), atau Latin. Diperlukan untuk penamaan judul serial dalam entri.

Skema `en_Latn` adalah sebagai berikut:

{% code title="schema.json > properties > title > properties > en\_Latn" %}
```javascript
{
    "type": "string",
    "pattern": "^[\\w\\s\\S]+$"
}
```
{% endcode %}

Untuk pengisian data, ikuti penamaan judul serial pada MyAnimeList, Kitsu, Shikimori, Otak Otaku, dan AniList.

Contoh:

{% code title="json/1.json" %}
```javascript
        "en_Latn": "Fugou Keiji: Balance:Unlimited",
```
{% endcode %}

### ar\_001

