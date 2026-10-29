# Dengo'nun Üçgen Sirki · Geometrik Şekiller

| Alan | Değer |
|---|---|
| gameId | matematik-7-dengo-ucgen-sirki |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Tema | 5. Tema: Geometrik Şekiller |
| Ekran yönü | Dikey |
| Oyun türü | Test ve doğru/yanlış içermeyen dokunmatik oyun: burnunda üçgen çeviren fok Dengo + gece sirki çadırı (doğru görevde çadıra renkli bir flama asılır, yanlışta gri yırtık flama kalır) + flama sayacı ve 🔥 seri. Görevler: noktayı kenar boyunca kaydırarak açıortay/kenarortay/yükseklik/kenar orta dikme kurma, kâğıt üçgeni katlama, yardımcı elemanlara etiket yapıştırma, araçla çizip kesişim noktasını bulma, halkalara top koyma, kart sıralama, doğru sayı topunu halkaya atma. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken türler dengelenir; süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 122 görev (26 kaydır ve kur, 25 topu at, 21 dengeyi bul, 17 halkalara top, 12 kâğıt katla, 11 sırala, 10 etiket yapıştır), index.html içine gömülüdür |

## Oyun

Rehber karakter **Dengo**, burnunda üçgen levha çevirerek denge gösterisi yapan bir foktur. Konuşma balonuyla görevi anlatır; doğru cevapta yüzgeçlerini çırpıp zıplar, yanlışta levhası düşer ve cesaret verir. Ekranın üstündeki sirk çadırına her doğru görevde bir flama asılır.

- **Kaydır ve kur:** Kırmızı nokta kenar (gerekirse kenarın uzantısı) boyunca kaydırılır. Ekranda cetvel ölçüleri (|BD|, |DC|) ve açıölçer ölçüleri (m(BAD), m(DAC), m(ADC)) canlı görünür; öğrenci hangi ölçünün eşit ya da 90° olması gerektiğine karar verir. Kenar orta dikmede doğru ayrıca sarı tutamaçla döndürülür. Ölçme payı 0,28 cm ve 4°'dir.
- **Kâğıt katla:** Kâğıttan üçgenin bir köşesi parmakla sürüklenir; kâğıt canlı olarak katlanır ve kat izi görünür. Köşe dört yıldızdan birine bırakılır (öbür köşe → kenar orta dikme, kenar üzerine kenar → açıortay, kat izi karşı köşeden geçecek biçimde kenar üzerine → yükseklik). “Kâğıdı aç” ile geri alınır.
- **Etiket yapıştır:** Renkli doğru parçaları eş açı yayları, eşlik çizgileri ve dik açı işaretleriyle (zor görevlerde ölçülerle) çizilir; Açıortay / Kenarortay / Yükseklik / Kenar orta dikme etiketleri sürüklenerek ya da dokunarak satırlara yapıştırılır. Bazı görevlerde bir etiket artar.
- **Dengeyi bul:** Kareli zeminde araç (açıortay, kenarortay, yükseklik, kenar orta dikme) seçilip köşelere dokunularak çizgiler çizilir; ⭐ kesişim noktasına sürüklenir (ağırlık merkezi, yüksekliklerin, açıortayların ya da kenar orta dikmelerin kesiştiği nokta; dış bölgede ve köşede olanlar dahil).
- **Halkalara top:** İfadeler; çeşitkenar/ikizkenar/eşkenar, dar/dik/geniş açılı, iç bölge/köşe/dış bölge, temel/yardımcı eleman ya da dört yardımcı eleman halkalarına göre sınıflandırılır (bazılarında birden çok halka doğrudur).
- **Sırala:** Kenarortay, kenar orta dikme ve açıortay inşa adımları, gönyeyle yükseklik çizme adımları ve aynı köşeden çizilen yükseklik/açıortay/kenarortayın uzunluk sırası.
- **Topu at:** Kenarortay, açıortay, yükseklik, katlama ve özel üçgen problemlerinde doğru sayı topu halkaya sürüklenir (her destede en fazla 2).

Yanlış-cevap kaydında öğrencinin yerleştirdiği nokta ve ekrandaki ölçüler, katladığı yer, yapıştırdığı etiketler, ⭐ konumu (sol alt köşe (0, 0) kabul edilen kare koordinatlarıyla) ve çizdiği çizgiler, halka seçimleri, kart sırası ya da seçtiği sayı ile doğru cevap yazılır. Şekiller kayda “[Şekil: …]” biçiminde metin olarak eklenir.

## Soru havuzu

| Grup | İçerik |
|---|---|
| aciortay | Açıortay tanımı ve kurulması, katlamayla açıortay, açıortay inşa adımları, açıortayların kesişim noktası, açı hesapları, katlamada çevre |
| yukseklik | Yükseklik (kenarın uzantısına inen dahil), katlamayla yükseklik, gönyeyle çizim, yüksekliklerin kesişim noktasının yeri, açı hesapları |
| ortadikme | Kenar orta dikme kurma ve katlama, orta dikme inşası, kenar orta dikmelerin kesişim noktası, katlamada eşit uzaklık ve çevre |
| kenarortay | Kenarortay, ağırlık merkezi, kenarortay inşası, kenarortaylı çevre problemleri |
| ozel | Çeşitkenar/ikizkenar/eşkenar üçgenlerde çakışan yardımcı elemanlar, temel ve yardımcı eleman, aynı köşeden çizilen elemanların uzunluk sırası |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır.

Kaynak: MEB Matematik 7. Sınıf Ders Kitabı 2. Kitap, 5. Tema (s. 12–34).
