# Kuvvet Kasabası · Kuvveti Tanıyalım

| Alan | Değer |
|---|---|
| gameId | fen-5-kuvvet-kasabasi |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 5 (oyun yalnızca 5. sınıf bağlamını kabul eder) |
| Ünite | 2. Ünite: Kuvveti Tanıyalım |
| Ekran yönü | Dikey |
| Oyun türü | Vahşi Batı temalı deney ve simülasyon oyunu, karakter yok. Test ve doğru/yanlış sorusu yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (altın puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 104 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:** Mor gece göğünde güneş doğar, çalı topu yuvarlanır. Zincirlere asılı "KUVVET KASABASI" tabelası sallanarak iner (sönümlü sarkaç hareketi). "KASABAYA GİR" ile salon kapıları iki yana açılır ve kasabaya girilir.
- **İlerleme:** Üstte 10 istasyonlu demir yolu vardır. Her görevde lokomotif bir istasyon ilerler; doğruda istasyona altın yıldız, yanlışta kaktüs konur.
- **Çıkış:** Gün batımında lokomotif dumanlar içinde ufka gider, "x/10" yazılı şerif yıldızı damga gibi iner. Ardından "ARANIYOR" afişi biçiminde sonuç ekranı açılır.

## Görevler (deney ve simülasyonlar)

| Tür | Görev | Mekanik |
|---|---|---|
| effect | Kuvvetin etkileri | Olay sahnesine bakıp 5 şerif yıldızından (harekete geçirir, hızlandırır, yavaşlatır/durdurur, yön değiştirir, şekil değiştirir) doğruları seçme; zor görevlerde iki etki |
| sort | Vagonlara yükleme | Kartları sürükleyip ya da dokunup 2 vagondan birine yükleme, "TRENİ GÖNDER" (esnek/esnek değil, kütle/ağırlık, artırır/azaltır, olumlu/olumsuz, pürüzlü/az pürüzlü, hava/su direnci) |
| read | Dinamometre okuma | Yay uzar ve cisim asılı kalır. Ölçüm "yazar kasa" sayı çarklarıyla girilir; kontrolde bölmeler tek tek sayılır. Özdeş dinamometre karşılaştırması da vardır |
| pick | Doğru dinamometre | Raftaki dinamometrelere dokunup seçme, "ÖLÇ!" deyince cisim hepsine asılır; ölçüm sınırını aşan yaylar "boing" sesiyle kopar (en hassas, ölçebilenler, esnekliği bozulanlar, en kalın yay) |
| spring | Yay deneyi | Kancaya 1/2/5/10 N'luk ağırlık asıp yayı bırakma, yay sönümlü salınarak uzar. Hedef çizgisine tam ulaşmalıdır |
| balance | Eşit kollu terazi | Gizli kütleli keseyi pirinç ağırlıklarla dengeleme (kollar canlı eğilir), dengelenince ikinci soru açılır: kütle, Ay'daki kütle ya da yaklaşık ağırlık (N) |
| lever | Konum değişince | Altın külçesi Kutup, Ekvator, deniz kenarı, dağ zirvesi, Ay arasında taşınır; "Kütle" ve "Ağırlık" kolları Artar/Değişmez/Azalır konumuna getirilir |
| moon | Dünya ve Ay | Yan yana Dünya ve Ay sahnesinde dinamometreler, verilen değerden istenen kütle ya da ağırlık sayı çarklarıyla bulunur (1 kg ≈ 10 N, Dünya Ay'dan 6 kat fazla çeker) |
| ramp | Rampa / çekme deneyi | Üç farklı yüzeyde önce tahmin (şeritlere 1-2-3 verme), sonra arabaları bırakma ya da kutuyu dinamometreyle çekme; arabalar yüzeye göre farklı uzaklıkta durur, dinamometreler farklı değer gösterir |
| drop | Düşme yarışı | Düz/buruşuk karton, paraşüt açık/kapalı, havada/suda silgi, tüy/para, sivri/küt model; önce ulaşacağı tarafa bayrak koyup "BIRAK!" |
| nose | Tasarım yarışı | Hızlı tren, yarış arabası, Kaan uçağı, gemi, denizaltı, kamyonun önüne doğru parçayı takıp yarıştırma; flap ve paraşüt ile güvenli iniş |

Sayısal cevaplar test seçeneğiyle değil sayı çarklarıyla alınır. Her deste kurulurken her konudan 2 görev seçilir ve görev türleri olabildiğince farklı tutulur (bir destede en az 8 farklı tür).

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| kuvvet | 21 | Kuvvetin etkileri, esnek cisimler |
| olcum | 22 | Dinamometre okuma, bölme değeri, özdeş dinamometreler, hassasiyet ve ölçüm sınırı, yay kalınlığı, yay uzaması orantısı, Newton |
| kutle | 23 | Eşit kollu terazi, kütle/ağırlık farkı, yer çekimi ve konum (kutup-Ekvator, yükseklik), Dünya-Ay ağırlığı |
| surtunme | 18 | Pürüzlü/az pürüzlü yüzeyler, rampa ve çekme deneyleri, sürtünmeyi artırma-azaltma, olumlu-olumsuz etkiler |
| direnc | 20 | Hava ve su direnci deneyleri, araç tasarımları (sivri burun, V pruva), paraşüt ve flap |

Görev türlerinin dağılımı: sort 23, effect 15, read 9, ramp 9, pick 8, drop 8, nose 8, lever 7, balance 6, moon 6, spring 5.

Yanlış-cevap kaydı: questionText görevi ve deney düzeneğini [Şekil: …]/[Deney: …] biçiminde metin olarak içerir. studentAnswer öğrencinin seçimini, yerleştirmelerini ya da girdiği değeri, correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 5. Sınıf Ders Kitabı, 2. Ünite (s. 56–95).
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
