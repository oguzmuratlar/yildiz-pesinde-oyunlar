# Usta Düellosu — Arkadaş Düellosu oyunu

| Alan | Değer |
|---|---|
| gameId | duello-usta |
| Sürüm | 1.0.0 |
| Ders | Karışık (subjectId `mixed`); yanlış kayıtlarında `subjectId` = science / math / turkish |
| Sınıf | 6 |
| Kapsam | 6. sınıf MEB programı (Fen 1, 3, 4, 5, 6, 7. üniteler; Matematik 7 tema; Türkçe 6 tema) |
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
| Test (4 seçenek) | Seçeneğe dokun (seçenekler her açılışta karışır) | 360 |
| Doğru / Yanlış | Doğru / Yanlış düğmesi | 120 |
| Eşleştirme (3 çift) | Soldan birini, sağdan eşini seç; 3 eşleşme bitince gönderilir | 120 |

## Soru havuzu
| Ders | Kolay | Orta | Zor | Test | D/Y | Eşleştirme |
|---|---|---|---|---|---|---|
| Fen Bilimleri | 50 | 100 | 50 | 120 | 40 | 40 |
| Matematik | 50 | 100 | 50 | 120 | 40 | 40 |
| Türkçe | 50 | 100 | 50 | 120 | 40 | 40 |

### Ünite/tema dağılımı
- **Fen Bilimleri:** 1. Ünite: Güneş Sistemi ve Tutulmalar (28); 3. Ünite: Canlılarda Sistemler (41); 4. Ünite: Işığın Yansıması ve Renkler (34); 5. Ünite: Maddenin Ayırt Edici Özellikleri (33); 6. Ünite: Elektriğin İletimi ve Direnç (31); 7. Ünite: Sürdürülebilir Yaşam ve Etkileşim (33)
- **Matematik:** 1. Tema: Sayılar ve Nicelikler (1) (46); 6. Tema: İşlemlerle Cebirsel Düşünme ve Değişimler (29); 5. Tema: Geometrik Şekiller (25); 7. Tema: Geometrik Nicelikler (24); 4. Tema: İstatistiksel Araştırma Süreci (12); 2. Tema: Veriden Olasılığa (5); 3. Tema: Sayılar ve Nicelikler (2) (59)
- **Türkçe:** 1. Tema: Dilimizin Zenginliği (58); 2. Tema: Bağımsızlık Yolu (54); 3. Tema: Farklı Dünyalar (57); 6. Tema: Lider Ruhlar (6); 4. Tema: İletişim ve Sosyal İlişkiler (14); 5. Tema: Bilim ve Teknoloji (11)

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
