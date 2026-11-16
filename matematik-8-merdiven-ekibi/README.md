# Merdiven Ekibi · Üçgenler

| Alan | Değer |
|---|---|
| gameId | matematik-8-merdiven-ekibi |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 9. Ünite: Üçgenler |
| Ekran yönü | Dikey |
| Oyun türü | Gece şehirde itfaiye merdiven ekibi, karaktersiz. Her görev bir kurtarma işidir: D noktasını kaydırarak kenarortay/açıortay/yükseklik çizme (canlı ölçüler), çubuk rafından üçgen kuran üç çubuğu seçme, üçüncü çubuğun en uzun/en kısa tam sayı uzunluğunu ayarlama, açı ya da kenar ölçülerine göre sıralama, Pisagor karelerinde eksik kareyi tamamlama, merdiveni açıp pencereye yetiştirme, ızgarada dik köşeyi koyup hortum uzunluğunu bulma, bölmeler, tuş takımı. Şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "hangi merdiven tam yetişir?" bonusu (pencere yüksekliği ve ayak uzaklığı verilir, iki merdivenden doğru olan seçilir). Doğruysa +30 💧 ve pencerede ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (💧 puanı yıldızı etkilemez) |
| Soru havuzu | 100 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Gece şehri, penceresinden alev ve duman çıkan tuğla bina, "MERDİVEN EKİBİ" tabelası; altta yalnızca "GÖREVE ÇIK" düğmesi.
- **Giriş:** Siren çalar, tepe lambası yanıp söner, itfaiye aracı gelir, merdiven açılıp pencereye uzanır, alev söner ve pencerede kurtarılan biri görünür; parlamayla oyuna geçilir.
- **İlerleme:** Üstte bina cephesinde 10 pencere; sıradaki pencerede 🔥, doğru görevde pencere ışıklanır ✓ (bonus doğruysa ★), yanlışta gri ✕.
- **Çıkış:** Bina cephesindeki 10 pencere sırayla belirir (kurtarılanlar ışıklı 🙋, kalanlar dumanlı 💨), "KURTARMA KARNESİ x/10 PENCERE" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| cevian | Yardımcı eleman çiz | D noktası BC üzerinde kaydırılır; BD, DC, ∠BAD, ∠DAC, ∠ADC canlı ölçülür; kenarortay, açıortay ya da yükseklik için doğru yerde bırakılır |
| rods | Üç çubuk seç | Raftaki çubuklardan üçü seçilir; üçgen kurulursa iskele birleşir, kurulmazsa uçlar açıkta kalır (her geçerli üçlü kabul) |
| rod3 | Üçüncü çubuk | İki çubuk verilir; üçgen kurulabilen en uzun/en kısa tam sayı uzunluk ayarlanır |
| angside | Sırala | Açılara göre kenarlar uzundan kısaya ya da kenarlara göre açılar büyükten küçüğe dokunularak sıralanır (şekil ölçekli değil) |
| squares | Pisagor kareleri | Dik üçgenin kenarlarındaki karelerden eksik olanın kenarı ayarlanır; alan canlı görünür |
| ladder | Merdiven kurtarma | Merdiven boyu, ayak uzaklığı ya da kurtarma yüksekliği ayarlanır; merdiven açılır, pencereye yetişirse kurtarma olur |
| grid | Hortum ızgarası | Izgarada dik üçgenin köşesi konur (dik kenarlar canlı ölçülür), iki musluk arası hortum uzunluğu ayarlanır |
| bin | Bölmeler | Yardımcı eleman özellikleri, tek türlü çizilebilirlik, üçgen olur/olmaz, dik üçgen olur/olmaz, kenar-açı ifadeleri |
| key | Tuş takımı | Açı, uzunluk, alan ve gerçek hayat problemleri |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| yardimci | 20 | Kenarortay, açıortay, yükseklik; yeterli elemanı verilen üçgeni çizme |
| esitsizlik | 20 | Üçgen eşitsizliği |
| kenaraci | 20 | Kenar uzunlukları ile karşı açılar arasındaki ilişki |
| pisagor | 20 | Pisagor bağıntısı |
| problem | 20 | Pisagor bağıntısıyla gerçek hayat problemleri |

Görev türlerinin dağılımı: key 26, cevian 12, angside 12, ladder 12, bin 9, squares 9, rods 7, rod3 7, grid 6.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (üçgenin köşe koordinatları, çubuk uzunlukları, açı/kenar ölçüleri, kare alanları, merdiven verileri, ızgaradaki noktalar) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (D noktasının konumu, seçilen çubuklar, sıralama, kare kenarı ve alanı, ayarlanan değer ve merdiven ucunun yüksekliği, köşe noktası ve hortum uzunluğu).
- correctAnswer doğru sonucu yazar; çubuk seçmede üçgen kuran her üçlü, ızgarada iki dik köşeden her biri kabul edilir.
- sourceRef: 8. Sınıf Öğretim Programı, 9. Ünite “Üçgenler”.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
