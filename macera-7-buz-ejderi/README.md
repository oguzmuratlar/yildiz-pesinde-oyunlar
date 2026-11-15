# Buz Ejderi — Macera Canavarı (Arena 12 · Kutup Işıkları)

| Alan | Değer |
|---|---|
| gameId | macera-7-buz-ejderi |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 7 |
| Kapsam | Fen Ü7, Matematik T8–T9, Türkçe T6 |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — Fen 4 (Ü7), Matematik 5 (T8+T9), Türkçe 3 (T6); 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 80 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Buz Ejderi kutup ışıkları altında, çevresinde 10 buz kristaliyle (mavi kristal, lacivert kontur, beyaz parıltı) bekliyor. Her doğru cevap bir kristali kırar: kristal parlar, buz parçalarına ayrılıp dağılır. 5. kristalde ejder buz nefesi üfler, ekranın kenarları buz tutar (“Buz Ejderi nefes üfledi!”). 10. kristalde ejder yenilir; kalan sorular “Bonus kristal”dir. Yanlışta ekran buz tutar ve çatlar; doğru cevap ve açıklama gösterilir. Üst sayaçta kırılan kristal sayısı ve kalan hata hakkı (2) görünür. İpucu ve süre yoktur. Matematikte π = 3 alınır.

## Giriş / çıkış
- **Giriş:** Kabarcıklar yükselir, Buz Ejderi kutup ışıklarının altında alttan çıkar, “BUZ EJDERİ” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa yenilmiş ejder, konfeti ve “Buz Ejderi yenildi!”; kaybedilirse ejder yukarı süzülüp kutup ışıklarına uçar. Sonuç kartında 12 cevaplık şerit, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 35 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 22 |
| tf | Doğru / Yanlış | 9 |
| match | Sol satıra sağdaki kartı yerleştir | 5 |
| order | Kartlara sırayla dokunarak diz | 5 |
| sort2 | Kartı seç, iki kutudan birine koy | 4 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü7 Sürdürülebilir Yaşam ve Enerji | 20 | Arıtma, Atık su türleri, Atık yağ, Ayrıştırıcılar, Ayrıştırıcıların yeri, Besin ağı, Besin zinciri, Biyolojik birikim, Enerji aktarımı, Görünmez su, Piramitte birey sayısı, Su ayak izi, Su ayak izi hesabı, Su tasarrufu, Tatlı su, Tatlı su oranı, Tuzlu su, Zincirde değişim, Zincirdeki görevler, Üreticiler |
| Mat T8 İşlemlerle Cebirsel Düşünme ve Değişimler | 20 | Benzer terim, Benzer terimler, Dağılma, Denge, Denklem, Eşitsizlik kurma, Eşitsizlik problemi, Eşitsizlik çözme, Gauss toplamı, Katsayı, Parantezli denklem, Sabit terim, Sadeleştirme, Sözelden cebire, Taksi algoritması, Ters dönen eşitsizlik, Varsayımı sınama, Çürütme, Çıkarma |
| Mat T9 Geometrik Nicelikler (2) | 20 | Alan formülleri, Alan formülü, Alanları sıralama, Daire dilimi, Dairenin alanı, Dilim oranı, Eşkenar dörtgen, Kalan alan, Köşegen bulma, Pizza karşılaştırma, Yamuk, Yarım daire, Yarıçap iki katına, Yükseklik bulma, Çaptan alan, Çeyrek daire |
| Türkçe T6 Hak ve Sorumluluklar | 20 | Akışı bozan cümle, Değer, Eşitlik ve adalet, Hak ve sorumluluk, Paragraf akışı, Problem çözme, Sadece, ancak, Sonraki adım, Sorumluluk, Sunum hazırlama, Söz varlıkları, Sınırlama, Sınırlama yok, Sıra bildiren, Sıra bildirmeyen, Çocuk hakları, Öykünün bölümleri, İkileme, “Ancak” |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- MEB Fen Bilimleri 7. Sınıf Ders Kitabı (2. kitap): 7. Ünite “Sürdürülebilir Yaşam ve Enerji”
- MEB Matematik 7. Sınıf Ders Kitabı 2. Kitap: 8. Tema “İşlemlerle Cebirsel Düşünme ve Değişimler”, 9. Tema “Geometrik Nicelikler (2)” (π = 3)
- MEB Türkçe 7. Sınıf Ders Kitabı 2. Kitap: 6. Tema “Hak ve Sorumluluklar”

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
