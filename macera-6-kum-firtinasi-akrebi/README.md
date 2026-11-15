# Kum Fırtınası Akrebi — Macera Canavarı (Arena 8 · Çöl Kervanı)

| Alan | Değer |
|---|---|
| gameId | macera-6-kum-firtinasi-akrebi |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 6 |
| Kapsam | Fen Ü7, Matematik T7, Türkçe T6 |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — her ünite/temadan 4 (Fen 4, Matematik 4, Türkçe 4); 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 60 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Kum Fırtınası Akrebi çölde 10 kum girdabı döndürüyor; girdaplar akrebin çevresinde hızla döner. Her doğru cevap bir girdabı dindirir: girdap yavaşlayıp kum yığınına dönüşür. 5. girdapta akrep kuyruğunu kaldırıp parlar. 10. girdapta fırtına diner ve akrep yenilir; kalan sorular “Bonus girdap”tır. Yanlışta ekranı kum fırtınası süpürür; doğru cevap ve açıklama gösterilir. Üst sayaçta dinen girdap sayısı ve kalan hata hakkı (2) görünür. İpucu ve süre yoktur.

## Giriş / çıkış
- **Giriş:** Kabarcıklar yükselir, akrep çöl kervanının önünde alttan çıkar, “KUM FIRTINASI AKREBİ” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa yenilmiş akrep, konfeti ve “Kum Fırtınası Akrebi yenildi!”; kaybedilirse akrep yukarı süzülüp kaçar. Sonuç kartında 12 cevaplık şerit, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 38 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 12 |
| sort2 | Kartı seç, iki kutudan birine koy | 3 |
| tf | Doğru / Yanlış | 3 |
| match | Sol satıra sağdaki kartı yerleştir | 3 |
| order | Kartlara sırayla dokunarak diz | 1 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü7 Sürdürülebilir Yaşam ve Etkileşim | 20 | Biyoçeşitlilik, Biyoçeşitliliği etkileyenler, Endemik canlı, Habitat, Karbon monoksit, Kirlilik türleri, Kirliliğin sağlığa etkisi, Neslin tükenmesi, Orman yangınları, Su kirliliği, Tarım ilaçları, Tehlike altındaki canlılar, Yakıtlar, Çevre bilinci, Çölleşme, Çözüm üretme |
| Mat T7 Geometrik Nicelikler | 20 | Alan bağıntıları, Alan birimleri, Alan problemi, Merkez açı, Merkez açı ve yay, Paralelkenarın alanı, Pi sayısı, Tam açı, Yarıçap, Yükseklik, Çap ve yarıçap, Çemberin uzunluğu, Üçgenin alanı |
| Türkçe T6 Lider Ruhlar | 20 | Atasözü, Azim, Benzerlik, Biyografi, Derin anlam, Deyim, Deyimler, Girişkenlik, Hoşgörü, Kelime anlamı, Kesme işareti, Liderlik özellikleri, Olumsuzluk, Piri Reis, Yazım, Çıkarım, Öncü kadınlar, Önemli bilgi, İbni Sina |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- MEB Fen Bilimleri 6. Sınıf Ders Kitabı (2. kitap): 7. Ünite “Sürdürülebilir Yaşam ve Etkileşim” (s. 100–120)
- MEB Matematik 6. Sınıf Ders Kitabı 2. Kitap: 7. Tema “Geometrik Nicelikler” (π = 3)
- MEB Türkçe 6. Sınıf Ders Kitabı 2. Kitap: 6. Tema “Lider Ruhlar”

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
