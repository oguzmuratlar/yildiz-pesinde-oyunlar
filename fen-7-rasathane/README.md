# Rasathane · Uzay Çağı

| Alan | Değer |
|---|---|
| gameId | fen-7-rasathane |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Ünite | 1. Ünite: Uzay Çağı |
| Ekran yönü | Dikey |
| Oyun türü | Dağ zirvesindeki gözlemevinde (rasathane) geçen gece gözlemi temalı uzay simülasyonları. Öğrenci karakteri yoktur; gök haritasındaki yıldızlar ilerlemeyi gösterir. Test ve doğru/yanlış sorusu yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (✨ puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 108 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:**
  1. Yıldızlı gece, Samanyolu ışıltısı, dağ silueti ve zirvede kubbeli gözlemevi; "RASATHANE" tabelası.
  2. "KUBBEYİ AÇ" denince kubbe kapakları iki yana kayar, teleskop gökyüzüne döner, ışık hüzmesi uzanır, bir yıldız kayar.
  3. Mercek görünümü: ekran teleskop okülerinden açılan bir daireyle oyuna geçer.
- **İlerleme:** Üstte 10 yıldızlık bir gök haritası vardır. Doğru görevde yıldız yanar ve önceki yanan yıldıza çizgiyle bağlanır; yanlışta yıldız sönük (✕) kalır.
- **Çıkış:**
  1. Gözlemevinin üstündeki gökyüzünde yanan yıldızlar sırayla parlar ve takımyıldız çizgileri çizilir.
  2. "GÖK HARİTASI x/10 YILDIZ" madalyası basılır.
  3. Sonuç "GÖZLEM RAPORU" olarak açılır.

## Görevler (simülasyonlar)
| Tür | Görev | Mekanik |
|---|---|---|
| feature | Görev panosu | Özellik × uzay aracı (sonda, roket, uydu, mekik, istasyon, teleskop) panosunda geçerli hücreler ✓ ile işaretlenir; araçlar tek tek test edilir |
| satellite | Uydu yörüngesi | Türk uyduları haberleşme / gözlem (zorda "görevi bitti") olarak atanır; uydular yörüngeye yerleşir, yayın ışını ya da gözlem konisi gösterilir |
| timeline | Fırlatma takvimi | Uydular fırlatılma sırasına dizilir; zaman çizelgesinde yıllarına fırlatılır |
| site | Gözlemevi yeri | Rakım, ışık kirliliği, hava, deprem, verici raporlarına göre en uygun bölge seçilir; her bölgenin gökyüzü yıldız sayısıyla gösterilir |
| debris | Uzay çöpü avı | Dünya çevresindeki cisimlerden uzay kirliliği oluşturanlar işaretlenir; temizlik ağı fırlatılır |
| lifecycle | Yıldız yaşam yolu | Kütlesi verilen yıldızın aşamaları (çeldiricilerle) sıraya dizilir; yıldız bulutsudan son aşamaya dönüşür (süpernova patlaması, kara delik …) |
| color | Yıldız termometresi | Renkli yıldızlara SICAK/ORTA/SOĞUK etiketi verilir; spektrometre termometrede sonucu gösterir |
| sizes | Yıldız boyları | Yıldızlar küçükten büyüğe dizilir; yan yana büyütülerek karşılaştırılır |
| polaris | Kuzeyi bul | Döndürülmüş Büyükayı’da Kutup Yıldızı adayı (A–D) seçilir; cezve ucundaki iki yıldız arası 5 kez uzatılır |
| constel | Gökyüzü atlası | Yıldız desenlerine (zorda çizgisiz) takımyıldız adı yerleştirilir; çizgiler çizilir |
| zoom | Evren zoomu | Dünya → Güneş sistemi → Avcı kolu → Samanyolu → Evren (ve adres benzetmesi) sıraya dizilir; iç içe halkalarla zoom geri çekilir |
| sort | Gözlem arşivi | Teleskop türleri, kavramlar, kurumlar, astronotlar, bilim insanları, teknoloji transferi, uzay kirliliği, bulutsular, yıldız yaşı |
| calc | Sayı çarkı | Uydu ve teleskop yılları, görev süreleri, Kutup Yıldızı mesafesi, ışığın hızı, bilim insanlarının yaşamları |

Her deste kurulurken her konudan 2 görev seçilir. Görev türleri olabildiğince farklı tutulur.

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| arac | 18 | Uzay sondası, roket, yapay uydu, mekik, istasyon, teleskop; uzay ve yer tabanlı teleskoplar; astronomi kavramları |
| turk | 21 | Türk uyduları ve fırlatma yılları, TÜBİTAK UZAY, TUA, TEKNOFEST, Alper Gezeravcı, Yuri Gagarin, Nüzhet Toydemir Gökdoğan, Ali Yar |
| sorun | 20 | Gözlemevi yeri seçimi, TUG/DAG, ışık kirliliği, uzay kirliliği ve çözümleri, uzay teknolojilerinin günlük hayattaki kullanımı |
| yasam | 24 | Bulutsular, küçük ve büyük kütleli yıldızların yaşam süreci, yıldız renkleri ve sıcaklıkları, yıldız büyüklükleri, yaş tahmini |
| evren | 25 | Kutup Yıldızı ve Büyükayı, takımyıldızlar, yıldız kayması, galaksi, evren, ışık yılı, Einstein, Hubble, Goddard |

Görev türlerinin dağılımı: sort 19, calc 15, feature 11, lifecycle 9, satellite 8, site 7, debris 7, color 6, polaris 6, constel 6, sizes 5, zoom 5, timeline 4.

Yanlış-cevap kaydı:
- questionText görevi, araçları, uyduları, aday bölgeleri, yıldızları ya da seçenekleri metin olarak içerir.
- studentAnswer öğrencinin işaretlerini, atamalarını, sıralamasını ya da girdiği sayıyı yazar.
- correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 7. Sınıf Ders Kitabı (1. kitap), 1. Ünite (s. 12–55).

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
