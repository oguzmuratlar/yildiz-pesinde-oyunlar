# Ramo'nun Veri Treni · İstatistiksel Araştırma Süreci

| Alan | Değer |
|---|---|
| gameId | matematik-7-ramo-veri-treni |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Tema | 3. Tema: İstatistiksel Araştırma Süreci |
| Ekran yönü | Dikey |
| Oyun türü | Test ve doğru/yanlış içermeyen dokunmatik oyun: kondüktör rakun Ramo + tepeler arasında ilerleyen veri treni (doğru görevde veriyle dolu renkli vagon eklenir, yanlışta gri boş vagon) + vagon sayacı ve 🔥 seri. Görevler: kartları vagonlara yükleme, evren/örneklem halkalarına bırakma, adım kartlarını raya dizme, çizgi grafiğinin noktalarını sürükleme, grafikte imleci kaydırarak nokta/aralık seçme, ortalama çizgisini ve ortalama mutlak sapma bandını sürükleme. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken türler dengelenir; süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 102 görev (43 vagon yükle, 16 ortalama bandı, 12 grafikte kaydır, 11 grafik çiz, 11 adım rayı, 9 evren-örneklem), index.html içine gömülüdür |

## Oyun

Rehber karakter **Ramo**, kondüktör şapkalı bir rakundur; konuşma balonuyla görevi anlatır, doğru cevapta kollarını kaldırıp zıplar, yanlışta üzülüp cesaret verir. Ekranın üstünde lokomotifi duman çıkaran bir tren vardır: her doğru görevde veriyle dolu renkli bir vagon bağlanır, yanlışta gri boş vagon kalır.

- **Vagon yükle:** Kartlar tutulup doğru vagona bırakılır (kategorik/kesikli/sürekli veri, araştırma sorusu/anket sorusu, sürecin adımları, kişisel veri, güvenilir kaynak, grafik türü, istikrarlı/dalgalı, veriye dayalı yorum/değil, gözlem/tahmin…). Yanlış konan kart başka vagona ya da yukarıya geri taşınabilir.
- **Evren ve örneklem:** Araştırma sorusuna göre gruplar evren halkasına, onun içindeki örneklem halkasına ya da "uygun değil" kutusuna bırakılır (yanlı örneklemler dahil).
- **Adım rayı:** Kartlar numaralı yerlere bırakılarak araştırma sürecinin, veri toplama planının, ortalama mutlak sapma ve ortanca bulmanın adımları sıralanır; dolu yere bırakılan kart yer değiştirir.
- **Grafik çiz:** Çizgi grafiğinin kırmızı noktaları değerlerine sürüklenir (▲▼ ile ince ayar). Tahmin görevlerinde son nokta eğilime uygun bir aralığa konur; aralıktaki her tahmin kabul edilir.
- **Grafikte kaydır:** Grafiğe dokunup parmak kaydırılır; imleç bir noktayı ya da iki ölçüm arasını seçer (en yüksek değer, en hızlı artış/azalış, azalmanın başladığı aralık…).
- **Ortalama bandı:** Sayı doğrusunda (nokta grafiği ya da veri listesiyle) kırmızı çizgi aritmetik ortalamaya, ortancaya ya da tepe değere; turuncu tutamaç ortalama mutlak sapma bandına; mor uçlar açıklık için en küçük ve en büyük veriye sürüklenir.

Yanlış-cevap kaydında öğrencinin yanlış yere koyduğu kartlar, adım sırası, işaretlediği noktalar, seçtiği aralık ya da değerler ve doğru cevap yazılır; grafikler ve veriler metinle tarif edilir.

## Soru havuzu

| Grup | İçerik |
|---|---|
| veri | Kategorik ve nicel (kesikli, sürekli) veri; araştırma sorusu ve anket sorusu; araştırma sürecinin dört adımı |
| orneklem | Evren ve örneklem, yanlı örneklem, veri toplama planı, değişebilirlik, kişisel veriler ve mahremiyet, güvenilir kaynak, etik |
| grafik | Çizgi grafiği çizme ve okuma; uygun grafik türünü seçme |
| ozet | Aritmetik ortalama, ortanca, tepe değer, açıklık, ortalama mutlak sapma; istikrarlı/dalgalı veri |
| yorum | Veriye dayalı yorum, gözlem/tahmin, genelleme hataları, karar verme, araştırma süreçlerini inceleme |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır. Kitabın tablolarındaki veriler kullanılmıştır; okunamayan grafik değerlerinin yerine soruda "örnek veri" diye belirtilen veriler verilmiştir.

Yeni soru türleri için `questions.json` alanları: `wagon_sort` (`wagons`, `items[].label`, `items[].wagon`), `venn_drop` (`items[].zone`: 0 evren, 1 örneklem, 2 uygun değil), `step_rail` (`steps` doğru sırada), `line_points` (`labels`, `values`, `yMin`, `yMax`, `yStep`, `given`, `freePoint`), `graph_scrub` (`labels`, `series`, `mode`: point/segment, `answerIndex`), `spread_band` (`data`, `low`, `high`, `step`, `bandStep`, `mode`: mean/median/mode/range/band, `answer`, `show`: dots/list).

Kaynak: MEB Matematik 7. Sınıf Ders Kitabı 1. Kitap, 3. Tema (s. 159–200).
