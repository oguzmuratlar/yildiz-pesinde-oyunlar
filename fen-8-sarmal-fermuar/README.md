# Sarmal Fermuar · DNA ve Genetik Kod

| Alan | Değer |
|---|---|
| gameId | fen-8-sarmal-fermuar |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 2. Ünite: DNA ve Genetik Kod |
| Ekran yönü | Dikey |
| Oyun türü | Terzi atölyesi ve dev bir fermuar, karaktersiz. Her görev bir düzenek ya da deneydir: fermuar dişlerine baz takıp fermuarı kapatma, model etiketlerini dikme, nükleotit sayaçları, eşleme makinesi, çaprazlama tezgâhı, kare tablo, ortam deneyi dolabı, mutasyon mercekle tarama, avcı gözüyle doğal seçilim, dikiş dolabı çekmeceleri, klonlama ve gen aktarımı tezgâhı. Şıklı soru yoktur. Görevlerin 64'i merkezî sınavda çıkmış soruların ikizi/gölgesidir; oyunda sınav, ders ya da sınıf adı geçmez. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "fermuar bonusu": üstteki 4 bazın eşini (A–T, G–C) sırayla takarak fermuarı kapatma; her diş +15 🧵. Ünitenin baz eşleşme kuralı oyun kuralıdır. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🧵 puanı yıldızı etkilemez) |
| Soru havuzu | 102 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Dikişli kumaş zemin, ortada renkli dişleri (A, T, G, C) kenetli kapalı bir fermuar ve dikişli "SARMAL FERMUAR" etiketi; altta yalnızca "FERMUARI AÇ" düğmesi.
- **Giriş:** Fermuar çekeceği aşağı kayar, kumaşın iki yanı açılır, altından dönen bir DNA sarmalı belirir; pembe-mavi parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 dişlik yatay fermuar; doğru görevde renkli baz çifti kenetlenir (bonus tamsa ★), yanlışta diş gri ve açık kalır.
- **Çıkış:** Dikey fermuar; çekecek yukarıdan aşağı inerken doğru görevlerin baz çiftleri kenetlenir, yanlışlar açık kalır; "SARMAL FERMUAR x/10 DİŞ" madalyası basılır, sonuç "TERZİ KARNESİ" olarak açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| zip | Fermuar | Boş dişlere dokunarak baz takılır (A→T→G→C); zor görevlerde aynı numaralı dişler aynı bazdır. Çekecek kayar, eşleşen dişler kenetlenir, eşleşmeyende fermuar takılır |
| parts | Etiket dikme | Fosfat/şeker/organik baz/nükleotit/gen/DNA/kromozom etiketleri modeldeki numaralı yerlere sürüklenir (fazladan etiketler var) |
| count | Nükleotit sayaçları | A=T, G=C ve şeker=fosfat=nükleotit kuralıyla sayaçlar ±1/±10 ile ayarlanır |
| copy | Eşleme makinesi | Ayrılan iki eski zincire uygun yeni zincir kartları sürüklenir (benzer çeldirici zincirler var); iki yeni DNA'nın her biri bir eski + bir yeni zincirden oluşur |
| cross | Çaprazlama tezgâhı | Ebeveynlere dokunarak genotip seçilir; hedef (ör. 3:1, yarı yarıya, hem mor hem beyaz) tutmalı. 2×2 tablo dolar, dört yavru çiçek/tohum açar. Hedefi tutan her çaprazlama kabul edilir |
| punnett | Kare tablo | Ebeveynleri verilen tablonun kutularına dokunarak yavru genotipleri yazılır; fenotip simgesi canlı değişir |
| env | Ortam deneyi | Örnek seçilir, deney dolabının ortamı (sıcaklık, toprak, buz torbası, hava/su) ayarlanır; gelişen canlı görünüşü gösterir (modifikasyon) |
| mutate | Mutasyon merceği | Normal ve değişmiş gen karşılaştırılıp değişen dişlere dokunulur; üreme/vücut hücresine göre yavrulara aktarılma ayarlanır |
| select | Avcı gözü | Ortama uymayan (avlanacak) ya da hayatta kalacak bireylere dokunulur; avcı geçer, uyumlular çoğalır |
| drawer | Dikiş dolabı | Kumaş kartları çekmecelere yerleştirilir (mutasyon/modifikasyon/adaptasyon; klonlama/gen tedavisi/ıslah/gen aktarımı; yarar/risk) |
| lab | Laboratuvar tezgâhı | Çekirdek ya da gen jetonu doğru kaynaktan hedefe sürüklenir; klonun görünüşü, yavrulara aktarılma gibi sonuçlar tahmin edilir |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur.

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| yapi | 19 | Nükleotit (fosfat-şeker-organik baz), DNA modeli, baz eşleşmesi, kromozom-DNA-gen-nükleotit ilişkisi, nükleotit sayıları |
| eslenme | 21 | DNA'nın kendini eşlemesi, eski ve yeni zincirler, eşleme sonrası nükleotit sayıları |
| kalitim | 21 | Mendel çaprazlamaları, baskın-çekinik, genotip-fenotip, saf döl-melez, 3:1 ve 1:1 oranları |
| degisim | 22 | Mutasyon, modifikasyon, adaptasyon, doğal seçilim |
| biyotek | 19 | Klonlama, gen aktarımı, gen tedavisi, ıslah, biyoteknolojinin yarar ve riskleri |

Görev türlerinin dağılımı: zip 14, lab 14, cross 12, count 10, copy 9, punnett 9, drawer 8, parts 7, env 7, mutate 6, select 6.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (zincir dizileri, model parçaları, bilgiler, ebeveynler, ortamlar ve örnekler, gen dizileri, bireyler, kartlar, kaynak-hedefler) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (taktığı bazlar, etiketler, sayaç değerleri, eşlediği zincirler, seçtiği çaprazlama, tablo, ortam, işaretlediği dişler/bireyler, çekmeceler, laboratuvar seçimleri).
- correctAnswer doğru çözümü (birden çok çözümlü görevlerde uygun bir çözümü) yazar.
- sourceRef: 8. Sınıf Öğretim Programı, 2. Ünite “DNA ve Genetik Kod”.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
