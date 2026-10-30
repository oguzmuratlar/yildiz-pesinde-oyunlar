# Posta Masası · İletişim ve Sosyal İlişkiler

| Alan | Değer |
|---|---|
| gameId | turkce-5-posta-masasi |
| Güncel sürüm | 1.0.0 |
| Ders | Türkçe (oyun içi subjectId: turkish; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 5 (oyun yalnızca 5. sınıf bağlamını kabul eder) |
| Tema | 5. Tema: İletişim ve Sosyal İlişkiler |
| Ekran yönü | Dikey |
| Oyun türü | Sağa-sola kaydırmalı (Tinder tarzı) mektup ayırma oyunu (karakter yok). Giriş: ekranı kaplayan uçak postası zarfının kırmızı mühürü çatlar, kapak açılır, zarf aşağı kayar ve posta masası içinden yükselir. Her tur bir "torba"dır: üstte görev cümlesi (ve gerekiyorsa metin), altta 5 mektupluk deste ile iki etiketli posta çuvalı vardır. Öğrenci üstteki mektubu parmağıyla sola ya da sağa fırlatır (alternatif: alttaki iki düğme veya ← → tuşları). Doğru mektup çuvala uçar ve çuval yutar; yanlışta çuval mektubu geri tükürür, mektuba "YANLIŞ ADRES → doğru çuval" damgası basılır ve mektup doğru çuvala gider. Doğru mektup 10 pul, üst üste 3+ doğruda 15 pul. Çıkış: masa zarfa geri iner, kapak kapanır, "TESLİM EDİLDİ" posta damgası vurulur, zarf uçarak ekrandan çıkar. Test ve doğru/yanlış sorusu yoktur; her tur iki adlandırılmış kategoriye ayırmadır. 10 torba, kolaydan zora (3 kolay · 4 orta · 3 zor); süre sınırı yok |
| Doğru sayılma | Torbadaki 5 mektubun hepsi doğru çuvala atılırsa torba doğru sayılır (correctCount = kusursuz torba sayısı) |
| Yıldız | 0–4 kusursuz torba 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (pul yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 124 torba (620 mektup), 28 kart havuzundan üretildi; index.html içine gömülüdür |

## Metinli torbalar
Metin ve şiir torbaları (20 torba) görev cümlesinin hemen altında metni tek parça gösterir; uzun metin kart içinde kaydırılır. Metinler: Ev (ana fikir/ayrıntı), Gülü İncitme Gönül şiiri (kıtaların öğütleri), Herkes Önemli (olay/ders), Siz Olsaydınız (empati ile hak vermeyi ayırma), Tatlı Günler (anne/baba özellikleri). Yanlış-cevap kaydında metin questionText içinde yer alır.

## Soru havuzu

| Grup | İçerik |
|---|---|
| soz | Gerçek/mecaz anlam, sesteş sözcükler (kır, yüz, mahsus, hayır), eş/zıt anlam, "gönül" atasözleri, ilişkiyi bozan/güçlendiren davranışlar (gönül kırmak, gönül almak…) |
| ifade | Açık/örtük ifade, öncelik-sonralık ve eş zamanlılık bağlantı ifadeleri, karşılaştırma ifadeleri, isimlerin yerini tutan sözcükler |
| yazim | Büyük/küçük harf (belirli tarih, kurum, yer, unvan, yön), aynen/dolaylı aktarma ve tırnak işareti, kesme işareti (çekim eki/yapım eki) |
| metin | Ana fikir ve ayrıntı, şiirde öğüt, olay ve ders, söz sanatları (benzetme/kişileştirme), bilgilendirici/öyküleyici metin |
| iletisim | Etkili iletişim davranışları, beden dili, dijital güvenlik, e-postada selam ve sonlandırma ifadeleri, bakış açısı ve empati |

Her oyunda her gruptan 2 torba gelir, aynı kart havuzundan bir oyunda en çok 1 torba ve en çok 3 metinli torba vardır. Son oynanan 40 torba cihazda hatırlanır.

Yanlış-cevap kaydı: studentAnswer ve correctAnswer, torbadaki her mektubu "mektup → çuval" biçiminde listeler.

Kaynak: MEB Türkçe 5. Sınıf Ders Kitabı 2. Kitap, 5. Tema (s. 70–111).
