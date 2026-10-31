# Fener Adası · Işığın Yansıması ve Renkler

| Alan | Değer |
|---|---|
| gameId | fen-6-fener-adasi |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 6 (oyun yalnızca 6. sınıf bağlamını kabul eder) |
| Ünite | 4. Ünite: Işığın Yansıması ve Renkler |
| Ekran yönü | Dikey |
| Oyun türü | Deniz feneri temalı ışık deneyleri oyunu. Karakter yoktur. Test ve doğru/yanlış sorusu yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (✨ puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 105 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:**
  1. Fırtınalı bir gece: yağmur yağar, şimşek çakar.
  2. Kayalıkta kırmızı-beyaz deniz feneri, açıkta karanlıkta bir yelkenli vardır.
  3. "FENERİ YAK" denince gök gürler, fener lambası yanar ve ışık huzmesi denizi tarar.
  4. Yağmur diner, gemi aydınlanıp limana yönelir, ışık patlaması olur.
- **İlerleme:** Üstte dalga çizgisi üzerinde 10 şamandıra vardır. Sıradaki şamandırada yelkenli durur. Doğru görevde şamandıra yanar (✦), yanlışta söner (✕).
- **Çıkış:**
  1. Gün doğar, gökyüzü turuncuya döner.
  2. Gemiler limana girer.
  3. Can simidi biçiminde "LİMANA ULAŞAN x/10 GEMİ" rozeti basılır.
  4. Sonuç "FENER BEKÇİSİ MADALYASI" olarak açılır.

## Görevler (ışık deneyleri)
| Tür | Görev | Mekanik |
|---|---|---|
| surface | Yüzey test tezgâhı | Ayna, durgun su, düz/buruşturulmuş folyo, dalgalı su, çim, halı için düzgün/dağınık yansıma (ya da net görüntü var/yok, paralel/dağılarak yansır) seçilir. Paralel ışınlar gönderilir, yansıyan ışınlar çizilir |
| beam | Işın yönlendirme | Aynaya gelen ışının açısı verilir. Yansıma ya da gelme açısı ±5° düğmeleriyle ayarlanır. Tahmin kesikli çizgiyle, gerçek yansıma sarı ışınla çizilir; açı doğruysa ışık gemiyi bulur. Zor görevlerde açı aynaya göre ya da iki ışın arasındaki toplam olarak verilir |
| label | Işın şeması | Kart seçilip şemadaki numaraya dokunularak gelen ışın, yansıyan ışın, yüzey normali, gelme açısı ve yansıma açısı etiketlenir. Zor görevlerde tuzak kart vardır |
| mirror | Ayna atölyesi | Perde arkasındaki aynada oluşan görüntülerden (büyük/küçük/aynı boy, düz/ters) ya da yansıyan ışınların biçiminden (paralel/toplanan/dağılan) ayna türü bulunur. Perde kalkınca ayna görünür |
| sym | Ayna simetrisi | Fener işaretinin düz aynadaki (ya da durgun su yüzeyindeki) görüntüsü 5×5 ızgarada kutulara dokunularak çizilir |
| prism | Prizma tezgâhı | Beyaz ışığın prizmadan çıkan renk bantlarındaki boşluklara renk kartları sırayla yerleştirilir; ışık açılınca tayf oluşur |
| mix | Işık panosu | Kırmızı, yeşil, mavi projektörlerden gerekenler açılarak hedef renk (sarı, cyan, magenta, beyaz) elde edilir |
| stage | Karanlık depo | Renkli ışıkla aydınlatılacak cisimlerin hangi renkte görüneceği seçilir; ışık yanınca cisimler gerçek görünüşüne bürünür |
| detect | Gizemli kutu | Karanlıktaki cisme kırmızı, yeşil, mavi ışıkla bakılır (ya da gözlem kayıtları okunur), cismin beyaz ışıktaki rengi bulunur |
| thermo | Güneş tepsisi | Farklı renkli kutular (ya da güneşli/gölge alan) ısınma sırasına göre dizilir; güneş açılınca termometreler yükselir |
| table | Ölçüm tablosu | Son sıcaklıkları verilen satırlara kutu renkleri yerleştirilir |
| sort | Seyir defteri | Kartlar bölmelere ayrılır (yansıma türleri, ayna kullanım yerleri, ana/ara renkler, kıyafet seçimi, güneş enerjisi, bilim insanları) |
| calc | Sayı çarkı | Açı, sıcaklık ve uzaklık hesapları ile bilim insanlarının yaşam süreleri sayı çarkıyla girilir |

Her deste kurulurken her konudan 2 görev seçilir. Görev türleri olabildiğince farklı tutulur, bir destede en az 8 farklı tür bulunur.

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| yansima | 16 | Düzgün ve dağınık yansıma, yüzeylerin pürüzlülüğü, net görüntü, cisimlerin görülmesi |
| kanun | 22 | Gelen ışın, yansıyan ışın, yüzey normali, gelme ve yansıma açısı, yansıma kanunları |
| ayna | 22 | Düz, çukur, tümsek aynalarda görüntü özellikleri; kullanım alanları; simetri; kaşık deneyi; İbnülheysem |
| renk | 27 | Beyaz ışık ve prizma, ana ve ara renkler, cisimlerin renkli ışık altında görünmesi |
| sogurma | 18 | Işığın soğurulması ve sıcaklık artışı, açık ve koyu renkler, güneş enerjisi uygulamaları, Farisi, Newton |

Görev türlerinin dağılımı: sort 17, beam 12, surface 11, mirror 10, calc 10, stage 8, thermo 7, label 6, sym 6, detect 6, prism 5, mix 4, table 3.

Yanlış-cevap kaydı:
- questionText görevi ve şemayı, yüzeyleri, cisimleri ya da tabloyu metin olarak içerir.
- studentAnswer öğrencinin ayarladığı açıyı, seçimlerini, sırasını ya da yerleştirmesini yazar.
- correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 6. Sınıf Ders Kitabı (1. kitap), 4. Ünite (s. 132–181).

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
