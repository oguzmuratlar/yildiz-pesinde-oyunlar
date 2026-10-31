# Halka Halka · Hak ve Sorumluluklar

| Alan | Değer |
|---|---|
| gameId | turkce-7-halka-halka |
| Güncel sürüm | 1.0.0 |
| Ders | Türkçe (oyun içi subjectId: turkish; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Tema | 6. Tema: Hak ve Sorumluluklar |
| Ekran yönü | Dikey |
| Oyun türü | Sıralama, zincir halkaları görünümünde, karakter yok. Giriş: Ekranı çapraz iki zincir ve ortasında altın bir asma kilit kaplar; bir anahtar gelip kilide girer ve döner, kilidin halkası açılır, kilit düşer, zincir halkaları dört bir yana saçılarak oyunu açar. Her turda 3, 4 ya da 5 karışık halka (cümle, olay ya da adım) alt alta zincir gibi dizilidir. Öğrenci halkayı basılı tutup yukarı-aşağı sürükler ya da ▲ ▼ düğmeleriyle taşır, sonra "Zinciri kontrol et" der. Doğru yerdeki halkalar altın renge döner ve kilitlenir, yanlışlar kırmızı yanar. Her zincirde 2 kontrol hakkı vardır; ikinci kontrolde de yanlış kalırsa doğru sıra gösterilir. Puan: ilk kontrolde yerine oturan halka başına 10, kusursuz zincire +40; ikinci kontrolde yeni yerine oturan halka başına 6. Çıkış: Yukarıdan altın tokmaklı bir zincir iner, oyun ekranını perde gibi yukarı çeker ve arkadaki sonuç ekranı görünür. Test ve doğru/yanlış sorusu yoktur. 10 zincir, kolaydan zora (kolay 3 · orta 4 · zor 5 halka; 3 kolay · 4 orta · 3 zor tur); süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (halka puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 105 sıralama turu, index.html içine gömülüdür |

## Önceki biçimlerden farkı
Önceki oyunlarda öğrenci ya cevap seçer, ya yazar, ya da kartları kümelere ayırır. Burada her şey baştan doğrudur; öğrenciden yalnızca doğru sırayı kurması beklenir. Paragraf turlarında cümleler arasındaki bağlayıcıları (“Bu yüzden”, “Oysa”, “Bunlara ek olarak” vb.) kullanarak düşünce akışını bulur.

## Metinli sorular
Olay örgüsü turları (21 tur) önce okuma kartında açılır. "METNİ OKUDUM, SIRALAMAYA GEÇ" düğmesiyle sıralamaya geçilir, "📖 Metni göster" düğmesiyle metne dönülür. Metinler, kitaptaki metinlerin kendi cümlelerimizle yazılmış özetleridir (telif nedeniyle aynen aktarılmadı). Halkalardaki olaylar özette geçen olaylardır. Özetlenen metinler: Kutadgu Bilig, Siyah İnci, Üç Soru. Paragraf turlarındaki paragraflar, temadaki hak, sorumluluk, çocuk hakları, eşitlik-adalet ve çevre konularında bu oyun için yazılmıştır. Kitaptaki bilgiler kullanılmıştır: 20 Kasım, 18 yaş, her on çocuktan biri, ayakkabı benzetmesi.

## Soru havuzu

| Grup | Tur | İçerik |
|---|---|---|
| hak | 21 | Hak ve sorumluluk paragrafları: hak-sorumluluk dengesi, trafik, çevre (Yeşil Vatan), hayvan hakları, ailede sorumluluk |
| cocuk | 21 | Çocuk Hakları Sözleşmesi, eşitlik ve adalet, eğitim hakkı, ifade özgürlüğü, oyun ve dinlenme hakkı |
| dil | 21 | İkilemeler (yavaş yavaş, uzun uzun, zar zor, az çok, eninde sonunda, karış karış), sınırlama işlevli söz varlıkları (-a kadar, -a dek, -a değin, -mak üzere, yalnızca, sadece, ancak, artık, bundan sonra) ve sıra bildiren ifadelerle kurulan olay akışları |
| surec | 21 | Sunum hazırlama, problem çözme, kurum tanıtan yazı, yazma süreci, çözüm öneren yazı, doğaçlama konuşma, öyküleyici metnin bölümleri (serim, düğüm, çözüm), “gelecek kumbarası” öyküsü |
| metin | 21 | Kutadgu Bilig, Siyah İnci ve Üç Soru özetlerinde olay örgüsü |

Her oyunda her gruptan 2 tur gelir. Bir oyunda aynı paragraf, süreç ya da metin iki kez gelmez, en çok 3 metinli tur vardır. Son oynanan 40 tur cihazda hatırlanır.

Yanlış-cevap kaydı: studentAnswer içinde öğrencinin her kontroldeki sıralaması yer alır. correctAnswer, doğru sıradır.

Kaynak: MEB Türkçe 7. Sınıf Ders Kitabı 2. Kitap, 6. Tema (s. 116–161).
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
