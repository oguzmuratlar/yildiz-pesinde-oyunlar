# Pino'nun Buz Kalesi · Alan Ölçme, Yükseklik, Çember, Merkez Açı

| Alan | Değer |
|---|---|
| gameId | matematik-6-pino-buz-kalesi |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 6 (oyun yalnızca 6. sınıf bağlamını kabul eder) |
| Tema | 7. Tema: Geometrik Nicelikler |
| Ekran yönü | Dikey |
| Oyun türü | Karakterli kutup oyunu: mimar penguen Pino + kuzey ışıkları altında 10 bloklu buz kalesi + buz bloğu sayacı ve 🔥 seri. Görevler: farklı buz kalıbını kırma (alan birimleri), yüksekliği bulma, çember çizme (yarıçap ayarlama), pist yayı (merkez açı oluşturma), balık tutma (sayısal cevap), test ve doğru/yanlış. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken oyun görevlerine öncelik verilir (bir oyunun 8–10 görevi etkileşimli, en fazla 3'ü balık tutma); süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 103 görev (36 balık tutma, 12 pist yayı, 11 çember çizme, 10 yükseklik bulma, 9 farklı kalıp, 18 doğru/yanlış, 7 test), index.html içine gömülüdür |

## Oyun

Rehber karakter **Pino**, bereli ve atkılı bir penguendir; konuşma balonuyla görevi anlatır, doğru cevapta kanatlarını kaldırıp zıplar, 3 doğru üst üste gelince coşar, yanlışta üzülüp cesaret verir. Ekranın üstünde, kuzey ışıkları altında 10 bloklu bir buz kalesi vardır: doğru görevde parlayan buz bloğu yerine oturur, yanlışta çatlak gri blok kalır.

- **Farklı kalıbı kır (alan birimleri):** Her sırada dört buz kalıbı vardır; üçü aynı alanı farklı birimlerle gösterir (ör. 0,05 m² = 5 dm² = 50 000 mm²), biri farklıdır. Her sırada farklı olana dokunulur, kalıp çatlar. Bütün sıralar doğruysa görev doğrudur.
- **Yüksekliği bul:** Kareli zeminde paralelkenar, dikdörtgen ya da üçgen çizilir; taban kalın mavi, gerekiyorsa uzantısı kesikli gösterilir. Dört renkli aday doğru parçasından mavi kenara ait yükseklik seçilir (geniş açılı üçgende ve paralelkenarda dışarıda kalan yükseklik, paralel doğrular arası yükseklik dahil). Kontrolde dik açı işareti çizilir.
- **Çember çiz:** Buz pistinin merkezinden turuncu düğme sürüklenir ya da − / + ile yarıçap ayarlanır; ekranda yalnızca r ve çap yazar, çemberin uzunluğu yazmaz. Verilen çember uzunluğuna (π = 3) uygun yarıçap kurulur; doğruysa Pino çemberin üstünde kayar.
- **Pist yayı:** Pino üstteki yarıçaptan başlayıp saat yönünde kayar. İkinci yarıçap 15°'lik adımlarla sürüklenerek merkez açı oluşturulur; istenen yay uzunluğuna uygun açı bulunur.
- **Balık tut:** Buz deliğinde sayı taşıyan dört balık yüzer; hesaplanan cevabı taşıyan balığa dokunulur (birim deliğin üstünde yazar). Alan, çember ve yay problemleri bu türdedir; gerekli şekil kartın üstünde çizilir.
- **Test ve D/Y:** Renkli seçenekler.

Yanlış-cevap kaydında seçilen kalıplar, seçilen doğru parçası, kurulan yarıçap ya da açı ve doğru cevap yazılır; şekiller kayıtta metinle tarif edilir.

## Soru havuzu

| Grup | İçerik |
|---|---|
| birim | km², hm², dam², m², dm², cm², mm² arasında dönüşüm; dikdörtgenin alanı farklı birimlerle |
| yukseklik | Kenara ait yükseklik; paralelkenarın ve üçgenin alanı; köşegen ve iki eş üçgen; alan problemleri |
| cember | Pi sayısı, çemberin uzunluğu (Ç = 2 · π · r = π · çap), yarıçap bulma, tekerlek ve tur problemleri |
| yay | Merkez açı, merkez açının gördüğü yay, yay uzunluğu ve açı ilişkisi |
| karma | Kaplama ve maliyet problemleri ile bütün türlerden karışık görevler |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır. Hesaplarda kitaptaki gibi π = 3 (bir görevde 3,14) alınır; çarpma için “·” kullanılır.

Yeni soru türleri için `questions.json` alanları: `unit_odd` (`rows`: dörder alan değeri, `answerIndices`: her sıradaki farklı değerin sırası), `height_pick` (`points`: köşeler, `base`: mavi kenarın köşe sıraları, `candidates`: dört doğru parçası — ilk aday doğru yüksekliktir ve ikinci noktası tabanın (ya da uzantısının) üzerindedir, `extension`, `parallel`), `circle_draw` (`targetRadius`, `maxRadius`, `lengthUnit`), `arc_set` (`targetAngle`, `step`), `fish_pick` (`options` — ilk seçenek doğrudur, `answerUnit`); `figure` (`kind`: rect / para / tri / circ) karttaki şekli çizer.

Kaynak: MEB Matematik 6. Sınıf Ders Kitabı 2. Kitap, 7. Tema (s. 98–160).
