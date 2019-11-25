---
description: >-
  Linux üzerinde çok sık kullanılan ve faydalı olacak olan bir kaç terminal
  yöntemleri
---

# 🤞 Terminal Numaraları

## 🔰 Numaralara Giriş

* Terminal üzerinden hızlıca dosya düzenlemek isterseniz `nano` komutunu kullanın
* Tüm terminal ön işlemleri `~/.bashrc` dosyasındadır.
* `alias` ile kendinize özgü komutlar oluşturabilirsiniz
  * sudo ile kullanılması için `alias sudo='sudo '` satırını `.bashrc` dosyanıza eklemeniz gerekmektedir
  * `echo "alias sudo='sudo '" >> ~/.bashrc`
  * Kaynak için [buraya](https://askubuntu.com/a/22043/898692) bakabilirsin
* `grep` komutu ile dosya araması yapabilirsiniz.
  * Kaynak için [buraya](https://stackoverflow.com/a/16957078/9770490) bakabilirsin.

## 📋 Detayları Komutlar

| Yöntem | Açıklama |  |  |
| :--- | :--- | :--- | :--- |
| `<komut> --help` | Komutlar için yardım metni |  |  |
| ⭾ Tab | Kod tamamlama |  |  |
| `cwd` | Çalışma dizini yolu |  |  |
| `-` | Son çalışan dizine gitme |  |  |
| `~` | Home dizini |  |  |
| `<komut>; <komut>;` | Birden fazla komut işleme \(birbirlerini beklemez\) |  |  |
| `<komut> && <komut>` | 1. komut çalışırsa 2.'yi işleme |  |  |
| \` |  | \` | 1. olmazsa 2. komutu işleme |
| \` | \` | İlk komutun sonucunu 2'ye aktarma \(pipeline\) |  |
| ✲ Ctrl + W | Kelime silme |  |  |
| ✲ Ctrl + R `<aranan_terim>` | Önceki komutlarda arama yapma |  |  |
| ✲ Ctrl + Q | Kitlenmiş terminali kurtarma |  |  |
| ✲ Ctrl + A | Komutların satırının başına gelme |  |  |
| ✲ Ctrl +E | Komut satırının sonuna gelme |  |  |
| `tail -f <dosya>` | Dosyayı anlık olarak okuma |  |  |
| `cat` ve `less` | Ufak ve büyük dosyaları okuma |  |  |
| `!$` | Bir önce kullanılan değişkeni kullanma |  |  |
| `!!` | Bir önceki komutu kullanma |  |  |
| `alias` | Komut yönlendirme, yeni komut oluşturma |  |  |
| ✲ Ctrl + ⎇ Alt + E | Oluşturulan komutların \(alias\) karşılıklarını gösterme |  |  |
| ✲ Ctrl + ⇧ Shift + C | Kopyalama işlemi |  |  |
| ✲ Ctrl + ⇧ Shift + V | Yapıştırma işlemi |  |  |
| \`yes | \` | İnteraktif veri isteyen işleme 'yes' verisi gönderme |  |
| `grep <aranan_kelime>` | Kelime arama |  |  |
| \` | grep \` | Komut sonucunda kelime arama |  |

