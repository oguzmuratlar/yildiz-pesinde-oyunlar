# Dev Ahtapot — Macera Canavarı (Arena 1 · Mercan Resifi)

| Alan | Değer |
|---|---|
| gameId | macera-5-dev-ahtapot |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 5 |
| Kapsam | Fen Ü1–Ü2, Matematik T1–T2, Türkçe T1–T2 |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — her üniteden 2 (Fen 4, Matematik 4, Türkçe 4); 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 120 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Dev Ahtapot resifin 8 ışık incisini kollarına sarmıştır. Her doğru cevap bir kolu çözer ve inci yukarı süzülür. 8 kol çözülünce ahtapot iki mürekkep bulutuyla kalkan açar; 9. ve 10. doğru bulutları dağıtır ve ahtapot yenilir. Kalan sorular “Bonus inci”dir. Yanlışta ahtapot güler ve ekrana mürekkep fışkırtır, doğru cevap ve açıklama gösterilir. Üst sayaçta çözülen kol ve kalan hata hakkı (2) görünür. İpucu ve süre sınırı yoktur.

## Giriş / çıkış
- **Giriş:** Kabarcıklar yükselir, mürekkep patlamasıyla ahtapot alttan çıkar, “DEV AHTAPOT” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa yenilmiş ahtapot, konfeti ve “Dev Ahtapot yenildi!”; kaybedilirse ahtapot mürekkep bırakıp yukarı kaçar. Sonuç kartında 12 cevaplık şerit, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 70 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 21 |
| sort2 | Kartı seç, iki kutudan birine koy | 10 |
| tf | Doğru / Yanlış | 10 |
| match | Sol satıra sağdaki kartı yerleştir | 5 |
| order | Kartlara sırayla dokunarak diz | 4 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü1 Gökyüzündeki Komşularımız ve Biz | 20 | Ay’ın evreleri, Ay’ın özellikleri, Güneş ve Ay, Güneş, Dünya ve Ay modeli, Güneş, Dünya ve Ay’ın büyüklükleri, Güneş, Dünya ve Ay’ın hareketleri, Güneş’in dönme hareketi, Güneş’in yapısı |
| Fen Ü2 Kuvveti Tanıyalım | 20 | Dinamometre, Hava direnci, Kuvvetin birimi, Kuvvetin etkileri, Kütle ve ağırlık, Su direnci, Sürtünme kuvveti |
| Mat T1 Geometrik Şekiller | 20 | Açı çeşitleri, Açılarına göre üçgenler, Açıyı ikiye bölme, Bütünler açılar, Eşkenar üçgen, Kenarlarına göre üçgenler, Komşu açılar, Köşegen, Temel geometrik çizimler, Tümler açılar, İç açılar toplamı |
| Mat T2 Sayılar ve Nicelikler (1) | 20 | Basamak değeri, Eksik terim, Karşılaştırma, Kısa yoldan bölme, Kısa yoldan çarpma, Problem çözme, Sayıları okuma, Sayıları yazma, Tahmin, Yuvarlama |
| Türkçe T1 Oyun Dünyası | 20 | Eş anlam, Eş sesli kelime, Gerçek ve hayal, Kısa çizgi, Nokta, Okuma (metin soruda verilir), Soru işareti, Tahmin işlevli söz varlığı, Zıt anlam, İsim ve fiil |
| Türkçe T2 Atatürk’ü Tanımak | 20 | Atatürk’ün hayatı (bilgi soruda verilir), Bağlantı ifadeleri, Benzetme, Büyük harf, Kişileştirme, Niteleyen ve belirten kelimeler, Soru işareti, Virgül |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- MEB Fen Bilimleri 5. Sınıf Ders Kitabı: 1. Ünite “Gökyüzündeki Komşularımız ve Biz”, 2. Ünite “Kuvveti Tanıyalım”
- MEB Matematik 5. Sınıf Ders Kitabı 1. Kitap: 1. Tema “Geometrik Şekiller”, 2. Tema “Sayılar ve Nicelikler (1)”
- MEB Türkçe 5. Sınıf Ders Kitabı 1. Kitap: 1. Tema “Oyun Dünyası”, 2. Tema “Atatürk’ü Tanımak”

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
