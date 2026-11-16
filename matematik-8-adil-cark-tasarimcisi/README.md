# Adil Çark Tasarımcısı · Basit Olayların Olma Olasılığı

| Alan | Değer |
|---|---|
| gameId | matematik-8-adil-cark-tasarimcisi |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 5. Ünite: Basit Olayların Olma Olasılığı |
| Ekran yönü | Dikey |
| Oyun türü | Gece lunaparkında oyun tasarım atölyesi, karaktersiz. Her görev bir şans düzeneğidir: çarkı boyama, torbayı doldurma, desteden kart atma, olasılık cetveline pim sürükleme, olası durumlara dokunma, olasılığı kesir olarak kurma, olayları sıralama, bölmeler, tuş takımı. Şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "ödül çarkı" bonusu: kırmızı ödül için hangi çarkın çevrileceği seçilir (iki oranın karşılaştırılması). Doğruysa +30 🎟️ ve bilette ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🎟️ puanı yıldızı etkilemez) |
| Soru havuzu | 101 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Gece lunaparkı, sönük ampul dizileri, dev renkli çark ve okun üstünde kırmızı-altın "ADİL ÇARK TASARIMCISI" tabelası; altta yalnızca "ÇARKI ÇEVİR" düğmesi.
- **Giriş:** Ampuller yanıp söner, çark tik tik yavaşlayarak döner ve durur, altın parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 biletlik şerit; doğru görevde altın bilet (bonus doğruysa ★), yanlışta yırtık gri bilet.
- **Çıkış:** Görevlerin biletleri sırayla yağar (doğrular altın, yanlışlar yırtık), çark desenli "TASARIM KARNESİ x/10 ADİL ÇARK" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| wheel | Çark boyama | Renk seçilip eş dilimlere dokunarak boyanır; koşullar (P(renk) = a/b, eşit olasılıklı, daha olası, olasılığı 0) sağlanır; çark döner |
| bag | Torba | Renklerin top sayıları ayarlanır (bazıları sabit); olasılık ya da karşılaştırma koşulu sağlanır |
| cards | Kart atma | Desteden en az sayıda kart atılarak istenen olasılık elde edilir |
| pline | Olasılık cetveli | Olay pimleri 0–1 cetvelinde doğru yere sürüklenir (imkânsız, eşit şans, kesin ve aradakiler) |
| outs | Olası durumlar | Zar yüzleri, harf ya da sayı kartlarında olaya ait bütün durumlara dokunulur |
| frac | Olasılığı kur | Zar, para, torba, çark ya da kart sahnesine bakılarak pay ve payda ayarlanır (eşdeğer kesir kabul) |
| order | Sıralama | Olaylar en az olasıdan en çok olasıya doğru dokunarak sıralanır |
| bin | Bölmeler | İmkânsız/olası/kesin, eşit şanslı mı, olasılık değeri olabilir mi, A–B karşılaştırması |
| key | Tuş takımı | Torbadaki top sayısı, eklenecek/çıkarılacak top, dilim sayısı problemleri |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| durum | 20 | Olası durumlar, imkânsız/olası/kesin olaylar |
| esit | 20 | Eşit şanslı olaylar ve 1/n, olasılığın 0–1 aralığı |
| hesap | 20 | Basit bir olayın olasılığını hesaplama (torba, çark, zar, kart; ekleme ve çıkarmadan sonra) |
| karsilastir | 20 | Daha fazla, eşit, daha az olasılıklı olaylar |
| tasarim | 21 | Koşula göre çark, torba ve deste tasarlama; problemler |

Görev türlerinin dağılımı: frac 17, wheel 14, bag 14, outs 10, bin 10, pline 10, order 10, cards 8, key 8.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (çarkın dilim sayısı ve renkleri, torbadaki toplar, kartlar, olaylar) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (çarktaki renk sayıları, torbadaki toplar, atılan kartlar ve oluşan olasılık, cetveldeki konumlar, seçilen durumlar, kesir, sıra, bölmeler, yazılan sayı).
- correctAnswer koşulları ya da doğru sonucu yazar; birden çok çözümü olan tasarım görevlerinde koşulu sağlayan her çözüm kabul edilir.
- sourceRef: 8. Sınıf Öğretim Programı, 5. Ünite “Basit Olayların Olma Olasılığı”.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
