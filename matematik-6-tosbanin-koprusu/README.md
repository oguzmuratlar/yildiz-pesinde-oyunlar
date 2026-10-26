# Tosba'nın Köprüsü · Paralel Doğrular, Üçgen ve Dörtgenler, Çokgenlerin Açıları

| Alan | Değer |
|---|---|
| gameId | matematik-6-tosbanin-koprusu |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 6 (oyun yalnızca 6. sınıf bağlamını kabul eder) |
| Tema | 5. Tema: Geometrik Şekiller |
| Ekran yönü | Dikey |
| Oyun türü | Karakterli köprü oyunu: rehber kaplumbağa Tosba (baret takan usta) + paralel kıyılı nehirde 10 tahtalık köprü + tahta sayacı ve 🔥 seri. Görevler: açı avı, açı ayarı (ibre çevirme), geometri tahtasında dörtgen kurma, çokgeni köşegenlerle üçgenlere bölme, test ve doğru/yanlış. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken oyun görevlerine öncelik verilir (bir oyunun yaklaşık 7–8 görevi etkileşimli); süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 100 görev (31 açı ayarı, 22 test, 17 doğru/yanlış, 13 geometri tahtası, 11 açı avı, 6 çokgen bölme), index.html içine gömülüdür |

## Oyun

Rehber karakter **Tosba**, sarı baretli bir kaplumbağa ustadır; konuşma balonuyla görevi anlatır, doğru cevapta zıplar, 3 doğru üst üste gelince coşar, yanlışta üzülüp cesaret verir. Ekranın üstünde iki kıyısı birbirine paralel bir nehir vardır: her doğru görevde köprüye renkli bir tahta düşer, yanlışta tahta suya düşer. Minik Tosba köprüde ilerler; sonda karşıya geçilir.

- **Açı avı:** İki paralel doğru (d₁ // d₂) ve bir kesen çizilir; 8 açı dokunulabilir dilimlerdir. Turuncu açı ve ölçüsü verilir. İstenen açılar seçilir: yöndeşi, iç ters açısı, dış ters açısı, bütünler komşuları, ona eş olan bütün açılar, iç bölgedeki ya da dış bölgedeki açılar. Kontrolde doğru seçimler yeşil, yanlışlar kırmızı olur.
- **Açı ayarı:** Şekil (paralel doğrular ve kesen, paralel doğrular arasında kırık çizgi, üçgen ve dış açısı, yamuk/paralelkenar/dörtgen, dış açılar, düzgün çokgen) çizilir; bilinmeyen açı x olarak işaretlenir. Öğrenci x'i hesaplar ve açıölçer biçimindeki ibreyi sürükleyerek ya da −10/−1/+1/+10 düğmeleriyle x'e getirir. İbre başta cevaptan farklı bir yerde durur.
- **Geometri tahtası:** 7 x 7 çivili tahtada lastik dörtgenin A, B, C, D köşeleri sürüklenir (ya da köşeye, sonra çiviye dokunulur). Köşegenler kesikli çizilir. İstenen dörtgen kurulur: kare, yan yatmış kare, kare olmayan dikdörtgen, paralelkenar, eşkenar dörtgen, yamuk, dik yamuk ya da köşegen özellikleri verilen dörtgen. Kenar, açı ve paralellik kontrolü tam sayılarla yapılır; kuralı sağlayan her şekil kabul edilir. Kontrolde “Kurduğun şekil: …” yazılır.
- **Çokgeni böl:** Düzgün dörtgen–sekizgen çizilir. Öğrenci köşelere dokunarak kesişmeyen köşegenler çizer; komşu köşe ya da kesişen köşegen seçilirse nedeni yazılır. Üçgenler oluşunca numaralı renklerle boyanır ve iç açılar toplamı seçilir.
- **Test ve D/Y:** Renkli seçenekler.

Yanlış-cevap kaydında seçilen açıların konumları (ör. “üst kesişimde sol-alt açı”), ayarlanan x değeri, kurulan dörtgenin adı ve köşe koordinatları, çizilen köşegen sayısı ve seçilen toplam yazılır; şekiller kayıtta metinle tarif edilir.

## Soru havuzu

| Grup | İçerik |
|---|---|
| paralel | İki paralel doğru ve bir kesen: yöndeş, iç ters, dış ters, bütünler açılar; paralellik; paralel doğrular arasındaki noktada oluşan açı |
| ucgen | Üçgenin iç açıları toplamı, dış açı = komşu olmayan iki iç açının toplamı, dış açılar toplamı |
| dortgen | Yamuk, paralelkenar, eşkenar dörtgen, dikdörtgen, kare: tanımlar, kenar ve açı özellikleri, aralarındaki ilişkiler |
| kosegen | Dörtgenlerin köşegen özellikleri |
| cokgen | Çokgenin iç açıları toplamı (üçgenlere bölme), dış açılar toplamı 360°, düzgün çokgenin iç ve dış açısı |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır. Kitabın terimleri kullanılır (yöndeş açılar, iç ters açılar, dış ters açılar, bütünler açılar).

Yeni soru türleri için `questions.json` alanları: `angle_hunt` (`t`: kesenin doğruyla yaptığı açı, `highlight`, `highlightValue`, `ask`, `answerPositions`; konumlar 1–4 üst kesişim, 5–8 alt kesişim: sağ-üst, sol-üst, sol-alt, sağ-alt), `angle_turn` (`figure`, `target`), `geoboard` (`target`: kare, kare_egik, dikdortgen, paralelkenar, eskenar, yamuk, dikyamuk), `polygon_split` (`sides`, `triangles`, `total`).

Kaynak: MEB Matematik 6. Sınıf Ders Kitabı 2. Kitap, 5. Tema (s. 12–53).
