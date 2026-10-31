# Roket Rotası · Güneş Sistemi ve Tutulmalar

| Alan | Değer |
|---|---|
| gameId | fen-6-roket-rotasi |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 6 (oyun yalnızca 6. sınıf bağlamını kabul eder) |
| Ünite | 1. Ünite: Güneş Sistemi ve Tutulmalar |
| Ekran yönü | Dikey |
| Oyun türü | Uzay roketi temalı gezegen ve tutulma simülasyonu oyunu. Karakter yoktur. Test ve doğru/yanlış sorusu yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (⭐ puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 106 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:**
  1. Gece, fırlatma rampasında roket ve kule bekler.
  2. "ROKET ROTASI" tabelası yanar, Satürn ve Ay süzülür.
  3. "GERİ SAYIMI BAŞLAT" denince 3-2-1 geri sayımı başlar.
  4. Motorlar ateşlenir, duman yayılır, kule kolu açılır.
  5. Roket gökyüzüne fırlar, yıldızlar akar, ışık patlaması olur.
- **İlerleme:** Üstte 10 duraklı bir rota vardır. Roket simgesi sıradaki durağı gösterir. Doğru görevde durak altın yıldıza (★) dönüşür, yanlışta kuyruklu iz (☄) kalır.
- **Çıkış:**
  1. Paraşütlü kapsül Dünya'ya süzülür.
  2. "GÖREV TAMAM x/10" rozeti damga gibi basılır.
  3. Sonuç "ASTRONOT ROZETİ" olarak açılır.

## Görevler (uzay simülasyonları)
| Tür | Görev | Mekanik |
|---|---|---|
| orbit | Rota haritası | Güneş'ten başlayan yörünge listesindeki boş yörüngelere gezegen ya da asteroit kuşağı kartları sürüklenir. Bazı görevlerde hacim sırası doldurulur, bazılarında haritaya ait olmayan bir kart vardır. Roket rotayı tarar |
| rank | Fırlatma rampası | Gezegen kartlarına hacim ya da Güneş'e uzaklık sırasıyla dokunulur. Tarayıcı gezegenleri gerçek oranlı boyutlarda rampaya çizer |
| balls | Top modeli | Gezegenler hacimlerine göre basketbol, futbol, tenis ve pinpon toplarına yerleştirilir |
| scan | Gezegen taraması | Eşit boyutta çizilmiş 8 gezegenli haritada ölçütü sağlayanlar işaretlenir (uydusu olan, Dünya'dan küçük, rota üzerindekiler …). Roket soldan sağa tarama yapar |
| probe | Sonda tarayıcısı | Sondanın gönderdiği ipuçlarından gizemli gezegen bulunur, sonda gezegeni ortaya çıkarır |
| console | Kokpit paneli / gözlem raporu | Gezegenin yapı, uydu, halka ve sıra göstergeleri ayarlanır. Bir diziliş modeli verildiğinde tutulma türü, zaman, Ay evresi, gölge, alan ve süre göstergeleri ayarlanır |
| meteor | Gök taşı takibi | Kaya parçasının uzay → atmosfer → yeryüzü → çukur yolculuğundaki duraklara gök taşı, meteor, meteorit, meteor çukuru kartları yerleştirilir. Zor görevlerde açıklama ve tuzak kart vardır |
| eclipse | Tutulma simülatörü | Güneş, Dünya ve Ay (ya da basketbol, tenis, pinpon topu) üç konuma dizilir. Işık yanınca gölge konisi oluşur: Ay ortadaysa Güneş tutulması, Dünya ortadaysa Ay tutulması. Bazı görevlerde yanlış kurulmuş model düzeltilir |
| map | Gölge haritası | Dünya üzerindeki gözlem istasyonlarından tutulmayı görebilecekler seçilir: Güneş tutulmasında yalnızca gölge bölgesindekiler, Ay tutulmasında gece tarafındakiler |
| sort | Kargo bölmeleri | Kartlar 2–3 bölmeye ayrılır (karasal/gazsal, uydu-halka, gök taşı-meteor-meteorit, tutulma nitelikleri, bilim insanlarının katkıları) |
| calc | Sayı çarkı | Yıldızeli meteor çukuru, tutulma tarihleri, gölge hızı ve bilim insanlarına ait hesaplar sayı çarkıyla girilir |

Her deste kurulurken her konudan 2 görev seçilir. Görev türleri olabildiğince farklı tutulur, bir destede en az 8 farklı tür bulunur.

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| yorunge | 23 | Gezegenlerin Güneş'e yakınlık ve hacim sıralaması, top modelleri, rota soruları |
| nitelik | 26 | Karasal/gazsal yapı, uydu, halka; gezegenlerin ayırt edici özellikleri |
| gokcisim | 17 | Asteroit kuşağı, gök taşı, meteor, meteorit, meteor çukuru; Yıldızeli meteoriti; Biruni, Fergani, Bettânî |
| gunes | 19 | Güneş tutulmasının oluşumu, zamanı, gözlem alanı ve güvenliği; 1999, 2006 ve 2060 tutulmaları |
| ay | 21 | Ay tutulmasının oluşumu, iki tutulmanın karşılaştırılması, top modelleri; Zerkâle, Takıyyüddin, Dilhan Eryurt |

Görev türlerinin dağılımı: console 15, sort 13, eclipse 12, orbit 11, probe 11, scan 9, calc 9, map 8, rank 7, meteor 7, balls 4.

Yanlış-cevap kaydı:
- questionText görevi ve haritayı, dizilişi ya da kartları metin olarak içerir.
- studentAnswer öğrencinin yerleştirmesini, sırasını, seçimini ya da sayısını yazar.
- correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 6. Sınıf Ders Kitabı (1. kitap), 1. Ünite (s. 14–41).

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
