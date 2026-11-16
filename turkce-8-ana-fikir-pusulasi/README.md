# Ana Fikir Pusulası · Paragrafta Anlam

| Alan | Değer |
|---|---|
| gameId | turkce-8-ana-fikir-pusulasi |
| Güncel sürüm | 1.0.0 |
| Ders | Türkçe (oyun içi subjectId: turkish; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Konu | Paragrafta anlam |
| Ekran yönü | Dikey |
| Oyun türü | Şafakta dağ tırmanışı ve pusula, karaktersiz. Her görevde paragraf üstte, tek parça okunur; altında bir yol işi vardır: pusula iğnesini ana düşünce cümlesine çevirme, dört yönlü pusulada konu/amaç/ana düşünce/yol seçme, patikadan akışı bozan kaya-cümleyi atma, anahtar sözcüğün izini sürme, köprü tahtalarını sağlam/kırık yapıp geçme, başlık bayrağını zirveye dikme, yazarın tutumunu barometre ibresiyle gösterme, sırt çantalarına ayırma. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "bu cümle hangi yolu kullanıyor?" bonusu. Doğruysa +30 🧭 ve kampta ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🧭 puanı yıldızı etkilemez) |
| Soru havuzu | 100 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Şafak vakti mor-turuncu dağlar, kapağı kapalı pirinç pusula, "ANA FİKİR PUSULASI" tabelası; altta yalnızca "YOLA KOYUL" düğmesi.
- **Giriş:** Pusulanın kapağı açılır, iğne savrulup kuzeye oturur, güneş doğar, yamaçta kamp çadırları belirir; parlamayla oyuna geçilir.
- **İlerleme:** Üstte zirveye tırmanan patikada 10 kamp; doğru görevde çadır yanar ✓ (bonus doğruysa ★), yanlışta sönük ✕.
- **Çıkış:** Dağ yamacında 10 kamp sırayla belirir (doğrular çadır, onuncusu zirve bayrağı; yanlışlar sis), "ROTA KARNESİ x/10 KAMP" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| needle | Pusula iğnesi | Yarım daire pusulada iğne sürüklenerek ya da cümleye dokunarak istenen cümlenin numarasına çevrilir |
| dial | Dört yönlü pusula | Dört kart arasından biri seçilince pusula o yöne döner (konu, ana düşünce, yazarın amacı, düşünceyi geliştirme yolu) |
| rock | Kaya at | Paragrafın cümleleri patika taşlarıdır; akışı bozan taş kaldırılır |
| trail | İz sür | Anahtar sözcüğün paragrafta geçtiği her yere dokunulur |
| bridge | Köprü | Her tahta (yargı) sağlam ya da kırık yapılır; köprüden geçilir |
| flag | Zirve bayrağı | Uygun başlık bayrağı sürüklenip zirveye bırakılır |
| gauge | Barometre | İbre sürüklenerek yazarın tutumu (eleştirel / tarafsız / övgü dolu) gösterilir |
| bin | Sırt çantaları | Ana–yardımcı düşünce, değinilen–değinilmeyen, düşünceyi geliştirme yolları |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| anafikir | 20 | Ana düşünce, ana duygu |
| yardimci | 20 | Yardımcı düşünceler, akışı bozan cümle |
| konu | 20 | Konu, başlık, anahtar sözcük |
| cikarim | 20 | Çıkarım, yazarın amacı ve tutumu |
| gelistirme | 20 | Tanımlama, örnekleme, karşılaştırma, tanık gösterme, sayısal veri, benzetme |

Görev türlerinin dağılımı: dial 27, needle 19, bin 13, bridge 12, rock 9, flag 7, gauge 7, trail 6.

Bütün paragraflar özgündür.

Yanlış-cevap kaydı:
- questionText görevi ve paragrafın tamamını (numaralı cümlelerle) ve düzeneği (seçenekler, tahtalar, bayraklar) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (iğnenin gösterdiği cümle, seçilen yön, atılan taş, işaretlenen sözcükler, tahta durumları, dikilen bayrak, ibre konumu).
- correctAnswer doğru sonucu yazar; ana düşünce hem başta hem sonda verilmişse iki cümle de kabul edilir.
- sourceRef: 8. Sınıf Öğretim Programı, Okuma: Anlam Bilgisi.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
