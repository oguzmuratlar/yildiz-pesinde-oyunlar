# Fiilimsi Terzisi · Fiilimsiler

| Alan | Değer |
|---|---|
| gameId | turkce-8-fiilimsi-terzisi |
| Güncel sürüm | 1.0.0 |
| Ders | Türkçe (oyun içi subjectId: turkish; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Konu | Fiilimsiler (isim-fiil, sıfat-fiil, zarf-fiil) |
| Ekran yönü | Dikey |
| Oyun türü | Terzi atölyesi, karaktersiz. Her görev bir terzi işidir: kumaştaki fiilimsilere toplu iğne takma, mezurayla fiilimsi sayısını ölçme, makasla kökü ve fiilimsi ekini ayırma, köke ek düğmesi dikme, sıfat-fiili nitelediği isme / zarf-fiili belirttiği yükleme iplikle bağlama, dikiş makinesinde fiilimsileri doğru makaraya dikme, makaradan iplik çekerek eşleştirme, askılara ayırma. Şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "hangi düğme …-fiil?" bonusu. Doğruysa +30 🔘 ve şeritte ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🔘 puanı yıldızı etkilemez) |
| Soru havuzu | 100 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Pembe puantiyeli atölye duvarı, ahşap tezgâh, makaralar; altta yalnızca "DİKİŞE BAŞLA" düğmesi.
- **Giriş:** Tezgâha turkuaz bir kumaş serilir, dikiş iğnesi kumaşın üzerinden geçerken "FİİLİMSİ TERZİSİ" yazısı harf harf işlenir, makas kumaşı keser; parlamayla oyuna geçilir.
- **İlerleme:** Üstte dikişli kumaş şeritte 10 düğme yeri; doğru görevde pembe düğme dikilir ✓ (bonus doğruysa sarı düğme ★), yanlışta sarkan iplik ✕.
- **Çıkış:** Cansız mankendeki ceketin önüne 10 düğme sırayla dikilir (yanlışlar boş ilik), "TERZİ KARNESİ x/10 DÜĞME" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| pin | Toplu iğne | Kumaş parçası sözcüklerden fiilimsilere (ya da istenen türe) iğne takılır |
| tape | Mezura | Mezuradaki kırmızı işaret sürüklenerek cümledeki fiilimsi sayısı ölçülür |
| snip | Makas | Sözcüğün harfleri arasına dokunularak fiil kökü ile fiilimsi eki ayrılır |
| button | Ek düğmesi | Köke uygun ek düğmesi dikilip boşluğa istenen türde fiilimsi yerleştirilir |
| thread | İplik | Sıfat-fiil ile nitelediği isim ya da zarf-fiil ile belirttiği yüklem iplikle bağlanır |
| sew | Dikiş makinesi | Cümleler tek tek gelir; parlayan fiilimsi isim/sıfat/zarf-fiil makarasıyla dikilir |
| match | Makara eşleştirme | Fiilimsiler ekleriyle, görevleriyle ya da anlamlarıyla iplik çekilerek eşleştirilir |
| bin | Askılar | Fiilimsi / çekimli fiil / kalıcı isim; isim-, sıfat-, zarf-fiil ekleri ve özellikleri |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| tanima | 20 | Fiilimsileri tanıma, sayma; çekimli fiil ve kalıcı isimden ayırma |
| isimfiil | 20 | İsim-fiiller |
| sifatfiil | 20 | Sıfat-fiiller ve nitelediği isimler |
| zarffiil | 20 | Zarf-fiiller ve belirttiği yüklemler |
| karisik | 20 | Fiilimsi türlerini ayırt etme |

Görev türlerinin dağılımı: pin 17, button 17, tape 14, snip 14, thread 12, bin 11, sew 10, match 5.

Bütün cümleler özgündür.

Yanlış-cevap kaydı:
- questionText görevi ve cümleyi/düzeneği (ek düğmeleri, sözcük, makaralar) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (iğnelenen sözcükler, ölçülen sayı, kesik yeri, dikilen ek, bağlanan sözcükler, makara seçimleri, eşleştirmeler).
- correctAnswer doğru sonucu yazar; kaynaştırma harfli sözcüklerde iki kesik yeri de kabul edilir.
- sourceRef: 8. Sınıf Öğretim Programı, Dil Bilgisi: Fiilimsiler.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
