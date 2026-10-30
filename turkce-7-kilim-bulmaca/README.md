# Kilim Bulmaca · Türk Sanatı

| Alan | Değer |
|---|---|
| gameId | turkce-7-kilim-bulmaca |
| Güncel sürüm | 1.0.0 |
| Ders | Türkçe (oyun içi subjectId: turkish; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Tema | 4. Tema: Türk Sanatı |
| Ekran yönü | Dikey |
| Oyun türü | Çapraz bulmaca, kilim tezgâhı görünümünde, karakter yok. Giriş: Tezgâhın çözgü ipleri yukarıdan iner, mekik sağa sola giderek kilimi alttan üste sıra sıra dokur, ortada "Kilim Bulmaca" kartuşu belirir; sonra atkı sıraları sırayla sağa ve sola çekilip söküldükçe oyun görünür. Her kilimde 3 (kolay) ya da 4 (orta, zor) kesişen kelime vardır. Öğrenci bir kutuya ya da kelime düğmesine dokunur, ipucunu okur ve Türkçe klavyeyle yazar; kesişen kutuya ikinci kez dokununca yön değişir. ✓ ile kelime kontrol edilir: Doğruysa harfler ilmek ilmek dokunarak renklenir, yanlışsa hatalı harfler kırmızı yanıp silinir, doğru harfler kalır. Her kilimde 3 hatalı kontrol hakkı vardır. 💡 seçili kutunun harfini açar (−20 puan), "🏳️ Bulamadım" kilimi bitirir. Kilim ancak bütün kelimeler bulunursa doğru sayılır; bulunamayan harfler kırmızı çerçeveyle gösterilir. Puan: kelime başına 30, hatasız kilim için +30. Çıkış: Atkı sıraları yeniden dokunup ekranı kaplar, ardından kilim uçan halı gibi dalgalanarak gökyüzüne uçar ve sonuç ekranı açılır. Test ve doğru/yanlış sorusu yoktur. 10 kilim, kolaydan zora (3 kolay · 4 orta · 3 zor); süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (yumak puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 102 çapraz bulmaca (3–4 kelime, en çok 9 satır × 10 sütun), index.html içine gömülüdür |

## Önceki biçimlerden farkı
Wordle ve Lingo'da tek kelime renk ipuçlarıyla tahmin edilir. Burada kelimeler birbirini keser ve çözülen kelimenin harfleri öteki kelimelere ipucu olur. Çini Avı'nda kelimeler hazır harf tablosunda aranır; burada öğrenci harfleri kendisi yazar.

## Metinli sorular
Metinli bulmacalar (18 bulmaca) önce okuma kartında açılır. "METNİ OKUDUM, BULMACAYA GEÇ" düğmesiyle bulmacaya geçilir, "📖 Metni göster" düğmesiyle metne dönülür. Metinler, kitaptaki metinlerin kendi cümlelerimizle yazılmış özetleridir (telif nedeniyle aynen aktarılmadı). Her cevap gösterilen özette açıkça geçer. Özetlenen metinler: Anadolu'da Kilim Demek, Geleneksel Türk Tiyatrosu, Süleymaniye (şiirin özeti), Büyük Deha Koca Sinan, Sandıktaki Miras, Milas Halıları. Bir oyunda aynı metin iki kez gelmez. Yanlış-cevap kaydında metin questionText içinde yer alır.

## Soru havuzu

| Grup | Bulmaca | İçerik |
|---|---|---|
| soz | 21 | Kilim, peşkir, sedir, tezgâh, desen, belde, gergef, ilmek, hayalbaz, meddah, ahenk, ihtişam, doğaçlama, taşlama, şadırvan, tezhip, esrarengiz, matbu, cemaat |
| el | 21 | Ebru, çini, hat, oya, halı, İznik, Kütahya, Sinan, cami, tekne, yün, Pazırık, kök boya, Nallıhan, minyatür, Milas, ıstar, boyalık, dehliz, kurşun, Selimiye, kızılçam, sumak |
| sahne | 21 | Karagöz, Hacivat, kukla, ortaoyunu, Kavuklu, Pişekâr, yardak, kıssahan, tekerleme, seyirlik köy oyunları; ney, bağlama, davul, tef, kemençe, kanun, zurna, kudüm |
| dil | 21 | Zıtlık işlevli söz varlıkları (rağmen, yalnız, meğerse, oysaki, gelgelelim, zıddına); teşhis; örneklendirme, tanık gösterme, sayısal veri; tartışma paragrafı; problem-çözüm (sorun, çare, öneri, ikilem); kısa çizgi, noktalı virgül, yay ayraç |
| metin | 18 | Özet metinlerde önemli bilgi ve çıkarım |

Her oyunda her gruptan 2 bulmaca gelir. Bir oyunda aynı kelime mümkün olduğunca iki kez gelmez, en çok 3 metinli bulmaca vardır. Son oynanan 40 bulmaca cihazda hatırlanır.

Yanlış-cevap kaydı: studentAnswer içinde çözülen ve çözülemeyen kelimeler, kelime kelime bütün hatalı denemeler, "Bulamadım" seçimi ve açılan harf sayısı yer alır. correctAnswer, numara ve yönleriyle bütün kelimelerdir (ör. "1→ KİLİM, 2↓ SEDİR").

Kaynak: MEB Türkçe 7. Sınıf Ders Kitabı 2. Kitap, 4. Tema (s. 10–63).
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
