# Robo Atölye · İşlem, Örüntü, Algoritma

| Alan | Değer |
|---|---|
| gameId | matematik-5-robo-atolye |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 5 (oyun yalnızca 5. sınıf bağlamını kabul eder) |
| Tema | 6. Tema: İşlemlerle Cebirsel Düşünme |
| Ekran yönü | Dikey |
| Oyun türü | İşlem sırasına göre adım adım işlem çözme (doğru işleme dokunma) + kibrit dizerek şekil örüntüsünün sonraki adımını kurma + sayı çarkıyla cevap kurma + test + doğru/yanlış. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken işlem sırası, kibrit ve sayı çarkı görevlerine öncelik verilir; süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 114 görev (47 sayı çarkı, 32 test, 14 doğru/yanlış, 14 işlem sırası, 7 kibrit örüntüsü), index.html içine gömülüdür |

## Oyun

Ekranın üstünde bir robot atölyesi ve yarım kalmış bir robot vardır. Her doğru görev robota parlak bir parça takar (bacaklar, gövde, kollar, göğüs paneli, kafa, gözler, anten, ayaklar); yanlış görevde parça paslı takılır. 7 ve üzeri doğruda robotun gözleri yanar.

- **İşlem sırası:** Birden fazla işlem içeren ifade (parantez, kare ve küp dahil) büyük yazılır. Öğrenci önce yapılması gereken işlemin turuncu işaretine (üslü ifadede küçük üs düğmesine) dokunur; işlem kendiliğinden yapılır, ifade kısalır ve yapılan adım alta yazılır. Yanlış işleme dokunulursa görev yanlış sayılır, doğru işlem yeşil yanıp sönerek gösterilir ve öğrenci işlemi sonuna kadar tamamlar. Aynı önceliğe sahip ve birbirinden bağımsız işlemler (ör. 2 x 3 + 4 x 5'teki iki çarpma) hangi sırayla yapılırsa yapılsın kabul edilir.
- **Kibrit örüntüsü:** Örüntünün ilk üç adımı çizilidir. Öğrenci 8 × 5'lik zeminde çizgilere dokunarak veya parmağını sürükleyerek kibrit dizer ve 4. adımı kurar. Şekil zeminin herhangi bir yerine kurulabilir. Yanlışta fazla kibritler kırmızı, eksikler yeşil kesikli çizgiyle gösterilir.
- **Sayı çarkı:** Cevap, rakamları ▲ ▼ düğmeleriyle ya da parmakla yukarı-aşağı kaydırarak kurulur (3 veya 4 basamak).
- **Akış şeması:** Algoritma sorularında başla/bitir, giriş, işlem, karar ve çıktı şekilleriyle akış şeması (döngü okuyla) ekranda çizilir.
- Eşitlik soruları denklemi kutu içinde, ▲ ile gösterir. Bütün veriler ekrandadır.

Yanlış-cevap kaydında akış şeması ve kibrit örüntüsü metin olarak eklenir; işlem sırası görevlerinde öğrencinin önce seçtiği yanlış işlem ve doğru adımların tamamı yazılır.

## Soru havuzu

| Grup | İçerik |
|---|---|
| esitlik | Eşitliğin iki tarafına aynı sayıyı ekleme/çıkarma, aynı sayıyla çarpma/bölme; terazi ve halat çekme durumları |
| ozellik | Toplama ve çarpmada değişme ve birleşme özelliği, çarpmanın toplama ve çıkarma üzerine dağılma özelliği, zihinden işlem |
| oncelik | Kare ve küp (üslü ifade), işlem önceliği, problemlere uygun çok işlemli sayı cümlesi |
| oruntu | Sayı ve şekil örüntüleri, örüntünün kuralı, istenen adımı bulma, kibritle sonraki adımı kurma |
| algoritma | Algoritma ve akış şeması şekilleri, akış şemasını çalıştırma (döngüler dahil), tekrarlı çıkarma ile bölme |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır.

Yeni soru türleri için `questions.json` alanları: sayı çarkı `questionType: "number_dial"`, `answerNumber`, `digits`, `answerUnit`; işlem sırası `questionType: "operation_order"`, `expression`, `steps`, `result`; kibrit örüntüsü `questionType: "stick_pattern"`, `pattern`, `steps` (1–3. adım kibritleri), `target`, `board`; akış şeması `figure.kind: "flow"`.

Kaynak: MEB Matematik 5. Sınıf Ders Kitabı 2. Kitap, 6. Tema (s. 114–163).
