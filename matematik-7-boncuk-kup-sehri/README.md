# Boncuk'un Küp Şehri · Görünümler, Açınım, Yüzey Alanı, Hacim ve Ölçme Birimleri

| Alan | Değer |
|---|---|
| gameId | matematik-7-boncuk-kup-sehri |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Tema | 2. Tema: Geometrik Nicelikler (1) |
| Ekran yönü | Dikey |
| Oyun türü | Test ve doğru/yanlış içermeyen, tamamen dokunmatik oyun: renk değiştiren bukalemun Boncuk + gün batımında 10 kuleli izometrik küp şehri + kule sayacı ve 🔥 seri (seri büyüdükçe Boncuk'un rengi değişir). Görevler: küpleri plana sürükleyip yapı kurma, parmakla görünüm boyama, eksik yüzü açınıma sürükleme, renk damlalarını açınım yüzlerine sürükleme, tutamaçları çekerek prizma kurma, ölçü kaplarını tanka sürükleyip doldurma, sayı şeridini kaydırarak cevap seçme. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken türler dengelenir; süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 104 görev (48 sayı şeridi, 12 prizma kur, 11 küp kur, 11 kapla doldur, 8 görünüm çiz, 8 açınımı tamamla, 6 yüzleri boya), index.html içine gömülüdür |

## Oyun

Rehber karakter **Boncuk**, dalda duran bir bukalemundur; konuşma balonuyla görevi anlatır, doğru cevapta zıplar ve gökkuşağı renklerine bürünür, yanlışta solar ve cesaret verir. Ekranın üstünde gün batımında bir şehir vardır: doğru görevde rengârenk küplerden bir kule yükselir, yanlışta gri taş kalır.

- **Küp kur:** Küp yığınından küpü tutup plandaki kareye bırakınca o kareye bir küp eklenir (üst üste konabilir); fazla küp kareden tutulup çöpe atılır. Yanında yapının canlı izometrik görünümü vardır. Ya resimdeki yapının aynısı kurulur ya da önden/sağdan/üstten görünümleri verilen bir yapı kurulur (görünümlere uyan her yapı kabul edilir; "en az küp" görevlerinde küp sayısı da kontrol edilir).
- **Görünüm çiz:** İzometrik yapının istenen yönden (önden, sağdan, soldan, arkadan, üstten) görünümü, parmak kareli zeminde gezdirilerek boyanır.
- **Açınımı tamamla:** Beş yüzü verilen küp açınımına eksik yüz sürüklenir; açınımı küpe kapatan her yer kabul edilir, kontrolde bütün uygun yerler gösterilir.
- **Yüzleri boya:** Renk damlaları açınım yüzlerine sürüklenir; karşılıklı yüzler aynı renk olmalıdır (küp ve dikdörtgenler prizması açınımları).
- **Prizma kur:** İzometrik kutunun pembe (en), mavi (boy) ve sarı (yükseklik) tutamaçları çekilir; −/+ düğmeleri de vardır. Hacim, taban alanı, küp/kare prizma gibi koşulları sağlayan her prizma kabul edilir.
- **Kapla doldur:** 1 L, 1 dL, 1 cL, 1 mL kapları tanka sürüklenir; tankta sayı yazmaz, istenen miktar (L, dL, cL, mL, dm³, mm³ cinsinden verilir) kaplardan hesaplanır. Toplamı tutan her kap birleşimi kabul edilir.
- **Sayı şeridi:** Cetvel gibi şerit parmakla kaydırılır (fırlatınca kayar ve en yakın çizgiye oturur); ortadaki iğnenin gösterdiği sayı cevaptır. Yüzey alanı, hacim, birim dönüşümü ve problem sonuçları bu türdedir; gerekli prizma, yapı ya da görünüm kartın üstünde çizilir.

Yanlış-cevap kaydında öğrencinin kurduğu yapı (yükseklikler), çizdiği görünüm, koyduğu yer, boyaması, prizmanın ayrıtları, kullandığı kaplar ya da seçtiği sayı ve doğru cevap yazılır; şekiller metinle tarif edilir.

## Soru havuzu

| Grup | İçerik |
|---|---|
| gorunum | Eş küplerle yapıların önden, sağdan, soldan, arkadan, üstten görünümleri; görünümleri verilen yapıyı kurma; en az küp sayısı |
| acinim | Küp ve dikdörtgenler prizması açınımları, karşılıklı yüzler, yüzey alanı (küp, kare prizma, dikdörtgenler prizması) |
| hacim | Birim küp, katman, hacim = taban alanı × yükseklik, verilen hacimde prizma kurma, ayrıt değişince hacmin değişimi |
| birim | m³, dm³, cm³, mm³ dönüşümleri; 1 dm³ = 1 L; L, dL, cL, mL; taşan suyla hacim ölçme |
| problem | Konteyner, kutu kaplama maliyeti, akvaryum, su israfı, Anıtkabir sütunları, havuz, kargo problemleri |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır.

Yeni soru türleri için `questions.json` alanları: `cube_build` (`rows`, `cols`, `maxHeight`, `mode`: copy/views, `target` ya da `views` + `keys`, `minimal`, `minCount`, `allSame`), `view_draw` (`structure`: arka sıradan ön sıraya yükseklikler, `view`, `grid`: beklenen görünüm), `net_fix` (`gridRows`, `gridCols`, `cells`, `candidates`, `validSlots`), `face_paint` (`cells`, `preset`, `pairs`, `colWidths`, `rowHeights`), `prism_build` (`constraints`, `maxEdge`, `edgeUnit`, `solutions`), `pour_cups` (`targetMl`, `cups`, `tankMl`), `number_tape` (`answer`, `low`, `high`, `step`, `answerUnit`, `figure`).

Kaynak: MEB Matematik 7. Sınıf Ders Kitabı 1. Kitap, 2. Tema (s. 117–158).
