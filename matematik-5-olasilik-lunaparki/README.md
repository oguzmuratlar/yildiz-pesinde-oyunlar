# Olasılık Lunaparkı · Kesin mi, İmkânsız mı?

| Alan | Değer |
|---|---|
| gameId | matematik-5-olasilik-lunaparki |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 5 (oyun yalnızca 5. sınıf bağlamını kabul eder) |
| Tema | 7. Tema: Veriden Olasılığa |
| Ekran yönü | Dikey |
| Oyun türü | Olasılık göstergesinde (ibreli yarım daire) olayın bölgesini seçme + kurala göre kavanozdaki misketleri ya da çarkın bölgelerini boyayarak tasarlama + torba, çark, küp, yumurta kutusu, kuş ve tablo şekilli test + doğru/yanlış. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken gösterge ve tasarlama görevlerine öncelik verilir; süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 103 görev (42 test, 34 olasılık göstergesi, 17 doğru/yanlış, 10 tasarlama), index.html içine gömülüdür |

## Oyun

Ekranın üstünde gece ışıkları sönük bir dönme dolap vardır. Her doğru görev bir kabinin ışıklarını yakar; yanlış görevde kabin sönük kalır. Oyun sonunda dönme dolap döner (hareketi azaltma açıksa dönmez).

- **Olasılık göstergesi:** Bir olay yazılır (gerekirse torba, çark ya da küp şekliyle). Öğrenci beş bölgeli göstergede (İmkânsız · Az olası · Eşit olası · Çok olası · Kesin; altında 0 – 0,5 – 1) uygun bölgeye ya da alttaki renkli düğmeye dokunur, ibre o bölgeye döner.
- **Tasarla:** Kavanozdaki misketler ya da çarkın eş bölgeleri, renk seçilip dokunarak veya parmak sürüklenerek boyanır. Kural sağlanmalıdır (ör. “mavi kırmızıdan az olası olsun”, “kırmızı imkânsız olsun”, “yeşil %50 olsun”, “adil çark olsun”). Kurala uyan her boyama kabul edilir.
- **Test ve D/Y:** Torba, kavanoz, yumurta kutusu, daldaki kuşlar, çark, küp açınımı, dart tahtası ve tablo ekranda çizilir; her şeklin altında sayılar etiketle de yazılır.

Yanlış-cevap kaydında şekil metin olarak eklenir (ör. “[Torba: 3 kırmızı, 1 mavi]”); tasarlama görevlerinde öğrencinin boyaması ve kurala uyan örnek bir boyama yazılır.

## Soru havuzu

| Grup | İçerik |
|---|---|
| olay | Kesin, imkânsız ve olası olaylar; olasılık sözcükleri (kesinlikle, asla, belki…) |
| spektrum | Olasılık değerinin 0–1 arasında olması; kesir, ondalık ve yüzde gösterimi; olasılık spektrumu |
| torba | Torba, kavanoz, yumurta ve kuş durumlarında az/çok/eşit olası; kurala göre kavanoz tasarlama |
| cark | Çark, renk ve harf küpü, dart; adil oyun; kurala göre çark tasarlama |
| veri | Geçmiş verilere dayalı tahmin (yağış tablosu, satış verisi, atış sonuçları), öznel olasılık ve geçerli gerekçe |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır.

Yeni soru türleri için `questions.json` alanları: olasılık göstergesi `questionType: "probability_gauge"`, `event`, `zones`, `answerZone` (0 İmkânsız … 4 Kesin); tasarlama `questionType: "color_design"`, `object` (jar/spinner), `slots`, `palette`, `rules` (lt, gt, eq, zero, nonzero, all, half); şekiller `figure.kind`: bag, eggs, birds, spinner, cube, dart, table.

Kaynak: MEB Matematik 5. Sınıf Ders Kitabı 2. Kitap, 7. Tema (s. 164–182).
