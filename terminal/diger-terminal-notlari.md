# ✨ Diğer Terminal Notları

## 📃 Terminal Üzerinden PDF işlemleri

* PDF'e dönüştürme işlemlerini [unoconv](https://github.com/unoconv/unoconv) paketi ile yapabilirsin
  * Çok fazla dosya formatını PDF'e dönüştürebilir
  * `sudo apt install unoconv` ile kurulur
* PDF işlemlerini [pdfkit](https://linuxhint.com/install_pdftk_ubuntu/) ile yapabilirsin

```bash
# convert to pdf
unoconv -f pdf myfile1.odt myfile2.odt ...
# merge pdfs
pdftk myfile1.pdf myfile2.pdf ...
# remove individual pdf documents
rm myfile1.pdf myfile2.pdf ...
```

## 💫 Kısayol oluşturma

Detaylar için [buraya](https://manpages.debian.org/stretch/coreutils/ln.1.en.html) tıklayabilirsin.

```bash
sudo ln -s /dosya/yolu/ dosyaAdi
```

* `ln` İki dosya arasında link oluşturma
* `-s` Statik link yerine sembolik link oluşturma
* `/dosya/yolu` Örneğin /home/$USER
* `dosyaAdi` Oluşturulacak kısayolun ismi

## 👨‍💻 Shell \(Bash\) Scripting

{% embed url="https://wiki.yemreak.com/code/yardimci/shell" %}

### 🎳 100MB ve Üzeri Dosyaları Bulma

```bash
find /User/mkyong -type f -size +100000k -exec ls -lh {} \; | awk '{ print $9 ": " $5 }'
Copy
```

## 🧐 Uygulamaların Terminal Komutlarını öğrenme

Alttaki komutu yazdıktan sonra pencerenin üstüne tıklamanız yeterlidir.

```bash
xprop | grep WM_CLASS
```

## 🔗 Harici Bağlantılar

* [Batch Script ile 'Yes/No' yapısı oluşturma](https://stackoverflow.com/a/226724/9770490)

