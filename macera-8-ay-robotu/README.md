# Ay Robotu — Macera Canavarı (Arena 14 · Ay Üssü)

| Alan | Değer |
|---|---|
| gameId | macera-8-ay-robotu |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 8 |
| Kapsam | Fen Ü3–Ü4, Matematik Ü4–Ü6, Türkçe Paragraf I ve Paragraf II |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — Fen 4 (Ü3+Ü4), Matematik 4 (Ü4+Ü5+Ü6), Türkçe 4 (Paragraf I + Paragraf II); 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 140 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Ay Robotu ay yüzeyinde, önünde yay biçiminde dizilmiş 10 güç hücresiyle (lacivert pil, beyaz kontur, yeşil şarj çubukları, sarı şimşek) bekliyor. Her doğru cevap bir hücreyi söker: şarj çubukları sırayla kırmızıya dönüp söner, kıvılcımlar saçılır, hücre dönerek düşer. 5. hücrede robot yedek güce geçer, görüntüsü renk kayarak titrer (“Ay Robotu yedek güce geçti!”). 10. hücrede robot yenilir; kalan sorular “Bonus hücre”dir. Yanlışta sahneyi mavi bir tarama ışını boydan boya tarar, ekran parazitlenir.

## Giriş / çıkış
- **Giriş:** Yıldızlar parlar, Ay Robotu ay yüzeyinde alttan yükselir, “AY ROBOTU” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa yenilmiş robot (gülen ekran yüz, başında yıldızlar), konfeti ve “Ay Robotu yenildi!”; kaybedilirse robot üsse geri döner. Sonuç kartında 12 cevaplık şerit, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 67 |
| tf | Doğru / Yanlış | 24 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 20 |
| sort2 | Kartı seç, iki kutudan birine koy | 17 |
| match | Sol satıra sağdaki kartı yerleştir | 6 |
| order | Kartlara sırayla dokunarak diz | 6 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü3 Basınç | 20 | Baraj, Basıncı artır, azalt, Basınç hesabı, Derinlik, Derinliğe göre sırala, Deve, Fışkıran su, Günlük yaşam, Hangi basınç, Her yöne etki, Hidrolik sistemler, Kap şekli, Katı basıncının etkenleri, Kuvvet kazancı, Sandık, Sıvı basıncını ne değiştirir, Tatlı ve tuzlu su, Tuğla, Yoğunluk, Yüzey alanı |
| Fen Ü4 Madde ve Endüstri | 20 | Asit ve baz, Asit, baz, nötr, Aynı grup, Fiziksel ve kimyasal, Grup, Hâl değişimi, Isı alır, ısı verir, Isı ve sıcaklık, Kimya endüstrisi, Kütle korunumu, Kütlenin korunumu, Metal ve ametal, Nötrleşme, Sabit sıcaklık, Soygazlar, Turnusol, Yanma, pH, pH sırası, Öz ısı |
| Mat Ü4 Veri Analizi | 20 | Azalan ay, Açıdan yüzde, Bütçe, Daire grafiği, Dilimden sayıya, Eksik sütun, Grafiği yorumla, Gösterimler, Hangi grafik, Kesişen çizgiler, Merkez açı, Merkez açılar, Sütun grafiği, Tablodan sıralama, Toplam fidan, Uygun grafik, Çizgi grafiği, Çoklu veri, İki amaç, İki sınıf |
| Mat Ü5 Basit Olayların Olma Olasılığı | 20 | 0–1 aralığı, Eşit olasılık, Eşit şans, Kartlar, Kesin olay, Kesin ve imkânsız, Kırmızı ekleme, Olasılık aralığı, Olasılık sırası, Sekiz dilimli çark, Top ekleme, Top eklenince, Torba, Yarıdan büyük mü, Yeşil olmayan, Zar olasılıkları, Zarın durumları, Çark, Çark tasarımı, Öğrenci seçme |
| Mat Ü6 Cebirsel İfadeler ve Özdeşlikler | 20 | (x + 2) çarpanı, 5x ile benzer, Benzer mi, Benzer terimler, Dağılma, Değer hesaplama, Dikdörtgen alanı, Karenin alanı, Ortak çarpan, Tam kare, Tam kare ayırma, Yanılgı, Zihinden fark, Zihinden kare, Çarpanlara ayırma, Çarpım, Çarpımlar, Çevre, İki kare farkı, İki terimli çarpım |
| Türkçe Paragraf I (konu, ana düşünce, başlık) | 20 | Ana düşünce, Ana düşüncenin yeri, Anahtar sözcük, Başlık, Başlık bul, Değinilmeyen, Karşı çıkılan görüş, Konu, Konu mu ana düşünce mi, Konu ve ana düşünce, Yazarın amacı, Yazarın tutumu, Çıkarım |
| Türkçe Paragraf II (akış, cümle ekleme, düşünceyi geliştirme) | 20 | Akışı bozan cümle, Anlatım biçimi, Betimleme, Betimleme ve öyküleme, Cümle ekleme, Cümle sıralaması, Düşünceyi geliştirme, Fidan dikimi, Giriş cümlesi, Karşılaştırma, Sonuç cümlesi, Tanık gösterme, Tanımlama ve sayısal veri, Tartışma ve açıklama, Örnekleme, İkiye bölme |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- 8. Sınıf Fen Bilimleri Öğretim Programı: 3. Ünite “Basınç”, 4. Ünite “Madde ve Endüstri” (periyodik sistem, fiziksel ve kimyasal değişimler, asitler ve bazlar, maddenin ısı ile etkileşimi, kimya endüstrisi)
- 8. Sınıf Matematik Öğretim Programı: 4. Ünite “Veri Analizi”, 5. Ünite “Basit Olayların Olma Olasılığı”, 6. Ünite “Cebirsel İfadeler ve Özdeşlikler”
- 8. Sınıf Türkçe Öğretim Programı: Paragrafta anlam (konu, ana düşünce, başlık, çıkarım) ve paragrafın yapısı (akış, cümle ekleme, düşünceyi geliştirme yolları, anlatım biçimleri)

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
