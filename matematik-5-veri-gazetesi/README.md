# Veri Gazetesi · Araştır, Say, Grafiğe Dök

| Alan | Değer |
|---|---|
| gameId | matematik-5-veri-gazetesi |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 5 (oyun yalnızca 5. sınıf bağlamını kabul eder) |
| Tema | 5. Tema: İstatistiksel Araştırma Süreci |
| Ekran yönü | Dikey |
| Oyun türü | Sütun/nokta grafiği kurma (sürükleyerek veya dokunarak) + grafikte cevabı bulup dokunma (sütun, nokta sütunu, daire dilimi) + test + doğru/yanlış. 10 haber, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken grafik kurma ve grafikte bulma görevlerine öncelik verilir; süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 105 görev (58 test, 24 doğru/yanlış, 12 grafik kurma, 11 grafikte bulma), index.html içine gömülüdür |

## Oyun

Ekranın üstünde yarınki gazetenin boş ön sayfası vardır. Her doğru görev sayfaya grafikli bir haber olarak basılır (matbaa sesiyle); yanlış görevde haberin yerine mürekkep lekesi kalır. Kitaptaki gazete, TÜİK ve bakanlık grafiklerini inceleme etkinliklerinden esinlenmiştir.

- **Grafik kur:** Ekranda bir sıklık tablosu, çetele, ham veri listesi ya da başka bir grafik verilir. Öğrenci verileri boş bir sütun grafiğine (sütunu parmakla yukarı-aşağı sürükleyerek ya da istenen yüksekliğe dokunarak) veya nokta grafiğine (kaçıncı noktaya dokunursa o kadar nokta konur, en üstteki noktaya tekrar dokunursa silinir) aktarır. “Kontrol et”ten sonra yanlış sütunlar kırmızı olur, doğru yükseklik yeşil kesikli çizgiyle gösterilir.
- **Grafikte bul:** Sütun, yatay sütun, nokta ya da daire grafiğinde sorunun cevabı olan kategoriye dokunulur (daire grafiğinde dilime veya açıklama satırına).
- **Test ve D/Y:** Seçeneğe dokunulur.
- Bütün tablo, çetele, ham veri ve grafikler soruyla birlikte ekranda çizilir; iki grafiği karşılaştıran sorularda iki grafik alt alta, sıkışık boyutta gösterilir. Yanıltıcı grafik soruları (eksenin 0'dan başlamaması, yüzdeleri %100 etmeyen daire grafiği) da ekranda çizilir.

Yanlış-cevap kaydında ekrandaki veri metin olarak eklenir (ör. “[Tablo: … Elma 4, Muz 3 …]”); grafik kurma görevlerinde öğrencinin kurduğu grafiğin değerleri ve doğru değerler yazılır.

## Soru havuzu

| Grup | İçerik |
|---|---|
| soru | İstatistiksel araştırma sorusunun özellikleri (gruba yönelik, birden çok cevap, değişken, değişkenlik, veriyle cevaplanabilme), karşılaştırma soruları, uygun grup |
| veri | Araştırma adımları, hazır veri kaynakları (TÜİK, gazete, yıllık), anket sorusu ve seçenekleri, gizlilik, çetele, sıklık tablosu, kategorik veri, hatalı tabloyu bulma |
| grafik | Tablodan/çeteleden/ham veriden sütun ve nokta grafiği kurma, grafikleri birbirine dönüştürme, daire grafiğinde parça–bütün |
| okuma | Sütun, yatay sütun, nokta ve daire grafiklerinden en çok/en az, fark, toplam, kat ve kesir okuma |
| yorum | Yorumlama, değişebilirlik, objektif yorum, veriye dayalı karar, yanıltıcı ve hatalı grafikler, iki grafiği karşılaştırma, başkalarının yorumlarını değerlendirme |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır.

Yeni soru türleri için `questions.json` alanları: her soruda isteğe bağlı `figure` (tek nesne veya dizi; `kind`: table, tally, raw, bar, hbar, dot, pie) ve `figureText`; grafik kurma `questionType: "chart_build"`, `chart` {kind, title, cats, max, step, snap, yl}, `targetValues`; grafikte bulma `questionType: "chart_tap"`, `answerIndex`.

Kaynak: MEB Matematik 5. Sınıf Ders Kitabı 2. Kitap, 5. Tema (s. 56–113).
