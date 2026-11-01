# Madde Dedektifi · Maddenin Ayırt Edici Özellikleri

| Alan | Değer |
|---|---|
| gameId | fen-6-madde-dedektifi |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 6 (oyun yalnızca 6. sınıf bağlamını kabul eder) |
| Ünite | 5. Ünite: Maddenin Ayırt Edici Özellikleri |
| Ekran yönü | Dikey |
| Oyun türü | Dedektif bürosu temalı madde teşhis deneyleri oyunu. Karakter yoktur. Test ve doğru/yanlış sorusu yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🔍 puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 102 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:**
  1. Yağmurlu gece, şehir silueti, pencerelerde ışıklar.
  2. "MADDE DEDEKTİFİ" neon tabelası titreyerek yanar.
  3. "DOSYAYI AÇ" denince masa lambası yanar, büyüteç dosyanın üzerine kayar, ayak izi ortaya çıkar, "GİZLİ" damgası basılır.
  4. Dosyaya yakınlaşılır, ışık patlaması olur.
- **İlerleme:** Üstte iple asılı 10 dosya vardır. Doğru görevde dosya sarıya döner (✔), yanlışta grileşir (✕).
- **Çıkış:**
  1. Kanıt panosunda notlar raptiyelenir, kırmızı iplerle bağlanır.
  2. "DOSYA KAPANDI x/10 ÇÖZÜLEN VAKA" damgası basılır.
  3. Sonuç "DEDEKTİF ROZETİ" olarak açılır.

## Görevler (teşhis deneyleri)
| Tür | Görev | Mekanik |
|---|---|---|
| heat | Isı kanıtı | Küre-halka, madenî para-çivi, şişe-balon, termometre, top, elektrik teli, kavanoz kapağı deneylerinde sonuç tahmin edilir (geçer/geçemez, şişer/söner, yükselir/alçalır …); deney masası çalışınca cisimler genleşir ya da büzülür |
| match | Kanıt eşleştirme | Referans maddeyle aynı maddeden olan örnekler seçilir. Isıtıcılar ya da ölçüm cihazı çalışınca uzama, erime/kaynama noktası ya da kütle ÷ hacimden yoğunluk ortaya çıkar. Kütle farklı örnekler, kütlenin ayırt edici olmadığını gösteren tuzaklardır |
| log | Isıtma kaydı | Sıcaklık-zaman kaydında sıcaklığın sabit kaldığı satırlar işaretlenir, erime/donma/kaynama noktasından madde teşhis edilir; kayıt oynatılınca grafik çizilir |
| rooms | Sıcaklık odaları | Erime ve kaynama noktası verilen maddelerin farklı sıcaklıktaki odalarda katı, sıvı ya da gaz hâlde olacağı hücrelere dokunarak belirlenir |
| pure | Tanecik mikroskobu | Tanecik modellerinin saf madde mi, saf olmayan madde mi olduğu seçilir |
| cyl | Ölçüm masası | Dereceli silindirde yükselen sıvı, taşırma kabından taşan sıvı ya da terazideki boş/dolu beherglas ile hacim veya kütle bulunur |
| dens | Yoğunluk ölçer | Terazi ve dereceli silindir verileriyle yoğunluk (virgüllü) sayı çarkına girilir |
| float | Su tankı | Cisimlerin su, etil alkol ya da cıvada batacağı, askıda kalacağı ya da yüzeceği tahmin edilir; cisimler bırakılınca konumlarını alır |
| layers | Katman kulesi | Birbiri içinde çözünmeyen sıvılar alttan üste sıralanır; kap durulunca gerçek dizilim görünür |
| sort | Dosya bölmeleri | Genleşme/büzülme olayları, saf/saf olmayan maddeler, ayırt edici/ortak özellikler, kütle-hacim aletleri, buz-su, bilim insanları |
| calc | Sayı çarkı | Eyfel Kulesi uzaması, sıcaklık farkları, hacim farkı ve bilim insanlarının yaşam süreleri |

Her deste kurulurken her konudan 2 görev seçilir. Görev türleri olabildiğince farklı tutulur, bir destede en az 8 farklı tür bulunur.

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| genlesme | 20 | Genleşme ve büzülme deneyleri, günlük hayattan örnekler, esneme payı, termostat, metallerin farklı genleşmesi |
| hal | 18 | Saf ve saf olmayan madde, erime ve donma noktası, hâl değişiminde sabit sıcaklık |
| kaynama | 19 | Kaynama noktası tabloları, ısıtma kayıtları, maddelerin farklı sıcaklıklardaki hâli |
| olcum | 24 | Kütle ve hacim ölçümü, taşırma kabı, dereceli silindir, yoğunluk hesabı |
| yogunluk | 21 | Batma, yüzme, askıda kalma; sıvı katmanları; buzun suda yüzmesi ve canlılar için önemi; Arşimet, Biruni, Marie Curie, Oktay Sinanoğlu |

Görev türlerinin dağılımı: sort 13, match 12, heat 11, dens 10, rooms 9, cyl 9, float 9, calc 9, log 8, layers 7, pure 5.

Yanlış-cevap kaydı:
- questionText görevi ve deney verilerini (sıcaklık kaydı, kütle-hacim, yoğunluklar …) metin olarak içerir.
- studentAnswer öğrencinin tahminlerini, seçimlerini, sırasını ya da sayısını yazar.
- correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 6. Sınıf Ders Kitabı (2. kitap), 5. Ünite (s. 12–63).

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
