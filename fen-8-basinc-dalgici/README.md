# Basınç Dalgıcı · Basınç

| Alan | Değer |
|---|---|
| gameId | fen-8-basinc-dalgici |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 3. Ünite: Basınç |
| Ekran yönü | Dikey |
| Oyun türü | Okyanusta dalış, karaktersiz. Her görev bir deney düzeneğidir: kum havuzunda blok dizme, hazır düzeneklerden karşılaştırma seçme, tuğla çevirme, kar yürüyüşünde ayakkabı seçme, dalgıç ağlarına kart atma, iki tanklı kontrollü deney, fıskiye şişesi, taban basıncı rafları, tıpalı kap, hidrolik sistem, dalgıcı derinliğe indirme. Şıklı soru yoktur. Görevlerin 63'i merkezî sınavda çıkmış soruların ikizi/gölgesidir; oyunda sınav, ders ya da sınıf adı geçmez. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "dalış bilgisayarı" bonusu: dalgıcın derinliğine göre basınçölçer değeri ayarlanır (her 10 m'de 1 birim). Doğruysa +40 🫧 ve ilerleme göstergesinde 💎. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🫧 puanı yıldızı etkilemez) |
| Soru havuzu | 102 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Güneşli deniz yüzeyi, dalgalarda sallanan yelkenli ve perçinli metal "BASINÇ DALGICI" levhası; altta yalnızca "DALIŞA BAŞLA" düğmesi.
- **Giriş:** Su yüzeyi aşağı akar, dalgıç yukarıdan suya dalar; kabarcıklar yükselir, balıklar geçer, yanda 0–100 m derinlik cetveli belirir; mavi parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10–100 m işaretli dalış ipi; doğru görevde 🐚 (bonus doğruysa 💎), yanlışta 🪨.
- **Çıkış:** Derinden yüzeye çıkış; toplanan inciler ve kayalar hazine sandığında belirir, "BASINÇ DALGICI x/10 İNCİ" lombar madalyası basılır, sonuç "DALIŞ KARNESİ" olarak açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| sand | Kum havuzu | Sütunlara dokunarak özdeş bloklar dizilir; düzenekler kuma bırakılır, iz derinlikleri ölçülür. Amaca uyan her düzenek kabul edilir |
| pick | Düzenek seçimi | Dört hazır düzenekten amaca uygun ikisine dokunulur |
| orient | Tuğla çevirme | Cisimlere dokunarak kuma değen yüzleri değiştirilir; istenen iz derinliği sağlanır |
| snow | Kar yürüyüşü | Kişilere dokunarak ayakkabıları (temas alanı) değiştirilir; kara gömülmeme ya da eşit iz koşulu sağlanır |
| net | Dalgıç ağları | Günlük yaşam kartları basıncı artıran/azaltan ya da derinlik/iletim ağlarına atılır |
| tank | İki tanklı deney | II. tankta sıvı, kap şekli, sıvı seviyesi (sürükle) ve basınçölçerin yeri (sürükle) ayarlanır; yalnızca istenen değişken farklı olmalı |
| holes | Fıskiye şişesi | Deliklerin fışkırma okları sürüklenerek uzunlukları derinliğe göre ayarlanır; aynı derinlikteki delikler eşit |
| order | Taban basıncı rafları | Kaplara dokunarak raf numarası verilir; eşit basınçlı kaplar aynı rafa |
| cork | Tıpalı kap | Kapağa basılınca ya da su dolarken fırlayacak tıpalara dokunulur; sıvı ile katının kuvvet/basınç iletimi karşılaştırılır |
| press | Hidrolik sistem | Küçük ve büyük piston alanları seçilir; yük kaldırılır |
| dive | Dalgıç derinliği | Dalgıç sürüklenerek basınçölçerin istenen değeri göstereceği derinliğe indirilir (göl, tuzlu deniz, zeytinyağı tankı) |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur.

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| kati | 21 | Katı basıncı: ağırlık ve yüzey alanının etkisi, kontrollü deney |
| katiy | 21 | Katı basıncının uygulamaları: sivri uç, geniş taban, kar ayakkabısı, perde halkaları, kitaplar |
| sivi | 19 | Sıvı basıncı: derinlik ve yoğunluk, kontrollü deney, dalgıç |
| siviy | 21 | Her yöne etki, kap şekli ve sıvı miktarından bağımsızlık, fıskiye şişesi |
| iletim | 20 | Sıvıların basıncı iletmesi, katı-sıvı karşılaştırması, hidrolik sistemler, günlük yaşam |

Görev türlerinin dağılımı: tank 14, sand 11, net 10, cork 10, orient 9, snow 9, holes 9, order 9, dive 8, press 7, pick 6.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (blok sayıları, cisimlerin ağırlık ve boyutları, kişiler ve ayakkabılar, tank ayarları, delik yükseklikleri, kaplar, tıpalar, piston seçenekleri) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (blok dizilimi, seçilen düzenekler, yüzler, ayakkabılar, tank ayarları, ok uzunlukları, raflar, işaretlenen tıpalar, piston alanları, derinlik).
- correctAnswer doğru çözümü (birden çok çözümlü görevlerde uygun bir çözümü) yazar.
- sourceRef: 8. Sınıf Öğretim Programı, 3. Ünite “Basınç”.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
