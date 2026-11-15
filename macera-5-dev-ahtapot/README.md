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
| Soru sayısı | 12 (her üniteden 2; 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez) |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 48 görev (ünite başına 8) |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Dev Ahtapot resifin 8 ışık incisini kollarına sarmıştır. Her doğru cevap bir kolu çözer ve inci yukarı süzülür. 8 kol çözülünce ahtapot iki mürekkep bulutuyla kalkan açar; 9. ve 10. doğru bulutları dağıtır ve ahtapot yenilir. Kalan sorular “Bonus inci”dir. Yanlışta ahtapot güler ve ekrana mürekkep fışkırtır, doğru cevap ve açıklama gösterilir. Üst sayaçta çözülen kol ve kalan hata hakkı (2) görünür. İpucu ve süre sınırı yoktur.

## Giriş / çıkış
- **Giriş:** Kabarcıklar yükselir, mürekkep patlamasıyla ahtapot alttan çıkar, “DEV AHTAPOT” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17). BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi gelir.
- **Çıkış:** Kazanılırsa yenilmiş ahtapot, konfeti ve “Dev Ahtapot yenildi!” gösterilir. Kaybedilirse ahtapot mürekkep bırakıp yukarı kaçar. Her iki durumda 12 incilik sonuç şeridi, yıldızlar ve x/12 görünür.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 27 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 9 |
| sort2 | Kartı seç, iki kutudan birine koy | 6 |
| match | Sol satıra sağdaki kartı yerleştir | 3 |
| order | Kartlara sırayla dokunarak diz | 2 |
| tf | Doğru / Yanlış | 1 |

Her destede en az 4 farklı tür bulunur ve seçmeli görev sayısı sınırlanır.

## Soru havuzu
| Ünite | Adet | Konular |
|---|---|---|
| Fen Ü1 Gökyüzündeki Komşularımız ve Biz | 8 | Ay’ın evreleri, Ay’ın özellikleri, Güneş ve Ay, Güneş, Dünya ve Ay’ın hareketleri, Güneş’in dönme hareketi, Güneş’in yapısı |
| Fen Ü2 Kuvveti Tanıyalım | 8 | Dinamometre, Hava direnci, Kuvvetin birimi, Kuvvetin etkileri, Kütle ve ağırlık, Su direnci, Sürtünme kuvveti |
| Mat T1 Geometrik Şekiller | 8 | Açı çeşitleri, Kenarlarına göre üçgenler, Komşu açılar, Köşegen, Temel geometrik çizimler, Tümler açılar, İç açılar toplamı |
| Mat T2 Sayılar ve Nicelikler (1) | 8 | Basamak değeri, Eksik terim, Karşılaştırma, Kısa yoldan çarpma, Problem çözme, Sayıları okuma, Sayıları yazma, Yuvarlama |
| Türkçe T1 Oyun Dünyası | 8 | Eş sesli kelime, Gerçek ve hayal, Kısa çizgi, Nokta, Okuma (metin soruda verilir), Tahmin işlevli söz varlığı, Zıt anlam, İsim ve fiil |
| Türkçe T2 Atatürk’ü Tanımak | 8 | Atatürk’ün hayatı (bilgi soruda verilir), Bağlantı ifadeleri, Benzetme, Büyük harf, Kişileştirme, Niteleyen ve belirten kelimeler, Soru işareti, Virgül |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraf ve bilgi metinleri özgündür ve soruda verilir.

## Yanlış cevap kaydı
Şu alanlar düz metin olarak yazılır: questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation. Sonuçta `totalQuestions: 12` bulunur.

## Kaynak
- MEB Fen Bilimleri 5. Sınıf Ders Kitabı 1. Kitap: 1. Ünite (s. 22–47) ve 2. Ünite “Kuvveti Tanıyalım”
- MEB Matematik 5. Sınıf Ders Kitabı 1. Kitap: 1. ve 2. Tema
- MEB Türkçe 5. Sınıf Ders Kitabı 1. Kitap: 1. ve 2. Tema

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0: `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade 5 ile yapılır.
- En düşük sürümler: iOS 15.4 WebView, Android WebView 98.
- CSP uygulanır; dış kaynak ve ağ isteği yoktur. Canavar ve arka plan görselleri `macera-gorselleri/a01`'den küçültülüp data URI olarak gömülüdür (~235 KB tek dosya).
- Köprü yoksa deneme modunda çalışır ve kayıt yapmaz. Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru: Arena 2–12 aynı motoru kendi ayarları, soru havuzu ve görselleriyle kullanır.
