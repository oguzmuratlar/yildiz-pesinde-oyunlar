# Enerji Şebekesi · Elektrik Yükleri ve Elektrik Enerjisi

| Alan | Değer |
|---|---|
| gameId | fen-8-enerji-sebekesi |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 7. Ünite: Elektrik Yükleri ve Elektrik Enerjisi |
| Ekran yönü | Dikey |
| Oyun türü | Gece elektrik şebekesi kontrol masası, karaktersiz. Her görev bir düzenek ya da deneydir: sürtünmede elektronları elle taşıma, iplere asılı küreler, elektroskop, topraklama akışı, cihazları enerji prizlerine kabloyla bağlama, güç × süre sayacı, evde israf avı, enerji etiketi, santral haritası, santral enerji dönüşüm hattı, sigorta panosu bölmeleri. Şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "şebeke dengesi" bonusu: hava ve baraj durumuna göre güneş, rüzgâr ya da hidroelektrik santrali devreye alınır. Doğruysa +30 ⚡ ve direkte ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (⚡ puanı yıldızı etkilemez) |
| Soru havuzu | 101 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Yıldızlı gece, karanlık santral, enerji nakil hattı direkleri ve sönük şehir; sönük "ENERJİ ŞEBEKESİ" tabelası; altta yalnızca "ŞEBEKEYİ BAĞLA" düğmesi.
- **Giriş:** Santralin türbini dönmeye başlar, bir kıvılcım hat boyunca şehre koşar, tel parlar, şehrin pencereleri yanar, tabela neon gibi aydınlanır; sarı parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 elektrik direği; doğru görevde direk sarı yanar ve hat bağlanır (bonus doğruysa ★), yanlışta direk söner ve hat kesikli kalır.
- **Çıkış:** Gece manzarasında 10 kasaba sırayla yanar (doğrular ışıl ışıl, yanlışlar karanlık), "ŞEBEKE KARNESİ x/10 AYDINLANAN KASABA" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| rub | Sürtünme | İki cismin proton (+) ve elektronları (−) görünür; elektronlar tek tek sürüklenerek taşınır, protonlar yerinden oynamaz; sonra cisimler sürtülür ve yükler okunur |
| pend | Asılı küreler | Küre çiftlerinde sağdaki küre sola (çeker) ya da sağa (iter) sürüklenir; ya da gözlemlerden soru işaretli kürelerin yükü bulunur |
| scope | Elektroskop | Yaklaştırma, dokundurma ya da topraklamadan sonra yaprakların açıklığı sürüklenerek ayarlanır, toplam (ya da yaprakların) yükü seçilir |
| ground | Topraklama | Her cismin toprak kablosundaki elektron akışının yönü (↓ toprağa, ↑ cisme, akış yok) ve gerekirse elektron sayısı ayarlanır |
| plug | Enerji prizleri | Cihazların fişleri ısı, ışık, hareket prizlerine kabloyla bağlanır (zor görevlerde bir cihaz birden çok prize) |
| meter | Güç × süre sayacı | Cihazların çalışma süreleri ayarlanır, sayaç çalıştırılınca toplam kWh hedefle karşılaştırılır |
| house | Evde israf avı | Ev kesitindeki durumlardan enerjiyi boşa harcayanlara dokunulur |
| label | Enerji etiketi | Yıllık tüketim (gerekirse hesaplanarak) bulunur, ok etiketin doğru sınıfına sürüklenir |
| map | Santral haritası | Santral kartları haritadaki uygun yerlere (barajlı nehir, rüzgârlı tepe, güneşli düzlük, sıcak su kaynağı, kömür ocağı) yerleştirilir |
| pipe | Dönüşüm hattı | Santraldeki enerji dönüşümleri hattın kutularına sırayla dizilir, hat elektrik enerjisiyle biter |
| bin | Sigorta panosu | Kartlar pano bölmelerine ayrılır (çeker/iter, elektriklenme türü, fırtına güvenliği, yenilenebilir kaynak, santral avantaj/dezavantajı) |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| yuk | 21 | Elektrik yükleri, sürtünme/dokunma/etki ile elektriklenme, yüklerin etkileşimi |
| skop | 20 | Elektroskop, topraklama, yıldırım, paratoner |
| donusum | 20 | Elektrik enerjisinin ısı, ışık ve hareket enerjisine dönüşümü; güç, süre ve harcanan enerji |
| tasarruf | 20 | Bilinçli ve tasarruflu kullanım, enerji etiketi |
| santral | 20 | Santraller, kaynakları, enerji dönüşümleri, avantaj ve dezavantajlar |

Görev türlerinin dağılımı: meter 12, bin 15, rub 9, pend 9, scope 9, house 8, ground 8, plug 8, map 8, pipe 8, label 7.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (cisimlerin proton ve elektron sayıları, küreler ve gözlemler, elektroskobun başlangıç yükü ve yapılan işlem, cisimlerin yükleri, cihazlar ve güçleri, ev durumları, etiket sınıfları, haritadaki yerler, hat kartları) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (son elektron sayıları, etkileşimler, seçilen yükler, yaprak değişimi, akış yönleri, kablo bağlantıları, süreler ve sayaç toplamı, seçilen durumlar, sınıf, yerleşimler).
- correctAnswer doğru çözümü (birden çok çözümlü görevlerde uygun bir çözümü) yazar.
- sourceRef: 8. Sınıf Öğretim Programı, 7. Ünite “Elektrik Yükleri ve Elektrik Enerjisi”.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
