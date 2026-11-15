# Fener Balığı — Macera Canavarı (Arena 3 · Derin Deniz Mağarası)

| Alan | Değer |
|---|---|
| gameId | macera-5-fener-baligi |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 5 |
| Kapsam | Fen Ü5–Ü6, Matematik T5–T6, Türkçe T4–T5 |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — her ünite/temadan 2 (Fen 4, Matematik 4, Türkçe 4); 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 120 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Fener Balığı derin mağaranın 10 ışığını feneriyle esir tutuyor; ışıklar balığın çevresinde döner, mağara karanlıktır. Her doğru cevap bir ışığı serbest bırakır: ışık parlayıp yukarı süzülür, mağarada küçük bir plankton ışığına dönüşür; balığın feneri her vuruşta biraz söner ve mağara aydınlanır. 5. ışıkta fener titrer. 10. ışıkta fener tamamen söner ve balık yenilir; kalan sorular “Bonus ışık”tır. Yanlışta fener göz kamaştırıcı bir ışık patlaması yapar, doğru cevap ve açıklama gösterilir. Üst sayaçta sönen ışık sayısı ve kalan hata hakkı (2) görünür. İpucu ve süre yoktur.

## Giriş / çıkış
- **Giriş:** Kabarcıklar yükselir, fener balığı karanlık mağarada alttan çıkar, “FENER BALIĞI” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa feneri sönmüş, sersemlemiş balık, konfeti ve “Fener Balığı yenildi!”; kaybedilirse balık karanlığa doğru yukarı süzülüp kaybolur. Sonuç kartında 12 cevaplık şerit, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 73 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 20 |
| sort2 | Kartı seç, iki kutudan birine koy | 8 |
| tf | Doğru / Yanlış | 8 |
| match | Sol satıra sağdaki kartı yerleştir | 6 |
| order | Kartlara sırayla dokunarak diz | 5 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü5 Maddenin Doğası | 20 | Hâl değişimi, Hâl değişimleri, Isı alarak ve vererek, Isı alışverişi, Isı iletimi, Isı iletkenliği, Isı ve sıcaklık, Isı yalıtımı, Isının birimi, Karışımın sıcaklığı, Katı ve sıvı, Kaynama, Sıcaklık, Sıkıştırılabilirlik, Tanecikler arası boşluk, Tanecikli yapı, Termometre okuma, Yoğuşma, İletken ve yalıtkan |
| Fen Ü6 Yaşamımızdaki Elektrik | 20 | Ampul sayısı, Bağımlı değişken, Bağımsız değişken, Devre şeması, Devrenin çalışması, Değişkenler, Hipotez, Kontrol edilen değişken, Parlaklık, Parlaklık karşılaştırma, Pil sayısı, Pil sayısı ve parlaklık, Semboller |
| Mat T5 İstatistiksel Araştırma Süreci | 20 | Araştırma adımları, Araştırma sorusu, Daire grafiği, Değişkenlik, Gizlilik, Grafik dönüştürme, Grafik türleri, Kategorik veri, Nokta grafiği, Sütun grafiği, Sıklık tablosu, Uygun grup, Veriye dayalı karar, Yanıltıcı grafik, Yorumu değerlendirme, Çetele |
| Mat T6 İşlemlerle Cebirsel Düşünme | 20 | Akış şeması, Algoritma, Birleşme özelliği, Dağılma özelliği, Değişme özelliği, Eşitliğin korunumu, Sayı örüntüsü, Örüntünün kuralı, Üslü ifadeler, İşlem önceliği, Şekil örüntüsü |
| Türkçe T4 Geleneklerimiz | 20 | Atasözü, Bağlamda anlam, Bağlantı ifadeleri, Büyük harf, Deyim, Eş anlam, Gerçek ve mecaz anlam, Kalıplaşmış söz, Karşılaştırma, Kesme işareti, Mecaz anlam, Metin yapısı, Sayıların yazımı, Sıralı metin, Tanıtma paragrafı, Zıt anlam, Özet ifadesi, Üç nokta, İsimlerin yerini tutan sözcükler |
| Türkçe T5 İletişim ve Sosyal İlişkiler | 20 | Bağlantı ifadesi, Beden dili, Büyük harf, Dijital güvenlik, Empati, Etkili dinleme, Gönül deyimleri, Kesme işareti, Mecaz anlam, Metin türü, Sesteş kelimeler, Sonlandırma ifadesi, Söz sanatları, Tırnak işareti, Zıt anlam, Çıkarım, Önemli ve önemsiz bilgi, Örtük ifade, İsimlerin yerini tutan sözcükler |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- MEB Fen Bilimleri 5. Sınıf Ders Kitabı: 5. Ünite “Maddenin Doğası” (s. 57–89) ve 6. Ünite “Yaşamımızdaki Elektrik” (s. 105–127)
- MEB Matematik 5. Sınıf Ders Kitabı 2. Kitap: 5. Tema “İstatistiksel Araştırma Süreci” ve 6. Tema “İşlemlerle Cebirsel Düşünme”
- MEB Türkçe 5. Sınıf Ders Kitabı 2. Kitap: 4. Tema “Geleneklerimiz” ve 5. Tema “İletişim ve Sosyal İlişkiler”

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
