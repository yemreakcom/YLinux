---
description: Linux üzerine genel notlarım
---

# ⛺ Genel Notlar

## 👨‍🔧 Linux'ta Varsayılan Olarak Python3 Kullanma

Alttaki komut ile python2'yi kaldırıp, python3'e bağlantı oluşturarak varsayılan olarak python3 kullanabilirsin.

```bash
sudo apt purge python2.x-minimal
sudo ln -sfn /usr/bin/python3.6 /usr/bin/python # python -> python3
sudo ln -s /usr/bin/pip3 /usr/bin/pip # pip -> pip3
```

{% hint style="info" %}
Detaylı bilgiler için [How to safely switch to python3 as default after upgrade to Ubuntu 18.04](https://askubuntu.com/questions/1065572/how-to-safely-switch-to-python3-as-default-after-upgrade-to-ubuntu-18-04) alanına bakabilirsin
{% endhint %}

## 📶 Telefon ile PC Arasında Dosya Paylaşımı

* Telefonunuza [Share Music & Transfer Files - Mi Drop](https://play.google.com/store/apps/details?id=com.xiaomi.midrop) uygulamasını indirin
* Uygulamaya **sadece Dosya Erişim İzni** vermeniz yeterlidirs
* PC ile aynı WiFi ağına bağlanın
* İndirdiğiniz uygulamanın arayüzünden:
  * Sol üstteki buton
  * Connect to Computer
  * Start
  * Portable
* Telefonunzda gözüken `ftp://...` ile başlayan veriyi aklınızda tutun
* Uygulamayı **kapatmadan** ve sol üstteki **geri tuşuna basmadan**, aşağı alabilirsiniz
* Dosya gezgini \(`nautilus`\) açın
  * `Other Locations`
  * _Connect to Server_ alanına **ftp** adresini yazın
  * `Connect`
* Artık `Other Locations` üzerinden direkt olarak erişebilirsiniz

## 🎴 Ekran Paylaşımı

* [Web üzerinden ekran paylaşma](https://askubuntu.com/questions/335158/share-desktop-via-web-browser/536958)
* [guacamole ile web üzerinden paylaşma](http://guacamole.apache.org/)

## 🔤 Font Yükleme

```bash
mkdir -p ~/.font # Yerel font dizinini oluşturma
mv <font.ttf> ~/.font # Font dosyasını gerekli yere aktarma
fc-cache -fv # Fontları yeniden derleme
```

## 🚀 Çalışma Alanlarını Bağımsızlaştırma \(Isolate Workspace\)

Bu işlem için `isolate workspaces` ayarını dash, dock ya da panel ayarlarında aktif hale getirmemiz lazım.

> Panel için `dock` yazan kısma `panel` yazıp komutu kullanın.

```bash
gsettings set org.gnome.shell.extensions.dash-to-dock isolate-workspaces true
```

## 🏃‍♂️ Grub Menüyü Atlama

* `sudo nano /etc/default/grub` ile grub yapılandırma dosyasını açın
* En alt kısmına `GRUB_HIDDEN_TIMEOUT=0` yazın ve `GRUB_TIMEOUT=0` yapın
* ✲ Ctrl + S e basarak kayıt edin, ✲ Ctrl + X ile çıkış yapın
* `sudo update-grub` ile yine grub ayarlarını aktifleştirin

## 🔗 Faydalı Bağlantılar

* [Ubuntu 19.04 yenilikleri](https://itsfoss.com/ubuntu-19-04-release-features/)
* [Linux bilgisayarlarını birbirine bağlama](https://www.maketecheasier.com/netcat-transfer-files-between-linux-computers/)
* [Uygulamalar için neden sudo -h kullanılmalı](https://askubuntu.com/questions/270006/why-should-users-never-use-normal-sudo-to-start-graphical-applications)

