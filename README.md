<div align="center">

# Google Maps Scraper

**A Python and Selenium tool that collects business listings from Google Maps into an Excel file, with a desktop GUI.**

![Python](https://img.shields.io/badge/Python-3776ab?style=flat-square&logo=python&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-43b02a?style=flat-square&logo=selenium&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

[Türkçe](README.tr.md) · English

</div>

> **Responsible use.** Automated collection from Google Maps may violate Google's terms of service, and bulk or
> automated messaging may violate WhatsApp's terms. In Turkey, commercial electronic messages require the
> recipient's consent (Law No. 6563) and personal data is protected by KVKK (Law No. 6698). This project is provided
> for learning and for use on data you are legally allowed to process. **You are solely responsible for how you use it.**
> The author accepts no liability.

## What it does

1. You enter a business type and a city, for example *dentist* and *Istanbul*.
2. Selenium opens Google Maps in Chrome, scrolls the results list and opens each place.
3. Each place's name and phone number are extracted and de-duplicated.
4. The results are saved to an Excel file with pandas.
5. Optionally, the tool can send a message (with optional images) through WhatsApp Web using `pywhatkit`,
   with a delay between messages.

It ships with a **Tkinter GUI** (`gui_main.py`) and a simple **command-line mode** (`main.py`). PyInstaller spec
files are included to build a Windows executable.

## Requirements

- Python 3.12 or newer
- Google Chrome (Selenium Manager downloads a matching driver automatically with Selenium 4.6 or newer)
- For WhatsApp messages: WhatsApp Web signed in on the same computer

## Installation

```bash
git clone https://github.com/yusufgunduz-dev/google-maps-scraper.git
cd google-maps-scraper
python -m venv .venv
.venv/Scripts/python -m pip install -r requirements.txt
```

## Usage

GUI:

```bash
python gui_main.py
```

Command line:

```bash
python main.py
```

Enter the business type and the city; results are written to Excel. If a phone number cannot be read, Google
may have changed its page structure: update the CSS selectors in `scraper.py`.

## Project structure

```
scraper.py     Selenium extraction from Google Maps
exporter.py    Excel export (pandas, openpyxl)
messenger.py   optional WhatsApp messages (pywhatkit)
gui_main.py    Tkinter desktop interface
main.py        command-line entry point
```

## Contributing and security

See [CONTRIBUTING.md](CONTRIBUTING.md) and [SECURITY.md](SECURITY.md).

## License

[MIT](LICENSE) © 2026 Yusuf Gündüz
