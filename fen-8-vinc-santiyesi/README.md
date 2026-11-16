# Vinç Şantiyesi · Basit Makineler

| Alan | Değer |
|---|---|
| gameId | fen-8-vinc-santiyesi |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 5. Ünite: Basit Makineler |
| Ekran yönü | Dikey |
| Oyun türü | İnşaat şantiyesi, karaktersiz. Her görev bir düzenek kurma ya da deneydir: kaldıraç dengesi, kaldıraç kurma, makara sistemi, iş terazisi, rampa, eğim rafları, vida seçimi, çıkrık, dişli çarklar, kasnaklar, malzeme kasaları. Şıklı soru yoktur. Görevlerin 42'i merkezî sınavda çıkmış soruların ikizi/gölgesidir; oyunda sınav, ders ya da sınıf adı geçmez. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "vinç dengesi" bonusu: vincin taşıdığı yüke göre karşı ağırlığın bölmesi seçilir (yük × kol = karşı ağırlık × kol). Doğruysa +30 🔩 ve kirişte ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🔩 puanı yıldızı etkilemez) |
| Soru havuzu | 102 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Gece şantiyesi, kule vinç, yerde sarı-siyah şeritli "VİNÇ ŞANTİYESİ" tabelası; altta yalnızca "ŞANTİYEYİ AÇ" düğmesi.
- **Giriş:** Projektörler yanar, gökyüzü aydınlanır, arkada bina yükselir; vincin kancası tabelayı yukarı kaldırır; sarı parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 kirişlik bir şerit; doğru görevde turuncu çelik kiriş yerleşir (bonus doğruysa ★), yanlışta boş kesikli çerçeve.
- **Çıkış:** Gün batımında bina kat kat yükselir (doğru görevler pencereli kat, yanlışlar iskele), tepesine bayrak dikilir, "VİNÇ ŞANTİYESİ x/10 KAT" madalyası basılır, sonuç "ŞANTİYE KARNESİ" olarak açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| lever | Kaldıraç dengesi | Eşit bölmeli çubukta blok ya da destek sürüklenir veya boş kancanın yükü ayarlanır; çubuk dengeye göre eğilir |
| build | Kaldıraç kur | Destek, Yük ve Kuvvet kartları çubuğun deliklerine sürüklenir; kuvvet kolu ve yük kolu çizilir |
| pulley | Makara sistemi | Hareketli/sabit makara eklenip çıkarılır; kuvvet sınırı ve yön koşulu sağlanmalı |
| trade | İş terazisi | Kuvvet ve yol sayaçları ayarlanır; "yük × yol" ile "kuvvet × yol" kefeleri dengelenir |
| ramp | Rampa | Rampanın ucu sürüklenerek uzunluğu ayarlanır; kutu kamyona itilir |
| slope | Eğim rafları | Rampalara gereken kuvvete göre raf numarası verilir (eşit eğimler aynı raf) |
| screw | Vida | Diş aralığına göre en az kuvvet ya da en az tur gerektiren vida seçilir |
| wheel | Çıkrık | Kol uzunluğu sürüklenir, silindir değiştirilir; kova kuyudan çekilir |
| gear | Dişliler | Dişlilere dokunarak dönme yönü, sayaçla tur sayısı ayarlanır |
| belt | Kasnaklar | Düz/çapraz kayış seçilir, 2. kasnağın tur sayısı ayarlanır |
| crate | Malzeme kasaları | Alet ve ifade kartları kasalara yüklenir (makine türü, kazanç türü, kaldıraç türü, doğru/yanlış) |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur.

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| kaldirac | 21 | Denge, kuvvet kolu-yük kolu, kaldıraç türleri |
| makara | 21 | Sabit-hareketli makara, palanga, yön değişimi, kuvvet-yol |
| egik | 20 | Eğik düzlem uzunluğu ve eğimi, vida |
| cark | 21 | Çıkrık, dişli çarklar, kasnaklar |
| genel | 19 | İşten kazanç olmaması, kuvvet-yol ilişkisi, bileşik makineler, günlük yaşam aletleri |

Görev türlerinin dağılımı: crate 16, trade 15, pulley 12, lever 10, build 9, ramp 9, wheel 7, gear 7, belt 7, slope 5, screw 5.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (çubuktaki yükler ve konumları, yük ve kuvvet sınırları, rampa/çıkrık değerleri, diş sayıları, kasnak yarıçapları, kartlar) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (blok/destek konumu, kart yerleşimi, makara sayısı, sayaç değerleri, rampa uzunluğu, seçilen vida, kol ve silindir, dönme yönleri, kayış türü, kasalar).
- correctAnswer doğru çözümü (birden çok çözümlü görevlerde uygun bir çözümü) yazar.
- sourceRef: 8. Sınıf Öğretim Programı, 5. Ünite “Basit Makineler”.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
