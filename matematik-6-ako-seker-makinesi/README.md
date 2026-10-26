# Ako'nun Şeker Makinesi · Cebirsel İfadeler, Örüntüler, Algoritma

| Alan | Değer |
|---|---|
| gameId | matematik-6-ako-seker-makinesi |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 6 (oyun yalnızca 6. sınıf bağlamını kabul eder) |
| Tema | 6. Tema: İşlemlerle Cebirsel Düşünme ve Değişimler |
| Ekran yönü | Dikey |
| Oyun türü | Karakterli şekerleme mutfağı: aşçı ahtapot Ako + 10 kavanozlu şeker rafı + şeker sayacı ve 🔥 seri. Görevler: tarif kartlarıyla cebirsel ifade / örüntü kuralı kurma, şeker makinesi (ifadenin değerini hesaplayıp şekeri doğru kavanoza gönderme), akış şemasında hatalı bloğu bulma ya da boş bloğu doldurma, katsayı-sabit terim-değişken etiketleme, test ve doğru/yanlış. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken oyun görevlerine öncelik verilir (bir oyunun yaklaşık 7–8 görevi etkileşimli); süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 103 görev (40 tarif kartı, 19 şeker makinesi, 18 test, 10 doğru/yanlış, 8 etiketleme, 8 akış şeması), index.html içine gömülüdür |

## Oyun

Rehber karakter **Ako**, aşçı şapkalı pembe bir ahtapottur; konuşma balonuyla görevi anlatır, doğru cevapta kollarını kaldırıp zıplar, 3 doğru üst üste gelince coşar, yanlışta üzülüp cesaret verir. Ekranın üstündeki rafta 10 boş kavanoz vardır: doğru görevde kavanoz rengârenk şekerle dolar, yanlışta çatlak kalır.

- **Tarif kartları (ifade kurma):** Harf (değişken), sayı ve işlem kartlarına (+ − · ÷ ( )) sırayla dokunularak ifade kurulur; ⌫ ile silinir. Yan yana sayı ve harf çarpma demektir (4a = 4 · a). İfade eksikse (ör. açık parantez) kontrol düğmesi açılmaz ve uyarı yazılır. Değerlendirme, değişkenlere birkaç farklı değer verilerek yapılır: denk her ifade kabul edilir (3 · x + 5, 5 + 3x, x · 3 + 5 …). Şekil örüntüsü görevlerinde adımlar renkli şekerlerle çizilir.
- **Şeker makinesi:** Makinenin ekranında ifade ya da örüntü kuralı yazar (ör. 4 · a + 3). Banttan gelen her şekerin üstünde değişkenin değeri vardır (a = 8, 12. adım, x = 120, y = 20 …). Öğrenci değeri hesaplayıp şekeri doğru kavanoza gönderir; şeker kavisle kavanoza uçar. “Geri al” vardır. Bütün şekerler doğru kavanozdaysa görev doğrudur.
- **Akış şeması:** Bloklar kitaptaki şekilleriyle çizilir (oval: başla/bitir, paralelkenar: giriş/çıktı, dikdörtgen: işlem/atama, eşkenar dörtgen: karar). Ya hatalı blok bulunur (ör. altıgenin kenarı x · 6, ortalamada ÷ 2 yerine ÷ 3, b girilmeden toplam) ya da boş bloğa doğru şekil ve içerikteki kart konur.
- **Etiketle:** İfadenin kartlarından katsayıya, sabit terime ya da değişkenlere dokunulur.
- **Test ve D/Y:** Renkli seçenekler.

Yanlış-cevap kaydında kurulan ifade, yanlış kavanoza gönderilen şekerler, seçilen blok ya da etiketler ve doğru cevap yazılır; akış şemaları kayıtta metinle tarif edilir.

## Soru havuzu

| Grup | İçerik |
|---|---|
| ifade | Sözel ifadeden cebirsel ifade (fazlası, eksiği, katı, yarısı, çeyreği, parantezli ifadeler), değişken |
| terim | Katsayı, sabit terim, değişken; cebirsel ifadeye uygun sözel ifade; değişkenin değerine göre ifadenin değeri; problemler |
| oruntu | Sayı ve şekil örüntülerinin kuralı (an + b), istenen adımdaki terim |
| algoritma | Sözde kod, akış şeması blokları, hatalı adım, döngü, algoritmanın çıktısı |
| karma | İki değişkenli ifadeler ve karışık uygulamalar |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır. Kitaptaki gibi çarpma için “·” kullanılır.

Yeni soru türleri için `questions.json` alanları: `expression_build` (`target`: ASCII ifade, ör. `5*(x+8)`; `variables`; `tiles`), `candy_machine` (`machine`, `inputs[].label`, `inputs[].value`, `jars`), `flow_fix` (`mode`: error / blank, `blocks[].shape`: oval / par / rect / dia / ?, `blocks[].text`, `answerIndex`, `options` — blank modunda ilk seçenek doğrudur), `term_tag` (`tokens`, `answerIndices`).

Kaynak: MEB Matematik 6. Sınıf Ders Kitabı 2. Kitap, 6. Tema (s. 54–97).
