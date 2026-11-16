# Özdeşlik Yapbozu · Cebirsel İfadeler ve Özdeşlikler

| Alan | Değer |
|---|---|
| gameId | matematik-8-ozdeslik-yapbozu |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 6. Ünite: Cebirsel İfadeler ve Özdeşlikler |
| Ekran yönü | Dikey |
| Oyun türü | Ahşap yapboz atölyesi, karaktersiz. Her görev bir yapboz parçasıdır: katsayı kurucuyla ifade sadeleştirme, cebir karolarını okuma, şekilden alan/çevre ifadesi, çarpım tablosuna terim karoları sürükleme, alan modeline (özdeşlik) parça sürükleme, ifade–eş yapbozu, çarpanlara ayırma kalıbı seçip sayıları ayarlama, bölmeler, tuş takımı. Şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "kayıp parça" bonusu: iki eşitlikten doğru özdeşlik seçilir. Doğruysa +30 🧩 ve parçada ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🧩 puanı yıldızı etkilemez) |
| Soru havuzu | 102 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Ahşap masada boş yapboz tahtası, etrafa saçılmış renkli parçalar, mavi "ÖZDEŞLİK YAPBOZU" tabelası; altta yalnızca "YAPBOZU AÇ" düğmesi.
- **Giriş:** Dokuz parça dönerek uçup tahtaya tık tık oturur, altında (a + b)² = a² + 2ab + b² yazısı belirir; parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 parçalık şerit; doğru görevde renkli parça oturur (bonus doğruysa ★), yanlışta kesik çizgili boş parça.
- **Çıkış:** Görevlerin parçaları sırayla tahtaya iner (doğrular renkli, yanlışlar boş), "YAPBOZ KARNESİ x/10 PARÇA" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| poly | İfade sadeleştir / çarp / aç | x², x ve sayı katsayıları ▲▼ (basılı tutunca hızlanır) ile kurulur; canlı önizleme |
| tiles | Cebir karoları | Pozitif ve negatif x², x, 1 karoları okunup sıfır çiftleri götürülerek ifade kurulur |
| geo | Şekil ifadesi | Dikdörtgen, kare ya da kareden kare çıkarılmış şeklin alanı/çevresi katsayılarla kurulur |
| box | Çarpım tablosu | (ax + b)(cx + d) tablosunun hücrelerine terim karoları sürüklenir |
| model | Alan modeli | (a + b)² karesinin ya da a² − b² modelinin numaralı bölgelerine alan karoları sürüklenir |
| match | Yapboz eşleme | İfadeler eşleriyle (açılım, çarpanlar, sözel → cebirsel) yapboz yuvalarına yerleştirilir |
| factor | Çarpanlara ayırma | Kalıp seçilir (k(x + m), kx(x + m), (px + m)², (px − m)(px + m)) ve sayılar ayarlanır |
| bin | Bölmeler | Benzer terimler, özdeşlik olan/olmayan eşitlikler, çarpanlara ayırma yöntemi |
| key | Tuş takımı | Değer hesaplama ve özdeşlikle hızlı hesap (99 · 101, 51² − 49², x² + y²) |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 9 tür, aynı türden en çok 2).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| ifade | 21 | Cebirsel ifadeler, benzer terimler, sözel ifadeler, değer hesaplama |
| carpim | 20 | Bir terimli ve iki terimli ifadelerin çarpımı |
| ozdeslik | 20 | Tam kare ve iki kare farkı özdeşlikleri, alan modelleri |
| carpan | 20 | Ortak çarpan parantezi, özdeşliklerle çarpanlara ayırma |
| problem | 21 | Alan ve çevre ifadeleri, özdeşlikle hesaplama |

Görev türlerinin dağılımı: poly 24, factor 15, geo 14, key 12, box 9, tiles 8, match 8, model 7, bin 5.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (ifade, karolar, şeklin kenarları, tablo satır/sütunları, model, kalıplar) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (kurulan ifade, tablo hücreleri, model bölgeleri, eşleşmeler, seçilen kalıp ve sayılar, yazılan sayı).
- correctAnswer doğru ifadeyi ya da sonucu yazar; çarpanlara ayırmada aynı açılımı veren her doğru yazım kabul edilir.
- sourceRef: 8. Sınıf Öğretim Programı, 6. Ünite “Cebirsel İfadeler ve Özdeşlikler”.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
