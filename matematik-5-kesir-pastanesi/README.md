# Kesir Pastanesi · Boya, Yerleştir, Tart

| Alan | Değer |
|---|---|
| gameId | matematik-5-kesir-pastanesi |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 5 (oyun yalnızca 5. sınıf bağlamını kabul eder) |
| Tema | 4. Tema: Sayılar ve Nicelikler (2) — Kesirler |
| Ekran yönü | Dikey |
| Oyun türü | Kesir modeli boyama + sayı doğrusunda işaret sürükleme + terazi ile karşılaştırma + test + doğru/yanlış. 10 sipariş, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken boyama, sayı doğrusu ve terazi görevlerine öncelik verilir; süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 101 görev (50 test, 17 boyama, 13 doğru/yanlış, 13 terazi, 8 sayı doğrusu), index.html içine gömülüdür |

## Oyun

Bir pastanenin vitrini 10 siparişle dolar. Doğru sipariş vitrine çilekli bir pasta koyar; yanlış sipariş yanık bir kurabiye olarak kalır. Kesirler bütün oyunda alt alta (pay/payda) yazılır; tam sayılı kesirler de doğru biçimde gösterilir.

- **Boya:** Pasta dilimleri, çikolata parçaları, iki ayrı pasta ya da yüzlük tablo verilir. Parçalara dokunarak (yüzlük tabloda parmağı sürükleyerek) istenen kesir boyanır. Denk kesir görevlerinde model farklı sayıda parçaya bölünmüştür (ör. {3/4}'ü 8 dilimli pastada boya → 6 dilim). Hangi parçaların boyandığı değil, kaç parça boyandığı değerlendirilir.
- **Sayı doğrusu:** Pastacı işareti sürüklenip ya da doğruya dokunularak doğru çizgiye bırakılır (çizgilere yapışır).
- **Terazi:** Kefelerde kesir, ondalık veya yüzde gösterimleri vardır. “Sol ağır basar / Dengede / Sağ ağır basar” seçilir; terazi doğru yöne eğilir.
- **Test ve D/Y:** Seçeneğe dokunulur.

Yanlış-cevap kaydında kesirler düz metin (ör. “3/4”, “1 tam 1/4”) olarak yazılır; boyama ve sayı doğrusu görevlerinde öğrencinin yaptığı işlem ve doğrusu kaydedilir.

## Soru havuzu

| Grup | İçerik |
|---|---|
| temsil | Kesir modeli, birim kesir, bileşik ve tam sayılı kesir, dönüşümler, sayı doğrusu |
| denk | Genişletme, sadeleştirme, denk kesirleri boyama ve sayı doğrusunda gösterme |
| ondalik | Paydası 10 ve 100 olan kesirler, ondalık gösterimin okunuşu, para (TL–kuruş), sayı doğrusu |
| yuzde | % sembolü, kesir–ondalık–yüzde dönüşümleri, yüzlük tablo |
| kars | Eşit paydalı/paylı kesirler, ondalıkları karşılaştırma (0,7 = 0,70), farklı gösterimleri karşılaştırma ve sıralama |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır.

Yeni soru türleri için `questions.json` alanları: boyama `questionType: "fraction_shading"`, `model` (pie, pie2, bar, grid100), `parts`, `target`; sayı doğrusu `questionType: "number_line"`, `line {min,max,div}`, `targetTick`; terazi `questionType: "comparison"`, `left`, `right`, cevap `<`, `=` veya `>` (sol ile sağın karşılaştırması). Metinlerde `{a/b}` kesir, `{w a/b}` tam sayılı kesir yazımıdır; `textPlain` düz metin karşılığıdır.

Kaynak: MEB Matematik 5. Sınıf Ders Kitabı 2. Kitap, 4. Tema (s. 12–55).
