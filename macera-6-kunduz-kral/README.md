# Kunduz Kral — Macera Canavarı (Arena 7 · Nehir Vadisi)

| Alan | Değer |
|---|---|
| gameId | macera-6-kunduz-kral |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış cevaplarda `answers[].subjectId` = science / math / turkish |
| Sınıf | 6 |
| Kapsam | Fen Ü5–Ü6, Matematik T5–T6, Türkçe T4–T5 |
| Ekran yönü | Dikey |
| Oyun türü | Macera canavarı (bölüm sonu karma tekrar) |
| Soru sayısı | 12 — her ünite/temadan 2 (Fen 4, Matematik 4, Türkçe 4); 4 kolay → 4 orta → 4 zor; art arda aynı ders gelmez |
| Yıldız | 10–12 doğru 3★ (canavar yenilir) · 8–9 2★ · 6–7 1★ · 0–5 0★ |
| Havuz | 120 görev |
| Katalog | “Macera oyunu” işaretli, ders “Karışık” |

## Mekanik
Kunduz Kral nehri 10 kütüklük bir barajla kesmiş; kütükler canavarın önünde 4-3-2-1 piramit biçiminde üst üste durur. Her doğru cevap en üstten başlayarak bir kütüğü çeker: kütük parlayıp savrulur, aradaki boşluktan su fışkırır ve nehir yükselir. 6. kütükte baraj sızdırmaya başlar. 10. kütükte baraj yıkılır ve Kunduz Kral yenilir; kalan sorular “Bonus kütük”tür. Yanlışta kunduz kuyruğunu suya vurur: sahne sarsılır, ekrana su sıçrar; doğru cevap ve açıklama gösterilir. Üst sayaçta çekilen kütük sayısı ve kalan hata hakkı (2) görünür. İpucu ve süre yoktur.

## Giriş / çıkış
- **Giriş:** Kabarcıklar yükselir, Kunduz Kral nehir vadisinde alttan çıkar, “KUNDUZ KRAL” başlığı vurulur. Ekranda yalnızca ad, görsel ve BAŞLA düğmesi bulunur. BAŞLA sonrası “SAVAŞ BAŞLASIN!” perdesi. Oyunun hiçbir yerinde ders, sınıf, ünite, konu ya da zorluk yazmaz (kural 17).
- **Çıkış:** Kazanılırsa yenilmiş kunduz, konfeti ve “Kunduz Kral yenildi!”; kaybedilirse kunduz yukarı süzülüp kaçar. Sonuç kartında 12 cevaplık şerit, yıldızlar ve x/12.

## Görev türleri
| Tür | Mekanik | Adet |
|---|---|---|
| choice | 3 seçenekten birini seç (şekil veya metin olabilir) | 82 |
| num | Rakam kadranlarını ▲▼ ile ayarla | 17 |
| tf | Doğru / Yanlış | 6 |
| sort2 | Kartı seç, iki kutudan birine koy | 6 |
| match | Sol satıra sağdaki kartı yerleştir | 6 |
| order | Kartlara sırayla dokunarak diz | 3 |

Her destede en az 4 farklı tür bulunur; seçmeli görev sayısı sınırlanır. Kesirler ekranda alt alta gösterilir, kayıtta düz metin yazılır (“3/8”, “2 tam 3/4”).

## Soru havuzu
| Ünite/Tema | Adet | Konular |
|---|---|---|
| Fen Ü5 Maddenin Ayırt Edici Özellikleri | 20 | Askıda kalma, Ayırt edici özellikler, Batma ve yüzme, Donma noktası, Erime, Erime noktası, Erime ve donma noktası, Genleşme, Kaynama noktası, Kütle hesabı, Madde tanıma, Maddenin hâli, Suyun donması, Sıvı katmanları, Yoğunluk, Yoğunluk hesabı, Yoğunluk karşılaştırma |
| Fen Ü6 Elektriğin İletimi ve Direnç | 20 | Deney tasarımı, Değişkenler, Direnç, Direnç ve cins, Direnç ve kalınlık, Direnç ve uzunluk, Elektrik güvenliği, Kontrol edilen değişken, Reosta, Reosta kullanımı, Sıvı testi, Sıvıların iletkenliği, Yalıtkan, İletken metal, İletken ve yalıtkan, İletkenlik testi |
| Mat T5 Geometrik Şekiller | 20 | Bütünler açılar, Dörtgenin iç açıları, Dörtgenler, Düzgün çokgen, Dış ters açılar, Köşegenler, Paralelkenar, Yöndeş açılar, Çokgenin dış açıları, Çokgenin iç açıları, Üçgenin dış açısı, Üçgenin iç açıları |
| Mat T6 İşlemlerle Cebirsel Düşünme ve Değişimler | 20 | Akış şeması, Algoritma, Cebirsel ifade, Değişken, Döngü, Katsayı, Problem, Sabit terim, Örüntü, Örüntü kuralı, Örüntüde terim, İfadenin değeri |
| Türkçe T4 İletişim ve Sosyal İlişkiler | 20 | Atasözü, Bağlantı ifadesi, Beden dili, Ben dili, Ben dili ve sen dili, Deyim, Düzeltme işareti, Empati, Geçiş ifadesi, Hikâye yapısı, Kalıp ifade, Kalıp ifadeler, Kişileştirme, Metnin amacı, Ses olayı, Soru işareti, Yazım, Önemli bilgi |
| Türkçe T5 Bilim ve Teknoloji | 20 | Açık anlatım, Benzetme, Biyomimetik, Deyim, Eğik çizgi, Kelime anlamı, Kişileştirme, Kısa çizgi, Kısaltma, Kısaltmalara gelen ekler, Olay sırası, Tanık gösterme, Tanımlama, Uzay teknolojisi, Yapay zekâ, Çıkarım, Önemli bilgi, Özne-yüklem uyumu |

Sorular oyunlarda kullanılanların kopyası değildir; aynı kazanımlara göre yeniden yazılmıştır. Paragraflar özgündür ve soruda verilir.

## Yanlış cevap kaydı
questionId, isCorrect, subjectId, questionText (şekil tarifiyle), studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation (düz metin). Sonuçta `totalQuestions: 12`.

## Kaynak
- MEB Fen Bilimleri 6. Sınıf Ders Kitabı (2. kitap): 5. Ünite “Maddenin Ayırt Edici Özellikleri” (s. 18–59) ve 6. Ünite “Elektriğin İletimi ve Direnç” (s. 69–91)
- MEB Matematik 6. Sınıf Ders Kitabı 2. Kitap: 5. Tema “Geometrik Şekiller” ve 6. Tema “İşlemlerle Cebirsel Düşünme ve Değişimler”
- MEB Türkçe 6. Sınıf Ders Kitabı 2. Kitap: 4. Tema “İletişim ve Sosyal İlişkiler” ve 5. Tema “Bilim ve Teknoloji”

Her görevin sayfa bilgisi questions.json içindeki `sourceRef` alanındadır.

## Teknik
- Bridge 1.0, `window.YildizPesindeGame.receiveMessage`; init doğrulaması gameId, gameVersion ve grade ile.
- En düşük: iOS 15.4 WebView, Android WebView 98. CSP; dış kaynak ve ağ isteği yok. Canavar ve arka plan görselleri `macera-gorselleri/` klasöründen küçültülüp data URI olarak gömülü.
- Köprü yoksa deneme modu (kayıt yok). Hareket azaltma desteklenir; Web Audio ses kapatma düğmesi vardır.
- Ortak canavar motoru (Dev Ahtapot ile aynı); bu canavara özgü olanlar: soru havuzu, görseller, ayarlar ve imza mekaniği modülü.
