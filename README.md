# Yıldız Peşinde — HTML Oyunları

Bu depo, Yıldız Peşinde mobil uygulamasında WebView içinde açılan HTML oyunlarını barındırır. Oyunlar GitHub Pages üzerinden HTTPS ile yayınlanır.

## Klasör yapısı

```
<gameId>/<gameVersion>/index.html
```

- Her oyun kendi `gameId` klasöründedir.
- Her sürüm ayrı bir klasördür. **Yayınlanmış bir sürüm klasörü asla değiştirilmez.** İçerikte, soruda veya kodda değişiklik olursa yeni sürüm klasörü açılır (ör. `1.0.1/`) ve uygulamadaki oyun kaydı yeni adres ve sürümle güncellenir.
- `index.html` kendi başına çalışır; soru verisi içine gömülüdür. Yanındaki JSON dosyası yalnızca içerik kaynağı ve inceleme içindir.

## Oyunlar

| Oyun | gameId | Sürüm | Ders | Sınıf | Ekran yönü | Adres (yol) |
|---|---|---|---|---|---|---|
| Gökyüzü Milyoneri | gokyuzu-milyoneri | 1.1.1 | Fen Bilimleri | 5 | Dikey | `/gokyuzu-milyoneri/1.1.1/index.html` |
| Yörünge Kapsülü | yorunge-kapsulu | 1.0.0 | Fen Bilimleri | 5 | Dikey | `/yorunge-kapsulu/1.0.0/index.html` |
| Harf Şenliği | harf-senligi | 1.0.0 | Fen Bilimleri | 6 | Dikey | `/harf-senligi/1.0.0/index.html` |
| Yaşam Bahçesi | yasam-bahcesi | 1.0.0 | Fen Bilimleri | 6 | Dikey | `/yasam-bahcesi/1.0.0/index.html` |
| Yaşam Milyoneri | yasam-milyoneri | 1.0.0 | Fen Bilimleri | 6 | Dikey | `/yasam-milyoneri/1.0.0/index.html` |
| Sinir Sinyali: Bilim Çarkı | sinir-sinyali | 1.0.0 | Fen Bilimleri | 6 | Dikey | `/sinir-sinyali/1.0.0/index.html` |
| Operasyon: Yaşam Akışı | yasam-akisi | 1.0.0 | Fen Bilimleri | 7 | Dikey | `/yasam-akisi/1.0.0/index.html` |
| Elmi'nin Sindirim Yolculuğu | fen-7-sindirim-asmaca | 1.0.0 | Fen Bilimleri | 7 | Dikey | `/fen-7-sindirim-asmaca/1.0.0/index.html` |
| Nefes Atölyesi: Bağlantıyı Kur | nefes-atolyesi | 1.0.0 | Fen Bilimleri | 7 | Dikey | `/nefes-atolyesi/1.0.0/index.html` |
| Arıtım Üssü: Robotun Rotası | aritim-ussu | 1.0.0 | Fen Bilimleri | 7 | Dikey | `/aritim-ussu/1.0.0/index.html` |
| Periyodik Galaksi | fen-8-periyodik-galaksi | 1.0.0 | Fen Bilimleri | 8 | Dikey | `/fen-8-periyodik-galaksi/1.0.0/index.html` |
| Asit-Baz Laboratuvarı | fen-8-asit-baz-laboratuvari | 1.0.0 | Fen Bilimleri | 8 | Dikey | `/fen-8-asit-baz-laboratuvari/1.0.0/index.html` |
| Kimya Ligi: Potaya Tepki! | kimya-ligi | 1.0.0 | Fen Bilimleri | 8 | Dikey | `/kimya-ligi/1.0.0/index.html` |
| Buz & Ateş Laboratuvarı | fen-8-isi-buz-ates-laboratuvari | 1.0.0 | Fen Bilimleri | 8 | Dikey | `/fen-8-isi-buz-ates-laboratuvari/1.0.0/index.html` |
| Gölge Saati | fen-8-golge-saati | 1.0.0 | Fen Bilimleri | 8 | Dikey | `/fen-8-golge-saati/1.0.0/index.html` |
| Sarmal Fermuar | fen-8-sarmal-fermuar | 1.0.0 | Fen Bilimleri | 8 | Dikey | `/fen-8-sarmal-fermuar/1.0.0/index.html` |
| Basınç Dalgıcı | fen-8-basinc-dalgici | 1.0.0 | Fen Bilimleri | 8 | Dikey | `/fen-8-basinc-dalgici/1.0.0/index.html` |
| Vinç Şantiyesi | fen-8-vinc-santiyesi | 1.0.0 | Fen Bilimleri | 8 | Dikey | `/fen-8-vinc-santiyesi/1.0.0/index.html` |
| Cam Fanus | fen-8-cam-fanus | 1.0.0 | Fen Bilimleri | 8 | Dikey | `/fen-8-cam-fanus/1.0.0/index.html` |
| Enerji Şebekesi | fen-8-enerji-sebekesi | 1.0.0 | Fen Bilimleri | 8 | Dikey | `/fen-8-enerji-sebekesi/1.0.0/index.html` |
| Karo Ustası | matematik-8-karo-ustasi | 1.0.0 | Matematik | 8 | Dikey | `/matematik-8-karo-ustasi/1.0.0/index.html` |
| Mega Mikro | matematik-8-mega-mikro | 1.0.0 | Matematik | 8 | Dikey | `/matematik-8-mega-mikro/1.0.0/index.html` |
| Skor Analisti | matematik-8-skor-analisti | 1.0.0 | Matematik | 8 | Dikey | `/matematik-8-skor-analisti/1.0.0/index.html` |
| Adil Çark Tasarımcısı | matematik-8-adil-cark-tasarimcisi | 1.0.0 | Matematik | 8 | Dikey | `/matematik-8-adil-cark-tasarimcisi/1.0.0/index.html` |
| Özdeşlik Yapbozu | matematik-8-ozdeslik-yapbozu | 1.0.0 | Matematik | 8 | Dikey | `/matematik-8-ozdeslik-yapbozu/1.0.0/index.html` |
| Eğim Pisti | matematik-8-egim-pisti | 1.0.0 | Matematik | 8 | Dikey | `/matematik-8-egim-pisti/1.0.0/index.html` |
| Yük Sınırı | matematik-8-yuk-siniri | 1.0.0 | Matematik | 8 | Dikey | `/matematik-8-yuk-siniri/1.0.0/index.html` |
| Dev Ahtapot (Macera canavarı · Arena 1) | macera-5-dev-ahtapot | 1.0.0 | Karışık | 5 | Dikey | `/macera-5-dev-ahtapot/1.0.0/index.html` |
| Paslı Çapa Golemi (Macera canavarı · Arena 2) | macera-5-pasli-capa-golemi | 1.0.0 | Karışık | 5 | Dikey | `/macera-5-pasli-capa-golemi/1.0.0/index.html` |
| Fener Balığı (Macera canavarı · Arena 3) | macera-5-fener-baligi | 1.0.0 | Karışık | 5 | Dikey | `/macera-5-fener-baligi/1.0.0/index.html` |
| Kraken (Macera canavarı · Arena 4) | macera-5-kraken | 1.0.0 | Karışık | 5 | Dikey | `/macera-5-kraken/1.0.0/index.html` |
| Hindistan Cevizi Yengeci (Macera canavarı · Arena 5) | macera-6-hindistan-cevizi-yengeci | 1.0.0 | Karışık | 6 | Dikey | `/macera-6-hindistan-cevizi-yengeci/1.0.0/index.html` |
| Dev Bukalemun (Macera canavarı · Arena 6) | macera-6-dev-bukalemun | 1.0.0 | Karışık | 6 | Dikey | `/macera-6-dev-bukalemun/1.0.0/index.html` |
| Kunduz Kral (Macera canavarı · Arena 7) | macera-6-kunduz-kral | 1.0.0 | Karışık | 6 | Dikey | `/macera-6-kunduz-kral/1.0.0/index.html` |
| Kum Fırtınası Akrebi (Macera canavarı · Arena 8) | macera-6-kum-firtinasi-akrebi | 1.0.0 | Karışık | 6 | Dikey | `/macera-6-kum-firtinasi-akrebi/1.0.0/index.html` |
| Taş Dev (Macera canavarı · Arena 9) | macera-7-tas-dev | 1.0.0 | Karışık | 7 | Dikey | `/macera-7-tas-dev/1.0.0/index.html` |
| Kar Yetisi (Macera canavarı · Arena 10) | macera-7-kar-yetisi | 1.0.0 | Karışık | 7 | Dikey | `/macera-7-kar-yetisi/1.0.0/index.html` |
| Şimşek Kuşu (Macera canavarı · Arena 11) | macera-7-simsek-kusu | 1.0.0 | Karışık | 7 | Dikey | `/macera-7-simsek-kusu/1.0.0/index.html` |
| Buz Ejderi (Macera canavarı · Arena 12) | macera-7-buz-ejderi | 1.0.0 | Karışık | 7 | Dikey | `/macera-7-buz-ejderi/1.0.0/index.html` |
| Çaylak Düellosu | duello-caylak | 1.0.0 | Karışık | 5 | Dikey | `/duello-caylak/1.0.0/index.html` |
| Usta Düellosu | duello-usta | 1.0.0 | Karışık | 6 | Dikey | `/duello-usta/1.0.0/index.html` |
| Uzman Düellosu | duello-uzman | 1.0.0 | Karışık | 7 | Dikey | `/duello-uzman/1.0.0/index.html` |
| Efsane Düellosu | duello-efsane | 1.0.0 | Karışık | 8 | Dikey | `/duello-efsane/1.0.0/index.html` |

## Uyumluluk

- Köprü sürümü: 1.0 (Yıldız Peşinde HTML Oyun Entegrasyon Şartnamesi)
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyunlar "Deneme modu"nda çalışır ve sonuç kaydetmez.
