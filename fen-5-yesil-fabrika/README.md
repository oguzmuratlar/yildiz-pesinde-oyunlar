# Yeşil Fabrika · Sürdürülebilir Yaşam ve Geri Dönüşüm

| Alan | Değer |
|---|---|
| gameId | fen-5-yesil-fabrika |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 5 (oyun yalnızca 5. sınıf bağlamını kabul eder) |
| Ünite | 7. Ünite: Sürdürülebilir Yaşam ve Geri Dönüşüm |
| Ekran yönü | Dikey |
| Oyun türü | Geri dönüşüm fabrikası temalı ayrıştırma ve süreç simülasyonu oyunu. Karakter yoktur. Test ve doğru/yanlış sorusu yoktur. 10 tur, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🌱 puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 102 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:**
  1. Tuğla duvarlı fabrikanın bacalarından buhar yükselir.
  2. Konveyör bantta atıklar akar.
  3. "YEŞİL FABRİKA" tabelası dişlisiyle birlikte yanar.
  4. "VARDİYAYA BAŞLA" denince kepenk açılır, içeriden yeşil ışık patlar.
- **İlerleme:** Üstte 10 kasa vardır. Doğru turda kasa yeşillenir (♻️), yanlışta çöpe gider (🗑️).
- **Çıkış:**
  1. Kepenk iner, tabela "VARDİYA BİTTİ" olur.
  2. "SIFIR ATIK x/10 BELGESİ" mühür gibi basılır.
  3. Sonuç "SIFIR ATIK BELGESİ" olarak açılır.

## Turlar (fabrika simülasyonları)
| Tür | Tur | Mekanik |
|---|---|---|
| belt | Bant ayrıştırma | Bantta sırayla gelen atıklar dokunarak doğru kutuya atılır (plastik, cam, kâğıt, metal, atık pil, organik, atık yağ, dönüşmez, tıbbi atık). Sonra denetçi robot kutuları kontrol eder |
| sort | Kasalar | Kartlar 2–3 kasaya sürüklenir ya da dokunarak yerleştirilir (kutu türleri, yeniden kullanım/ileri/geri dönüşüm, bilim insanı ve katkısı …) |
| pick | Mıknatıslı kepçe | Bir kutuya girmemesi gereken atıklar seçilir, kepçe onları çıkarır |
| machine | Dönüşüm makinesi | Her eski ürün → yeni ürün satırı için yeniden kullanım, ileri dönüşüm ya da geri dönüşüm seçilir. Makine çalışınca yeni ürün belirir |
| chain | Hat sırala | Kartlara sırayla dokunularak süreç adımları sıralanır. Bazı turlarda hattı bozan tuzak kart vardır |
| habit | Çöp poşeti tart | Sıfır atığa uygun davranışlar seçilir. Poşet tartılır, atık azalma yüzdesi gösterilir |
| chart | Enerji grafiği | Ders kitabındaki verilerle çizilmiş sütunlardan en büyüğü seçilir ya da sütunlar sıralanır, sonra ölçülür |
| calc | Sayı çarkı | Atık ve tasarruf hesapları sayı çarkıyla girilir. Sonuç görsel olarak da gösterilir (ör. biriken pet şişeler) |

Her deste kurulurken her konudan 2 tur seçilir. Tur türleri olabildiğince farklı tutulur, bir destede en az 8 farklı tür bulunur.

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| ayrim | 21 | Atıkların türlerine göre ayrıştırılması; geri dönüşen ve dönüşmeyen atıklar; atık pil, atık yağ, tıbbi atık |
| atik | 20 | Evsel atıklar, ayrıştırma kutularının içeriği |
| surec | 22 | Geri dönüşüm süreci, yeniden kullanım, ileri dönüşüm, evsel atık ayrıştırma sistemi |
| sifir | 19 | Sıfır atık; israfı önleme, atık oluşumunu azaltan davranışlar |
| kaynak | 20 | Kaynakların korunması, geri dönüşümün enerji ve ham madde tasarrufu; hesaplamalar |

Görev türlerinin dağılımı: sort 26, belt 18, habit 13, pick 10, machine 10, chain 9, calc 9, chart 7.

Yanlış-cevap kaydı:
- questionText görevi ve atıkları metin olarak içerir.
- studentAnswer öğrencinin kutulara attıklarını, sırasını ya da sayısını yazar.
- correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 5. Sınıf Ders Kitabı, 7. Ünite (s. 137–159).

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
