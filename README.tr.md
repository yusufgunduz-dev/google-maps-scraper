<div align="center">

# Google Maps Scraper

**Google Haritalar'daki işletme kayıtlarını Excel dosyasına aktaran, masaüstü arayüzlü bir Python ve Selenium aracı.**

![Python](https://img.shields.io/badge/Python-3776ab?style=flat-square&logo=python&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-43b02a?style=flat-square&logo=selenium&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Lisans](https://img.shields.io/badge/Lisans-MIT-green?style=flat-square)

Türkçe · [English](README.md)

</div>

> **Sorumlu kullanım.** Google Haritalar'dan otomatik veri toplamak Google'ın kullanım şartlarına, toplu veya
> otomatik mesaj göndermek WhatsApp'ın şartlarına aykırı olabilir. Türkiye'de ticari elektronik iletiler için
> alıcının onayı gerekir (6563 sayılı Kanun) ve kişisel veriler KVKK ile (6698 sayılı Kanun) korunur. Bu proje
> öğrenme amacıyla ve yasal olarak işleme hakkınız olan veriler için sunulmuştur. **Nasıl kullanacağınızdan yalnızca
> siz sorumlusunuz.** Yazar hiçbir sorumluluk kabul etmez.

## Ne yapar?

1. İşletme türü ve şehir girersiniz, örneğin *diş hekimi* ve *İstanbul*.
2. Selenium, Chrome'da Google Haritalar'ı açar, sonuç listesini kaydırır ve her mekânı açar.
3. Her mekânın adı ve telefon numarası çekilir ve tekrarlar ayıklanır.
4. Sonuçlar pandas ile Excel dosyasına kaydedilir.
5. İsteğe bağlı olarak araç, `pywhatkit` ile WhatsApp Web üzerinden (isteğe bağlı görsellerle) mesaj gönderebilir;
   mesajlar arasında bekleme süresi vardır.

**Tkinter arayüzü** (`gui_main.py`) ve basit bir **komut satırı modu** (`main.py`) içerir. Windows çalıştırılabilir
dosyası üretmek için PyInstaller spec dosyaları da bulunur.

## Gereksinimler

- Python 3.12 veya üzeri
- Google Chrome (Selenium 4.6 ve üzerinde Selenium Manager uygun sürücüyü otomatik indirir)
- WhatsApp mesajları için: aynı bilgisayarda oturum açılmış WhatsApp Web

## Kurulum

```bash
git clone https://github.com/yusufgunduz-dev/google-maps-scraper.git
cd google-maps-scraper
python -m venv .venv
.venv/Scripts/python -m pip install -r requirements.txt
```

## Kullanım

Arayüz:

```bash
python gui_main.py
```

Komut satırı:

```bash
python main.py
```

İşletme türünü ve şehri girin; sonuçlar Excel'e yazılır. Telefon numarası okunamıyorsa Google sayfa yapısını
değiştirmiş olabilir: `scraper.py` içindeki CSS seçicilerini güncelleyin.

## Proje yapısı

```
scraper.py     Google Haritalar'dan Selenium ile veri çekme
exporter.py    Excel çıktısı (pandas, openpyxl)
messenger.py   isteğe bağlı WhatsApp mesajları (pywhatkit)
gui_main.py    Tkinter masaüstü arayüzü
main.py        komut satırı girişi
```

## Katkı ve güvenlik

[CONTRIBUTING.md](CONTRIBUTING.md) ve [SECURITY.md](SECURITY.md) dosyalarına bakın.

## Lisans

[MIT](LICENSE) © 2026 Yusuf Gündüz
