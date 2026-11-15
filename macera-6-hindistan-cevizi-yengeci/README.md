# Hindistan Cevizi Yengeci — Macera Canavarı (Arena 5 · Tropik Ada)

| Alan | Değer |
|---|---|
| gameId | macera-6-hindistan-cevizi-yengeci |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 6 |
| Kapsam | Fen Ü1, Matematik T1–T2, Türkçe T1–T2 (Fen Ü2 Kuvvetin Etkisinde Hareket oyunu henüz olmadığı için kullanıcı kararıyla dışarıda bırakıldı) |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — Fen 4 (Ü1), Matematik 4 (2 + 2), Türkçe 4 (2 + 2); 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 100 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Hindistan Cevizi Yengeci adanın 10 hindistan cevizini kıskaçlarında tutuyor; cevizler yengecin çevresinde dizilidir. Her doğru cevap bir cevizi düşürür: ceviz parlar, yere düşüp seker ve yuvarlanarak gider. 5. cevizde yengeç öfkelenir ve kızıl parlar. 10. cevizde yengeç yenilir; kalan sorular “Bonus ceviz”dir. Yanlışta yengeç ekrana ceviz fırlatır, “bonk” sesiyle ceviz sütü sıçrar; doğru cevap ve açıklama gösterilir. Üst sayaçta düşen ceviz sayısı ve kalan hata hakkı (2) görünür. İpucu ve süre yoktur.

## Giriş / çıkış
- **Giriş:** Kabarcıklar yükselir, yengeç tropik kumsalda alttan çıkar, “HİNDİSTAN CEVİZİ YENGECİ” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa sersemlemiş yengeç, konfeti ve “Hindistan Cevizi Yengeci yenildi!”; kaybedilirse yengeç yukarı süzülerek kaçar. Sonuç kartında 12 cevaplık şerit, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 67 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 13 |
| sort2 | Kartı seç, iki kutudan birine koy | 7 |
| tf | Doğru / Yanlış | 6 |
| order | Kartlara sırayla dokunarak diz | 4 |
| match | Sol satıra sağdaki kartı yerleştir | 3 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü1 Güneş Sistemi ve Tutulmalar | 20 | Asteroit kuşağı, Ay tutulması, Gazsal gezegenlerin hacmi, Gezegen bulmaca, Gök taşları, Gözlem alanı, Güneş tutulması, Güneş’e yakınlık, Güvenli gözlem, Hacim, Halkalar, Hizalanma, Karasal ve gazsal, Meteorit çukuru, Tutulmaların karşılaştırılması, Uydular |
| Mat T1 Sayılar ve Nicelikler (1) | 20 | 10 ile bölünebilme, 4 ile bölünebilme, 6 ile bölünebilme, 9 ile bölünebilme, Aralarında asal, Asal sayılar, Asal çarpanlar, Bölenler, Eksik rakam, Katlar, Ortak bölen, Ortak kat, Çarpanlar |
| Mat T2 Veriden Olasılığa | 20 | Deney, Deney sayısı, Deney ve çıktı, Deneysel olasılık, Eksik değer, Göreli sıklık, Karşılaştırma, Nokta grafiği, Olay, Sıklık tablosu, Yüzde, Yüzde olarak olasılık, Çıktı sayısı, Çıktılar |
| Türkçe T1 Dilimizin Zenginliği | 20 | -da/-de eki, Ana fikir, Atasözleri, Atasözü, Açıklayıcı metin, Deyimler, Halk edebiyatı, Kalıp sözler, Söz varlığı, Türkçe karşılık, Virgül, Yüzey anlam, da/de bağlacı, ki, mi eki, mi soru eki, İkileme, Şiir bilgisi |
| Türkçe T2 Bağımsızlık Yolu | 20 | Abartma, Benzetme, Ek sırası, Hikâye unsurları, Karşılaştırma, Karşıtlık, Kelime anlamı, Kesme işareti, Kişileştirme, Kök, Millî bayramlar, Olay örgüsü, Yapım eki, Yapım ve çekim eki, Çekim eki, Özetleme |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- MEB Fen Bilimleri 6. Sınıf Ders Kitabı (1. kitap): 1. Ünite “Güneş Sistemi ve Tutulmalar” (s. 20–40)
- MEB Matematik 6. Sınıf Ders Kitabı 1. Kitap: 1. Tema “Sayılar ve Nicelikler (1)” ve 2. Tema “Veriden Olasılığa”
- MEB Türkçe 6. Sınıf Ders Kitabı 1. Kitap: 1. Tema “Dilimizin Zenginliği” ve 2. Tema “Bağımsızlık Yolu”

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
