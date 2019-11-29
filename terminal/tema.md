---
description: Linux üzerindeki terminale tema ekleme
---

# 🎨 Terminal Teması

## 👀 Temanın Görünüşü

![](../.gitbook/assets/image%20%281%29.png)

## 👨‍💻 Temayı Derleme

Alttaki komutlarla temayı indirin ve derleyin

```bash
sudo apt install golang-go
go get -u github.com/justjanne/powerline-go
```

## 📑 Bashrc Dosyasına Script Ekleme

* VsCode ile `.bashrc`'yi açın \(`code ~/.bashrc`\) 
* Alttaki komutları dosyanın en altına kopyalayın

```bash
GOPATH=$HOME/go
function _update_ps1() {
    PS1="$($GOPATH/bin/powerline-go -error $?)"
}
if [ "$TERM" != "linux" ] && [ -f "$GOPATH/bin/powerline-go" ]; then
    PROMPT_COMMAND="_update_ps1; $PROMPT_COMMAND"
fi
```

## 🔤 Gerekli olan Font Kurulumu

* [Delugia Nerd Fonts](https://github.com/adam7/delugia-code/releases?WT.mc_id=-blog-scottha)'u kurun
* Windows Terminal üzerinden ayarlara girip, Ubuntu ayarlarına alttakini ekleyin

```javascript
"fontFace": "Delugia Nerd Font"
```

## 🔗 Referanslar

{% embed url="https://www.hanselman.com/blog/HowToMakeAPrettyPromptInWindowsTerminalWithPowerlineNerdFontsCascadiaCodeWSLAndOhmyposh.aspx" %}

{% hint style="success" %}
Ayrıntılı bilgi için **STEP TWO FOR UBUNTU/WSL** alanına bakabilirsin.
{% endhint %}

