# Volt Park · Yaşamımızdaki Elektrik

| Alan | Değer |
|---|---|
| gameId | fen-5-volt-park |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 5 (oyun yalnızca 5. sınıf bağlamını kabul eder) |
| Ünite | 6. Ünite: Yaşamımızdaki Elektrik |
| Ekran yönü | Dikey |
| Oyun türü | Gece lunaparkı temalı devre simülasyonu oyunu. Karakter yoktur. Test ve doğru/yanlış sorusu yoktur. 10 tur, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🎟️ bilet puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 103 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:**
  1. Gece karanlık ve sessiz bir lunapark.
  2. Dev şalter kolu iner, kıvılcım saçılır.
  3. Dönme dolabın 24 ampulü sırayla yanar, dolap dönmeye başlar.
  4. "VOLT PARK" tabelasının ampul çerçevesi yanar.
  5. "PARKA GİR" denince parka doğru yakınlaşılır, ışık patlaması olur.
- **İlerleme:** Üstte 10 ampullü bir ışık zinciri vardır. Doğru turda ampul yanar, yanlışta patlar (✕).
- **Çıkış:**
  1. Gece gökyüzünde havai fişekler patlar.
  2. Dönme dolap ışıkları yanıp söner.
  3. "VOLT PARK BİLETİ x/10" damga gibi basılır.
  4. Sonuç "LUNAPARK BİLETİ" olarak açılır.

## Turlar (devre simülasyonları)
Bütün devrelerde akım, kapalı devrede kablolar boyunca dolaşan noktalarla gösterilir. Ampul parlaklığı pil sayısı / ampul sayısı oranına göre ışık halesiyle canlandırılır.

| Tür | Tur | Mekanik |
|---|---|---|
| match | Sembol eşleştirme | Pil, ampul, kablo, açık/kapalı anahtar sembollerinin altına ad, gerçek resim ya da görev kartları sürüklenir. Bazı turlarda sembolü olmayan pil yatağı/duy kartı boşta kalmalıdır |
| sort | Pano bölmeleri | Kartlar 2–3 bölmeye ayrılır (sembolü var/yok, ışık verir/vermez, parlaklık artar/azalır, bağımsız/bağımlı/kontrol değişkeni, hipotez mi?) |
| build | Şema tahtası | Düzenek resmine ya da istenen sayılara göre şemadaki boş yerlere sembol paletinden pil, ampul, kapalı/açık anahtar ve kablo yerleştirilir. Test edilince kapalı devrede akım dolaşır |
| count | Şemayı say | Şemadaki pil, ampul ve anahtar sayıları sayaçlarla girilir, düzenek kurulur |
| works | Hangisi yanar? | Şema ya da gerçek düzeneklerden ampulün yanacakları seçilir (açık anahtar, kopuk kablo, pilsiz devre) |
| fix | Arıza bul | Gerçek görünümlü devrede açık anahtar ve kopuk kablolar işaretlenir, tamir ekibi onarır ve ampul yanar |
| bright | Hangisi parlak? | Özdeş pil ve ampullü 2–4 devrede parlaklık karşılaştırılır (daha parlak/eşit, en parlak/en sönük) |
| tune | Parlaklık ayarı | "Önce" devresine göre sayaçlarla pil ya da ampul eklenip çıkarılır; diğer değişken sabit tutularak parlaklık artırılır ya da azaltılır |
| pair | Hipotez için çift | Verilen hipotezi test edecek, yalnız bağımsız değişkeni farklı iki devre (K, L, M, N) seçilir |

Her deste kurulurken her konudan 2 tur seçilir. Tur türleri olabildiğince farklı tutulur, bir destede en az 8 farklı tür bulunur.

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| sembol | 19 | Pil, ampul, kablo, açık/kapalı anahtar sembolleri; pil yatağı ve duyun sembolü olmaması; sembollerin ortak bilimsel dil olması |
| sema | 22 | Düzenekten şema kurma, istenen devrenin şeması, şemadaki elemanları sayma, şema-düzenek farkı |
| ariza | 20 | Ampulün yanma koşulları (pil, kapalı anahtar, kesintisiz kablo), arıza bulma |
| parlak | 24 | Pil ya da ampul sayısının ampul parlaklığına etkisi, karşılaştırma ve ayarlama |
| degisken | 18 | Bağımlı, bağımsız ve kontrol edilen değişken; hipotez; hipotezi test edecek devre çiftleri |

Görev türlerinin dağılımı: sort 22, match 13, bright 13, build 12, fix 9, tune 9, pair 9, count 8, works 8.

Yanlış-cevap kaydı:
- questionText görevi ve devreleri metin olarak içerir ([Devre: …] / [Devreler: …] biçiminde).
- studentAnswer öğrencinin kurduğu şemayı, seçimlerini ya da sayılarını yazar.
- correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 5. Sınıf Ders Kitabı (2. kitap), 6. Ünite (s. 104–133).

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
