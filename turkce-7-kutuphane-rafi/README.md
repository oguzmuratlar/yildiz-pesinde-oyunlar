# Kütüphane Rafı · Okuma Kültürü

| Alan | Değer |
|---|---|
| gameId | turkce-7-kutuphane-rafi |
| Güncel sürüm | 1.0.0 |
| Ders | Türkçe (oyun içi subjectId: turkish; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Tema | 5. Tema: Okuma Kültürü |
| Ekran yönü | Dikey |
| Oyun türü | Raflara yerleştirerek sınıflandırma (sürükle-bırak), kütüphane görünümünde, karakter yok. Giriş: Ekranın ortasında kırmızı deri kaplı dev bir kitap belirir, kapağı açılır, sayfalar hızla çevrilir ve açık kitaba yakınlaşılarak oyuna girilir. Her turda 2–3 etiketli raf ve kitap arabasında 4–6 kitap kartı vardır. Öğrenci kartı sürükleyip rafa bırakır ya da önce karta, sonra rafa dokunur; raftaki karta dokunup başka rafa ya da arabaya taşıyabilir. Araba boşalınca "Rafları kontrol et" düğmesine basar. Yanlış raftaki kitaplar kırmızı yanıp arabaya geri döner. Her rafta 2 kontrol hakkı vardır; ikinci kontrolde de yanlış varsa doğru yerleşim gösterilir (yanlış konan kitaplar kırmızı çerçeveli). Puan: ilk kontrolde doğru kitap başına 15, kusursuz rafa +40; ikinci kontrolde yeni düzeltilen kitap başına 8. Çıkış: Kitap yeniden açık hâlde belirir, sayfalar geri çevrilir, kapak kapanır ve kitap kütüphane rafındaki boşluğa sırtıyla yerleşir; ardından sonuç ekranı açılır. Test ve doğru/yanlış sorusu yoktur. 10 raf, kolaydan zora (3 kolay · 4 orta · 3 zor); süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (kitap puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 102 raf turu (kolay: 2 raf 4 kitap, orta: 3 raf 5 kitap, zor: 3 raf 6 kitap), index.html içine gömülüdür |

## Önceki biçimlerden farkı
Posta Masası'nda kartlar tek tek, iki çuvala kaydırılır ve her kart anında değerlendirilir. Burada 2–3 raf vardır. Öğrenci bütün kitapları istediği sırayla yerleştirir, istediği zaman yerini değiştirir ve rafı bir bütün olarak kontrol ettirir.

## Metinli sorular
Metinli turlar (18 tur) önce okuma kartında açılır. "METNİ OKUDUM, RAFLARA GEÇ" düğmesiyle raflara geçilir, "📖 Metni göster" düğmesiyle metne dönülür. Metinler, kitaptaki metinlerin kendi cümlelerimizle yazılmış özetleridir (telif nedeniyle aynen aktarılmadı). Her kitap kartındaki bilgi gösterilen özette açıkça geçer. Özetlenen metinler:
- İlber Hoca Cevaplıyor (Atatürk ve okuma)
- 19. yüzyıl Osmanlı'sında okuma (bilgi kutusu)
- Kitap
- Kitaplarla Kurulan Dostluk (şiir)
- Canım Kitap
- Medya Okuryazarlığı

Bir oyunda aynı metin iki kez gelmez. Yanlış-cevap kaydında metin questionText içinde yer alır.

## Soru havuzu

| Grup | Tur | İçerik |
|---|---|---|
| soz | 21 | Raf = kelime, kitap = anlamı ya da eş anlamlısı: ilim, kadim, engin, tercüman, kıraathane, yoldaş, nüsha, efsun, kitle, diplomat, müfredat, sahaf, mürşit, litografi (taş baskı), cüz, diplomasi, harbiye, hipermetin |
| zarf | 21 | Koyu yazılmış zarfları türüne göre: durum, zaman, miktar, yer-yön, soru zarfı |
| yazim | 21 | Sayıların yazımı (üçlü gruplar, kesir, üleştirme, ayrı yazılan sayılar, sıra sayıları); tırnak işareti (aktarılan söz / vurgulanan söz ve eser adı), yay ayraç, köşeli ayraç |
| okuma | 21 | Eleştirel yazmanın aşamaları (konuyu belirleme, ölçütle karşılaştırma, yargıya ulaşma, gerekçeli çözüm); söz sanatları (benzetme, kişileştirme, abartma); düşünceyi geliştirme yolları (örneklendirme, sayısal veri, tanık gösterme, karşılaştırma) |
| metin | 18 | Özet metinlerdeki bilgileri ölçüte göre sınıflandırma |

Her oyunda her gruptan 2 tur gelir. Bir oyunda aynı kitap kartı mümkün olduğunca iki kez gelmez, en çok 3 metinli tur vardır. Son oynanan 40 tur cihazda hatırlanır.

Yanlış-cevap kaydı: studentAnswer içinde her kontrolde yanlış rafa konan kitaplar ve kondukları raf yer alır (ör. "1. kontrolde yanlış rafta: “epey” → Durum zarfı"). correctAnswer, raf raf doğru yerleşimdir.

Ekran notu: 320×568 gibi çok kısa ekranlarda 6 kitaplı 5 turda raf alanı 40 pikseli geçmeyen bir kaydırma ister. Kitap sürüklenirken alan kendiliğinden kayar.

Kaynak: MEB Türkçe 7. Sınıf Ders Kitabı 2. Kitap, 5. Tema (s. 66–115).
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
