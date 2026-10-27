# Fındık'ın Veri Bahçesi · İstatistiksel Araştırma Süreci

| Alan | Değer |
|---|---|
| gameId | matematik-6-findik-veri-bahcesi |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 6 (oyun yalnızca 6. sınıf bağlamını kabul eder) |
| Tema | 4. Tema: İstatistiksel Araştırma Süreci |
| Ekran yönü | Dikey |
| Oyun türü | Karakterli bahçe oyunu: rehber sincap Fındık + 10 fidanlık meyve bahçesi + palamut ve 🔥 seri. Görevler: sepete palamut fırlatma (sınıflandırma), kök-yaprak dallarına yaprak takma, kuleleri eşitleme (aritmetik ortalama), hayvanları sıralayıp ortancayı bulma, ağaçtaki meyveleri sayıp tepe değeri seçme, test ve doğru/yanlış. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken oyun görevlerine öncelik verilir (bir oyunun yaklaşık 7–8 görevi etkileşimli); süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 101 görev (38 test, 20 sepete atma, 14 doğru/yanlış, 9 kök-yaprak, 7 kule eşitleme, 7 meyve sayma, 6 sıralama-ortanca), index.html içine gömülüdür |

## Oyun

Rehber karakter **Fındık** turuncu, kabarık kuyruklu bir sincaptır. Konuşma balonuyla görevi anlatır; doğru cevapta zıplar ve kuyruğunu sallar, 3 doğru üst üste gelince coşar, yanlışta üzülür ve cesaretlendirir. Ekranın üstündeki bahçede 10 fidan vardır: doğru görevde sıradaki fidan büyüyerek meyveli bir ağaca dönüşür, yanlışta solgun kalır. Her doğru cevap bir palamut 🌰 kazandırır. Sonda yaprak ve meyve yağmuru olur.

- **Sepete at:** Üzerinde araştırma sorusu ya da veri yazan palamut, dokunulan sepete kavis çizerek uçar. Sepetler: Kategorik / Nicel (kesikli); Karşılaştırma gerektirir / Gerektirmez; Yanlı / Yanlı değil; Uygun / Uygun değil (araştırma sorusu ölçütleri); Yakın çevreden / Resmî kaynaktan; Aritmetik ortalama / Ortanca / Tepe değer. “Geri al” ile son atış alınabilir. Kontrolde her palamut yeşil/kırmızı olur; görev, hepsi doğru sepetteyse doğru sayılır.
- **Yaprak tak (kök-yaprak):** Sayılar yaprak olarak durur. Öğrenci yaprağa, sonra o sayının kökünü gösteren dala dokunur; yaprak dala uçar ve küçükten büyüğe dizilir. Yanlış dalda dal sallanır, nedeni yazılır (görev yanlış sayılır ama tamamlatılır). Boş kalan kök ve 0 kökü (bir basamaklı sayılar) vardır.
- **Kuleleri eşitle:** Bilye, fındık, elma, pul kuleleri. Bir kuleye dokununca üstteki parça kalkar, başka kuleye dokununca oraya geçer. Bütün kuleler eşit boy olunca “EŞİTLEDİM!” — bu boy aritmetik ortalamadır.
- **Sırala, ortancayı bul:** Tabela tutan hayvanlar dalda durur. İki hayvana dokununca zıplayarak yer değiştirirler. Sıralanınca (küçükten büyüğe ya da büyükten küçüğe) ikinci aşamaya geçilir: ortadaki hayvan(lar) seçilir; çift veri sayısında ortadaki iki hayvan seçilir ve ortanca bunların ortalamasıdır.
- **Meyve say (tepe değer):** Ağaçtaki meyvelerde veriler yazılıdır. Bir meyveye dokununca aynı değerdeki bütün meyveler parlar ve “23: 5 tane” gibi sayılır. Birden fazla tepe değer seçilebilir; “Tepe değer yok” düğmesi de vardır.
- **Test ve D/Y:** Renkli seçenekler; gereken yerde tablo ve kök-yaprak gösterimi çizilir.

Yanlış-cevap kaydında: yanlış sepete atılan ifadeler; kök-yaprak hataları; kulelerin son durumu; öğrencinin kurduğu sıra ve seçtiği ortadaki değer(ler); seçilen tepe değer(ler) ile doğru cevap yazılır.

## Soru havuzu

| Grup | İçerik |
|---|---|
| arastirma | Kategorik ve nicel (kesikli) veri, karşılaştırma gerektiren araştırma soruları |
| planlama | Araştırma sorusu ölçütleri, veri kaynakları (yakın çevre / resmî kaynak), hedef kitle, anket, yanlı sorular |
| kokyaprak | Kök-yaprak gösterimi oluşturma ve okuma (en büyük/küçük, veri sayısı, fark, tepe değer, ortanca) |
| merkez | Aritmetik ortalama, ortanca, tepe değer, açıklık |
| yorum | Veri setini en iyi temsil eden ölçü, tablo yorumlama, başkalarının yorumlarını tartışma |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır.

Yeni soru türleri için `questions.json` alanları: `sort_fling` (`targets`, `items[].text`, `items[].target`), `stem_leaf` (`data`, `stems`), `mean_level` (`values`, `thing`, `mean`), `median_line` (`values`, `median`), `mode_pick` (`values`, `modes` — boşsa tepe değer yoktur). Veri gereken testlerde `figure` (`table` ya da `stemleaf`) ve düz metin karşılığı `figureText` vardır.

Kaynak: MEB Matematik 6. Sınıf Ders Kitabı 1. Kitap, 4. Tema (s. 162–220).
