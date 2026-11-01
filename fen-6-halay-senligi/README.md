# Halay Şenliği · Elektriğin İletimi ve Direnç

| Alan | Değer |
|---|---|
| gameId | fen-6-halay-senligi |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 6 (oyun yalnızca 6. sınıf bağlamını kabul eder) |
| Ünite | 6. Ünite: Elektriğin İletimi ve Direnç |
| Ekran yönü | Dikey |
| Oyun türü | Köy meydanında halay şenliği temalı elektrik deneyleri oyunu. Öğrenci karakteri yoktur; halay oyuncuları ilerlemeyi gösterir. Test ve doğru/yanlış sorusu yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🎉 puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 101 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:**
  1. Gece köy meydanı, evlerin silueti, sönük ışık zincirleri.
  2. "HALAY ŞENLİĞİ" tabelası yanar.
  3. "DAVULU ÇAL" denince davul vurur, ışık zincirleri sırayla yanıp göz kırpar.
  4. Mendil sallayan halaybaşıyla yedi oyuncu omuz omuza halaya başlar, ışık patlaması olur.
- **İlerleme:** Üstte 10 halay yeri vardır. Doğru görevde o yere renkli bir halay oyuncusu katılır; yanlışta yer boş (kesikli) kalır.
- **Çıkış:**
  1. Işıklı meydanda yalnızca doğru görevlerde kazanılan oyuncular halay çeker.
  2. Bayraklı "HALAYDAKİ x/10 OYUNCU" madalyası basılır.
  3. Sonuç "ŞENLİK MADALYASI" olarak açılır.

## Görevler (elektrik deneyleri)
| Tür | Görev | Mekanik |
|---|---|---|
| tester | Işık zinciri testi | Malzemeler için "yanar / yanmaz" tahmini yapılır; test başlayınca her malzeme test uçlarına konur, ampul yanar ya da yanmaz |
| dart | Şenlik dartı | 8 dilimli dart tahtasında istenen gruptaki (iletken katı, yalıtkan sıvı …) bölgeler hedeflenir; oklar fırlatılır |
| beaker | Sıvı testi | Levhalar daldırılınca lambayı yakacak sıvıların beherglası seçilir |
| kit | Şenlik elektrikçisi | Kablo içi/dışı, priz, eldiven, filaman, ısıtıcı teli için doğru malzeme seçilir; güvenlik kontrolü geçerse meydan ışıkları yanar |
| wires | Işık zinciri telleri | Cinsi, uzunluğu ve kalınlığı verilen teller ampul parlaklığına göre sıralanır; ışıklar yanınca parlaklık farkı görünür |
| design | Deney masası | İstenen değişkenin etkisini görmek için 2. telin cinsi, uzunluğu, kalınlığı (zorda bağımlı değişken de) ayarlanır; iki devre yan yana çalışır, "adil deney" denetlenir |
| reo | Sahne ışığı (reosta) | Reosta sürgüsü 1/2 yönüne kaydırılarak istenen parlaklık kademesi bulunur; akımın geçtiği tel bölümü sarı gösterilir |
| trend | Parlaklık grafiği | Parlaklık grafiğindeki her aşamada sürgünün yönü ya da direncin değişimi seçilir |
| sort | Şenlik sandıkları | İletken/yalıtkan, katı/sıvı, direnç artar/azalır, yol benzetmesi, reosta kullanan aletler, değişken türleri, bilim insanları |
| calc | Sayı çarkı | Edison’un filamanı, tel uzunluğu/kalınlığı ve bilim insanlarının yaşam süreleri |

Her deste kurulurken her konudan 2 görev seçilir. Görev türleri olabildiğince farklı tutulur.

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| iletken | 20 | Katı iletken ve yalıtkanlar, test devresi, dart oyunu |
| sivi | 20 | İletken ve yalıtkan sıvılar, yalıtkanların güvenlik amaçlı kullanımı |
| direnc | 20 | Uzunluk, dik kesit alanı ve cinsin direnç ve ampul parlaklığına etkisi; filaman, ısıtıcı |
| reosta | 22 | Reosta sürgüsü, parlaklık grafikleri, reosta kullanılan aletler; Edison, Tesla, Emin Kalmuk, Fuat Külünk |
| deney | 19 | Değişken kontrolü, bağımlı/bağımsız/sabit değişken, tel çiftleri |

Görev türlerinin dağılımı: sort 16, wires 13, design 12, tester 11, reo 9, calc 8, dart 8, beaker 8, kit 8, trend 8.

Yanlış-cevap kaydı:
- questionText görevi, malzemeleri, telleri ya da grafiği metin olarak içerir.
- studentAnswer öğrencinin tahminlerini, seçimlerini, sırasını ya da sürgü kademesini yazar.
- correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 6. Sınıf Ders Kitabı (2. kitap), 6. Ünite (s. 64–95).

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
