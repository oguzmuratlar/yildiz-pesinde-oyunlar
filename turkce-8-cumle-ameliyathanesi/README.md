# Cümle Ameliyathanesi · Cümlenin Ögeleri ve Cümle Türleri

| Alan | Değer |
|---|---|
| gameId | turkce-8-cumle-ameliyathanesi |
| Güncel sürüm | 1.0.0 |
| Ders | Türkçe (oyun içi subjectId: turkish; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Konu | Cümlenin ögeleri (yüklem, özne, gizli özne, nesne, dolaylı tümleç, zarf tümleci) ve cümle türleri |
| Ekran yönü | Dikey |
| Oyun türü | Cümle ameliyathanesi, karaktersiz. Her cümle bir hastadır ve her görev bir tıbbi işlemdir: ögeleri lazer neşterle ayırma, ögelere hasta bilekliği takma, röntgen tarayıcısıyla istenen ögeyi bulma, boş öge yuvasına organ nakli, gizli özne kapsülünü seruma ekleme, nabız monitöründe öge sayısını ayarlama, stetoskopla ögeyi buldurmak için yükleme sorulacak soruyu seçme, tahlil tüplerine ayırma. Şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "Acil vaka" (iki kısa cümleden doğrusunu seç). Doğruysa +30 💓 ve monitörde sarı atım ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (💓 puanı yıldızı etkilemez) |
| Soru havuzu | 100 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Karanlık, fayanslı ameliyathane; tavanda sönük ameliyat lambası, boş monitör; altta yalnızca "AMELİYATA GİR" düğmesi.
- **Giriş:** Lamba üç kez yanıp söner, ışık odayı doldurur; monitörde EKG çizgisi akar, "CÜMLE AMELİYATHANESİ" yazısı yanar; röntgen şeridi bir cümleyi tarayıp ögelerini tek tek aydınlatır; parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 bölmeli nabız monitörü; doğru görevde yeşil kalp atımı (bonus doğruysa sarı atım ★), yanlışta kırmızı düz çizgi ✕.
- **Çıkış:** Hasta takip çizelgesine 10 sonuç sırayla düşer (💚 / ⭐ / 🩹), "TABURCU KARNESİ x/10 CÜMLE" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| laser | Lazer neşter | Sözcüklerin arasına dokunularak öge sınırlarına kesik atılır; lazer ışını cümleyi tarar |
| tag | Hasta bilekliği | Renkli bileklik (Yüklem, Özne, Nesne, Dolaylı tümleç, Zarf tümleci) seçilip ögelere takılır |
| scan | Röntgen | Tarayıcı çubuğu yukarı-aşağı sürüklenip istenen ögenin üstünde bırakılır, röntgen çekilir |
| transplant | Organ nakli | Kavanozdaki parça sürüklenerek cümledeki boş öge yuvasına yerleştirilir |
| pills | Kapsül | Gizli özne olan kişi zamiri kapsülü seruma eklenir |
| monitor | Nabız monitörü | "Atım" düğmeleriyle EKG'deki atım sayısı cümledeki öge sayısına eşitlenir |
| steth | Stetoskop | Parlayan ögeyi buldurmak için yükleme sorulacak soru baloncuğu seçilir |
| bin | Tahlil tüpleri | Fiil/isim cümlesi; belirtili/belirtisiz nesne; kurallı/devrik; olumlu/olumsuz/soru; basit/birleşik/sıralı/bağlı |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| yuklem | 20 | Yüklem; isim ve fiil cümlesi; öge sınırları |
| ozne | 20 | Özne ve gizli özne |
| nesne | 20 | Belirtili ve belirtisiz nesne; nesne ile dolaylı tümleci ayırma |
| tumlec | 20 | Dolaylı tümleç ve zarf tümleci |
| tur | 20 | Yüklemin türüne, yerine, anlamına ve yapısına göre cümleler |

Görev türlerinin dağılımı: scan 17, tag 17, bin 16, laser 14, steth 12, transplant 10, monitor 7, pills 7.

Bütün cümleler özgündür.

Yanlış-cevap kaydı:
- questionText görevi ve cümleyi/düzeneği (ögeler, kavanozdaki parçalar, soru baloncukları, tüpler) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (kesiklerle ayrılan ögeler, takılan bileklikler, taranan parça, nakledilen parçayla cümle, seçilen kapsül, ayarlanan öge sayısı, seçilen soru, tüp yerleşimleri).
- correctAnswer doğru sonucu yazar.
- sourceRef: 8. Sınıf Öğretim Programı, Dil Bilgisi: Cümlenin ögeleri, cümle türleri.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
