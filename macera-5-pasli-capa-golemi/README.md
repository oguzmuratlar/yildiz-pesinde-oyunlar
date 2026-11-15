# Paslı Çapa Golemi — Macera Canavarı (Arena 2 · Batık Gemi)

| Alan | Değer |
|---|---|
| gameId | macera-5-pasli-capa-golemi |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 5 |
| Kapsam | Fen Ü3–Ü4, Matematik T3–T4, Türkçe T3 |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — Fen 5 (bir üniteden 3, diğerinden 2; her denemede rastgele), Matematik 4 (2 + 2), Türkçe 3; 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 100 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Paslı Çapa Golemi batık gemiyi 10 halkalı paslı bir zincirle bekliyor. Her doğru cevap bir halkayı koparır: halka parlar, kıvılcım saçar ve dibe düşer. 5. halkada golem öfkelenir ve kızıl bir ışıkla parlar. 10. halka koptuğunda golem yenilir; kalan sorular “Bonus halka”dır. Yanlışta golem çapasını sallar: sahne sarsılır, ekrana pas yağar, doğru cevap ve açıklama gösterilir. Üst sayaçta kopan halka sayısı ve kalan hata hakkı (2) görünür. İpucu ve süre yoktur.

## Giriş / çıkış
- **Giriş:** Kabarcıklar yükselir, golem batık geminin önünde su patlamasıyla alttan çıkar, “PASLI ÇAPA GOLEMİ” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa sersemlemiş golem, konfeti ve “Paslı Çapa Golemi yenildi!”; kaybedilirse golem suyun içinde yukarı süzülerek uzaklaşır. Sonuç kartında 12 cevaplık şerit, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 58 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 16 |
| tf | Doğru / Yanlış | 9 |
| sort2 | Kartı seç, iki kutudan birine koy | 7 |
| match | Sol satıra sağdaki kartı yerleştir | 5 |
| order | Kartlara sırayla dokunarak diz | 5 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü3 Canlıların Yapısına Yolculuk | 20 | Bitki ve hayvan hücresi, Destek ve hareket, Eklemler, Hücre, Hücreden organizmaya, Kas çeşitleri, Kıkırdak, Mikroskop, Mikroskop kullanımı, Organellerin görevleri |
| Fen Ü4 Işığın Dünyası | 20 | Gölge büyüklüğü, Gölgenin şekli, Görme, Işık geçirgenliği, Işık geçirgenliğinin kullanımı, Işık kaynakları, Işığın yayılması, Kalınlığın etkisi, Tam gölge |
| Mat T3 Geometrik Nicelikler | 20 | Alan, Alan birimi, Alandan çevre, Birim kare, Birleşik şekil, Eksik kenar, En büyük alan, Karenin çevresi, Problem, Yüzey kaplama, Çevre uzunluğu, Çevre ve alan |
| Mat T4 Kesirler | 20 | Bir çokluğun kesri, Birim kesir, Birim kesirleri sıralama, Denk kesir, Farklı gösterimler, Kalan kısım, Karşılaştırma, Kesir modeli, Ondalık gösterim, Sadeleştirme, Tam sayılı kesir, Yüzde |
| Türkçe T3 Duygularımı Tanıyorum | 20 | Amaç bildiren ifadeler, Deyim, Duygu bildiren ifadeler, Düşünceyi geliştirme yolları, Hikâye unsurları, Somut ve soyut isimler, Topluluk ismi, Uzun çizgi, Ünlem |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- MEB Fen Bilimleri 5. Sınıf Ders Kitabı: 3. Ünite “Canlıların Yapısına Yolculuk” (s. 99–123) ve 4. Ünite “Işığın Dünyası”
- MEB Matematik 5. Sınıf Ders Kitabı: 3. Tema “Geometrik Nicelikler” ve 4. Tema “Kesirler”
- MEB Türkçe 5. Sınıf Ders Kitabı: 3. Tema “Duygularımı Tanıyorum”

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
