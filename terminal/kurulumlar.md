---
description: Linux üzerinde uygulamaların kurulumu
---

# 👷‍♂️ Uygulama Kurulumları

## 📢 Önemli Hususlar

Linux ile kurulumlar terminal üzerinden bir kaç komut gerektirir.

{% hint style="danger" %}
😫 Yeni Linux kurulum yöntemi olan **snapd** ilk açılmada gecikmeye sebebiyet vermekte
{% endhint %}

## ⏬ Snapd Kurulum

Ubuntu yerel mağazasından yapılan indirmelerdir

* Snapd kurulum önceden derlenmiş ve hazırlanmış uygulamalardır.
* Hız açısından **dpkg** daha iyidir, lakin ek paketler ve bağımlılıklar gerektirir
* Hızlı ve çalışabilirlik açısından **snapd** daha verimlidir, her platformda çalışır

## 📦 Dpkg - Debian Paket Kurma

### ✨ Apt ile kurulum

```bash
sudo apt install -f ./dosya.deb # Hatalı paketleri yenileyerek kurma (-f: --fix-broken)
sudo apt autoremove # Artıkları temizleme
```

### 👨‍💼 Dpkg ile Kurulum

* `sudo dpkq -i deb_uzantılı.deb` \(kurulumu başlatma\)
* `sudo apt-get install --fix-broken` \(kurulum için gerekli paketleri kurma\)
* `sudo dpkq -i deb_uzantılı.deb` \(kurulumu yeniden deneme\)
* `sudo apt-get autoremove` \(gereksizleri kaldırma\)

> Kaynak için [buraya](https://unix.stackexchange.com/a/159114/344875) bakabilirsin.

## 📂 Tar dosyalarının kurulumları

Tar.gz uzantılı dosyayı bulup, sağ tıklayıp, buraya çıkar diyoruz. Ya da terminal yardımıyla arşivi çıkarın

| Parametre | Açıklama |
| :--- | :--- |
| `x` | Çıkarmak \(e**x**tract\) |
| `c` | Arşivelemek \(**c**ompress\) |
| `z` | G**z**ip ile işleme sokma |
| `v` | Yapılan işlemleri gösterme \(**v**erbose\) |
| `f` | Dosya ismi belirtme \(**f**ilename\) |
| `C` | Çıkartılacak dizin |

```bash
tar xzvf "dosya.tar.gz" -C "./dizin"
```

> Terminal komutlarını kullandıysanız, direk alttaki komutları uygulayabilirisiniz.

Ardından çıkarılan dosyaların olduğu dizine girip, alttaki komutları yazıyoruz.

```bash
./configure
make -j $(nproc --all)
sudo make install
```

## 💿 AppImage Uzantılı Dosyaların Kurulumu

AppImage özelliği uygulamaları kurmadan çalıştırabilmemizi sağlar.

```bash
chmod a+x <appimage_dosyası>
./<appimage_dosyası>
```

## 🏃‍♂️ Run Uzantılı Dosyaların Kurulumu

Run dosyaları kurulum dosyalarıdır bu sebeple yetkileri olmadan çalıştırılamaz.

```bash
chmod +x <run_dosyası>
./<run_dosyası>
```

## 👨‍💼 Seçmeli veya Koşul Kabul Etmeli Kurulumlar \(Butonu\)

`<OK>` butonunu veya başka butonları seçmek için:

* ⭾ Tab tuşuna basıp ENTER'a basın

## 🧹 Kaldırma Notları

* `sudo apt remove` veya `sudo dpkg -r` komutu ile kaldırabilrsiniz
* `sudo apt remove --purge` veya `sudo dpkg -P` komutu ile yapılandırma ayarları ile kaldırabilirsiniz

