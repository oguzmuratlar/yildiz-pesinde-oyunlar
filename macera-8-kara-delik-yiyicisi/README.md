# Kara Delik Yiyicisi — Macera Canavarı (Arena 16 · Yıldızlar)

| Alan | Değer |
|---|---|
| gameId | macera-8-kara-delik-yiyicisi |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 8 |
| Kapsam | Fen Ü7, Matematik Ü10–Ü12, Türkçe Söz sanatları ve metin türleri, Sözel mantık ve görsel okuma |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — Fen 4 (Ü7), Matematik 4 (Ü10+Ü11+Ü12), Türkçe 4 (iki ünite); 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 120 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Kara Delik Yiyicisi yıldızların arasında, karnındaki galaksi girdabıyla çevresindeki 10 altın yıldızı (koyu konturlu, gülümseyen, parıldayan) yutmaya çalışıyor. Her doğru cevap bir yıldızı kurtarır: yıldız parlar, ışıltılar saçar, dönerek gökyüzüne yükselir; yiyici yutkunur. 5. yıldızda yiyici çekimini artırır, mor parlar ve sahne merkeze doğru esner (“Kara Delik çekimini artırdı!”). 10. yıldızda yiyici yenilir; kalan sorular “Bonus yıldız”dır. Yanlışta mor girdap sahnenin ortasında dönerek küçülür, sahne içe çekilir.

## Giriş / çıkış
- **Giriş:** Yıldızlar parlar, Kara Delik Yiyicisi alttan yükselir, “KARA DELİK YİYİCİSİ” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa yenilmiş yiyici, konfeti ve “Kara Delik Yiyicisi yenildi!” ile 8. sınıf macerasının tamamlandığı notu; kaybedilirse yiyici karanlığa süzülür. Sonuç kartında 12 cevaplık şerit, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 57 |
| tf | Doğru / Yanlış | 24 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 19 |
| sort2 | Kartı seç, iki kutudan birine koy | 15 |
| match | Sol satıra sağdaki kartı yerleştir | 5 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü7 Elektrik Yükleri ve Elektrik Enerjisi | 20 | Aktarılan tanecik, Aylık tüketim, Aynı cins yükler, Elektriklenme, Elektrikli süpürge, Elektroskop, Elektroskop yaprakları, Enerji dönüşümü, Enerji etiketi, Enerji tüketimi, Fatura, Güneş paneli, Nötr kâğıt, Paratoner, Santraller, Tasarruf, Termik santral, Topraklama, Yenilenebilir kaynak, Çekme ve itme |
| Mat Ü10 Eşlik ve Benzerlik | 20 | 2 × 3’e benzer, Açı bulma, Açılar, Benzer dikdörtgen, Benzer kareler, Benzer ve eş, En uzun kenar, Eş ve benzer, Eşkenar üçgenler, Fotoğraf, Gölge, Harita ölçeği, Her zaman benzer mi, Her zaman doğru, Karşılık gelen kenar, Kenar oranı, Plan ölçeği, Tanımlar, Çevre, Şehirler arası |
| Mat Ü11 Dönüşüm Geometrisi | 20 | Apsis, Ardışık dönüşüm, Aynı sonuç, Bilinmeyen apsis, Değişmeyen nokta, Hangi dönüşüm, Kurallar, Ordinat, Sağa öteleme, Sıra fark eder mi, Yansıma ve eşlik, Yansıma ve öteleme, x eksenine yansıma, y eksenine yansıma, Öteleme, Ötelemeyi bul, Üçgeni ötele, İki yansıma, İki yönde öteleme |
| Mat Ü12 Geometrik Cisimler | 20 | Dikdörtgenin kenarı, Hacim, Hacim değişimi, Koni, Koni açınımı, Köşe sayıları, Küp, Küpün yüzey alanı, Küpün yüzleri, Piramidin yan yüzleri, Prizma hacmi, Silindir açınımı, Silindir hacmi, Silindirin elemanları, Taban alanı, Yanal alan, Yükseklik, Yüzey alanı, Yüzeyler, Üçgen prizma |
| Türkçe Söz Sanatları ve Metin Türleri | 20 | Abartma ve karşıtlık, Anlatıcı, Anı, Benzetilen, Benzetme, Benzetme edatı, Benzetme yönü, Fabl, Güçlü benzetme, Hikâye unsurları, Kişileştirme, Konuşturma, Makale ve deneme, Masal, Metin türleri, Otobiyografi, Roman, Tiyatro, Utangaç güneş, Öyküleyici mi bilgilendirici mi |
| Türkçe Sözel Mantık ve Görsel Okuma | 20 | Afiş, Bazı kuşlar, Bazı öğrenciler, Beş kişilik sıra, Dört etkinlik, Dört kişilik sıra, Grafik, Günler, Kafede içecekler, Kesin çıkarım, Kim çay içti, Menü, Sondan kaçıncı, Spor dalları, Ters çıkarım, Çizgi grafiği, Üç gün, Üç kişilik sıra, İçecekler, Şapkalar |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- 8. Sınıf Fen Bilimleri Öğretim Programı: 7. Ünite “Elektrik Yükleri ve Elektrik Enerjisi”
- 8. Sınıf Matematik Öğretim Programı: 10. Ünite “Eşlik ve Benzerlik”, 11. Ünite “Dönüşüm Geometrisi”, 12. Ünite “Geometrik Cisimler” (π = 3)
- 8. Sınıf Türkçe Öğretim Programı: söz sanatları ve metin türleri; sözel mantık ve görsel okuma

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
