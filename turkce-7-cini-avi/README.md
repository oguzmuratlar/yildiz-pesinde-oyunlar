# Çini Avı · İletişim ve Sosyal İlişkiler

| Alan | Değer |
|---|---|
| gameId | turkce-7-cini-avi |
| Güncel sürüm | 1.0.0 |
| Ders | Türkçe (oyun içi subjectId: turkish; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Tema | 3. Tema: İletişim ve Sosyal İlişkiler |
| Ekran yönü | Dikey |
| Oyun türü | Kelime avı (bulmaca tablosu), İznik çinisi görünümünde, karakter yok. Giriş: Ekranın dört yanından dönerek uçan çini karolar merkezden dışa doğru yerine oturup bir mozaik pano oluşturur, ortada "Çini Avı" kartuşu belirir. Ardından karolar çapraz bir dalga hâlinde dönüp kaybolur ve oyun tahtası görünür. Her panoda 3 ipucu ve 8×8–10×10 harf tablosu vardır. Öğrenci kelimenin ilk harfinden son harfine düz bir çizgide parmağını sürükler; sürüklemek yerine ilk ve son harfe ayrı ayrı da dokunabilir. Bulunan kelime kendi renginde (lacivert, turkuaz, mercan) boyanır. Yön zorluğa göre değişir: kolay panolarda sağa/aşağı, orta panolarda çapraz da, zor panolarda ters yönler de vardır. Her panoda 3 hatalı seçim hakkı vardır (lale simgeleri). 🔍 ile bir kelimenin ilk harfi parlatılır (−20 puan); "🏳️ Bulamadım" panoyu bitirir. Pano ancak 3 kelimenin üçü bulunursa doğru sayılır. Bulunamayan kelimeler sonunda kırmızıyla gösterilir. Puan: kelime başına 30, hatasız pano için +30. Çıkış: karolar dalga hâlinde dönerek ekranı yeniden kaplar, sonra alttan başlayarak dönerek aşağı düşer ve arkadaki sonuç ekranı açılır. Test ve doğru/yanlış sorusu yoktur. 10 pano, kolaydan zora (3 kolay · 4 orta · 3 zor); süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (lale puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 103 pano (her biri 3 kelime), index.html içine gömülüdür; tablo her oynayışta yeniden ve rastgele dizilir |

## Yeni biçim
Önerilen yedi biçimin (Pasaparola, Kelimelik, Tinder, Lingo, Çarkıfelek, Reels, Wordle) yedisi de önceki oyunlarda kullanıldığı için bu oyunda yeni bir biçim olarak kelime avı kullanıldı. Klavye, çark ya da kart kaydırma yoktur. Etkileşim, tabloda çizgi çekmektir.

## Metinli sorular
Metinli panolar (15 pano) önce okuma kartında açılır. "METNİ OKUDUM, AVA BAŞLA" düğmesiyle tabloya geçilir, "📖 Metni göster" düğmesiyle metne dönülür. Eskici, Ya Hayır Söyle ve Sağlıklı Aile metinleri, kitaptaki metinlerin kendi cümlelerimizle yazılmış özetleridir (telif nedeniyle aynen aktarılmadı). Her cevap gösterilen özette açıkça geçer. Karacaoğlan'ın "Öğüt" şiirinin ilk üç dörtlüğü aynen verilmiştir; şiir halk edebiyatına ait, telifi olmayan bir eserdir. Yanlış-cevap kaydında metin questionText içinde yer alır.

## Soru havuzu

| Grup | İçerik |
|---|---|
| soz | Yetim, eskici, güverte, avlu, nasihat, peltek, kösele, vinç, kelam, akıbet, rıhtım, yeğlemek, fend, hacil, zâyi, nasır |
| deyim | "Hayır" deyim ve kalıp sözleri (hayra alamet, hayır işlemek, hayır sahibi, hayra yormak, hayrola, hayır görmemek, hayır kalmamak, hayırla yâd etmek); nezaket kalıpları (lütfen, rica ederim, özür dilerim); atasözü ve şiirden kalıp sözler |
| dil | Pekiştirmeli kelimeler (tertemiz, dosdoğru, apaçık, sımsıcak, kapkara, sapsarı, büsbütün); yargının gerçekleşme zamanı (geçmiş, gelecek, şimdiki, geniş); kısa çizgi, eğik çizgi, ayraç içinde ünlem; ikna teknikleri (otorite, kıtlık, uzlaşma) |
| iletisim | Nezaket, görgü, empati, selam, mimik, jest, beden dili, mizah, sanal zorbalık, koşulsuz sevgi, güven, saygı, dinleme |
| metin | Eskici, Ya Hayır Söyle, Sağlıklı Aile (özet) ve Öğüt şiirinde önemli bilgi ve çıkarım |

Her oyunda her gruptan 2 pano gelir. Bir oyunda aynı kelime mümkün olduğunca iki kez gelmez, en çok 3 metinli pano vardır. Son oynanan 40 pano cihazda hatırlanır.

Yanlış-cevap kaydı: studentAnswer içinde bulunan ve bulunamayan kelimeler, hatalı seçimler, "Bulamadım" seçimi ve ipucu sayısı yer alır. correctAnswer, panonun üç kelimesidir.

Kaynak: MEB Türkçe 7. Sınıf Ders Kitabı 1. Kitap, 3. Tema (s. 120–167).
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
