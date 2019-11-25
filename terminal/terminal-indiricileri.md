---
description: Linux üzerinde tarayıcı kullanmadan terminal üzerinden indirmek
---

# ⏬ Terminal İndiricileri

## 👨‍💼 Aria2c, Dosyayı Parçalayarak İndirme \(IDM gibi\)

Toplu olarak dosya indirmeyi sağlayan CLI tabanlı bir araçtır.

* [Dökümantasyon](https://aria2.github.io/manual/en/html/aria2c.html)
* [İndirme sayfası](https://aria2.github.io/)

| Flag | Açıklama |
| :--- | :--- |
| `-q` | Sesiz çalışma |
| `-c` | İndirmeye kalındığı yerden devam etme ayarı |
| `-P` | Parametreli url `http://host/image[000-100:2].img` veya `http://{sv1,sv2,sv3}/foo.iso` |
| `-x <sayı>` | İndirme sırasında sunucuya `<sayı>` kadar bağlanılır |
| `-s <sayı>` | Dosyayı `<sayı>` kadar url ile indirir, url sayısı azsa bir url birden fazla kullanılır |
| `-k <boyut>` | Verileri `<boyut>` kadar parçalara ayırıp indirir |
| `-i <url_file>` | Dosya ile indirme |
| `-d <dir_path>` | Çıktı dizini |
| `-o <path>` | Çıktı yolu |

## ⭐ Örnekler

```bash
# Çoklu indirme
aria2c -x 16 -s 16 <url>

# Download from WEB:
aria2c http://example.org/mylinux.iso

# Download from 2 sources:
aria2c http://a/f.iso ftp://b/f.iso

# Download using 2 connections per host:
aria2c -x2 http://a/f.iso

# BitTorrent:
aria2c http://example.org/mylinux.torrent

# BitTorrent Magnet URI:
aria2c 'magnet:?xt=urn:btih:248D0A1CD08284299DE78D5C1ED359BB46717D8C'

# Metalink:
aria2c http://example.org/mylinux.metalink

# Download URIs found in text file:
aria2c -i uris.txt

# Download to dir
aria2c -i <file> -d <dir>
aria2c -i urls.txt -d downloads # örnek
```

## ⏬ Wget, Linux Standart CLI İndiricisi

* Linux için kurulum gerektirmez.
* Kurulum sayfasına [buraya](https://eternallybored.org/misc/wget/) tıklayarak yönlenebilrsin.
  * [Windows x64](https://drive.google.com/open?id=1UULzjZVRpjVgDiDsVhLtWW7oggVfHFUK)

> `wget -h` ile komutlarına bakabilirsin

Temel kullanım: `wget <flag> <yol>`

| Flag | Açıklama |
| :--- | :--- |
| `-q` | Çıktısız indirme \(quiet\) |
| `-i <url_file>` | Dosya ile indirme |
| `-O <path>` | Çıktı dosyası |
| `-P <dir_path>` | Çıktı dizini |
| `-r` | Tüm indirilebilir içeriği indirme |
| `nd` | İndirme sırasında dizin oluşturmayı engelleme \(nodir\) |
| `-A <ext>` | Sadece verilen uzantıdaki dosyaları indirme |

