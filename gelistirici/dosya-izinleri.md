---
description: Linux üzerindeki dosyalara okuma/yazma izinleri verme
---

# 👮‍♂️ Dosya İzinleri

## 🔰 Dosya İzinlerine Giriş 

Dosya izinleri `chmod <parametre> <izin_no> <dosya_veya_dizin>` komutuyla yapılır.

| Parametreler | Açılımı | Anlamı |
| :--- | :--- | :--- |
| `-R` | Recursive | Dizin ve alt dizinlerini de ele alır |

## 🧮 İzin Kodu Hesaplama

İzin kodu, aşağıdaki formattaki kod yapısıdır.

* Sırasıyla `owner`, `group`, `others` basamaklarına alttaki yetkilerin toplamının atanmasıdır
  * `4` Read \(okuma\)
  * `2` Write \(yazma\)
  * `1` Execute \(çalıştırma\)
  * `0` No permission \(izin yok\)

```bash
mkdir temp
sudo chmod 777 temp # Her gruba tüm yekileri verme
sudo chmod 751 temp # Oner: Hepsi Group: Read & Write Others: Execute
sudo chmod 000 temo # Hiç yetki yok
sudo chmod -R 777 temp # Dizine ve altdizinlere herkes için tam yetki verme
```

> `Root` her şeye erişebilir.

## ✨ Dizine ve Alt Dizinlerine Okuma ve Yazma İzni Verme

Alttaki komutla dizine ve alt dizinlerine herkes için okuma ve yazma erişimi verebilirsin.

```bash
sudo chmod -R 757 /opt/lampp/htdocs/wordpress/
```

