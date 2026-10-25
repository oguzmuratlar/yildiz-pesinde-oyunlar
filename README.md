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
| Gökyüzü Milyoneri | gokyuzu-milyoneri | 1.1.1 | Fen Bilimleri | 5 | Yatay | `/gokyuzu-milyoneri/1.1.1/index.html` |
| Yörünge Kapsülü | yorunge-kapsulu | 1.0.0 | Fen Bilimleri | 5 | Yatay | `/yorunge-kapsulu/1.0.0/index.html` |
| Harf Şenliği | harf-senligi | 1.0.0 | Fen Bilimleri | 6 | Yatay | `/harf-senligi/1.0.0/index.html` |
| Yaşam Bahçesi | yasam-bahcesi | 1.0.0 | Fen Bilimleri | 6 | Yatay | `/yasam-bahcesi/1.0.0/index.html` |
| Yaşam Milyoneri | yasam-milyoneri | 1.0.0 | Fen Bilimleri | 6 | Yatay | `/yasam-milyoneri/1.0.0/index.html` |
| Sinir Sinyali: Bilim Çarkı | sinir-sinyali | 1.0.0 | Fen Bilimleri | 6 | Yatay | `/sinir-sinyali/1.0.0/index.html` |
| Operasyon: Yaşam Akışı | yasam-akisi | 1.0.0 | Fen Bilimleri | 7 | Yatay | `/yasam-akisi/1.0.0/index.html` |
| Elmi'nin Sindirim Yolculuğu | fen-7-sindirim-asmaca | 1.0.0 | Fen Bilimleri | 7 | Yatay | `/fen-7-sindirim-asmaca/1.0.0/index.html` |
| Nefes Atölyesi: Bağlantıyı Kur | nefes-atolyesi | 1.0.0 | Fen Bilimleri | 7 | Yatay | `/nefes-atolyesi/1.0.0/index.html` |
| Arıtım Üssü: Robotun Rotası | aritim-ussu | 1.0.0 | Fen Bilimleri | 7 | Yatay | `/aritim-ussu/1.0.0/index.html` |
| Periyodik Galaksi | fen-8-periyodik-galaksi | 1.0.0 | Fen Bilimleri | 8 | Yatay | `/fen-8-periyodik-galaksi/1.0.0/index.html` |
| Asit-Baz Laboratuvarı | fen-8-asit-baz-laboratuvari | 1.0.0 | Fen Bilimleri | 8 | Yatay | `/fen-8-asit-baz-laboratuvari/1.0.0/index.html` |
| Kimya Ligi: Potaya Tepki! | kimya-ligi | 1.0.0 | Fen Bilimleri | 8 | Yatay | `/kimya-ligi/1.0.0/index.html` |
| Buz & Ateş Laboratuvarı | fen-8-isi-buz-ates-laboratuvari | 1.0.0 | Fen Bilimleri | 8 | Yatay | `/fen-8-isi-buz-ates-laboratuvari/1.0.0/index.html` |

## Uyumluluk

- Köprü sürümü: 1.0 (Yıldız Peşinde HTML Oyun Entegrasyon Şartnamesi)
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyunlar "Deneme modu"nda çalışır ve sonuç kaydetmez.
