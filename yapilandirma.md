---
description: Linux ortamında yaptığınız tüm değişikleri yönetme
---

# 👨‍🔧 Yapılandırma Ayarları

## 🔰 Yapılandırma Ayarları Hakkında

İşletim sistemi üzerinde yapmış olduğunuz değişikliklerin hepsi `dconf` komutu tarafından kontrol edilir.

* 💖 Kısayol ayarları
* ✨ Uygulamalara özgü özelleştirmeler
* 💻 Masaüstü, ikon teması vs ayarlar
* 😅 Ve diğer saymaya üşendiklerim

## ⏫ Yapılandırma Ayalarını Dosyaya Aktarma

Yapılandırma ayarlarını `dconf dump <dizin> > <dosya_ismi>` komutu ile dosyaya aktarabilrisiniz

* `<dizin>` Hangi dizinden itibaren yapılandırma verileri yedeklensin
  * `/` olursa tüm yapılandırma ayarlarını dahil eder
* `<dosya_ismi>` Ayarların yazılacağı dosya ismi
  * `dconf-settings.ini` yaparsanız, `dconf-settings.ini` isimli dosya oluşturup içine ayarları yazacaktır

## ⏬ Yapılandırma Ayarlarını Dosyadan Alma

Yapılandırma ayarlarını `dconf load <dizin> < <dosya_ismi>` komutu ile dosyaya aktarabilrisiniz

* `<dizin>` Hangi dizinden itibaren yapılandırma verileri yedeklensin
  * `/` olursa tüm yapılandırma ayarlarını dahil eder
* `<dosya_ismi>` Ayarların alınacağı dosya ismi
  * `dconf-settings.ini` yaparsanız, `dconf-settings.ini` isimli dosya dosyadan ayarları okuyup sisteme kaydeder

