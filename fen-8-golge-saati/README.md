# Gölge Saati · Mevsimler ve İklim

| Alan | Değer |
|---|---|
| gameId | fen-8-golge-saati |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 1. Ünite: Mevsimler ve İklim |
| Ekran yönü | Dikey |
| Oyun türü | Güneş saati gözlemevi, karaktersiz. Her görev bir deney ya da gözlem düzeneğidir: yörüngeye Dünya yerleştirme, Yerküre'de şehirleri enlemlere sürükleyip ışın gönderme, yıl boyu grafiği elle çizme, ölçüme göre sıralama, gece-gündüz kadranı çevirme, sıcaklık tablosundan mühür basma, kanıt dosyalama, haber kartı fırlatma, el feneri açısı ayarlama. Şıklı soru yoktur. Görevlerin 48'i merkezî sınavda çıkmış soruların ikizi/gölgesidir; oyunda sınav, ders ya da sınıf adı geçmez. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Yok: görevler arasında ek bonus adımı yoktur, doğru görev doğrudan ⚡ puanı verir |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (⚡ puanı yıldızı etkilemez) |
| Soru havuzu | 109 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Gece gökyüzü, yıldızlar, ufukta pirinç bir güneş saati ve "GÖLGE SAATİ" tabelası; altta yalnızca "GÜNEŞİ DOĞUR" düğmesi.
- **Giriş:** Gökyüzü şafak renklerine döner, Güneş ufuktan yükselip yay çizer; güneş saatinin gölgesi uzun hâlinden kısalarak döner, saat tıkırdar, gün ağarır ve altın bir parlamayla oyuna geçilir.
- **İlerleme:** Üstte I–X roma rakamlı 10 saat işareti; doğru görevde ☀️, yanlışta ☁️.
- **Çıkış:** Gün batımı; büyük saat kadranında gölge ibresi döner, 10 saat işareti sırayla güneş ya da bulut olarak belirir; "GÜNEŞ SAATİ x/10 SAAT" madalyası basılır, sonuç "SAATÇİ KARNESİ" olarak açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| orbit | Yörünge | Dünya kartları (ekseni hep aynı yöne eğik) yörüngedeki 4 konuma sürüklenir; “Yörüngeyi döndür” ile Dünya bir tur atar, konumların tarihleri açılır |
| place | Enlem yerleştirme | Şehir işaretleri Yerküre'deki enlem çizgilerine sürüklenir; koşullar (gölge, enerji, gündüz süresi, yarım küre, dik ışın) tek tek ışın gönderilerek sınanır. Koşulları sağlayan her yerleşim kabul edilir |
| curve | Yıl boyu grafik | Aralık–Mart–Haziran–Eylül–Aralık noktaları yukarı-aşağı sürüklenerek gölge boyu, enerji ya da gündüz süresi grafiği çizilir; Güneş grafiği yürür, doğru eğri kesikli çizgiyle gelir |
| rank | Ölçüm rafı | Yerküre'deki şehirler raf yuvalarına sıralanır; ışınlar gelince ölçüm çubukları gerçek sırayı gösterir |
| day | Gece-gündüz kadranı | Her şehrin kadranına dokunularak gündüz dilimi uzun / eşit / kısa ayarlanır; ışınlar ve gece yarısı Yerküre'ye düşer |
| stamp | Sıcaklık mührü | Aylık sıcaklık tablosuna bakılarak şehirlere yarım küre (ve istenen ayın mevsimi) mührü basılır |
| facts | Kanıt panosu | Panodaki bilgilere göre ifade kartları “Bilgilere göre doğru” ya da “Yanlış ya da kesin değil” dosyasına taşınır |
| news | Yayın masası | Haber/görev kartları sağa-sola fırlatılarak Hava Durumu ↔ İklim Belgeseli ya da Meteorolog ↔ İklim bilimci tarafına gönderilir |
| lens | El feneri deneyi | Fener yay üzerinde sürüklenerek ışığın geliş açısı ayarlanır; aydınlanan alan ve birim alana düşen ışık canlı değişir |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur.

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| olusum | 16 | Eksen eğikliği, yörünge konumları, 21 Mart / 21 Haziran / 23 Eylül / 21 Aralık, yarım kürelerde zıt mevsimler, eksen eğik olmasaydı |
| isin | 21 | Işınların geliş açısı, birim yüzeye düşen enerji, dik ışın alan enlemler, el feneri modeli |
| golge | 24 | Öğle gölgesi boyu, yıl boyu gölge değişimi, gölge ile tarih/konum ilişkisi |
| gunduz | 30 | Gece-gündüz süreleri, yarım küreler, sıcaklık tablosundan yarım küre ve mevsim |
| iklim | 18 | Hava olayı ve iklim farkı, uzun yılların ortalaması, meteoroloji ve iklim bilimi (klimatoloji) |

Görev türlerinin dağılımı: place 19, orbit 16, rank 16, news 14, facts 12, curve 11, day 8, stamp 7, lens 6.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (kartlar, koşullar, enlem çizgileri, şehirlerin yeri, tablo değerleri, pano bilgileri) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (kartların konumları, şehirlerin enlemleri, grafik yükseklikleri, sıralama, kadran ayarları, mühürler, dosyalama, fener açısı).
- correctAnswer doğru çözümü (birden çok çözümlü görevlerde örnek bir doğru çözümü) yazar.
- sourceRef: 8. Sınıf Öğretim Programı, 1. Ünite “Mevsimler ve İklim”.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
