# Akıl Kafe · Sözel Mantık ve Görsel Okuma

| Alan | Değer |
|---|---|
| gameId | turkce-8-akil-kafe |
| Güncel sürüm | 1.0.0 |
| Ders | Türkçe (oyun içi subjectId: turkish; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Konu | Sözel mantık (sıralama, masa yerleşimi, eşleştirme tablosu, takvim yerleştirme), kesin ve olası çıkarımlar, görsel okuma (menü, afiş, sütun grafiği) |
| Ekran yönü | Dikey |
| Oyun türü | Bulmaca kafesi, karaktersiz. İpuçları her görevde tebeşir panoda yazar (ipucuna dokunarak üstü çizilebilir). Görevler: kasa sırasını yer değiştirerek dizme, dört arkadaşı kare masaya oturtma, sipariş tablosunda ✔/✘ işaretleme, etkinlik kartlarını haftalık panoya asma, yargılara fincan mührü basma (kesin doğru / kesin yanlış / kesin değil), menüden isteğe uyan içeceği tepsiye koyma, afişte gerekçe satırını fosforlu kalemle işaretleme, satış grafiğinde sütun seçme, yargı kartlarını raflara dizme. Şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "Bahşiş sorusu" (iki seçenekli kısa akıl sorusu). Doğruysa +30 🪙 ve fincan rafında kalpli fincan ♥. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🪙 puanı yıldızı etkilemez) |
| Soru havuzu | 100 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Tuğla duvarlı kafe, sönük neon tabela, boş tebeşir pano, tezgâhta fincanlar; altta yalnızca "KAFEYE GİR" düğmesi.
- **Giriş:** Kapı zili çalar, "AKIL KAFE" neonu cızırdayarak yanar, fincanlardan buhar yükselir, tebeşir panoya "Bugünün bulmacası: Kim, nerede, ne zaman? Afiyetle düşün!" yazılır; parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 fincanlık raf; doğru görevde dolu ve buharlı fincan (bonus doğruysa kalpli ♥), yanlışta devrilmiş fincan ✕.
- **Çıkış:** Adisyon yazarkasadan satır satır çıkar (10 bulmaca ✔/✕ ve toplam), "ADİSYON KARNESİ x/10 BULMACA" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| queue | Kasa sırası | İki müşteriye sırayla dokunularak yerleri değiştirilir; sıra ipuçlarına göre kurulur |
| seat | Kare masa | Arkadaş seçilip koltuğa (pencere, tezgâh, kapı, kitaplık) oturtulur; karşılıklı / yan yana ipuçları |
| grid | Sipariş tablosu | Kişi × içecek tablosunda kareler ✔ / ✘ / boş arasında değiştirilir |
| week | Haftalık pano | Etkinlik kartları günlere asılır; “bir gün önce, daha sonra, arasında bir gün” ipuçları |
| verdict | Fincan mühürleri | Kısmi bilgilere göre her yargıya “Kesin doğru / Kesin yanlış / Kesin değil” mührü basılır |
| menu | Sipariş tepsisi | Müşterinin koşullarına (sıcak/soğuk, sütlü, meyveli, fiyat, en ucuz/en pahalı) uyan tek içecek tepsiye konur |
| sign | Afiş | Duruma gerekçe olan afiş satırı fosforlu kalemle işaretlenir |
| chart | Satış panosu | Sütun grafiğinde betimlenen içeceğin sütununa dokunulur |
| bin | Raflar | Kısmi bilgilere göre yargı kartları “kesin doğru / kesin yanlış / kesin değil” raflarına dizilir |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| sira | 20 | Kasa sırası (4–5 kişi), kare masa yerleşimi, sıralama çıkarımları |
| tablo | 20 | Kişi–içecek eşleştirme tabloları (3×3, 4×4; “ya … ya da”, sıcak/soğuk ipuçları), eşleştirme çıkarımları |
| cikarim | 20 | Sıralama, eşleştirme ve takvim durumlarından kesin / olası çıkarımlar |
| gorsel | 20 | Menü okuma, afiş/duyuru okuma, sütun grafiği okuma |
| takvim | 20 | 4–5 günlük haftalık etkinlik yerleştirme ve çıkarımları |

Görev türlerinin dağılımı: verdict 20, bin 19, grid 12, week 12, queue 10, menu 7, seat 7, sign 7, chart 6.

Bütün bulmacalar program tarafından üretilmiş ve tek çözümlü olduğu bütün olasılıklar denenerek doğrulanmıştır. “Kesin doğru / kesin yanlış / kesin değil” sınıflandırmaları da bilgilerle uyumlu bütün durumlar taranarak hesaplanmıştır. Oyuncunun yerleştirmesi bu tek çözümle karşılaştırılır.

Yanlış-cevap kaydı:
- questionText görevi, bütün ipuçlarını ve düzeneği (kişiler, içecekler, günler, menü satırları, afiş satırları, grafik değerleri) metin olarak içerir.
- studentAnswer öğrencinin kurduğu sırayı, oturma düzenini, tablo işaretlerini, pano yerleşimini, mühürleri, seçtiği ürünü, satırı ya da sütunu yazar.
- correctAnswer tek doğru çözümü yazar.
- sourceRef: 8. Sınıf Öğretim Programı, Okuma: Akıl yürütme, çıkarım yapma; görsel ve grafik okuma.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).
- Küçük ekranlarda (320×568) ipucu panosu kendi içinde kaydırılabilir.

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
