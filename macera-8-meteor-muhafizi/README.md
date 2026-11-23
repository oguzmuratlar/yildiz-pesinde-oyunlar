# Meteor Muhafızı — Macera Canavarı (Arena 13 · Atmosferin Sınırı)

| Alan | Değer |
|---|---|
| gameId | macera-8-meteor-muhafizi |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 8 |
| Kapsam | Fen Ü1–Ü2, Matematik Ü1–Ü3, Türkçe sözcükte anlam ve cümlede anlam |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — Fen 4 (Ü1+Ü2), Matematik 4 (Ü1+Ü2+Ü3), Türkçe 4 (sözcükte anlam + cümlede anlam); 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 140 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Meteor Muhafızı dünyanın kavisli ufkunun üstünde, çevresinde yay biçiminde dizilmiş 10 meteorla (kahverengi kaya, beyaz kontur, turuncu kuyruk; hafifçe süzülür) nöbet tutuyor. Her doğru cevap bir meteoru savurur: meteor parlar, kıvılcımlar saçılır, kayan yıldız gibi yukarı fırlayıp söner. 5. meteorda muhafız kalkan ellerini kaldırır ve turuncu parlar (“Muhafız kalkanlarını kaldırdı!”). 10. meteorda muhafız yenilir. Canavar yenildiği anda oyun biter ve sonuç açılır; bonus soru yoktur (değerlendirme 12 soruluk ölçeğe göre: 10 doğru = 3★). 10 doğruya ulaşılamazsa 12 sorunun tamamı oynanır. Yanlışta ekrana meteor yağmuru iner ve sahne sarsılır.

## Giriş / çıkış
- **Giriş:** Yıldızlar parlar, Meteor Muhafızı atmosferin sınırında alttan yükselir, “METEOR MUHAFIZI” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa yenilmiş muhafız (el sallar, başında yıldızlar), konfeti ve “Meteor Muhafızı yenildi!”; kaybedilirse muhafız uzaya süzülür. Sonuç kartında cevaplanan soruların şeridi, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 58 |
| tf | Doğru / Yanlış | 27 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 22 |
| sort2 | Kartı seç, iki kutudan birine koy | 17 |
| match | Sol satıra sağdaki kartı yerleştir | 9 |
| order | Kartlara sırayla dokunarak diz | 7 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü1 Mevsimler ve İklim | 20 | 21 Haziran, Dik ışın, Ekvator ve kutup, En kısa gölge, En uzun gündüz, Enerji sıralaması, Eğiklik olmasaydı, Gece süresi, Gölge boyu, Güney Yarım Küre, Hava durumu ve iklim, Klimatolog ve meteorolog, Kutuplarda yaz, Mevsimlerin nedeni, Uzaklık yanılgısı, Uzayan gölge, Önemli tarihler, İki şehir, İklim, İklim bilimci |
| Fen Ü2 DNA ve Genetik Kod | 20 | Adenin sayısı, Baz eşleşmesi, Biyoteknoloji, Büyüklük sırası, Eşlenme adımları, Eşlenme zamanı, Gen aktarımı ve ıslah, Gen tedavisi, Islah, Karşı zincir, Kelebekler, Kutup tilkisi, Mavi gözlü çocuk, Mendel, Modifikasyon, Mutasyon ve modifikasyon, Nükleotit sayısı, Saf döl ve melez, Saf döl çaprazlama, Çekinik olasılık |
| Mat Ü1 Çarpanlar ve Katlar | 20 | Aralarında asal, Aralarında asal mı, Aralarında asalların EBOB’u, Asal sayı, Asal çarpanlar, Asal çarpanlara ayırma, Bir kişi artıyor, EBOB, EBOB mu EKOK mu, EBOB ve EKOK ilişkisi, EBOB(48, 60), EKOK, EKOK yanılgısı, EKOK’tan sayı bulma, Kare parseller, Kurdeleler, Otobüsler, Çarpan sayısı, Üç zil |
| Mat Ü2 Üslü İfadeler | 20 | 10’un kuvvetleri, Bilimsel gösterim, Bilimsel gösterimleri sırala, Bölme, Işık, Karma işlem, Kuvvet bulma, Kuvvetin kuvveti, Kuvvetleri sırala, Kuvvetlerin çarpımı, Küçük sayının bilimsel gösterimi, Negatif tabanın tek kuvveti, Negatif tabanın çift kuvveti, Negatif üs, Negatif üslerin toplamı, Ondalık karşılık, Sıfırıncı kuvvet, Çözümleme, İki katı, İşaret |
| Mat Ü3 Kareköklü İfadeler | 20 | Bölme, Karekök tahmini, Kareköklerin değeri, Karenin kenarı, Karma işlem, Katsayılı çarpma, Kök içine alma, Ondalık ve kök, Ondalığın karekökü, Rasyonel ve irrasyonel, Sıralama, Tam kare, Tam kare mi, Toplama, Toplamada sadeleştirme, Yakın tam sayı, a√b biçimi, Çarpma, İki kare, İrrasyonel olan |
| Türkçe Sözcükte Anlam, Deyim, Atasözü | 20 | Anlam türleri, Damlaya damlaya, Deyim ve atasözü, Deyimi tamamla, Deyimler, Eş anlamlılar, Eş sesli “yüz”, Genelden özele, Kalbi kırılmak, Kulak asmak, Mecaz anlam, Somut ve soyut, Sütten ağzı yanan, Terim anlam, Uygun atasözü, Yan anlam, Yansıma, Zıt anlam, Zıt anlamlı sözcükler, İkileme |
| Türkçe Cümlede Anlam | 20 | Amaç-sonuç, Anlam ilişkileri, Cümle tamamlama, Cümle yorumlama, Karşılaştırma, Karşılaştırma yok, Koşul, Koşul mu neden mi, Neden mi amaç mı, Neden-sonuç, Nesnel tamamlama, Nesnel yargı, Örtülü anlam, Öznel ve nesnel, Öznel yargı, Şart eki olmadan koşul, “bile”, “bu kez” |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- 8. Sınıf Fen Bilimleri Öğretim Programı: 1. Ünite “Mevsimler ve İklim”, 2. Ünite “DNA ve Genetik Kod”
- 8. Sınıf Matematik Öğretim Programı: 1. Ünite “Çarpanlar ve Katlar”, 2. Ünite “Üslü İfadeler”, 3. Ünite “Kareköklü İfadeler”
- 8. Sınıf Türkçe Öğretim Programı: Söz varlığı (sözcükte ve söz öbeklerinde anlam), anlam bilgisi (cümlede anlam)

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
