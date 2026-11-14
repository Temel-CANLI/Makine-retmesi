# ML Vize Hazırlık

Makine öğrenmesi dersi (1-7. hafta) için çalışma sitesi: konu anlatımı, çözümlü örnekler, 300+ alıştırma, Bayes ağları / d-ayrışma, PDF (işbirlikçi filtreleme) ve Excel (kNN + Naive Bayes) bölümleri, etkileşimli araçlar (kNN, regresyon, sigmoid, metrikler, ön işleme, Bayes, d-ayrışma denetleyicisi), formül kartı ve deneme sınavı.

Derleme/kurulum gerekmez; saf HTML + CSS + JavaScript.

## Yerelde açma

```bash
python -m http.server 8000
```

Sonra tarayıcıda `http://localhost:8000` adresini aç. (`index.html` dosyasını çift tıklayarak da açılır.)

## GitHub Pages ile yayınlama

1. Bu klasörü bir GitHub deposuna push et (`index.html` deponun kökünde olmalı).
2. Depoda **Settings → Pages → Build and deployment → Source: Deploy from a branch** seç.
3. Branch: `main`, klasör: `/ (root)` → **Save**.
4. Birkaç dakika sonra site `https://<kullanici-adi>.github.io/<depo-adi>/` adresinde yayında olur.

## Dosya yapısı

Tüm site (HTML, CSS, JavaScript, içerik ve sorular) tek dosyada: `index.html`.

## Soru eklemek

`index.html` içinde ilgili haftanın `qs` listesini bul (`WEEKS.push({ id: 4, ...` gibi) ve ekle:

```js
{ t: "mcp", q: "Soru?", o: ["A", "B", "C", "D"], a: 1, e: "Açıklama" }   // çoktan seçmeli (a = doğru şıkkın indeksi, 0'dan başlar)
{ t: "num", q: "Hesapla...", a: 0.85, tol: 0.001, e: "Açıklama" }           // sayısal (tol = kabul edilen hata)
{ t: "tf",  q: "İfade...", a: true, e: "Açıklama" }                         // doğru/yanlış
```

İlerleme her kullanıcının kendi tarayıcısında (`localStorage`) saklanır.
