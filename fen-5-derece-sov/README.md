# Derece Şov · Maddenin Doğası

| Alan | Değer |
|---|---|
| gameId | fen-5-derece-sov |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 5 (oyun yalnızca 5. sınıf bağlamını kabul eder) |
| Ünite | 5. Ünite: Maddenin Doğası |
| Ekran yönü | Dikey |
| Oyun türü | Yarışma stüdyosu temalı deney ve simülasyon oyunu. Karakter yoktur. Test ve doğru/yanlış sorusu yoktur. 10 tur, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🏆 puan yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 103 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:**
  1. Karanlık stüdyoda iki spot ışığı süzülür.
  2. LED duvarın önünde neon "DERECE ŞOV" logosu belirir, logodaki termometrenin cıvası maviden kırmızıya yükselir.
  3. "ALKIŞ" tabelası yanıp söner, seyirci zıplar.
  4. "YARIŞMAYA BAŞLA" denince konfeti patlar, alkış kopar, LED duvar iki yana açılır.
- **İlerleme:** Üstte 10 bölmeli dev termometre vardır. Doğru turda bölme kırmızıya (🔥), yanlışta maviye (🧊) boyanır.
- **Çıkış:**
  1. Spotlar ortada birleşir.
  2. Dev termometre doğru sayısı kadar yükselir.
  3. "x/10" kupası iner, "ALKIŞ" tabelası yanar.
  4. Sonuç "YARIŞMA KARTI" olarak açılır.

## Turlar (deney ve simülasyonlar)

| Tür | Tur | Mekanik |
|---|---|---|
| model | Tanecik modeli | Diziliş (sıkı-düzenli / yakın-düzensiz / uzak-dağınık) ve hareketler (titreşim, dönme, öteleme) seçilir. Tanecikler kutuda seçime göre canlı hareket eder; kilitleyince gerçek model yanında oynar |
| syringe | Şırınga deneyi | Ucu kapalı şırıngalardan hangilerinin sıkışacağı tahmin edilir, pistonlar itilir: gaz sıkışır, katı ve sıvı direnir |
| tag | Madde etiketleri | Kitaptaki 8 etiketten maddeye uyanlar seçilir, kavanozdaki tanecikler canlanır |
| sort | Yarışma kutuları | Kartlar sürüklenerek ya da dokunularak 2–3 kutuya ayrılır |
| fill | Hata Avı | Cümlelerdeki boşluklara dokunarak "ısı / sıcaklık", birim ve ölçüm aracı seçilir; jüri yanlışları düzeltir |
| thermo | Termometre okuma | Termometre(ler) okunur; değer, fark ya da en yüksek sıcaklık sayı çarklarıyla girilir |
| mix | Sıvıları karıştır | Isının yönü (A➜B / B➜A / alışveriş yok) ve son sıcaklık tahmin edilir; kaplar dökülür, ısı akar, karışımın sıcaklığı görünür |
| room | Oda sıcaklığı | Cisimlerin uzun süre sonra ulaşacağı sıcaklık ayarlanır, zaman ileri sarılır |
| flow | Isı akışı | Günlük çiftlerde (çay-kaşık, el-kartopu vb.) ısının yönü seçilir, "ısı kamerası" akışı gösterir |
| phase | Hâl değişimi üçgeni | Olaylar katı-sıvı-gaz üçgenindeki 6 oktan doğrusuna bağlanır; tanecikler canlı olarak hâl değiştirir, ısı alır/verir gösterilir |
| curve | Isınma / soğuma grafiği | Ölçüm grafiğinde sıcaklığın sabit kaldığı bölümlere erime, kaynama ya da donma yerleştirilir (yanıltıcı kartlar da var); deney oynatılır |
| rod | Balmumu çubuk deneyi | Sıcak suya daldırılan çubuklardan hangilerinin boncuğunun düşeceği seçilir; ısı metallerde yükselir, boncuklar düşer |
| design | Yalıtım tasarımı | Tencere, ütü, ev, dondurma kutusu, termos vb. parçalara iletken ya da yalıtkan malzeme yerleştirilir, ısı kamerasıyla test edilir |

Her deste kurulurken her konudan 2 tur seçilir. Tur türleri olabildiğince farklı tutulur, bir destede en az 10 farklı tür bulunur.

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| tanecik | 25 | Katı, sıvı ve gaz tanecik modelleri, titreşim/dönme/öteleme, sıkıştırılabilme, akışkanlık, şekil ve hacim |
| isisic | 18 | Isı ve sıcaklığın farkı (ölçüm aracı, birim, enerji türü), termometre okuma, ısı ve sıcaklık kavramlarının doğru kullanımı |
| alisveris | 20 | Sıvıların karıştırılması, ısının yönü, son sıcaklık, eşit sıcaklıkta alışveriş olmaması, ortam sıcaklığına ulaşma, günlük örnekler |
| hal | 20 | Erime, donma, buharlaşma (kaynama), yoğuşma, süblimleşme, kırağılaşma; ısı alma/verme; ısınma-soğuma grafikleri; buharlaşma-kaynama farkı |
| iletim | 20 | Isı iletkenleri ve yalıtkanları, balmumu deneyi, ısı yalıtımı uygulamaları (ev, termos, strafor kutu, kümbet evler) |

Görev türlerinin dağılımı: sort 24, model 11, mix 9, phase 9, fill 8, design 8, flow 6, rod 6, syringe 5, tag 5, thermo 5, curve 5, room 2.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği metin olarak içerir ([Deney: …] / [Madde: …] biçiminde).
- studentAnswer öğrencinin seçimlerini, ayarlarını ya da girdiği değeri yazar.
- correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 5. Sınıf Ders Kitabı (2. kitap), 5. Ünite (s. 52–101).

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
