# Uzman Düellosu — Arkadaş Düellosu oyunu

| Alan | Değer |
|---|---|
| gameId | duello-uzman |
| Sürüm | 1.1.0 (önceki 1.0.0 korunur) |
| Ders | Karışık (subjectId `mixed`); yanlış kayıtlarında `subjectId` = science / math / turkish |
| Sınıf | 7 |
| Kapsam | 7. sınıf MEB programı (Fen 7 ünite; Matematik 9 tema; Türkçe 6 tema) |
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
- **Fen Bilimleri:** 1. Ünite: Uzay Çağı (28); 2. Ünite: Kuvvet ve Enerjiyi Keşfedelim (29); Vücudumuzdaki Sistemler (16); 3. Ünite: Vücudumuzdaki Sistemler (16); 4. Ünite: Işığın Kırılması ve Mercekler (28); 5. Ünite: Maddenin Doğasına Yolculuk (29); 6. Ünite: Elektriklenme (26); 7. Ünite: Sürdürülebilir Yaşam ve Enerji (28)
- **Türkçe:** 2. Tema: Bir Hilal Uğruna (65); 5. Tema: Okuma Kültürü (27); 1. Tema: Hayat Boyu Gelişim (56); 3. Tema: İletişim ve Sosyal İlişkiler (11); 4. Tema: Türk Sanatı (24); 6. Tema: Hak ve Sorumluluklar (17)
- **Matematik:** 1. Tema: Sayılar ve Nicelikler (1) (69); 2. Tema: Geometrik Nicelikler (1) (26); 7. Tema: Veriden Olasılığa (12); 4. Tema: Dönüşüm (3); 8. Tema: İşlemlerle Cebirsel Düşünme ve Değişimler (47); 6. Tema: Sayılar ve Nicelikler (2) (17); 5. Tema: Geometrik Şekiller (4); 3. Tema: İstatistiksel Araştırma Süreci (11); 9. Tema: Geometrik Nicelikler (2) (11)

## Yanlış cevap kaydı
`duel.answer.record` = {questionId, isCorrect:false, questionText, studentAnswer, correctAnswer, unit, topic, outcome, sourceRef, explanation, subjectId}. Metinler düz Türkçedir; paragraf, şekil açıklaması ve seçenekler questionText’e eklenir.

## Kaynak
Sorular MEB ders kitaplarına dayanan mevcut oyun havuzlarımızın konu, kazanım ve sayfa bilgileriyle özgün olarak yazıldı; Matematik soruları konu şablonlarıyla üretildi. Paragraflar özgündür. 

## Sürüm 1.1.0 — Düello mesajları
- 1.0.0 değişmedi; 1.1.0 ayrı klasördedir. Admin'de oyunun adresi ve sürümü birlikte 1.1.0 yapılmalıdır (oyun init'te sürümü doğrular).
- Oyuncular yalnız sunucunun gönderdiği **hazır mesajlardan** seçerek mesaj atar; serbest metin yoktur.
- Mesaj düğmesi (💬, sol üst) yalnız şu durumda görünür: `app.init.payload.duel.features` içinde `"chat"` var **ve** `duel.chat.enabled === true` **ve** mesaj listesi dolu. Eski uygulama sürümleri `features` göndermediği için düğme çıkmaz; oyun 1.0.0 gibi çalışır.
- Oyun → uygulama: `duel.chat {chatId}`. Uygulama → oyun: `duel.chat {chatId, emoji, text}` (rakipten gelen), `duel.chatAck {ok, chatId, emoji, text, remaining | reason: cooldown|limit|disabled|invalid}`.
- Gelen mesaj, rakibin avatarının altında 3 sn balon olarak görünür; "Rakibin mesajlarını gizle" ile düello boyunca gizlenebilir. Metin her zaman düz metin olarak basılır (HTML çalışmaz).
- Bekleme süresi ve düello başına hak `duel.chat.cooldownMs` / `maxPerDuel` ile gelir (varsayılan 3000 ms / 10); asıl sınırı sunucu uygular.
- Deneme modunda bot da hazır mesajla cevap verir.

## Teknik
- Uygulamadan oyuna: `window.YildizPesindeGame.receiveMessage(json)`; oyundan uygulamaya: YildizPesindeBridge taşıması.
- Düello dışı açılış reddedilir (“Bu oyun yalnızca düelloda açılır.”).
- CSP: harici ağ yok; görseller data URI (webp).
- Tarayıcıda doğrudan açılınca “Deneme modu”: bot rakiple yerel düello, kayıt yok.
- En düşük WebView: iOS 15.4, Android System WebView 98.
