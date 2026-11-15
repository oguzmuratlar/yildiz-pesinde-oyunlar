# Kraken — Macera Canavarı (Arena 4 · Su Üstü)

| Alan | Değer |
|---|---|
| gameId | macera-5-kraken |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 5 |
| Kapsam | Fen Ü7, Matematik T7, Türkçe T6 |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — her ünite/temadan 4 (Fen 4, Matematik 4, Türkçe 4); 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 60 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Kraken, öğrencinin küçük teknesine 10 dev dalga gönderiyor; dalgalar canavarın çevresinde kabarır. Her doğru cevap bir dalgayı geri çevirir: dalga parlar, köpüğe dönüşüp denize çöker ve tekne biraz yükselir. 5. dalgada Kraken öfkelenir, kalan dalgalar büyüyüp kabarır. 10. dalgada Kraken yenilir; kalan sorular “Bonus dalga”dır. Yanlışta dev bir dalga ekranı alttan yalayıp geçer, tekne sallanır; doğru cevap ve açıklama gösterilir. Üst sayaçta geri çevrilen dalga sayısı ve kalan hata hakkı (2) görünür. İpucu ve süre yoktur.

## Giriş / çıkış
- **Giriş:** Kabarcıklar yükselir, Kraken denizden alttan yükselir, “KRAKEN” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa sersemlemiş Kraken, konfeti ve “Kraken yenildi!”; kaybedilirse Kraken yukarı doğru süzülüp kaybolur. Sonuç kartında 12 cevaplık şerit, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 41 |
| tf | Doğru / Yanlış | 6 |
| sort2 | Kartı seç, iki kutudan birine koy | 5 |
| match | Sol satıra sağdaki kartı yerleştir | 4 |
| order | Kartlara sırayla dokunarak diz | 3 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 1 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü7 Sürdürülebilir Yaşam ve Geri Dönüşüm | 20 | Atık kutuları, Atık pil, Atık yönetimi, Cam kutusu, Doğal kaynaklar, Dönüşüm türleri, Evsel atıklar, Geri dönüşüm, Geri dönüşüm süreci, Kaynakların etkili kullanımı, Kaynakların korunması, Sıfır atık, Yeniden kullanım, İleri dönüşüm |
| Mat T7 Veriden Olasılığa | 20 | Adil oyun, Az olası, Eşit olasılık, Kesin olay, Kesin ve imkânsız, Olası olay, Olasılık değeri, Olasılık ifadeleri, Olasılık spektrumu, Torba, Veriye dayalı tahmin, Öznel olasılık, İmkânsız olay |
| Türkçe T6 Sağlıklı Yaşıyorum | 20 | Ana fikir, Büyük harf ve sayı, Deyim, Düşünceyi geliştirme, Eş anlam, Karşılaştırma, Kelime anlamı, Metin türü, Niteleyen kelime, Sayıların yazımı, Sağlıklı yaşam, Soru işareti, Tırnak işareti, Yabancı kelime, Yabancı kelimeler, Zıt anlam, Çıkarım, Önemli bilgi, Örnek bildiren ifade, İsmin yerini tutan kelime |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- MEB Fen Bilimleri 5. Sınıf Ders Kitabı: 7. Ünite “Sürdürülebilir Yaşam ve Geri Dönüşüm” (s. 138–158)
- MEB Matematik 5. Sınıf Ders Kitabı 2. Kitap: 7. Tema “Veriden Olasılığa”
- MEB Türkçe 5. Sınıf Ders Kitabı 2. Kitap: 6. Tema “Sağlıklı Yaşıyorum”

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
