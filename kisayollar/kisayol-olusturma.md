---
description: Linux üzerinde herhangi bir uygulama için kısayol oluşturma
---

# ✨ Kısayol Oluşturma

## ✨ Uygulama için `WM_CLASS` metnini tanımlama

To do this, you need to make desktop app.

* Terminale `sudo -H gedit /usr/share/applications/<appname>.desktop` komutunu yazın
* Açılan dosyada gerekli bilgileri, [buradaki](https://askubuntu.com/a/282187) bilgiden de yararlanarak doldurun
* Örnek dosya içeriği aşağıdaki gibi olacaktır

```text
#!/usr/bin/env xdg-open
[Desktop Entry]
Name=WhatsApp
GenericName=WhatsApp
Comment=WhatsApp desktop webapp
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

## 📑 Herhangi bir uygulamanın `WM_CLASS` metnini alma

* Terminal üzerinde `xprop | grep WM_CLASS` komutu ile `WM_CLASS` metnini alabiliriz
* Komutu yazıp ENTER'a bastıktan sonra kısayolunu oluşturmak istediğimiz uygulamaya tıklıyoruz
* Yandaki gibi bir çıktı gelecektir `WM_CLASS(STRING) = "gnome-terminal-server", "Gnome-terminal`
* `gnome-terminal-server` olan metni ✲ Ctrl + ⇧ Shift + C ile kopyalıyoruz

## 🚀 Kısayolu oluşturma

* SUPER tuşuna basıp arama yerine `shortcut` yazıyoruz
* Açılan pencerenin en altındaki `+` butonuna tıklayarak kısayol ekliyoruz
* **name** alanına herhangi bir isim giriyoruz
* Ardından **command** alanına `bash -c "wmctrl -xa <wm_class> || <wm_class>` yazıyoruz
* Son olarak klavye kısayolunu atıyoruz ve kaydediyoruz

