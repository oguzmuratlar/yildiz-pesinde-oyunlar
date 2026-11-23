# Şimşek Kuşu — Macera Canavarı (Arena 11 · Bulutlar Diyarı)

| Alan | Değer |
|---|---|
| gameId | macera-7-simsek-kusu |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 7 |
| Kapsam | Fen Ü5–Ü6, Matematik T6–T7, Türkçe T4–T5 |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — Fen 4 (Ü5+Ü6), Matematik 4 (T6+T7), Türkçe 4 (T4+T5); 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 120 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Şimşek Kuşu bulutların üstünde, çevresinde 10 yüklü fırtına bulutuyla bekliyor (koyu mor bulut, beyaz kontur, sarı şimşek). Her doğru cevap bir bulutu boşaltır: bulut parlar, aşağı bir şimşek çakar ve bulut dağılır. 5. bulutta kuş yüklenip parlar, ekranda şimşek çakar (“Şimşek Kuşu çaktı!”). 10. bulutta kuş yenilir. Canavar yenildiği anda oyun biter ve sonuç açılır; bonus soru yoktur (değerlendirme 12 soruluk ölçeğe göre: 10 doğru = 3★). 10 doğruya ulaşılamazsa 12 sorunun tamamı oynanır. Yanlışta ekranda şimşek çakar ve gök gürler; doğru cevap ve açıklama gösterilir. Üst sayaçta boşalan bulut sayısı ve kalan hata hakkı (2) görünür. İpucu ve süre yoktur.

## Giriş / çıkış
- **Giriş:** Kabarcıklar yükselir, Şimşek Kuşu bulutların arasından alttan çıkar, “ŞİMŞEK KUŞU” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa yenilmiş kuş, konfeti ve “Şimşek Kuşu yenildi!”; kaybedilirse kuş yukarı süzülüp bulutlara kaçar. Sonuç kartında cevaplanan soruların şeridi, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 68 |
| tf | Doğru / Yanlış | 16 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 15 |
| sort2 | Kartı seç, iki kutudan birine koy | 9 |
| match | Sol satıra sağdaki kartı yerleştir | 9 |
| order | Kartlara sırayla dokunarak diz | 3 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü5 Maddenin Doğasına Yolculuk | 20 | Atom modelleri, Atom sayısı, Atomun yapısı, Ayırma hunisi, Ayırma sırası, Bilim insanları, Elektron sayısı, Element, Element ve bileşik, Formül, Grup, Karışım türleri, Magnezyum iyonu, Molekül, Periyot, Rutherford, Semboller, Çözelti, Çözünme hızı, İyon |
| Fen Ü6 Elektriklenme | 20 | Aynı yükler, Baca filtresi, Balon deneyi, Dokunma, Elektrik kelimesi, Elektron alışverişi, Etki ile elektriklenme, Etki ile yük dağılımı, Franklin, Paratoner, Paratonerin yapısı, Tarak, Teknolojide elektriklenme, Yer değiştiren yük, Yük etkileşimi, Yük çıkarımı, Yünün yükü, Yıldırım, Çeker mi iter mi, Şimşek |
| Mat T6 Sayılar ve Nicelikler (2) | 20 | Birim fiyat, Birimli oran, Denk oran, Doğru orantı, En ekonomik, Hız problemi, Karışım oranı, Musluk, Oran, Oranla paylaşma, Oranla paylaştırma, Orantı türü, Orantıda bilinmeyen, Paket karşılaştırma, Sadeleştirme, Tablodan orantı, Tarif, Ters orantı |
| Mat T7 Veriden Olasılığa | 20 | Asal sayı, Ayrık olaylar, Ayrık olmayan, Değişen olasılık, Eşit olasılık, Eşit olasılıklı, Kesin olay, Kesin ve imkânsız, Olasılık, Olasılık aralığı, Olayın çıktıları, Tek sayı, Top sayısı, Tümleyen, Tümleyen toplamı, Yüzdeyle tümleyen, Zar olasılıkları, Çark, Çıktı sayısı, Örnek uzay |
| Türkçe T4 Türk Sanatı | 20 | Benzetme, Ebru, El sanatları, Karagöz, Kişileştirme, Kukla, Kök boya, Meddah, Metinden bilgi, Meğerse, Mimar Sinan, Ortaoyunu, Tekerleme, Tiyatro ve müzik, Yay ayraç, Zıtlık, Zıtlık bildirmeyen, Zıtlık ifadeleri, Çalgılar, Örneklendirme |
| Türkçe T5 Okuma Kültürü | 20 | Abartma, Bağlamdan anlam, Benzetme, Durum zarfı, Eleştirel yazma, Köşeli ayraç, Medya okuryazarlığı, Miktar zarfı, Noktalama, Sayıların yazımı, Soru zarfı, Sıra sayısı, Tırnak işareti, Tırnağın işlevi, Yay ayraç, Zaman ve yer-yön, Zaman zarfı, Zarf türleri, Üleştirme sayıları, “En” sözcüğü |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- MEB Fen Bilimleri 7. Sınıf Ders Kitabı (2. kitap): 5. Ünite “Maddenin Doğasına Yolculuk”, 6. Ünite “Elektriklenme”
- MEB Matematik 7. Sınıf Ders Kitabı 2. Kitap: 6. Tema “Sayılar ve Nicelikler (2)”, 7. Tema “Veriden Olasılığa”
- MEB Türkçe 7. Sınıf Ders Kitabı 2. Kitap: 4. Tema “Türk Sanatı”, 5. Tema “Okuma Kültürü”

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
