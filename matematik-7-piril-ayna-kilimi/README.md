# Pırıl'ın Ayna Kilimi · Dönüşüm

| Alan | Değer |
|---|---|
| gameId | matematik-7-piril-ayna-kilimi |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Tema | 4. Tema: Dönüşüm |
| Ekran yönü | Dikey |
| Oyun türü | Test ve doğru/yanlış içermeyen dokunmatik oyun: kelebek Pırıl + tezgâhta dokunan ayna kilimi (doğru görevde simetrik renkli bir motif işlenir, yanlışta gri söküklü motif kalır) + motif sayacı ve 🔥 seri. Görevler: köşeleri simetri doğrusunun öbür yanına sürükleme, kilim desenini parmakla boyama, şekillerin simetri doğrularını parmakla çizme, görüntü noktalarını iple bağlama, pergel ve cetvelle orta dikme/açıortay inşası, ışını döndürme ve doğruyu kaydırma. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken türler dengelenir; süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 115 görev (29 ayna çiz, 26 yansıt, 20 kilim boya, 16 pergelle inşa, 14 döndür ve kaydır, 10 iple bağla), index.html içine gömülüdür |

## Oyun

Rehber karakter **Pırıl**, kanatları simetrik bir kelebektir; konuşma balonuyla görevi anlatır, doğru cevapta kanatlarını hızla çırpıp zıplar, yanlışta üzülüp cesaret verir. Ekranın üstünde bir dokuma tezgâhı vardır: her doğru görevde kilime simetrik bir motif (göz, bereket, kuş, hayat ağacı…) işlenir.

- **Yansıt:** Kareli zeminde verilen nokta, doğru parçası ya da çokgenin d doğrusuna (dikey, yatay ya da eğik) göre görüntüsü, pembe köşeler doğru noktalara sürüklenerek çizilir. Bazı görevlerde hatalı çizilmiş bir köşe düzeltilir, bazılarında görüntüden asıl şekil bulunur. Görüntü çokgen aynı şekli verdiği sürece köşelerin hangi sırayla konduğu önemsizdir.
- **Kilim boya:** Desenin bir yarısı (ya da bir çeyreği) verilir; renk seçilip kareler parmakla boyanarak dikey, yatay, köşegen ya da iki simetri doğrusuna göre tamamlanır.
- **Ayna çiz:** Parmak şeklin bir yanından öbür yanına sürüklenerek simetri doğrusu çizilir (çizgiye dokununca silinir). Şeklin bütün simetri doğruları çizilmelidir; simetri doğrusu yoksa hiç çizmeden kontrol edilir. İki eş şekil arasındaki gizli simetri doğrusu görevleri de vardır.
- **İple bağla:** Simetri doğrusunun iki yanındaki noktalardan birbirinin görüntüsü olanlar sürüklenerek iple bağlanır; eşi olmayan noktalar boşta kalır.
- **Pergelle inşa:** Pergelin sivri ucu bir noktaya, kalem ucu istenen açıklığa sürüklenir ve ✏️ ile çember çizilir; cetvelin iki ucu kesişim noktalarına sürüklenerek orta dikme ya da açıortay çizilir. Yarım kalmış ve hatalı yapılmış inşaları tamamlama görevleri vardır.
- **Döndür ve kaydır:** Açıortay ışını ya da açının kolu tutamaçla döndürülür (↺ ↻ ile 1° ince ayar); orta dikme görevlerinde M noktası doğru parçası boyunca kaydırılır ve doğru döndürülür.

Yanlış-cevap kaydında öğrencinin yerleştirdiği noktalar (sol alt köşe (0, 0) kabul edilen kare koordinatlarıyla), boyamadaki hatalı kare sayısı, çizdiği doğru sayısı ve yönleri, bağladığı çiftler, çizdiği çemberler ve cetvel konumu ya da açı ölçüsü ile doğru cevap yazılır.

## Soru havuzu

| Grup | İçerik |
|---|---|
| yansima | Nokta, doğru parçası ve çokgenlerin dikey/yatay/eğik doğruya göre yansıması; doğru üzerindeki noktalar; üçgenin kenarına göre yansımasıyla oluşan dörtgenler; hatalı görüntüyü düzeltme; görüntü çiftlerini bağlama |
| desen | Kilim ve bayrak desenlerini bir ya da iki simetri doğrusuna göre tamamlama |
| simetri | Üçgen, dörtgen, düzgün çokgen, yarım daire, daire dilimi, harf ve rakamların simetri doğruları; eş şekiller arasındaki gizli simetri doğrusu |
| ortadikme | Pergel ve ölçüsüz cetvelle orta dikme inşası (yarım kalmış, hatalı, gizli doğru); orta dikmenin konumu ve açısı |
| aciortay | Pergel ve ölçüsüz cetvelle açıortay inşası (daire dilimi dahil); açıortay ışınını ve açının kolunu yerleştirme |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır.

Yeni soru türleri için `questions.json` alanları: `mirror_points` (`grid`, `line`, `shape.pts/labels/closed`, `answer`, `start`, `fix`, `hlabels`), `paint_mirror` (`rows`, `cols`, `lines`, `palette`, `names`, `answer`, `editable`, `start`), `axis_draw` (`canvas`, `shapes`, `keys`, `axes`), `pair_link` (`grid`, `line`, `pts`, `pairs`), `compass_build` (`mode`: perp/bis, `named`, `arms`, `pre`, `compass`, `ruler`, `decor`), `ray_turn` (`mode`: perp/bis/arm, `A`, `len`, `scale`, `tilt`, `O`, `a1`, `a2`, `c`, `start`, `answer`). Koordinatlar kare birimindedir; y aşağı doğru artar.

Kaynak: MEB Matematik 7. Sınıf Ders Kitabı 1. Kitap, 4. Tema (s. 201–217).
