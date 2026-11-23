# Kar Yetisi — Macera Canavarı (Arena 10 · Karlı Zirve)

| Alan | Değer |
|---|---|
| gameId | macera-7-kar-yetisi |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 7 |
| Kapsam | Fen Ü3–Ü4, Matematik T4–T5, Türkçe T3 |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — Fen 5 (Ü3+Ü4), Matematik 4 (T4+T5), Türkçe 3 (T3); 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 100 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Kar Yetisi karlı zirvede çevresine 10 kartopu dizmiş; kartopları hafifçe sallanır. Her doğru cevap bir kartopunu patlatır: kartopu şişip kar tanelerine dağılır, yerinde küçük bir su birikintisi kalır. 5. kartopunda yeti kükrer, ekrana tipi çöker (“Kar Yetisi kükredi!”). 10. kartopunda yeti yenilir. Canavar yenildiği anda oyun biter ve sonuç açılır; bonus soru yoktur (değerlendirme 12 soruluk ölçeğe göre: 10 doğru = 3★). 10 doğruya ulaşılamazsa 12 sorunun tamamı oynanır. Yanlışta ekranı tipi süpürür, kenarlar buz tutar; doğru cevap ve açıklama gösterilir. Üst sayaçta patlayan kartopu sayısı ve kalan hata hakkı (2) görünür. İpucu ve süre yoktur.

## Giriş / çıkış
- **Giriş:** Kabarcıklar yükselir, Kar Yetisi karlı zirvenin önünde alttan çıkar, “KAR YETİSİ” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa yenilmiş yeti, konfeti ve “Kar Yetisi yenildi!”; kaybedilirse yeti yukarı süzülüp tipiye karışır. Sonuç kartında cevaplanan soruların şeridi, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 55 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 15 |
| tf | Doğru / Yanlış | 12 |
| match | Sol satıra sağdaki kartı yerleştir | 9 |
| sort2 | Kartı seç, iki kutudan birine koy | 6 |
| order | Kartlara sırayla dokunarak diz | 3 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü3 Vücudumuzdaki Sistemler | 20 | Akciğer atardamarı, Alveol, Besinin yolu, Boşaltım organları, Böbrekler, Büyük kan dolaşımı, Damarlar, Kan bağışı, Kan bağışı sıklığı, Kanın yapısı, Küçük kan dolaşımı, Organ bağışı, Proteinlerin sindirimi, Safra, Sindirim sağlığı, Sindirimin başladığı yer, Soluk alma, Solunum organları, Terleme ve idrar, Yemek borusu |
| Fen Ü4 Işığın Kırılması ve Mercekler | 20 | Dalgıcın gördüğü, Dik gelen ışık, Gelme açısı, Gökkuşağı, Görünür konum, Havadan suya, Kalın kenarlı mercek, Kapı dürbünü, Kırılan ışın, Kırılma, Kırılma açısı, Kırılma kuralları, Mercek kavramları, Mercek kullanımı, Paralel ışınlar, Prizma, Renk sırası, Su dolu şişe, Sudan havaya, İnce kenarlı mercek |
| Mat T4 Dönüşüm | 20 | Açıortay, Dikdörtgenin köşegeni, Düzgün altıgen, Eşkenar dörtgen, Eşkenar üçgen, Görüntüyü birleştiren, Harflerde simetri, Karenin simetrisi, Kendisine yansıyan nokta, Nokta ile görüntüsü, Orta dikme, Orta dikme inşası, Orta dikme üzerindeki nokta, Simetri sayısı, Simetrik harfler, Yansımada boyut, Yansımada uzaklık, İkizkenar dik üçgen, İnşalar |
| Mat T5 Geometrik Şekiller | 20 | Açıortay, Açıortay ile yükseklik arası, Açıortay ve iç açı, Ağırlık merkezi, Ağırlık merkezinin yeri, Dik üçgende orta dikmeler, En kısa yardımcı eleman, Eşkenar üçgen, Geniş açılı üçgende yükseklik, Kenar orta dikmeler, Kenarortay, Köşeden geçer mi, Yardımcı elemanlar, Yükseklik, Yükseklik ve açı, Çevre ve kenarortay, İkizkenar üçgen, İkizkenar üçgende yükseklik |
| Türkçe T3 İletişim ve Sosyal İlişkiler | 20 | Atasözü, Beden dili, Empati, Eğik çizgi, Geniş zaman, Gerçekleşme zamanı, Kısa çizgi, Metinden bilgi, Mizah ve zorbalık, Nezaket, Otorite, Pekiştirme, Pekiştirme yazımı, Sanal zorbalık, Yazım yanlışı, Zaman ekleri, Ünlem işareti, İletişim kavramı, “Hayırdır”, “Hayır” ile kurulan sözler |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- MEB Fen Bilimleri 7. Sınıf Ders Kitabı: 3. Ünite “Vücudumuzdaki Sistemler” (1. kitap, s. 90–137), 4. Ünite “Işığın Kırılması ve Mercekler” (2. kitap)
- MEB Matematik 7. Sınıf Ders Kitabı: 4. Tema “Dönüşüm” (1. kitap), 5. Tema “Geometrik Şekiller” (2. kitap)
- MEB Türkçe 7. Sınıf Ders Kitabı 1. Kitap: 3. Tema “İletişim ve Sosyal İlişkiler”

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
