# Cam Fanus · Enerji Dönüşümleri ve Çevre Bilimi

| Alan | Değer |
|---|---|
| gameId | fen-8-cam-fanus |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 6. Ünite: Enerji Dönüşümleri ve Çevre Bilimi |
| Ekran yönü | Dikey |
| Oyun türü | Kapalı cam fanus (teraryum) laboratuvarı, karaktersiz. Her görev bir deney ya da düzenektir: besin ağı, enerji/birey/zararlı madde çubukları, iki fanuslu kontrollü deney, ışık rengi ve fotosentez hızı, gaz göstergeleri, maya balonları, madde döngüleri, karbon ayak izi şehri, saksılara ayırma. Şıklı soru yoktur. Görevlerin 61'i merkezî sınavda çıkmış soruların ikizi/gölgesidir; oyunda sınav, ders ya da sınıf adı geçmez. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "fanus dengesi" bonusu: fanustaki gaz durumuna göre ışığı açmak, kapatmak ya da salyangoz eklemek seçilir. Doğruysa +30 🍃 ve kabarcıkta ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🍃 puanı yıldızı etkilemez) |
| Soru havuzu | 101 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Karanlıkta, toprağı boş bir cam fanus ve üstünde "CAM FANUS" tabelası; altta yalnızca "FANUSU AYDINLAT" düğmesi.
- **Giriş:** Lamba yanar, ortam yeşile döner, topraktan filiz çıkıp yaprak açar, fanusta oksijen kabarcıkları yükselir, tabela yukarı süzülür; yeşil parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 kabarcıklık şerit; doğru görevde yeşil "O₂" kabarcığı (bonus doğruysa ★), yanlışta gri "CO₂" kabarcığı.
- **Çıkış:** Aydınlık fanustan sırayla kabarcıklar yükselir (doğrular yeşil O₂, yanlışlar gri CO₂), "FANUS KARNESİ x/10 O₂ KABARCIĞI" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| web | Besin ağı | Oklu besin ağında istenen role uyan canlılara dokunulur (üretici, birincil tüketici, hepçil, etçil, en üst tüketici) |
| flow | Ekoloji piramidi çubukları | Besin zincirinin basamaklarındaki enerji, birey sayısı ya da zararlı madde birikimi çubukları yukarı-aşağı sürüklenir |
| rate | Deney çubukları | Işık rengi, uzaklık, CO₂, su, sıcaklık, egzersiz gibi durumlarda fotosentez/solunum hızı çubukları kurulur; gerçek sıralama çizgilerle gösterilir |
| jar | İki fanuslu deney | I. fanus sabit; II. fanusun düğmeleri (ışık, ışığın rengi, CO₂/KOH, su, sıcaklık) yalnızca istenen değişken farklı olacak biçimde ayarlanır; fanuslarda kabarcıklar çıkar |
| gas | Gaz göstergeleri | Fanus sahnesindeki her gösterge için artar / azalır / değişmez seçilir, 24 saat beklenir |
| balloon | Maya balonları | Şeker, maya ve sıcaklığı farklı şişelerin balonlarına dokunarak büyüklük tahmini yapılır |
| cycle | Madde döngüleri | Su, karbon, oksijen ve azot döngüsü şemasındaki numaralı oklara olay kartları sürüklenir |
| foot | Karbon ayak izi şehri | Ulaşım, elektrik, ısınma, atık, alışveriş seçimleri değiştirilir; ayak izi sınırın altına indirilir |
| bin | Saksılar | Kavram kartları saksılara yerleştirilir (üretici/tüketici/ayrıştırıcı, fotosentez/solunum, oksijenli/oksijensiz solunum, geri dönüşüm/yeniden kullanım, küresel ısınmanın nedeni/sonucu) |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| zincir | 22 | Besin zinciri ve ağı, üretici-tüketici-ayrıştırıcı, enerji akışı, ekoloji piramidi, biyolojik birikim |
| foto | 24 | Fotosentez, etkileyen faktörler (ışık şiddeti ve rengi, CO₂, su, sıcaklık), kontrollü deney |
| solunum | 20 | Oksijenli ve oksijensiz solunum, mayalanma, fermantasyon, solunum hızı |
| dongu | 17 | Su, karbon, oksijen ve azot döngüleri |
| cevre | 18 | Küresel ısınma, karbon ve ekolojik ayak izi, geri dönüşüm, sürdürülebilir kaynak kullanımı |

Görev türlerinin dağılımı: bin 26, gas 12, rate 11, web 10, jar 10, cycle 9, flow 8, foot 8, balloon 7.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (besin ağındaki canlılar ve oklar, zincirin basamakları, fanusların ayarları, sahne, şişelerin içeriği, döngü kutuları, şehir seçenekleri ve sınır, kartlar) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (seçtiği canlılar, çubuk değerleri, II. fanusun ayarları, gösterge tahminleri, balon büyüklükleri, oklara konan kartlar, şehir seçimleri ve toplam, saksılar).
- correctAnswer doğru çözümü (birden çok çözümlü görevlerde uygun bir çözümü) yazar.
- sourceRef: 8. Sınıf Öğretim Programı, 6. Ünite “Enerji Dönüşümleri ve Çevre Bilimi”.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
