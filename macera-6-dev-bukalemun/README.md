# Dev Bukalemun — Macera Canavarı (Arena 6 · Yağmur Ormanı)

| Alan | Değer |
|---|---|
| gameId | macera-6-dev-bukalemun |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 6 |
| Kapsam | Fen Ü3–Ü4, Matematik T3–T4, Türkçe T3 |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — Fen 5 (bir üniteden 3, diğerinden 2; her denemede rastgele), Matematik 4 (2 + 2), Türkçe 3; 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 100 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Dev Bukalemun yağmur ormanında renk değiştirerek saklanıyor; ekranda yarı saydam ve orman renklerine karışmış görünür. Çevresinde 10 renkli boya kavanozu vardır. Her doğru cevapta bir kavanozdaki boya bukalemuna fırlatılır, kavanoz boşalır ve bukalemun biraz daha görünür hâle gelir. 5. boyada bukalemun hızla renk değiştirir. 10. boyada bütün renkleriyle ortaya çıkar ve yakalanır; kalan sorular “Bonus boya”dır. Yanlışta bukalemun yapraklara karışıp bir an kaybolur, yapraklar ekranı süpürür; doğru cevap ve açıklama gösterilir. Üst sayaçta kullanılan boya kavanozu sayısı ve kalan hata hakkı (2) görünür. İpucu ve süre yoktur.

## Giriş / çıkış
- **Giriş:** Kabarcıklar yükselir, bukalemun orman zemininden alttan çıkar, “DEV BUKALEMUN” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa yakalanmış bukalemun, konfeti ve “Dev Bukalemun yakalandı!”; kaybedilirse bukalemun yukarı süzülüp kaybolur. Sonuç kartında 12 cevaplık şerit, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 63 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 20 |
| match | Sol satıra sağdaki kartı yerleştir | 5 |
| tf | Doğru / Yanlış | 5 |
| sort2 | Kartı seç, iki kutudan birine koy | 4 |
| order | Kartlara sırayla dokunarak diz | 3 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü3 Canlılarda Sistemler | 20 | Adrenalin, Başkalaşım, Beynin bölümleri, Ergen sağlığı, Ergenlik, Eşeyli ve eşeysiz üreme, Eşeyli üreme, Eşeysiz üreme, Eşeysiz üreme çeşitleri, Hipofiz bezi, Merkezî sinir sistemi, Refleks, Tozlaşma ve döllenme, Çevresel sinir sistemi, Çimlenme, Çimlenme deneyi, Çiçeğin kısımları, İç salgı bezleri |
| Fen Ü4 Işığın Yansıması ve Renkler | 20 | Ana renkler, Ayna çeşitleri, Beyaz cisim, Cisimlerin rengi, Dik gelen ışın, Düz ayna, Düzgün ve dağınık yansıma, Düzgün yansıma, Görme, Güneş enerjisi, Renklerin karışımı, Renkli ışık, Soğurma, Tümsek ayna, Yansıma kanunu, Çukur ayna |
| Mat T3 Sayılar ve Nicelikler (2) | 20 | Basamak değeri, Birim dönüştürme, Devirli ondalık gösterim, Doğal sayı ile kesir çarpımı, Kesir problemi, Kesir ve bölme, Kesirle kesrin bölümü, Kesirlerle toplama, Kısa yoldan çarpma, Ondalık bölme, Ondalık toplama, Ondalık çarpma, Sıralama, Uzunluk birimleri, Yuvarlama, Yüzde, İki kesrin çarpımı |
| Mat T4 İstatistiksel Araştırma Süreci | 20 | Aritmetik ortalama, Açıklık, Karşılaştırma sorusu, Kategorik ve nicel veri, Kök-yaprak, Merkezî eğilim ölçüleri, Nicel veri, Ortanca, Planlama, Sonuçları yorumlama, Tepe değer, Uygun ölçü, Yanlı sorular |
| Türkçe T3 Farklı Dünyalar | 20 | Düşünceyi geliştirme, Kelime anlamı, Metnin bölümleri, Nesnel yargı, Sayısal veri, Sebep, Ses olayları, Yapım ekleri, Yardımcı ünsüz, Yazım, Yüzey anlam, Zıtlık, mi soru eki, Öznel yargı, Ünlü daralması, Ünlü düşmesi, Ünsüz türemesi, Ünsüz yumuşaması, İki nokta |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- MEB Fen Bilimleri 6. Sınıf Ders Kitabı (1. kitap): 3. Ünite “Canlılarda Sistemler” (Maarif Modeli, s. 82–127) ve 4. Ünite “Işığın Yansıması ve Renkler”
- MEB Matematik 6. Sınıf Ders Kitabı 1. Kitap: 3. Tema “Sayılar ve Nicelikler (2)” ve 4. Tema “İstatistiksel Araştırma Süreci”
- MEB Türkçe 6. Sınıf Ders Kitabı 1. Kitap: 3. Tema “Farklı Dünyalar”

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
