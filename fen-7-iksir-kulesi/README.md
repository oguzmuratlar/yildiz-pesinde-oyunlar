# İksir Kulesi · Maddenin Doğasına Yolculuk

| Alan | Değer |
|---|---|
| gameId | fen-7-iksir-kulesi |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Ünite | 5. Ünite: Maddenin Doğasına Yolculuk |
| Ekran yönü | Dikey |
| Oyun türü | Gece kulesinde kimyagerlik temalı atom, element, bileşik ve karışım simülasyonları. Öğrenci karakteri yoktur; iksir rafındaki 10 şişe ilerlemeyi gösterir. Test ve doğru/yanlış sorusu yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🔮 puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 107 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:**
  1. Yıldızlı gece, dolunay, tepede taş kule, kulenin dibinde yeşil fokurdayan kazan; "İKSİR KULESİ" tabelası.
  2. "KAZANI YAK" denince kule penceresi yanar, kazandan baloncuklar yükselir.
  3. Deney şişeleri dönerek göğe uçar, mor-yeşil bir patlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 şişelik iksir rafı vardır. Doğru görevde şişe renkli iksirle dolar; yanlışta boş kalır (✕).
- **Çıkış:**
  1. Raf belirir, doğru görevlerin şişeleri sırayla iksirle dolar.
  2. "KULE KİMYAGERİ x/10 İKSİR" madalyası basılır.
  3. Sonuç "KİMYAGER KARNESİ" olarak açılır.

## Görevler (simülasyonlar)
| Tür | Görev | Mekanik |
|---|---|---|
| particle | Parçacık şişeleri | Özellik kartlarına PROTON / NÖTRON / ELEKTRON etiketi verilir |
| models | Model aynası | Dalton, Thomson, Rutherford, Bohr, modern atom modelleri çizimleriyle geçmişten günümüze sıralanır; yıllarıyla zaman çizelgesi oynar |
| jar | Kavanoz rafı | Renkli tanecik modelli kavanozlara ELEMENT / BİLEŞİK / KARIŞIM etiketi verilir |
| formula | Formül terazisi | Formülden (ya da molekül modelinden) her atom çeşidinin sayısı çarklarla girilir; molekül kurulur |
| symbol | Rün ustası | Element adlarına sembol rünleri (bir çeldirici) yerleştirilir |
| shells | Yörünge kazanı | Atom numarası verilen elementin katmanlarına dokunarak elektron sayıları (2-8-8 kuralı) ayarlanır |
| ptable | Periyodik raf | Element şişesi ipucuna (dağılım, atom numarası, katman bilgisi) göre ilk 18 elementlik tablodaki göze yerleştirilir |
| ion | İyon kazanı | Atomun oluşturacağı iyonun yükü seçilir; elektronlar verilir ya da alınır |
| mix | Kazan karışımları | Karışımlara HOMOJEN / HETEROJEN etiketi verilir |
| dissolve | Çözünme yarışı · Kontrollü deney | Hangi kazanda şekerin daha hızlı çözüneceği ya da bir faktörü test etmek için hangi iki kazanın kullanılacağı seçilir; süreölçer çalışır |
| separate | Ayırma tezgâhı | Karışım için doğru ayırma düzeneği (buharlaştırma, ayırma hunisi, damıtma, süzme, eleme, mıknatıs) seçilir |
| sort | İksir dolapları | Atom-hücre, hipotez-teori, modeller, sembol-formül, element-bileşik-karışım, iyonlar, çözücü-çözünen, iletkenlik, alaşımlar, ayırma ilkeleri, bilginler |
| calc | Sayı çarkı | Elektron-proton kütle oranı, model yılları, iyon yükü, element ve grup sayıları, glikozdaki atom sayısı, bilginlerin yılları |

Her deste kurulurken her konudan 2 görev seçilir. Görev türleri olabildiğince farklı tutulur.

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| atom | 17 | Atomun yapısı, proton-nötron-elektron, atom-hücre karşılaştırması, atom modelleri, hipotez ve teori |
| saf | 26 | Saf madde, element, bileşik, tanecik modelleri, ilk 18 element ve 9 yaygın elementin sembolü, bileşik formülleri |
| periyot | 30 | Elektron dizilimi, grup ve periyot, helyum istisnası, dublet-oktet, iyonlar, periyodik tablo |
| karisim | 17 | Homojen-heterojen karışımlar, çözelti, çözücü-çözünen, alaşımlar, iletkenlik, çözünme hızını etkileyen faktörler |
| ayirma | 17 | Buharlaştırma, ayırma hunisi, damıtma, süzme, eleme, mıknatıs; Câbir bin Hayyân, Râzî, Lavoisier, Boyle, Sinanoğlu |

Görev türlerinin dağılımı: sort 13, separate 11, calc 10, jar 9, shells 9, ptable 9, formula 8, ion 8, dissolve 7, particle 6, symbol 6, mix 6, models 5.

Yanlış-cevap kaydı:
- questionText görevi, kartları, kavanoz içeriklerini, atom numarasını, ipuçlarını ya da kazan koşullarını metin olarak içerir.
- studentAnswer öğrencinin etiketlerini, sıralamasını, girdiği sayıları, seçtiği gözü, yükü ya da düzeneği yazar.
- correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 7. Sınıf Ders Kitabı (2. kitap), 5. Ünite (s. 42–101).

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
