# Contributing / Katkıda Bulunma

## English

Thanks for your interest in **google-maps-scraper**. Contributions of any size are welcome: bug reports,
documentation fixes, translations and code.

1. Fork the repository and create a branch from `main` (`fix/short-description` or `feat/short-description`).
2. Set up the project:

```bash
python -m venv .venv
.venv/Scripts/python -m pip install -r requirements.txt
```

Google Maps changes its page structure often. If extraction breaks, update the CSS selectors in `scraper.py`.

3. Run the checks before opening a pull request:

```bash
python -m compileall -q .
```

4. Open a pull request that explains **what** changed and **why**. Keep it focused on one topic.

By contributing you agree that your contribution is licensed under the [MIT License](LICENSE).
Please be respectful and constructive in issues and reviews.

## Türkçe

**google-maps-scraper** projesine ilginiz için teşekkürler. Hata bildirimi, dokümantasyon düzeltmesi, çeviri ve kod
katkılarının hepsi değerlidir.

1. Depoyu çatallayın ve `main` dalından bir dal açın (`fix/kisa-aciklama` veya `feat/kisa-aciklama`).
2. Projeyi kurun:

```bash
python -m venv .venv
.venv/Scripts/python -m pip install -r requirements.txt
```

Google Haritalar sayfa yapısını sık değiştirir. Veri çekme bozulursa `scraper.py` içindeki CSS seçicilerini güncelleyin.

3. Pull request açmadan önce kontrolleri çalıştırın:

```bash
python -m compileall -q .
```

4. Neyi **ve neden** değiştirdiğinizi anlatan, tek konuya odaklı bir pull request açın.

Katkı vererek çalışmanızın [MIT Lisansı](LICENSE) ile lisanslanmasını kabul etmiş olursunuz.
Issue ve incelemelerde saygılı ve yapıcı olun.
