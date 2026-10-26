# Piksel Kilim · Atkı Atkı Çevre ve Alan

| Alan | Değer |
|---|---|
| gameId | matematik-5-piksel-kilim |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 5 (oyun yalnızca 5. sınıf bağlamını kabul eder) |
| Tema | 3. Tema: Geometrik Nicelikler |
| Ekran yönü | Dikey |
| Oyun türü | Kareli zeminde dikdörtgen çizme + sayı tuş takımıyla cevap yazma + test + doğru/yanlış. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken çizim ve hesaplama görevlerine öncelik verilir; süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 103 görev (57 hesapla, 20 test, 13 doğru/yanlış, 13 çizim), index.html içine gömülüdür |

## Oyun

Ekranın üstünde bir dokuma tezgâhı ve boş bir kilim vardır. Her görev kilime bir atkı (desen şeridi) dokur: doğru cevapta şerit kırmızı, lacivert, hardal renklerde Türk kilimi motifiyle dokunur; yanlış cevapta ham (boyasız) yün kalır. Mekik her görevde bir sonraki şeride kayar. Kitaptaki “Piksel Boyama” performans görevi ve halı/kilim bağlamından esinlenmiştir.

- **Çiz:** 10 × 8 birimlik kareli zeminde parmak bir köşeden karşı köşeye sürüklenerek (ya da iki köşeye sırayla dokunarak) dikdörtgen çizilir. Çizerken yalnız kenar uzunlukları gösterilir; çevre ve alanı öğrenci hesaplar. “Kontrol et”ten sonra çevre ve alan da yazılır. Birden çok doğru cevap varsa (ör. çevresi 12 olan her dikdörtgen) hepsi kabul edilir.
- **Hesapla:** Cevap sayı tuşlarıyla yazılır, birim (cm, m, cm², m², br, br², TL, tane) kutuda hazır durur.
- **Test ve D/Y:** Seçeneğe dokunulur.
- Şekil gereken sorularda dikdörtgen (kenar uzunlukları yazılı), kareli zeminde dikdörtgen veya birleşik (L, U biçimli) boyalı bölgeler ekranda çizilir. Bütün sayısal veriler soru metninde ya da şekilde verilir.

Yanlış-cevap kaydında şekil metin olarak eklenir; çizim görevlerinde öğrencinin çizdiği dikdörtgen (kenarlar, çevre, alan) ve bütün doğru seçenekler yazılır.

## Soru havuzu

| Grup | İçerik |
|---|---|
| cevre | Dikdörtgen ve karenin çevresi, kareli zeminde çevre, eksik kenar, aynı çevreli dikdörtgenler, birleşik şeklin çevresi |
| alan | Birim kare, alan = ardışık kenarların çarpımı, cm²/m², eksik kenar, birleşik şeklin alanı, eşit alanlı dikdörtgenler |
| iliski | Aynı çevre–farklı alan, aynı alan–farklı çevre, en büyük alan, en kısa çevre, verilen çevre ve alana uygun dikdörtgeni çizme |
| kaplama | Yüzeyi boşluksuz kaplama, parke/karo/fayans sayısı, arsaya ev yerleştirme |
| problem | Çit, çerçeve, boya, pano, metrekare fiyatı, serbest bölge gibi gerçek yaşam problemleri |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır.

Yeni soru türleri için `questions.json` alanları: hesapla `questionType: "numeric_input"`, `answerNumber`, `answerUnit`; çizim `questionType: "rect_drawing"`, `grid`, `constraints`, `solutions`.

Kaynak: MEB Matematik 5. Sınıf Ders Kitabı 1. Kitap, 3. Tema (s. 138–166).
