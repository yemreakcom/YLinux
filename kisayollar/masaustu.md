---
description: Masaüstü kısayolları (desktop shortcuts) oluşturma
---

# 💫 Masaüstü Kısayolları

## 🧱️ Kısayol Oluşturma Temeli

Text editörü açıp

```bash
gedit dosya/yolu.desktop
```

Alttaki alanda gerekli yerleri doldurun.

```text
#!/usr/bin/env xdg-open

[Desktop Entry]
Version=1.0
Type=Application
Terminal=false
Exec=command to run here
Name=visible name here
Comment=comment here
Icon=icon path here
```

Son olarak dosyanın bulunduğu dizinde terminali açıp, dosyayı güvenilir olarak işaretleyin \(?\)

```bash
chmod +x dosyadi.desktop
```

> Detaylı bilgi için [buraya](https://askubuntu.com/a/282187) bakabilirsin.

## 📞 Whatsapp Kısayolu

Text editörü açıp;

```bash
sudo -H gedit /usr/share/applications/whatsapp-webapp.desktop
```

açılan yere alttaki verileri kopyalayın;

```text
#!/usr/bin/env xdg-open
[Desktop Entry]
Name=WhatsApp
GenericName=WhatsApp
Comment=WhatsApp desktop webapp
#Exec=webapp-container --store-session-cookies --webappUrlPatterns=https?://*.whatsapp.com/* --user-agent-string='Mozilla/5.0 (Windows NT 6.1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/41.0.2228.0 Safari/537.36' https://web.whatsapp.com %u
Exec=/opt/google/chrome/google-chrome --app=https://web.whatsapp.com/
Terminal=false
Type=Application
StartupNotify=true
MimeType=text/plain;
# Alttaki alana ikon yolunuzu kopyalayın
# Icon=
Categories=Network;Application;
Keywords=WhatsApp;webapp;
X-Ubuntu-Gettext-Domain=WhatsApp
StartupWMClass=web.whatsapp.com
```

### 🎴 Whatsapp İkonu Ekleme

İlk olarak [buradaki](https://github.com/yedhrab/YWiki/tree/169abadfd1b8862c004399268f6ca1f9f9359d61/res/whatsapp-webapp.svg) ikonu indirin.

* İndirdiğiniz dosyanın yolunu kopyalayın
* `gedit /usr/share/applications/whatsapp-webapp.desktop` komutu ile dosyayı tekrar açın
* İçerisinde `Icon=` olan satırın başındaki `#` karkterini silin ve yolu kopyalayın
  * Örn: `Icon=/home/yemreak/Pictures/Ikons/Svg/whatsapp-webapp.svg`

## 👷‍♂️ Wmctrl ile Kısayol Oluşturma

Alttaki komut ile wapp açıksa gösterme, kapalıysa oluşturmayı sağlayabilirsin.

```bash
bash -c "wmctrl -xa web.whatsapp.com || /opt/google/chrome/google-chrome --app=https://web.whatsapp.com/"
```

