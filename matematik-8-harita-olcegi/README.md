# Harita Ölçeği · Eşlik ve Benzerlik, Dönüşüm Geometrisi

| Alan | Değer |
|---|---|
| gameId | matematik-8-harita-olcegi |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 10. Ünite: Eşlik ve Benzerlik · 11. Ünite: Dönüşüm Geometrisi |
| Ekran yönü | Dikey |
| Oyun türü | Haritacı masası, karaktersiz. Her görev bir harita işidir: adayı sürükleyerek öteleme, öteleme okunu kurma, yansıma görüntüsünün köşelerini ızgaraya koyma, yansıma ekseni + öteleme okunu seçip çalıştırma (ardışık dönüşüm), doğru haritayı seçme, köşe tutamacını sürükleyerek benzer/eş parsel çizme, benzer şekilde eksik kenarı ayarlama, bölmeler, tuş takımı. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "fener nerede?" bonusu: bir noktanın x ya da y eksenine göre yansıması iki seçenekten bulunur. Doğruysa +30 🧭 ve rota iğnesinde ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🧭 puanı yıldızı etkilemez) |
| Soru havuzu | 100 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Ahşap haritacı masası, rulo parşömen, "HARİTA ÖLÇEĞİ" tabelası; altta yalnızca "HARİTAYI AÇ" düğmesi.
- **Giriş:** Parşömen açılır, adalar belirir, pusula gülü dönerek yerine oturur, kesikli rota çizilir ve yelkenli rota boyunca ilerler; parlamayla oyuna geçilir.
- **İlerleme:** Üstte parşömen şeritte kesikli rota üzerinde 10 iğne; doğru görevde iğne kırmızı ✓ (bonus doğruysa ★), yanlışta gri ✕.
- **Çıkış:** Parşömende 10 bölge sırayla belirir (doğrular ada/dağ ✓, yanlışlar sis ☁️ ✕), "HARİTA KARNESİ x/10 BÖLGE" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| trans | Adayı taşı | Şekil koordinat düzleminde sürüklenir, tam birimlere oturur; istenen ötelemeye bırakılır |
| tvec | Öteleme oku | Şekil ve görüntüsü verilir; yatay ve dikey kayma ayarlanır, ok canlı çizilir, çalıştırınca şekil kayar |
| refl | Yansıt | Yansıma (ya da ardışık dönüşüm) görüntüsünün köşeleri A′, B′, C′… sırasıyla ızgaraya konur; geri alınabilir |
| chain | Ardışık dönüşüm | Yansıma ekseni seçilir, öteleme oku kurulur; çalıştırınca şekil önce yansır sonra kayar |
| gsel | Harita seç | Dönüşüm sonucu oluşan görüntü üç mini haritadan seçilir |
| enlarge | Parsel çiz | Köşe tutamacı sürüklenerek örnek parsele eş ya da verilen oranda benzer dikdörtgen/dik üçgen çizilir |
| missing | Eksik kenar | Benzer iki şeklin (üçgen, dikdörtgen, yamuk) eksik kenarı ayarlanır |
| bin | Bölmeler | Eş/benzer/benzer değil, her zaman benzer mi, değişen–değişmeyen, öteleme mi yansıma mı, eksen türü |
| key | Tuş takımı | Koordinat, açı, kenar, çevre, alan ve oran soruları |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| esbenz | 20 | Eşlik ve benzerlik; eş ve benzer şekillerin kenar ve açı özellikleri |
| oran | 20 | Benzerlik oranı; eş ve benzer çokgen oluşturma |
| oteleme | 20 | Öteleme |
| yansima | 20 | Eksenlere göre yansıma |
| ardisik | 20 | Ardışık öteleme ve yansıma |

Görev türlerinin dağılımı: key 21, refl 16, missing 13, enlarge 11, trans 8, bin 8, gsel 8, chain 8, tvec 7.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (köşe koordinatları, görüntü koordinatları, parsel ölçüleri ve oran, şekillerin kenarları) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (kaydırma miktarı ve yeni köşeler, öteleme oku, konulan noktalar, seçilen eksen ve ok, seçilen harita, çizilen parsel ölçüleri, x değeri).
- correctAnswer doğru sonucu yazar.
- sourceRef: 8. Sınıf Öğretim Programı, 10. Ünite “Eşlik ve Benzerlik” ve 11. Ünite “Dönüşüm Geometrisi”.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
