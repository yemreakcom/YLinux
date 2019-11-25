# 👨‍💼 Pencere Yönetimi

## 🧹 Ubuntu 19.04 için Pencere Kısayollarını Kaldırma \(Super + Num\)

```bash
gsettings set org.gnome.shell.extensions.dash-to-dock hot-keys false
gsettings set org.gnome.shell.keybindings switch-to-application-1 []
gsettings set org.gnome.shell.keybindings switch-to-application-2 []
gsettings set org.gnome.shell.keybindings switch-to-application-3 []
gsettings set org.gnome.shell.keybindings switch-to-application-4 []
gsettings set org.gnome.shell.keybindings switch-to-application-5 []
gsettings set org.gnome.shell.keybindings switch-to-application-6 []
gsettings set org.gnome.shell.keybindings switch-to-application-7 []
gsettings set org.gnome.shell.keybindings switch-to-application-8 []
gsettings set org.gnome.shell.keybindings switch-to-application-9 []
```

## 👮‍♂️ Window Manager Controls

Uygulamaların durumlarını kontrol eden `wmctrl` adlı komuttur.

* `wmctrl -xa <uygulama_komutu>` uygulama açıksa ekrana getirir.
* `wmctrl -v <uygulama>` Uygulama varsa 1 döndürür
* `wmctrl -xc <uygulama_komutu>` uygulamayı kibarca kapatma
* `wmctrl -lxG` açık olan uygulamalar hakkında bilgi basar.
* `wmctrl -xr $WM_CLASS -b toggle,shaded` uygulamayı gizleme \(shaded özelliğini toggle'lar\)
* `wmctrl -xr $WM_CLASS -b add,maximize_vert,maximize_hor` uygulmaya tam ekran özelliği verir

### 🆔 Window ID Alma

* `xwininfo | grep "Window id:"` Pencere yöneticisi üzerinden Fare seçimiyle Windows ID olarak alma
* `xprop | grep "window id #"` Process yöneticisi üzerinden Fare seçimiyle Windows ID olarak alma
* `xprop -id $WID | grep _NET_WM_STATE` Pencere durumunu gösterme

## 👨‍💼 Xdotool ile Pencere Yönetimi

* `$NAME` Pencere başlığı
* `xdotool search --name $NAME` VM\_NAME'e \(isme\) göre Windows ID alma
* `xdotool search --class $WM_CLASS` Temel VM\_CLASS'a \(sınıfa\) göre Windows ID alma \(en sondaki WM\_CLASS öğesi\)
* `xdotool search --classname $WM_CLASS` VM\_CLASS'a \(sınıfa\) göre Windows ID alma
* `xdotool search --desktop $(xdotool get_desktop) --class $WM_CLASS` Aktif masaüstünde temel VM\_CLASS'a \(sınıfa\) göre Windows ID alma \(en sondaki WM\_CLASS öğesi\)
* `xdotool search --desktop $(xdotool get_desktop) --classname $WM_CLASS` Aktif masaüstünde VM\_CLASS'a \(sınıfa\) göre Windows ID alma
* `xdotool getwindowfocus` Seçili olan ekranın WID'ini alır
* `xdotool getwindowfocus getwindowname` Seçili olan ekranın ismini alır
* `WID=$(xdotool search --name $NAME)` Windows ID'yi değişkende tutma
* `xdotool windowminimize $WID` Pencereyi gizleme
* `xdotool windowactivate $WID` Pencreyi gösterme ve odaklanma
* `xdotool get_desktop` Seçili olan masaüstünü gösterir \(0, 1, 2...\)

> Burada WID xdotool'a özgü id değeridir.

