# Cezerî Atölyesi · Kuvvet ve Enerjiyi Keşfedelim

| Alan | Değer |
|---|---|
| gameId | fen-7-cezeri-atolyesi |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Ünite | 2. Ünite: Kuvvet ve Enerjiyi Keşfedelim |
| Ekran yönü | Dikey |
| Oyun türü | Cezerî’nin atölyesinde çıraklık temalı iş ve enerji deneyleri. Öğrenci karakteri yoktur; çark dizisi ilerlemeyi gösterir. Test ve doğru/yanlış sorusu yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🔩 puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 102 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:**
  1. Kemerli, çinili bir atölye; duvarda rampalar, zil, ipe asılı ağırlık, altın çarklar ve mekanik bir kuş; "CEZERÎ ATÖLYESİ" parşömeni.
  2. "DÜZENEĞİ ÇALIŞTIR" denince bilye rampalardan zikzak yuvarlanır (potansiyel → kinetik), zile çarpar.
  3. Ağırlık iniyor, çarklar dönüyor, mekanik kuş zıplıyor; altın bir parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 yuvalı bir çark dizisi vardır. Doğru görevde yuvaya altın çark takılır; yanlışta kırık koyu çark (✕) kalır.
- **Çıkış:**
  1. Atölye düzeneğinin önünde 10 çarklık bir dişli dizisi belirir; altın çarklar dönmeye başlar.
  2. "USTA MÜHENDİS x/10 ÇARK" madalyası basılır.
  3. Sonuç "USTALIK BELGESİ" olarak açılır.

## Görevler (deneyler ve simülasyonlar)
| Tür | Görev | Mekanik |
|---|---|---|
| workcheck | İş dedektörü | Kuvvet (kırmızı) ve hareket (mavi) okları çizili durum kartlarına “İŞ VAR / İŞ YOK” damgası vurulur; cisimler ok yönünde hareket eder |
| workcalc | İş terazisi | Kuvvet ve yol grafikleri verilen kitaplar yapılan işe göre büyükten küçüğe sıralanır; kuvvet × yol alanları çizilir |
| classify | Enerji etiketi | Örneklere HAREKET / YÜKSEKLİK / ESNEKLİK etiketi verilir; örnekler canlanır |
| compare | Taş kulesi · Ağırlık düşürme · Yay mancınığı | Kütle-hız, kütle-yükseklik ya da sıkışma miktarı farklı düzeneklerden en büyük etkiyi yapacak olan (ya da “hepsi eşit”) seçilir; arabalar taş devirir, ağırlıklar su sıçratır, yaylar bilye fırlatır |
| bars | Enerji sütunları | Sarkaç, düşen top, eğik düzlem, pist, yay-araba ve yay-rampa düzeneklerinde her konumun K ve P küpleri (toplam 4) ayarlanır; deney oynatılır |
| trend | Kaykay pisti | Pistin her bölümünde P ve K’nin arttığı ya da azaldığı seçilir; kaykaycı kayar |
| convert | Dönüşüm zinciri | Bir olaydaki enerji dönüşümleri çeldiricilerle birlikte baştan sona sıralanır; düzenek çalışır |
| sort | Atölye defteri | İş yapılan/yapılmayan durumlar, esnek cisimler, enerji çeşitleri, etkenler, korunum, sürtünme, Cezerî ve bilim insanları |
| calc | Sayı çarkı | Raf yükseklikleri, kaçış rampası, küp sayıları, yedikule taşları, bilim insanlarının yılları |

Her deste kurulurken her konudan 2 görev seçilir. Görev türleri olabildiğince farklı tutulur.

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| is | 21 | Fiziksel anlamda işin koşulları, kuvvet ve yol ile ilişkisi, joule |
| tur | 18 | Kinetik, çekim potansiyel ve esneklik potansiyel enerjisi; esnek cisimler; enerji çeşitleri |
| etken | 20 | Kütle-hız (kinetik), ağırlık-yükseklik (çekim potansiyel), sıkışma-gerilme (esneklik potansiyel) |
| donusum | 22 | Sarkaç, top, eğik düzlem, pist ve yay düzeneklerinde kinetik-potansiyel dönüşümü |
| korunum | 21 | Enerjinin korunumu kanunu, sürtünme ile ısı ve ses, dönüşüm zincirleri, Cezerî, Galilei, Helmholtz, Joule, Rankine |

Görev türlerinin dağılımı: sort 17, compare 16, calc 12, classify 12, bars 12, convert 11, workcheck 9, trend 7, workcalc 6.

Yanlış-cevap kaydı:
- questionText görevi, durumları, kuvvet ve yol değerlerini, düzenekleri ya da kartları metin olarak içerir.
- studentAnswer öğrencinin damgalarını, etiketlerini, küp sayılarını, sıralamasını ya da girdiği sayıyı yazar.
- correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 7. Sınıf Ders Kitabı (1. kitap), 2. Ünite (s. 56–83).

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
