# Söz Müzesi · Söz Sanatları, Metin Türleri, Hikâye ve Şiir Unsurları

| Alan | Değer |
|---|---|
| gameId | turkce-8-soz-muzesi |
| Güncel sürüm | 1.0.0 |
| Ders | Türkçe (oyun içi subjectId: turkish; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Konu | Benzetme ve ögeleri; kişileştirme, konuşturma, abartma, karşıtlık; öyküleyici ve bilgilendirici metin türleri; hikâye unsurları, anlatıcı, dize, kıta, uyak ve redif |
| Ekran yönü | Dikey |
| Oyun türü | Gece müzesi, karaktersiz. Her görev bir küratörlük işidir: tabloda spot ışığı gezdirerek benzetme ögesini bulma, kırık heykeli parçalarla onarma, kaidedeki eserin söz sanatını kadran çevirerek etiketleme, sesli rehberin okuduğu eseri kat planında doğru salona götürme, bilet makinesinin makaralarını çevirerek hikâye unsurlarını eşleştirme, şiirde ses benzerliği taşıyan dize sonlarını bulma, üç tablodan doğrusuna spot yakma, eserleri salonlara yerleştirme. Şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "Rehber sorusu" (iki seçenekten doğrusu). Doğruysa +30 🎟️ ve galeri duvarında altın çerçeve ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🎟️ puanı yıldızı etkilemez) |
| Soru havuzu | 100 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Mor duvarlı, mermer zeminli müze salonu; altın çerçeveli eserler, kadife kordon; altta yalnızca "MÜZEYE GİR" düğmesi.
- **Giriş:** Karanlık salonda bir el feneri ışığı dolaşır, ışıklar yanar, eserlerin üstündeki spotlar sırayla açılır; "SÖZ MÜZESİ" pirinç levhası belirir, kadife kordon kalkar; parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 çerçeveli galeri duvarı; doğru görevde çerçeveye tablo asılır (bonus doğruysa altın çerçeve ★), yanlışta çerçeve örtüyle kapanır ✕.
- **Çıkış:** Galeri duvarında 10 eser sırayla aydınlanır (yanlışlar örtülü), "KÜRATÖR KARNESİ x/10 ESER" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| spotlight | Spot ışığı | Karanlık tablo üzerinde parmakla ışık gezdirilir; istenen benzetme ögesi aydınlatılır |
| restore | Heykel onarımı | Kırık parçalar boş yuvalara takılarak benzetme cümlesi tamamlanır |
| dial | Kadran | Kaidedeki eserin söz sanatı, kadran çevrilerek (ya da etikete dokunularak) seçilir |
| map | Sesli rehber | Rehberin okuduğu metin, kat planındaki doğru tür salonuna götürülür |
| reels | Bilet makinesi | Makaralar çevrilerek kişi, yer, zaman (ve olay) unsurları eşleştirilir |
| rhyme | Ahenk avı | Parlayan dize sonuyla ses benzerliği taşıyan dize sonları seçilir |
| frames | Tablo seç | Üç tablodan istenen sanatı ya da türü taşıyana spot yakılır |
| bin | Salonlar | Eser ve özellik kartları salonlara (türlere, ögelere) yerleştirilir |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| benzetme | 20 | Benzetme; benzeyen, benzetilen, benzetme yönü, benzetme edatı; güçlü benzetme |
| sanat | 20 | Kişileştirme, konuşturma, abartma, karşıtlık |
| oykuleyici | 20 | Masal, fabl, hikâye, roman, tiyatro, şiir |
| bilgi | 20 | Biyografi, otobiyografi, anı, günlük, mektup, gezi yazısı, makale, deneme, haber, röportaj, sohbet |
| unsur | 20 | Kişi, yer, zaman, olay; giriş-gelişme-sonuç; anlatıcı; dize, kıta, uyak, redif |

Görev türlerinin dağılımı: bin 24, map 20, frames 17, dial 10, spotlight 8, reels 8, rhyme 7, restore 6.

Bütün metin parçaları ve şiirler özgündür; kitaptaki bir metni okumuş olmayı gerektiren görev yoktur.

Yanlış-cevap kaydı:
- questionText görevi ve eseri (cümle, metin parçası, şiir, parçalar, salonlar, makaralar) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (aydınlattığı parça, onardığı cümle, seçtiği sanat ya da salon, makara eşleşmeleri, seçtiği dize sonları, seçtiği tablo, kart yerleşimleri).
- correctAnswer doğru sonucu yazar.
- sourceRef: 8. Sınıf Öğretim Programı, Okuma: Söz sanatları, metin türleri, metnin unsurları.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
