# Taş Dev — Macera Canavarı (Arena 9 · Dağ Yamacı)

| Alan | Değer |
|---|---|
| gameId | macera-7-tas-dev |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 7 |
| Kapsam | Fen Ü1–Ü2, Matematik T1–T3, Türkçe T1–T2 |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — Fen 4 (Ü1+Ü2), Matematik 5 (T1+T2+T3), Türkçe 3 (T1+T2); 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 140 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Taş Dev, dağ yamacında 10 taş zırh plakasıyla korunuyor; plakalar devin çevresinde dizilidir. Her doğru cevap bir plakayı çatlatır: plaka kırılıp aşağı düşer, çakıl taşlarına ayrılır. 5. plakada dev yere vurur, ekran sarsılır (“Taş Dev yere vurdu!”). 10. plakada zırh tamamen düşer ve dev yenilir. Canavar yenildiği anda oyun biter ve sonuç açılır; bonus soru yoktur (değerlendirme 12 soruluk ölçeğe göre: 10 doğru = 3★). 10 doğruya ulaşılamazsa 12 sorunun tamamı oynanır. Yanlışta yukarıdan kayalar yuvarlanır ve gümbürtü duyulur; doğru cevap ve açıklama gösterilir. Üst sayaçta kırılan plaka sayısı ve kalan hata hakkı (2) görünür. İpucu ve süre yoktur.

## Giriş / çıkış
- **Giriş:** Kabarcıklar yükselir, Taş Dev dağ yamacının önünde alttan çıkar, “TAŞ DEV” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa yenilmiş dev, konfeti ve “Taş Dev yenildi!”; kaybedilirse dev yukarı süzülüp dağa çekilir. Sonuç kartında cevaplanan soruların şeridi, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 69 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 27 |
| tf | Doğru / Yanlış | 17 |
| sort2 | Kartı seç, iki kutudan birine koy | 10 |
| match | Sol satıra sağdaki kartı yerleştir | 9 |
| order | Kartlara sırayla dokunarak diz | 8 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü1 Uzay Çağı | 20 | Büyük yıldızların sonu, Evren ve galaksi, Geçmişten gelen ışık, Gözlemevi seçimi, Gözlemevi yeri, Işık yılı, Işık yılı hesabı, Kutup Yıldızı, Takımyıldız, Takımyıldız uzaklıkları, Teknoloji transferi, Teleskop, Türk astronot, Türk uyduları, Türkiye uzay çalışmaları, Uzay teknolojileri, Yıldız mı, Yıldızların rengi, Yıldızın yaşamı |
| Fen Ü2 Kuvvet ve Enerjiyi Keşfedelim | 20 | Dönüşüm zinciri, Düşen top, Enerji türleri, Enerji yok olur mu, Enerjinin korunumu, Esneklik potansiyel enerjisi, Kaldırma işi, Kinetik enerji, Kinetik enerji değişimi, Kütle ve kinetik enerji, Kütle ve potansiyel, Sürtünme, Sürtünmesiz rampa, Yol hesabı, Yükseklik, İş hesabı, İş karşılaştırma, İş var mı, İş yapılması, İşin birimi |
| Mat T1 Sayılar ve Nicelikler (1) | 20 | Asansör problemi, Bölme, Dalgıç problemi, Mutlak değer, Negatif sonuç, Ondalık sıralama, Pozitif ve negatif, Rasyonel sayı, Rasyonel toplama, Sıcaklık problemi, Sıralama, Tam sayı, Toplama, Çarpma, Çıkarma, Üslü ifade, Üslü ifadelerde işaret, İşlem önceliği |
| Mat T2 Geometrik Nicelikler (1) | 20 | Akvaryum, Ayrıt iki katına, Birim dönüşümleri, Hacim sıralama, Küpün açınımı, Küpün hacmi, Küpün yüzey alanı, Litre ve dm³, Litre ve mililitre, Prizmalar, Prizmanın hacmi, Prizmanın yüzey alanı, Prizmanın yüzleri, Su deposu, Sıvı dönüşümü, Yükseklik bulma, cm³ ve dm³, cm³ ve mL, Üstten görünüm, Şişe problemi |
| Mat T3 İstatistiksel Araştırma Süreci | 20 | Araştırma sorusu, Araştırma süreci, Aritmetik ortalama, Açıklık, Eksik veri, Evren, Grafik seçimi, Grafikten ortalama, Güvenilir kaynak, Kesikli ve sürekli, Kişisel veriler, Ortalama mutlak sapma, Ortanca, Tepe değer, Uç değer, Veri türleri, Yayılımı yorumlama, Çizgi grafiği okuma, Ölçüler, Örneklem |
| Türkçe T1 Hayat Boyu Gelişim | 20 | Abartma, Ana düşünce, Bağlamdan anlam, Benzetme, Deyim, Deyim kullanımı, Düğüm bölümü, Kişileştirme, Metin yapısı, Noktalı virgül, Noktalı virgülün yeri, Olay örgüsü, Söz sanatları, Tanık gösterme, Çıkarım, Üç nokta, İkileme yazımı, İkilemeler, İkna paragrafı, İkna paragrafı yapısı |
| Türkçe T2 Bir Hilal Uğruna | 20 | Bağlamdan anlam, Benzetme, Ek çözümleme, Görülen geçmiş zaman, Hâl ekleri, Kişi eki, Kişileştirme, Kıtlık, Metinden bilgi, Otorite, Sevgi tekniği, Tarih sırası, Toplumsal kanıt, Vurgulanan değer, Yönelme eki, Yönelme ve ayrılma, Zaman uyumu, İkna teknikleri, İlgi eki |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- MEB Fen Bilimleri 7. Sınıf Ders Kitabı (1. kitap): 1. Ünite “Uzay Çağı”, 2. Ünite “Kuvvet ve Enerjiyi Keşfedelim”
- MEB Matematik 7. Sınıf Ders Kitabı 1. Kitap: 1. Tema “Sayılar ve Nicelikler (1)”, 2. Tema “Geometrik Nicelikler (1)”, 3. Tema “İstatistiksel Araştırma Süreci”
- MEB Türkçe 7. Sınıf Ders Kitabı 1. Kitap: 1. Tema “Hayat Boyu Gelişim”, 2. Tema “Bir Hilal Uğruna”

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
