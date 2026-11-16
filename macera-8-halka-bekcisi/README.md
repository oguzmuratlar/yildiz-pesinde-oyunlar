# Halka Bekçisi — Macera Canavarı (Arena 15 · Gezegenler)

| Alan | Değer |
|---|---|
| gameId | macera-8-halka-bekcisi |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 8 |
| Kapsam | Fen Ü5–Ü6, Matematik Ü7–Ü9, Türkçe Fiilimsiler, Cümlenin ögeleri, Cümle türleri ve yazım-noktalama |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — Fen 4 (Ü5+Ü6), Matematik 4 (Ü7+Ü8+Ü9), Türkçe 4 (üç ünite); 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 160 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Halka Bekçisi gezegenlerin arasında, çevresindeki kesikli yörüngede dizilmiş 10 renkli uyduyla (açık renkli küre, koyu mor kontur, hafifçe süzülür) halkasını döndürüyor. Her doğru cevap bir uyduyu yörüngeden fırlatır: uydu parlar, yıldız tozu saçar, dönerek uzaya fırlayıp küçülür. 5. uyduda bekçi halkayı hızlandırıp sallanır ve sarı parlar (“Halka Bekçisi halkayı hızlandırdı!”). 10. uyduda bekçi yenilir; kalan sorular “Bonus uydu”dur. Yanlışta dev sarı halka sahnenin üstünden kamçı gibi geçer, sahne sarsılır.

## Giriş / çıkış
- **Giriş:** Yıldızlar parlar, Halka Bekçisi gezegenlerin arasında alttan yükselir, “HALKA BEKÇİSİ” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa yenilmiş bekçi (el sallar, başında yıldızlar), konfeti ve “Halka Bekçisi yenildi!”; kaybedilirse bekçi halkasıyla uzaklaşır. Sonuç kartında 12 cevaplık şerit, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 75 |
| tf | Doğru / Yanlış | 28 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 27 |
| sort2 | Kartı seç, iki kutudan birine koy | 19 |
| match | Sol satıra sağdaki kartı yerleştir | 8 |
| order | Kartlara sırayla dokunarak diz | 3 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü5 Basit Makineler | 20 | Bileşik makine, Dişli turları, Dişliler, El arabası, Eğik düzlem, Günlük yaşam, Hareketli makara, Kaldıraç dengesi, Kaldıraç türleri, Kazanç, Kuvvet kolu, Kuvvet ve yol, Makaralar, Palanga, Sabit makara, Vida, Vida adımı, Yük kolu, Çıkrık, İş kolaylığı |
| Fen Ü6 Enerji Dönüşümleri ve Çevre Bilimi | 20 | Azot döngüsü, Besin zinciri, Biyolojik birikim, Deney değişkeni, Ekolojik ayak izi, Enerji akışı, Fotosentez denklemi, Fotosentez hızı, Fotosentez ve solunum, Fotosentezin ürünleri, Karbon döngüsü, Karbondioksit, Küresel ısınma, Nerede gerçekleşir, Oksijensiz solunum, Solunum, Solunum türleri, Su döngüsü, Sürdürülebilirlik, Zincirden çıkarma |
| Mat Ü7 Doğrusal Denklemler | 20 | Bölgeler, Bölme, Denklem, Değer bulma, Değişim oranı, Doğrusal mı, Eksen üzerinde, Eğim, Eğim okuma, Eğimin işareti, Hangi eksen, Kesirli denklem, Mum, Parantezli denklem, Tablodan denklem, Taksi hesabı, Taksi ücreti, x eksenini kesme, y eksenini kesme, İki noktadan eğim |
| Mat Ü8 Eşitsizlikler | 20 | Aralık, Asansör, Defterler, En az, en fazla, En büyük tam sayı, Fatura, Gösterimler, Kamyon, Negatifle bölme, Sayı doğrusu, Sağlar mı, Tam sayılar, Yaş sınırı, Yön değişimi, x > −2, Çift eşitsizlik, Çözüm, İki koşul, İki tarafta bilinmeyen |
| Mat Ü9 Üçgenler | 20 | Dik kenar, Dik üçgen mi, Ekran köşegeni, En büyük açı, En kısa kenar, Hipotenüs, Kareköklü hipotenüs, Kaç değer, Kenar-açı, Kenarları sırala, Kenarortay, Kuş uçuşu, Merdiven, Pisagor, Yardımcı elemanlar, Yükseklik, Üçgen eşitsizliği, Üçgen olur mu, Üçüncü kenar, İkizkenar |
| Türkçe Fiilimsiler | 20 | -arak, Adlaşma, Durum bildiren, Ekler, Fiilimsi nedir, Fiilimsi sayısı, Fiilimsi var mı, Kalıcı isim, Sıfat-fiil, Sıfat-fiil bul, Sıfat-fiil ve zarf-fiil, Tür belirleme, Zaman bildiren, Zarf-fiil, Özne olan isim-fiil, Üç tür bir arada, İki fiilimsi, İsim-fiil, İsim-fiil bul, İsim-fiil ve sıfat-fiil |
| Türkçe Cümlenin Ögeleri (fiilde çatı hariç) | 20 | Belirtisiz nesne, Dolaylı tümleç, Durum bildiren, Gizli ve açık özne, Gizli özne, Gizli özne bulma, Neden, Nesne, Nesne türü, Nesnesiz cümle, Soru ve öge, Tümleçler, Yüklem, Zarf tümleci, Öbek hâlinde özne, Öge sayısı, Özne, İsim cümlesi, İsim soylu yüklem |
| Türkçe Cümle Türleri ve Yazım-Noktalama | 20 | -ki eki, Bağlaç de, Birleşik cümle, Bitişik ve ayrı, Biçim ve anlam, Büyük harf, Devrik cümle, Kesme işareti, Kesme yanlışı, Kurallı cümle, Kurallı ve devrik, Kısaltmaya ek, Noktalama, Noktalı virgül, Olumlu ve olumsuz, Saat yazımı, Soru işareti, Sıralı cümle, Virgül ve ve, Yazım yanlışı |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- 8. Sınıf Fen Bilimleri Öğretim Programı: 5. Ünite “Basit Makineler”, 6. Ünite “Enerji Dönüşümleri ve Çevre Bilimi”
- 8. Sınıf Matematik Öğretim Programı: 7. Ünite “Doğrusal Denklemler”, 8. Ünite “Eşitsizlikler”, 9. Ünite “Üçgenler”
- 8. Sınıf Türkçe Öğretim Programı: Fiilimsiler; cümlenin ögeleri (fiilde çatı arenadaki oyunlarda işlenmediği için sorulmadı); cümle türleri, yazım kuralları ve noktalama işaretleri

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
