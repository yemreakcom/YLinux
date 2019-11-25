# 🐛 Hata Notları

## 🔌 USB Bağlanma Sorunlarını Düzeltme

```bash
sudo apt install ntfs-3g
ntfsfix <adres>
```

* `<adres>` Takılan USB'nin bağlanmaya çalıştığı adres
  * Örn: `/dev/sbd1`

{% hint style="info" %}
🧙‍♂️ Detaylar için [Fix corrupt NTFS partition without Windows](https://askubuntu.com/questions/47700/fix-corrupt-ntfs-partition-without-windows/47711#47711) sorusuna bakabilirsin
{% endhint %}

## ‍🎊 Silinen Yerel Dosyaları Kurtarma

Home dizinin yanlışlıkla \(ya da bilinçli 🧐\) `rm -rf *` komutu uygulanması durumunda bu sorun meydana gelir. İster en alttaki script ile isterseniz talimatlarla sorunu çözebilirsiniz.

* `cd ~` ile `Home` dizinine gelin ve dizinlerinizi oluşturun
* `gedit ~/.config/user-dirs.dirs` ile dizinleri ayarların
* `xdg-user-dirs-update` komutu ile dizinleri güncelleyin

```bash
cd ~
mkdir Downloads Templates Shares Documents Musics Pictures Videos Desktop
echo '# This file is written by xdg-user-dirs-update' > ~/.config/user-dirs.dirs
echo '# If you want to change or add directories, just edit the line you are' >> ~/.config/user-dirs.dirs
echo '# interested in. All local changes will be retained on the next run.' >> ~/.config/user-dirs.dirs
echo '# Format is XDG_xxx_DIR="$HOME/yyy", where yyy is a shell-escaped' >> ~/.config/user-dirs.dirs
echo '# homedir-relative path, or XDG_xxx_DIR="/yyy", where /yyy is an' >> ~/.config/user-dirs.dirs
echo '# absolute path. No other format is supported.' >> ~/.config/user-dirs.dirs
echo '# YEmreAk' >> ~/.config/user-dirs.dirs
echo 'XDG_DOWNLOAD_DIR="$HOME/Downloads"' >> ~/.config/user-dirs.dirs
echo 'XDG_TEMPLATES_DIR="$HOME/Templates"' >> ~/.config/user-dirs.dirs
echo 'XDG_PUBLICSHARE_DIR="$HOME/Shares"' >> ~/.config/user-dirs.dirs
echo 'XDG_DOCUMENTS_DIR="$HOME/Documents"' >> ~/.config/user-dirs.dirs
echo 'XDG_MUSIC_DIR="$HOME/Musics"' >> ~/.config/user-dirs.dirs
echo 'XDG_PICTURES_DIR="$HOME/Pictures"' >> ~/.config/user-dirs.dirs
echo 'XDG_VIDEOS_DIR="$HOME/Videos"' >> ~/.config/user-dirs.dirs
echo 'XDG_DESKTOP_DIR="$HOME/Desktop"' >> ~/.config/user-dirs.dirs
xdg-user-dirs-update
```

## 🎨 Ubuntu Soluk Renk Sorunu

{% tabs %}
{% tab title="🏃‍♀️ Tek Seferlik" %}
```bash
xrandr --output HDMI-1 --set "Broadcast RGB" "Full"
```
{% endtab %}

{% tab title="🩹 Kalıcı" %}
```bash
echo 'xrandr --output HDMI-1 --set "Broadcast RGB" "Full"' >> ~/.xprofile
```
{% endtab %}
{% endtabs %}

## 🏓 Failed to load module “canberra-gtk-module”

```bash
sudo apt install libcanberra-gtk-module
```

## 🔗 Faydalı Bağlantılar

* [Windows yanına linux kurulduğunda windows saatinin bozulması](https://www.howtogeek.com/323390/how-to-fix-windows-and-linux-showing-different-times-when-dual-booting/)



