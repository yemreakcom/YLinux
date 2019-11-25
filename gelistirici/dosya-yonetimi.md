---
description: Linux üzerinde dosya yönetimi
---

# 📂 Dosya Yönetimi

## 👁‍🗨 Dosya içeriğinden Türünü Bulma

| Satr Metni | Açıklama |
| :--- | :--- |
| `!` | Çalıştırılabilir \(executable\) |
| `#!/bin/bash` | Bash script |
| `#usr/bin/env xdg-open` | Desktop uygulamaları |
| `#!/usr/bin/python` | Python dosyaları |

## 🤝 Başka İşletim Sistemlerinin Dosyalarına Erişme

Erişim yapmak için `mount` işlemi ile sisteme bağlamalısınız.

* Disk yolunu öğrenmek için `gparted` kullanabilisiniz
* `sudo apt install gparted`
* `sudo gparted`
* Partition kısmının altındaki disk yoludur

```bash
sudo mount <disk_yolu> <bağlacağı_yer>
# Örn: sudo mount /dev/sda4 /mnt/
```

