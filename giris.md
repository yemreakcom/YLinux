---
description: Linux dünyasına giriş
---

# 🔰 Linux'a Giriş

## ❔ Linux Nedir

Açık kaynak olan **Unix** tabanlı işletim sistemidir.

* Linux işletim sistemlerinde **python** gömülü olarak gelir, temel dili **bash** veya **shell** olarak geçmektedir.
* Farklı linux dağıtımlarına **distro** denir.

## ⭐ Birkaç Öneri Distro

| Distro | İyi Yanı | Kötü Yanı |
| :--- | :--- | :--- |
| [ubuntu](https://www.ubuntu.com/) | Çok fazla kaynak ve bilgi desteği vardır | Arayüz tasarımı hususunda geridedir |
| [deepin](https://www.deepin.org/) | Çok şık bir arayüz tasarımına sahiptir | Donanım ve bilgi desteği zayıftır |
| [elementary OS](http://www.elementary.io/) | Mac OS Temalı |  |
| Manjaro | Hız ve verimlilik | Linux bilgisi gerektirir |

## 👷‍♂️ Linux Kurulumu

* Yukarıdaki distrolardan birini indirin
* [Rüfus](https://github.com/pbatard/rufus/releases/download/v3.5/rufus-3.5.exe) programını indirin \(linux için etcher\)
* En az 8Gb olan bir usb belleği takıp, rüfus programını çalıştırın
* Sırasıyla disk imajını, GPT / UEFI ayarını seçin, DD image ile başlatın

### 🐞 BootMenu'de Gözükmeme Sorunu

* Ubuntu yükü olan USB ile Ubuntu'yu açın
* Alttaki komutlarla bootrepair'i kurun
* **Recommended Repair** butonuna tıklayın

```bash
sudo add-apt-repository ppa:yannubuntu/boot-repair
sudo apt-get update
sudo apt-get install -y boot-repair && boot-repair
```

{% hint style="info" %}
🧙‍♂️ Ayrıntılar için [RecoveringUbuntuAfterInstallingWindows](https://help.ubuntu.com/community/RecoveringUbuntuAfterInstallingWindows) alanına bakabilirsin.
{% endhint %}

## 📂 Linux Temel Dosyaları

| Yol | Açıklama |
| :--- | :--- |
| `~/.bashrc` | Terminal ayaları |
| `~/.config/user-dirs.dirs` | Temel dosya dizinleri |

## 

