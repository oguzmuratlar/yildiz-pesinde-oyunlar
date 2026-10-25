# Buz & Ateş Laboratuvarı

| Alan | Değer |
|---|---|
| gameId | fen-8-isi-buz-ates-laboratuvari |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (subjectId: science) |
| Sınıf | 8 |
| Ünite / konu | 8. Sınıf 4. Ünite: Madde ve Endüstri — Maddenin Isı ile Etkileşimi |
| Ekran yönü | Yatay (dikeyde "cihazını yan çevir" uyarısı gösterir) |
| Oyun türü | 5 istasyon × 4 deney: eşit ısıtma, özısı sıralama, grafik okuma, deney tasarımı, buz kalıbı ve ısı alışverişi |
| Toplam soru | 20 (soru başına 3 hak; yalnız ilk deneme doğru sayılır) |
| Yıldız eşikleri | %50: 1 · %70: 2 · %90: 3 (10–13 doğru 1★, 14–17 2★, 18–20 3★) |

## İçerik notları
- Kazanım ifadeleri çalışma kitabındaki test sorularından türetilmiş ("kitapta kazanım kodu yok" notu içerikte duruyor).
- `isi-v1-s4-buz-kutle` sorusunda buz kaplarının etiketi "Su · 30 g" görünüyor; "Buz" olması daha doğru olur (sonraki sürümde).

## Sürüm notları
- 1.0.0: Standart giriş kanalı `window.YildizPesindeGame.receiveMessage` eklendi; CSP eklendi; init'te subjectId zorunluluğu kaldırıldı.
