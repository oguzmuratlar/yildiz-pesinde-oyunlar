# Editör Masası · Yazım, Noktalama ve Anlatım Bozuklukları

| Alan | Değer |
|---|---|
| gameId | turkce-8-editor-masasi |
| Güncel sürüm | 1.0.0 |
| Ders | Türkçe (oyun içi subjectId: turkish; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Konu | Yazım kuralları (büyük harf, kesme işareti, bitişik/ayrı yazılanlar, sık karıştırılan sözcükler), noktalama işaretleri, anlatım bozuklukları |
| Ekran yönü | Dikey |
| Oyun türü | Yayınevi düzelti masası, karaktersiz. Her görev bir editörlük işidir: kırmızı kalemle büyük harf düzeltme, daktiloda ek yazma, boşluklara dokunarak mizanpaj (birleştir/ayır), yanlış yazılan sözcükleri daire içine alma, noktalama mühürlerini kutulara basma, gereksiz sözcüğün üstünü çizme, doğru düzelti notunu sayfaya yapıştırma, kartları dosyalara ayırma. Şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "Hızlı düzelti" (iki yazımdan doğrusunu seç). Doğruysa +30 ✒️ ve baskı sırasında ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (✒️ puanı yıldızı etkilemez) |
| Soru havuzu | 100 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Ahşap çalışma masası, masa lambası ışığı, kahve ve kitaplar; altta yalnızca "MASAYA OTUR" düğmesi.
- **Giriş:** Çizgili müsvedde sayfası masaya düşer; kırmızı kalem "herkez" ve "yanlız" sözcüklerini daire içine alıp doğrularını üstüne yazar; daktilo "EDİTÖR MASASI" başlığını harf harf yazar, zil çalar, "BASKIYA HAZIR" mührü basılır; parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 sayfalık baskı sırası; doğru görevde ✔ işaretli temiz sayfa (bonus doğruysa ★), yanlışta buruşturulmuş kâğıt topu ✕.
- **Çıkış:** Lacivert kitabın içine 10 sayfa sırayla dizilir (yanlışlar gri), "BASKI KARNESİ x/10 SAYFA" mührü basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| caps | Kırmızı kalem | Küçük harfle yazılmış taslakta büyük harfle başlaması gereken sözcüklere dokunulur; ilk harf kırmızıyla büyür |
| typewriter | Daktilo | Özel ada, kısaltmaya ya da rakama gelen ek daktilo tuşlarıyla yazılır (kesme işareti dahil) |
| joiner | Mizanpaj | Hatalı dizilmiş cümlede boşluklara dokunularak sözcükler birleştirilir ya da ayrılır (de, ki, mi, birleşik sözcükler) |
| hunt | Daire çiz | Yazımı yanlış olan bütün sözcükler kırmızı daire içine alınır |
| punct | Noktalama mührü | Mühür (. , ; : ? ! …) seçilip cümledeki boş kutulara basılır |
| strike | Üstünü çiz | Gereksiz sözcüğün üstünden kalemle çizgi çekilir |
| sticky | Düzelti notu | Bozuk cümleyi doğru düzelten yapışkan not sayfaya sürüklenir |
| bin | Dosyalama | Kesme işareti alır/almaz, bitişik/ayrı, bağlaç/ek, noktalama işlevleri, bozukluk türleri |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| buyuk | 20 | Büyük harflerin ve kesme işaretinin kullanımı |
| bitisik | 20 | Bitişik ve ayrı yazılanlar (de, ki, mi; birleşik sözcükler; sayılar) |
| yazim | 20 | Sık karıştırılan yazımlar; kısaltma ve rakamlara gelen ekler |
| noktalama | 20 | Nokta, virgül, noktalı virgül, iki nokta, üç nokta, soru ve ünlem işareti; kesme, tırnak, yay ayraç |
| anlatim | 20 | Gereksiz sözcük, özne-yüklem uyumsuzluğu, mantık hatası, yanlış anlamda sözcük, yüklem/öge eksikliği, çatı uyuşmazlığı, anlam belirsizliği |

Görev türlerinin dağılımı: bin 19, joiner 14, hunt 14, punct 14, typewriter 12, caps 10, strike 9, sticky 8.

Bütün cümleler özgündür.

Yanlış-cevap kaydı:
- questionText görevi ve taslağı (küçük harfli cümle, hatalı dizgi, boş kutulu cümle, notlar, kartlar) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (düzelttiği cümle, yazdığı ekli sözcük, dizdiği cümle, daire çizdiği sözcükler, mühürlü cümle, çizdiği sözcük, seçtiği not, kart yerleşimleri).
- correctAnswer doğru sonucu yazar.
- sourceRef: 8. Sınıf Öğretim Programı, Yazım ve Noktalama; Anlatım Bozuklukları.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
