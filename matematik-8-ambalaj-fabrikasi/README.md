# Ambalaj Fabrikası · Geometrik Cisimler

| Alan | Değer |
|---|---|
| gameId | matematik-8-ambalaj-fabrikasi |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 12. Ünite: Geometrik Cisimler |
| Ekran yönü | Dikey |
| Oyun türü | Ambalaj tasarım atölyesi, karaktersiz. Her görev bir ambalaj işidir: küp kutu kalıbına kare ekleme/çıkarma, prizma ve piramit kutunun yüz-ayrıt-köşe etiketini basma, teneke kutunun etiketini sürükleyerek kesme ya da kutunun yarıçapını ayarlama (silindir açınımı), yüzey alanı/hacim formül kartını doldurma, tankta sıvı seviyesini sürükleme, koni-piramit-silindir-prizma parçalarını sırayla işaretleme, piramit kalıbına yanal yüz ekleme, bölmeler, tuş takımı. Şıklı soru yoktur. π = 3 alınır. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "hangi kutu daha çok alır?" bonusu: iki silindirin hacmi karşılaştırılır. Doğruysa +30 🏷️ ve rafta ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🏷️ puanı yıldızı etkilemez) |
| Soru havuzu | 100 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Turkuaz atölye duvarı, tavan lambaları, tezgâhta açık duran karton küp kalıbı, "AMBALAJ FABRİKASI" tabelası; altta yalnızca "ÜRETİME BAŞLA" düğmesi.
- **Giriş:** Kalıbın yüzleri tek tek katlanır (3B), kapak kapanır, "KALİTE ✓" bandı yapışır, kutu kayarak çıkar; parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 bölmeli raf; doğru görevde rafa koli ya da teneke kutu gelir ✓ (bonus doğruysa sarı bant ★), yanlışta ezik kutu ✕.
- **Çıkış:** İki katlı rafa 10 ambalaj sırayla düşer (doğrular renkli ✓, yanlışlar gri ✕), "ÜRETİM KARNESİ x/10 KOLİ" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| netb | Küp kalıbı | 5×4 kesim tablasında kalıba bir kare eklenir ya da fazla kare çıkarılır; katlanınca küp olan her seçim kabul (katlama denetimi) |
| count | Etiket bas | Prizma/piramit çiziminden yüz, ayrıt ve köşe sayıları sayaçlarla girilir |
| cylnet | Etiket kes | Etiket şeridi cetvel üzerinde sürüklenerek taban çevresi kadar kesilir ya da kutunun yarıçapı ayarlanır; etiket kutuyu sarar |
| fill | Formül kartı | Taban alanı, yanal alan, yüzey alanı ya da hacim satırları tuş takımıyla doldurulur |
| level | Tank seviyesi | Verilen hacimdeki sıvının yüksekliği tutamaçla işaretlenir; sıvı dökülür ve gerçek seviye görünür |
| tap | Parçaları işaretle | Koni, piramit, silindir ya da prizmada istenen elemanlara (tepe noktası, ana doğru, yükseklik, yarıçap, taban, yanal yüz, ayrıtlar) sırayla dokunulur |
| pyrnet | Piramit kalıbı | Taban çokgeninin kenarlarına dokunularak eksik üçgen yanal yüzler eklenir |
| bin | Bölmeler | Prizma mı, silindir mi, piramit/koni/silindir özellikleri, taban/yanal alan, doğru–yanlış |
| key | Tuş takımı | Eleman sayıları, çevre, yanal alan, yüzey alanı, hacim, ana doğru problemleri |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| prizma | 20 | Dik prizmalar, elemanları ve açınımı |
| silindir | 20 | Dik dairesel silindirin elemanları ve açınımı |
| yuzey | 20 | Silindirin yüzey alanı |
| hacim | 20 | Silindirin hacmi |
| piramit | 20 | Dik piramit ve dik koni |

Görev türlerinin dağılımı: key 23, fill 16, count 11, cylnet 11, tap 11, netb 8, bin 8, level 8, pyrnet 4.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (kalıptaki kareler, cisim, yarıçap/yükseklik, hacim, istenen elemanlar) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (eklenen/çıkarılan kare, sayaç değerleri, etiket uzunluğu ya da yarıçap, kart satırları, seviye işareti, işaretlenen parçalar, eklenen yanal yüz sayısı).
- correctAnswer doğru sonucu yazar; küp kalıbında katlanınca küp olan her kare kabul edilir.
- sourceRef: 8. Sınıf Öğretim Programı, 12. Ünite “Geometrik Cisimler”.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
