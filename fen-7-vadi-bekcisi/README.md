# Vadi Bekçisi · Sürdürülebilir Yaşam ve Enerji

| Alan | Değer |
|---|---|
| gameId | fen-7-vadi-bekcisi |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Ünite | 7. Ünite: Sürdürülebilir Yaşam ve Enerji |
| Ekran yönü | Dikey |
| Oyun türü | Kurumuş bir vadiyi canlandıran bekçi oyunu. Her görev ayrı bir mini oyundur: ok çizme, blok dizme, çubuk sürükleme, basılı tutarak doldurma, boru çevirme, sepetle yakalama, yol ayrımı seçme, kol çevirme. Test ve şıklı soru yoktur. Üst katman: her başarılı görevden sonra vadiye bir canlı yerleştirilir; piramit kuralına uymayan canlı (alt basamakta yeterli besin yoksa) aç kalıp vadiyi terk eder. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🌱 puanı ve vadi canlıları yalnızca oyun içi eğlencedir, yıldızı etkilemez) |
| Soru havuzu | 104 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:**
  1. Kurumuş, çatlamış toprak; kuru kütük, ahşap "VADİ BEKÇİSİ" tabelası.
  2. "YAĞMURU ÇAĞIR" denince bulutlar gelir, gök gürler, yağmur yağar.
  3. Dere akmaya başlar, tepeler yeşerir, filizler, çiçekler, ağaçlar ve kelebekler belirir; yeşil-mavi patlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 yuvarlak alan vardır. Doğru görevde oraya yerleştirilen canlı (yoksa 🌱), yanlışta kurak toprak (🏜️) görünür.
- **Çıkış:**
  1. Güneşli vadi, akan dere.
  2. Oyuncunun yerleştirdiği canlılar sırayla vadide belirir.
  3. "VADİ BEKÇİSİ x/10 GÖREV" madalyası basılır, sonuç "BEKÇİ KARNESİ" olarak açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| chain | Zincir kur | Canlılara sırayla dokunarak besini verenden yiyene ok çizilir; Güneş enerjisi oklar boyunca akar. Zor görevlerde besin ağından istenen canlıyla biten zincir çıkarılır (fazla canlılar var) |
| pop | Popülasyon tahmini | Bir canlının sayısı artınca/azalınca diğer canlıların sayı çubukları yukarı-aşağı sürüklenir; “1 yıl ileri sar” gerçek değişimi gösterir |
| pyr | Piramit kulesi | Bloklar alttan üste kuleye dizilir; ayrıştırıcı piramidin yan yüzeyine konur; yanlışsa piramit çöker |
| gauge | Ölçüm istasyonu | Her basamağın birey sayısı, enerji, kütle, vücut büyüklüğü ya da zehirli madde çubuğu sağa-sola sürüklenerek ayarlanır; biyolojik birikimde zehir damlaları basamaklarda birikir |
| pour | Su doldurma | Musluğa basılı tutularak bardak doldurulur (dünyadaki su dağılımı, günlük içme/kullanım/toplam su) |
| pipe | Boru ustası | Boru parçaları döndürülerek kaynak (kızartma yağı, evsel/fabrika atık suyu, yağmur suyu, Kırk Çeşme…) doğru istasyona bağlanır; vana açılınca su akar ya da sızar |
| path | Gün yolu | Karakter yol ayrımlarında tabela seçerek ilerler; sonunda damla sayacı su ayak izini gösterir |
| dial | Su sayacı | Daire üzerindeki kol çevrilerek (log ölçek) bir ürünün su ayak izi tahmin edilir; tank gerçek değere dolar |
| catch | Yağmur oyunu | Gökten düşenlerden yalnızca hedef olanlar sepetle yakalanır (üretici, ayrıştırıcı, tatlı su, atık su türleri, bilim insanları) |

Her deste kurulurken her konudan 2 görev seçilir. Görev türleri olabildiğince farklı tutulur.

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| zincir | 29 | Üretici, tüketici, ayrıştırıcı; besin zinciri ve ok yönü; besin ağı (Görsel 7.1.3); popülasyon değişimleri; Charles Elton |
| piramit | 25 | Ekoloji piramidi, beslenme basamakları, birey sayısı, kütle, vücut büyüklüğü, enerji aktarımı, biyolojik birikim, gökdoğan, Rachel Carson |
| kaynak | 16 | Tuzlu-tatlı su, buzul, yer altı ve yüzey suyu yüzdeleri; tasarruf; Mimar Sinan, sarnıçlar, Kerecî; Dünya Su Günü |
| atik | 16 | Evsel, endüstriyel, tarımsal atık su; atık yağ; arıtma tesisleri; atık sudan biyogaz/gübre; su döngüsü |
| iz | 18 | Su ayak izi, doğrudan-dolaylı su kullanımı, ürünlerin su ayak izleri, tasarruflu tüketim, Tarık-Tuna karşılaştırması, Hoekstra |

Görev türlerinin dağılımı: catch 17, path 15, chain 14, pyr 11, gauge 11, pour 11, pipe 10, pop 9, dial 6.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (canlılar, zincir, basamaklar, bardaklar, boru istasyonları, yol ayrımları, düşen nesneler) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (çizilen oklar, kule sırası, çubuk tahminleri, doldurulan miktar, suyun ulaştığı yer, seçilen tabelalar, yakalanan/kaçırılanlar, sayaç tahmini).
- correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 7. Sınıf Ders Kitabı (2. kitap), 7. Ünite (s. 132–161).

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
