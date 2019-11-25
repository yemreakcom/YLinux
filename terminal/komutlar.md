# 👨‍💻 Terminal Komutları

## 🧱 Temel Komutlar

Detaylar için [buraya](https://gist.github.com/sayz/1130312/a45b548b82ee459e05a9159ec532224757a2ca56) tıklayarak, açıklamalara ulaşabilirsin.

* `clear` Terminali temizleme
* `sudo -s` Terminali root yapma `exit` rootlu terminali kapatma
* `sudo apt-get install <paket_adi>` Paket kurulumu
* `sudo apt-get install --fix-broken` Hatalı kurulumları veya gerekli bağımlılıkları kurma
* `sudo apt-get purge <paket_adi>` paket adı paketini kaldırma
* `sudo apt-get purge <paket_adi>*` Bulunan dizinde paket ile başlayan tüm paketleri kaldırma
* `sudo apt-get purge '<paket_adi>*'` paket ile başlayan tüm paketleri ve alt bileşenlerini kaldırma
* `sudo apt-cache search <paket_adi>` Depoda paketadi arama işlemi

## 👮‍♂️ Sudo Komutları

| Komut | Açıklama |
| :--- | :--- |
| `search` | search in package descriptions |
| `show` | show package details |
| `install` | install packages |
| `reinstall` | reinstall packages |
| `remove` | remove packages |
| `autoremove` | Remove automatically all unused packages |
| `update` | update list of available packages |
| `upgrade` | upgrade the system by installing/upgrading packages |
| `full-upgrade` | upgrade the system by removing/installing/upgrading packages |
| `edit-sources` | edit the source information file |

