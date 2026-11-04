# Yaban Kamera · Sürdürülebilir Yaşam ve Etkileşim

| Alan | Değer |
|---|---|
| gameId | fen-6-yaban-kamera |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 6 (oyun yalnızca 6. sınıf bağlamını kabul eder) |
| Ünite | 7. Ünite: Sürdürülebilir Yaşam ve Etkileşim |
| Ekran yönü | Dikey |
| Oyun türü | Doğa belgeseli çekimi temalı çevre ve biyoçeşitlilik simülasyonları. Öğrenci karakteri yoktur; film şeridindeki kareler ilerlemeyi gösterir. Test ve doğru/yanlış sorusu yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🌿 puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 101 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:**
  1. Gün doğumunda dağlar, sallanan ağaçlar, uçan kuşlar; ekranda kamera vizörü (köşe çerçeveleri, REC ışığı, zaman kodu).
  2. "KAYDA BAŞLA" denince klaket çarpar.
  3. Görüntü netleşir, odak artısı kayar, sağdan bir geyik kadraja girer, çalılıktan bir tilki başını uzatır.
  4. Deklanşör flaşıyla oyun başlar.
- **İlerleme:** Üstte 10 karelik film şeridi vardır. Doğru görevde kareye bir hayvan fotoğrafı düşer; yanlışta kare karanlık (✕) kalır.
- **Çıkış:**
  1. Karanlık gala salonunda projektör ışığı yanar.
  2. Film şeridi kayarak gelir; doğru görevlerin kareleri görünür.
  3. "ALTIN OBJEKTİF x/10 KARE" madalyası basılır.
  4. Sonuç "BELGESEL KARNESİ" olarak açılır.

## Görevler (simülasyonlar)
| Tür | Görev | Mekanik |
|---|---|---|
| scene | Vizör | Ekosistemdeki (orman, göl, deniz kıyısı, çayır) öğelere dokunularak "canlı/cansız" etiketi konur; kamera kadrajı öğeleri tek tek tarar, deklanşör çeker |
| count | Tür sayımı | Fotoğraftaki farklı canlı çeşidi sayılıp sayı çarkına girilir; analizde aynı türler sütunlarda toplanır, birey ve çeşit sayısı gösterilir |
| compare | İki kadraj | Hangi kadrajda biyoçeşitliliğin fazla olduğu seçilir; analizde tekrar eden türler soluklaşır, çeşitler numaralanır |
| chain | Domino etkisi | Bir olayın (arıların azalması, yangın, kirlilik, DDT …) sonuçları seçilir; domino taşları doğru sonuçlar için sırayla devrilir |
| census | Sayım raporu | Yerleşim öncesi/sonrası tür sayımları için "arttı/azaldı/değişmedi/tükendi" seçilir; çubuk grafik yirmi yıllık değişimi oynatır |
| threat | Biyoçeşitlilik göstergesi | Her insan faaliyeti "tehdit/korur" olarak işaretlenir; 10 yıl ileri sarılınca hayvanlar kaybolur ya da geri gelir, gösterge iner/çıkar |
| fuel | Yakıt deposu | Yakıtlar katı/sıvı/gaz tankına ayrılır; tanklar dolar |
| toggle | Anahtar paneli | Kış kampında karbon monoksit önlemleri, kirlenen vadiyi yeşertecek uygulamalar ve çölleşmeye karşı önlemler için anahtarlar açılır/kapatılır; CO dedektörü alarm verir ya da vadi/çöl yeşerir |
| pollute | Kirlilik katmanları | Kirlilik kaynakları hava/su/toprak katmanına ya da yol açtıkları hastalığa eşlenir; sahnede duman, petrol, pil izleri belirir |
| sort | Belgesel arşivi | Kavramlar, endemik türler, nesli tükenen/tehlike altındaki canlılar, CO belirtileri, yangın sebepleri, özel günler, bilim insanları |
| calc | Sayı çarkı | Tür sayımı farkları, endemik bitki oranı, özel gün ve bilim insanı yılları |

Her deste kurulurken her konudan 2 görev seçilir. Görev türleri olabildiğince farklı tutulur.

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| biyo | 25 | Tür, habitat, ekosistem, biyoçeşitlilik, canlı/cansız varlıklar, endemik türler, biyoçeşitliliğin önemi |
| tehdit | 21 | Biyoçeşitliliği tehdit eden faktörler, nesli tükenen ve tehlike altındaki hayvan ve bitkiler, tür sayımı verileri |
| yakit | 18 | Katı/sıvı/gaz yakıtlar, karbon monoksit zehirlenmesi belirtileri, önlemler, 187 ve 112 |
| kirlilik | 19 | Su, toprak, hava kirliliği ve kaynakları, sağlığa etkileri, Rachel Carson ve DDT |
| cozum | 18 | Ağaçlandırma, temiz enerji, filtre, çölleşme ve orman yangınları, 22 Mayıs ve 5 Haziran, bilim insanları |

Görev türlerinin dağılımı: sort 18, toggle 14, calc 11, pollute 10, scene 8, chain 8, threat 8, count 6, compare 6, census 6, fuel 6.

Yanlış-cevap kaydı:
- questionText görevi, öğeleri, sayımları ya da seçenekleri metin olarak içerir.
- studentAnswer öğrencinin etiketlerini, seçimlerini, açtığı anahtarları ya da girdiği sayıyı yazar.
- correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 6. Sınıf Ders Kitabı (2. kitap), 7. Ünite (s. 96–126).

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
