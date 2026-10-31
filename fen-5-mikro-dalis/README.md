# Mikro Dalış · Canlıların Yapısına Yolculuk

| Alan | Değer |
|---|---|
| gameId | fen-5-mikro-dalis |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 5 (oyun yalnızca 5. sınıf bağlamını kabul eder) |
| Ünite | 3. Ünite: Canlıların Yapısına Yolculuk |
| Ekran yönü | Dikey |
| Oyun türü | Mikroskop ve laboratuvar temalı deney ve simülasyon oyunu. Karakter yoktur, minik bir denizaltı vardır. Test ve doğru/yanlış sorusu yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (⚡ enerji puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 106 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:**
  1. Karanlık laboratuvarda tavan lambası titreyerek yanar.
  2. Raflar ve dev mikroskop belirir, neon "MİKRO DALIŞ" yazısı yanıp söner.
  3. "DALIŞA BAŞLA" denince mor küçültme ışını denizaltıyı preparatın içine küçültür.
  4. Kamera oküler merceğe dalar, iris açılımı ve kabarcıklarla hücrenin içine girilir.
- **İlerleme:** Üstte 10 duraklı dalış göstergesi vardır. Denizaltı her görevde bir durak ilerler; doğruda durağa 🌟, yanlışta 🫧 konur.
- **Çıkış:**
  1. Mercek irisi kapanır, laboratuvara dönülür.
  2. Denizaltı mikroskoptan kabarcıklarla fırlayıp büyür ve masaya iner.
  3. "DALIŞ x/10" madalyası damga gibi basılır.
  4. "DALIŞ SERTİFİKASI" sonuç ekranı açılır.

## Görevler (deney ve simülasyonlar)

| Tür | Görev | Mekanik |
|---|---|---|
| proc | Mikroskobu çalıştır / kapat, preparat hazırla | Adım kartları sırayla seçilir, sonra "DENEYİ BAŞLAT" ile canlandırılır. Işık yanar, preparat tablaya kayar, objektif revolveri döner. Kaba ve ince ayar vidaları dönerken mercek görüntüsü bulanıktan nete geçer. Kapatmada fiş çekilir, soğuyan lamba silinir, mikroskop taşıma kolundan kaldırılır. Preparatta damlalıktan su damlar, soğan zarı ya da ağız içi örneği konur, lamel eğik iner. Yanlış adımda deney durur. Zor görevlerde bir tuzak kart vardır (ör. en büyük objektifle başlamak) |
| parts | Mikroskop kısımları | İstenen kısma (adı ya da görevi verilir) mikroskop çiziminde dokunulur. Kontrolde etiketler çıkar |
| sort | Petri kapları | Kartlar sürüklenerek ya da dokunularak 2–3 petri kabına ayrılır, kontrolde kaplar sırayla parlar |
| build | Hücre modeli kur | Bitki ya da hayvan hücresine ait yapılar hücreye taşınır, ait olmayanlar dışarıda bırakılır (hücre duvarı konunca dış duvar belirir). "HÜCREYİ ÇALIŞTIR" denince yanlış yapılar dışarı atılır, eksikler kesikli çizgiyle eklenir |
| evid | Mikroskop teşhisi | Görüntüdeki hücre için önce bitki ya da hayvan seçilir, sonra kanıt olan yapı seçilir. "YAKINLAŞTIR" ile mercek seçilen yapıya yakınlaşır; yapı görüntüde yoksa bu söylenir |
| city | Hücre Şehri / Hücre Okulu | Organeller görevlerinin yazdığı binalara (ya da okul görevlilerine) yerleştirilir. Kontrolde doğru binalarda organelin makinesi çalışır, yanlışlarda duman çıkar |
| ladder | Yakınlaştırma merdiveni | Hücre → doku → organ → sistem → organizma basamakları kurulur. Ayrıca tuğla-duvar-oda-ev-köy, ev-mahalle-ilçe-il-ülke ve okul benzetmeleri eşlenir |
| bones | İskelet röntgeni | Üç biçimi vardır: (1) istenen kemiklere sırayla dokunma, (2) fırçayla kemikleri uzun, kısa ya da yassı diye boyama, (3) kıkırdak bulunan yerleri işaretleme. Kontrolde röntgen taraması yapılır |
| joints | İskelet kukla | Eklemler oynar, yarı oynar ya da oynamaz diye ayarlanır. "KUKLAYI OYNAT" ile kukla seçilen ayara göre kolunu, bacağını ve omurgasını oynatır |

Her deste kurulurken her konudan 2 görev seçilir. Görev türleri olabildiğince farklı tutulur, bir destede en az 7 farklı tür bulunur.

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| mikro | 21 | Mikroskobun kısımları, kullanım ve kapatma adımları, soğan zarı ve ağız içi epitel preparatı |
| hucre | 21 | Bitki ve hayvan hücresinin temel kısımları; hücre duvarı, kloroplast, koful ve sentrozom farkları; mikroskopta teşhis |
| organel | 20 | Çekirdek, mitokondri, endoplazmik retikulum, golgi, koful, kloroplast, lizozom, ribozom, sentrozom, hücre zarı ve duvarının görevleri; hücre-okul benzetmesi |
| hiyer | 20 | Hücre-doku-organ-sistem-organizma; kas, sinir, kalp, akciğer, kemik örnekleri; köy, ülke ve okul benzetmeleri |
| destek | 24 | Kemik adları ve biçimleri, kıkırdak, eklem çeşitleri, kas çeşitleri, kemik ve kıkırdak özellikleri, sağlıklı davranışlar |

Görev türlerinin dağılımı: sort 21, city 17, ladder 16, proc 13, bones 13, build 9, parts 6, evid 6, joints 5.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği metin olarak içerir ([Şekil: …] biçiminde).
- studentAnswer öğrencinin sırasını, yerleştirmelerini, boyamalarını ya da seçimlerini yazar.
- correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 5. Sınıf Ders Kitabı, 3. Ünite (s. 98–141).

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
