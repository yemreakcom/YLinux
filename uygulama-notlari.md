---
description: Linux uygulamaları hakkındaki notlarım
---

# 📦 Uygulama Notları

## 📑 Gedit Metin Editörü

| Renklendirme Tipi | Hangi uzantılar için |
| :--- | :--- |
| `Modelica` | `ini`, `cfg`, `config` |

## 📺 FFMPEG

### 💱 MP4'ü MP3'e çevirme

{% tabs %}
{% tab title="FFmpeg with Constant Bitrate Encoding \(CBR\)" %}
```bash
ffmpeg -i video.mp4 -vn \
    -acodec libmp3lame -ac 2 -ab 160k -ar 48000 \
    audio.mp3
```
{% endtab %}

{% tab title="FFmpeg with Variable Bitrate Encoding \(VBR\)" %}
```bash
ffmpeg -i video.mp4 -vn \
    -acodec libmp3lame -ac 2 -qscale:a 4 -ar 48000 \
    audio.mp3
```
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
The VBR example has a target bitrate of 165 Kbit/s with a bitrate range of 140...185. [Kaynak](https://askubuntu.com/a/84633/898692)
{% endhint %}

### 🦶 MP3 Sıkıştırma

```bash
ffmpeg -i input.file -map 0:a:0 -b:a 96k output.mp3
```

