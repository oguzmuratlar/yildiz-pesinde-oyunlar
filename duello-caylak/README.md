# Çaylak Düellosu — Arkadaş Düellosu oyunu

| Alan | Değer |
|---|---|
| gameId | duello-caylak |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış kayıtlarında `subjectId` = science / math / turkish |
| Sınıf | 5 |
| Kapsam | 5. sınıf MEB programı (Fen 7 ünite, Matematik 7 tema, Türkçe 6 tema) |
| Ekran yönü | Dikey |
| Oyun türü | Gerçek zamanlı arkadaş düellosu (Köprü 1.0 + duel.* eki, v1.7 bölüm 3.8) |
| Tur süresi | 30 sn (sunucu `durationMs/remainingMs` gönderir) |
| Yıldız | Üretilmez; game.completed gönderilmez |
| Soru havuzu | 600 |
| Katalog | “Düello oyunu” işaretli |

## Akış
- **Bekleme odası:** iki avatar çerçevede, karşılaşma amblemi, davet geri sayımı, “Vazgeç” (duel.cancel).
- **3-2-1:** seviye hakemi ve büyük geri sayım; ardından 12 tur (sunucunun duel.round sırasıyla).
- **Tur:** üstte iki avatar, ortada hakem ve skor; altında ortadan başlayan güç barı (fark kadar kayar); tik-tak sesli dairesel sayaç; ders etiketi ve soru kartı. Cevap verilince kart kilitlenir, duel.answer gider; rakip cevaplayınca “Rakip cevapladı” görünür; duel.score gelince doğru/yanlış rozetleri, doğru cevap ve açıklama gösterilir.
- **Uzatma:** 13. turdan itibaren “Uzatma!” afişi; tur adı “Uzatma n”.
- **Bitiş:** kazanınca kutlayan hakem, kazanan rozeti ve konfeti; kaybedince “Bu sefer … kazandı”; iki taraf koparsa “yarıda kaldı”. Rövanş (duel.rematch) ve Çık (duel.exit).
- Rakip koparsa/döndüğünde bilgi afişi; geri dönüşte `state:"resume"` + `resume` ya da ayrı `duel.resume` ile kaldığı turdan devam eder.

## Soru seçimi
- Sunucu her turda yalnızca ders ve zorluk gönderir. Soru türü `seed + roundNo` ile seçilir; iki oyuncuya aynı turda aynı tür gelir.
- Havuz, seed ile karıştırılır; iki oyuncu her turda aynı soruyu görür (taraf ve cihazdaki geçmiş seçimi etkilemez). Düello içinde soru tekrar etmez.
- Düello içinde soru tekrar etmez (seed’e göre saklanır). Son 360 soru cihazda hatırlanır ve önce görülmemiş sorular seçilir.

## Soru türleri
| Tür | Mekanik | Adet |
|---|---|---|
| Test (4 seçenek) | Seçeneğe dokun (seçenekler her açılışta karışır) | 357 |
| Doğru / Yanlış | Doğru / Yanlış düğmesi | 123 |
| Eşleştirme (3 çift) | Soldan birini, sağdan eşini seç; 3 eşleşme bitince gönderilir | 120 |

## Soru havuzu
| Ders | Kolay | Orta | Zor | Test | D/Y | Eşleştirme |
|---|---|---|---|---|---|---|
| Fen Bilimleri | 50 | 100 | 50 | 117 | 43 | 40 |
| Matematik | 50 | 100 | 50 | 120 | 40 | 40 |
| Türkçe | 50 | 100 | 50 | 120 | 40 | 40 |

### Ünite/tema dağılımı
- **Fen Bilimleri:** 1. Ünite: Gökyüzündeki Komşularımız ve Biz (29); 2. Ünite: Kuvveti Tanıyalım (29); 3. Ünite: Canlıların Yapısına Yolculuk (32); 4. Ünite: Işığın Dünyası (26); 5. Ünite: Maddenin Doğası (28); 6. Ünite: Yaşamımızdaki Elektrik (28); 7. Ünite: Sürdürülebilir Yaşam ve Geri Dönüşüm (28)
- **Matematik:** 1. Tema: Geometrik Şekiller (37); 4. Tema: Sayılar ve Nicelikler (2): Kesirler (43); 7. Tema: Veriden Olasılığa (15); 5. Tema: İstatistiksel Araştırma Süreci (11); 3. Tema: Geometrik Nicelikler (27); 6. Tema: İşlemlerle Cebirsel Düşünme (28); 2. Tema: Sayılar ve Nicelikler (1) (39)
- **Türkçe:** 1. Tema: Oyun Dünyası (40); 2. Tema: Atatürk’ü Tanımak (71); 3. Tema: Duygularımı Tanıyorum (29); 4. Tema: Geleneklerimiz (16); 5. Tema: İletişim ve Sosyal İlişkiler (24); 6. Tema: Sağlıklı Yaşıyorum (20)

## Yanlış cevap kaydı
`duel.answer.record` = {questionId, isCorrect:false, questionText, studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation, subjectId}. Metinler düz Türkçedir; paragraf, şekil açıklaması ve seçenekler questionText’e eklenir.

## Kaynak
Sorular MEB ders kitaplarına dayanan mevcut oyun havuzlarımızın konu, kazanım ve sayfa bilgileriyle özgün olarak yazıldı; Matematik soruları konu şablonlarıyla üretildi. Paragraflar özgündür. 

## Teknik
- Uygulamadan oyuna: `window.YildizPesindeGame.receiveMessage(json)`; oyundan uygulamaya: YildizPesindeBridge taşıması.
- Düello dışı açılış reddedilir (“Bu oyun yalnızca düelloda açılır.”).
- CSP: harici ağ yok; görseller data URI (webp).
- Tarayıcıda doğrudan açılınca “Deneme modu”: bot rakiple yerel düello, kayıt yok.
- En düşük WebView: iOS 15.4, Android System WebView 98.
