# Cümle Mikroskobu · Cümlede Anlam

| Alan | Değer |
|---|---|
| gameId | turkce-8-cumle-mikroskobu |
| Güncel sürüm | 1.0.0 |
| Ders | Türkçe (oyun içi subjectId: turkish; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Konu | Cümlede anlam |
| Ekran yönü | Dikey |
| Oyun türü | Aydınlık dil laboratuvarı, karaktersiz. Her görev bir laboratuvar işidir: cümle lamını iki renk boyayla boyama (neden/sonuç, amaç/eylem, koşul/sonuç, karşılaştırılan öğeler), neşterle cümleyi iki parçaya ayırma, döner objektifi çevirerek anlam ilişkisini seçme, lam kartlarını sola/sağa kaydırma, pipetle bağlayıcı damlatıp cümle birleştirme, büyüteci örtülü anlam ya da öznellik yaratan sözcüğe getirme, cümle sonunu sürükleyip lama bırakma, bölmeler. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "hangi lamda nesnel yargı var?" bonusu. Doğruysa +30 🔬 ve lam rafında ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🔬 puanı yıldızı etkilemez) |
| Soru havuzu | 100 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Fayanslı, aydınlık laboratuvar; tezgâhta mikroskop; altta yalnızca "LAMI YERLEŞTİR" düğmesi.
- **Giriş:** Renkli lam tablaya kayar, odak düğmesi döner, göz merceğindeki görüntüde bulanık "CÜMLE MİKROSKOBU" yazısı netleşir; parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 yuvalı lam rafı; doğru görevde lam renkli boyanır ✓ (bonus doğruysa ★), yanlışta çatlak gri lam ✕.
- **Çıkış:** Preparat kutusuna 10 lam sırayla kayar (doğrular boyalı ✓, yanlışlar gri ✕), "LAB KARNESİ x/10 PREPARAT" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| paint | Lamı boya | Mavi ve turuncu boya kabı seçilip sözcüklere dokunularak cümlenin iki bölümü boyanır; silgi vardır |
| cut | Neşter | Sözcükler arasındaki çizgiye dokunularak cümle neden/sonuç, amaç/eylem ya da koşul/sonuç olarak ikiye ayrılır |
| turret | Döner objektif | Dört mercekli objektif çevrilir; alttaki mercek cümledeki ilişkiyi (neden-sonuç, amaç-sonuç, koşul-sonuç, karşılaştırma, benzetme) gösterir |
| swipe | Lam kaydırma | Kartlar parmakla sola/sağa kaydırılır (nesnel/öznel, çıkarılabilir/çıkarılamaz, aynı/farklı anlam) |
| merge | Pipetle birleştir | Bağlayıcı pipeti iki parçanın arasına sürüklenip damlatılır |
| lens | Büyüteç | Büyüteç sözcükler üzerinde kaydırılır; örtülü anlam ya da öznellik yaratan sözcük incelenir |
| complete | Lamı kapat | Cümlenin uygun sonu sürüklenip lama bırakılır |
| bin | Bölmeler | İlişki türleri, nesnel/öznel, örtülü anlam var/yok, benzetme/karşılaştırma, tutarlı/çelişkili |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| neden | 20 | Neden-sonuç ve amaç-sonuç |
| kosul | 20 | Koşul-sonuç ve karşılaştırma |
| yargi | 20 | Öznel ve nesnel yargı |
| ortuk | 20 | Örtülü anlam ve çıkarım |
| yorum | 20 | Cümle yorumlama, anlamca yakın cümleler, cümle tamamlama, benzetme |

Görev türlerinin dağılımı: swipe 18, lens 15, complete 15, paint 12, turret 12, bin 12, cut 9, merge 7.

Bütün cümleler özgündür.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (cümle, mercekler, kartlar, pipetler, bölmeler) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (boyanan bölümler, kesik yeri, seçilen mercek, kart yönleri, birleştirilen cümle, incelenen sözcük, tamamlanan cümle).
- correctAnswer doğru sonucu yazar; boyamada bağlaç gibi sınırdaki sözcükler serbest bırakılır.
- sourceRef: 8. Sınıf Öğretim Programı, Okuma: Anlam Bilgisi.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
