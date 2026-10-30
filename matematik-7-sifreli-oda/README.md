# Şifreli Oda · Veriden Olasılığa

| Alan | Değer |
|---|---|
| gameId | matematik-7-sifreli-oda |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Tema | 7. Tema: Veriden Olasılığa |
| Ekran yönü | Dikey |
| Oyun türü | Kaçış odası (karakter yok). Kasanın 10 haneli şifresi her oyunda rastgele üretilir; her bulmaca bir haneyi açar (doğruda altın rakam, yanlışta not kâğıdı haneyi gösterir ve gri kesikli yazılır). 10 kilit bitince kasa çarkı döner, kapı açılır. Test ve doğru/yanlış sorusu yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 105 görev (30 olasılık çubuğu, 24 çıktılara dokun, 16 şalterler, 12 halkalara yerleştir, 12 sepetten çıkar, 11 kilit çarkları), index.html içine gömülüdür |

## Görevler

- **Çıktılara dokun:** Emanet dolapları (1–20), sayı küpü yüzleri, forma numaraları, harf kartları, asansör katları, kurs listesi, kan grupları, numaralı toplar arasında bir olayın (ya da tümleyeninin, iki olayın ortak çıktılarının) bütün çıktılarına dokunulur.
- **Olasılık çubuğu:** İmkânsız (0) – Kesin (1) çubuğunda ibre sürüklenir ya da ◀ ▶ ile ayarlanır; değer kesir, ondalık ve yüzde olarak canlı gösterilir. Torba, kart, fidan, hediye, çark sahneleri ekranda çizilir.
- **Sepetten çıkar:** Meyve, top, kalem ve şekerlere dokunarak en az sayıda nesne çıkarılır; eşit olasılık ya da verilen olasılık (tümleyen dahil) sağlanır. Her türün yanında güncel olasılığı yazar.
- **Halkalara yerleştir:** Çıktı etiketleri A ve B olay halkalarına (yalnız A, ortak, yalnız B, dışarıda) sürüklenir; ortak bölgeden olayların ayrık olup olmadığı anlaşılır.
- **Şalterler:** Her satırda şalter iki yönden birine çevrilir: ayrık / ayrık değil, eşit olasılıklı / değil, tümleyen / değil, deney / olay, örnek uzay / olay, çıktı / olay, olasılık değeri olabilir / olamaz.
- **Kilit çarkları:** ▲ ▼ ile çevrilen çarklarda olasılığın kesir, ondalık ve yüzde gösterimleri kurulur.

Yanlış-cevap kaydında öğrencinin seçtiği çıktılar, gösterdiği olasılık, çıkardığı nesneler, etiket yerleşimleri, şalter konumları ya da çark değerleri ile doğru cevap yazılır; sahneler kayda metin olarak eklenir.

## Soru havuzu

| Grup | İçerik |
|---|---|
| uzay | Deney, çıktı, örnek uzay, olay; olayın çıktılarını belirleme |
| teorik | Teorik olasılık, olasılık değerinin kesir/ondalık/yüzde gösterimi, imkânsız ve kesin olay |
| tumleyen | Tümleyen olay, P(A) + P(tümleyen) = 1 |
| esit | Eşit olasılıklı olaylar, eşit olasılık için nesne çıkarma |
| ayrik | Ayrık ve ayrık olmayan olaylar, ortak çıktılar |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır.

Kaynak: MEB Matematik 7. Sınıf Ders Kitabı 2. Kitap, 7. Tema (s. 73–90).
