# Virgül'ün Yolculuğu · Ondalık Gösterimler, Kesir-Bölme, Kesirlerle İşlemler, Uzunluk Ölçme

| Alan | Değer |
|---|---|
| gameId | matematik-6-virgulun-yolculugu |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 6 (oyun yalnızca 6. sınıf bağlamını kabul eder) |
| Tema | 3. Tema: Sayılar ve Nicelikler (2) |
| Ekran yönü | Dikey |
| Oyun türü | Karakterli macera: rehber karakter Virgül + 10 duraklı yol haritası + puan ve seri (🔥). Görevler: virgülü kaydırma, basamak abaküsü, adım adım bölme, pasta (alan) modeli, test, doğru/yanlış. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken etkileşimli görevlere öncelik verilir; süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 148 görev (73 test, 26 virgül kaydırma, 16 abaküs, 16 doğru/yanlış, 11 adım adım bölme, 6 pasta modeli), index.html içine gömülüdür |

## Oyun

Rehber karakter **Virgül**, virgül biçiminde mor ve sevimli bir karakterdir. Her görevde konuşma balonuyla ipucu verir. Doğru cevapta zıplar, sevinir; seri 3'ü geçince coşar. Yanlış cevapta üzülür ve cesaretlendirir. Ekranın üstünde 10 duraklı yol haritası vardır: Virgül her görevden sonra bir sonraki durağa zıplar, doğru duraklar altın yıldız olur, sonda hazine sandığı açılır. Doğru cevap 10 puan, 3 ve üzeri seride 15 puan kazandırır (puan ve seri yalnızca oyun içi motivasyon içindir; sonuç kaydı yıldız ve doğru sayısıyla yapılır). Duolingo tarzı akış: seçenek seçilir, alttaki **KONTROL ET** ile onaylanır, alttan yeşil/kırmızı geri bildirim paneli açılır.

- **Virgülü kaydır:** Sayının rakamları kutucuklarda durur; Virgül (karakterin küçük hâli) aralardan birinde bekler. Öğrenci aralara dokunarak ya da ◀ ▶ ile virgülü taşır; gerekirse soluk sıfırlar devreye girer (ör. 8 ÷ 1000 → 0,008; 42 km → 42 000 m). Birim dönüştürmede km–hm–dam–m–dm–cm–mm merdiveni gösterilir.
- **Abaküs:** Her çubuk bir basamak (binler … binde birler), birler ile onda birler arasında virgül vardır. Boncuk eklenip çıkarılarak ondalık gösterim kurulur: kesirlerin toplamı biçiminden, basamak değerlerinden, yuvarlama sonucundan, toplama/çıkarma sonucundan.
- **Adım adım bölme:** Payı paydaya bölerek ondalık gösterim bulunur. Öğrenci her adımda “bölen x ▢ en fazla … olabilir” sorusuna rakam seçer; kalan, virgül koyma ve sıfır ekleme adımları günlüğe yazılır. Aynı kalan tekrar gelince “Ne olur?” diye sorulur; devirli gösterim devir çizgisiyle yazılır. Hatalı rakamda nedeni anında gösterilir (görev yanlış sayılır ama tamamlatılır).
- **Pasta modeli:** Kare pastada sütun ve satır sekmeleriyle iki kesrin çarpımı gösterilir; ortak bölge yeşil olur (ör. 3/4'ünün 1/3'ü = 3/12). Hangi sütunların/satırların seçildiği önemli değildir, sayıları doğruysa kabul edilir.
- **Test ve D/Y:** Kesirler alt alta, devirli ondalık gösterimler devir çizgisiyle, tam sayılı kesirler “6 3/4” biçiminde gösterilir; gereken yerde tablo çizilir.

Yanlış-cevap kaydında öğrencinin kurduğu sayı / virgülün kaydığı basamak sayısı / abaküs değeri / bölmedeki hataları / modelde seçtiği sütun-satır sayısı ve doğru cevap düz metinle yazılır (kesir “3/4”, tam sayılı kesir “6 tam 3/4”, devirli gösterim “0,1666...”).

## Soru havuzu

| Grup | İçerik |
|---|---|
| basamak | Ondalık gösterimlerde basamak adı ve basamak değeri, paydası 10-100-1000 olan kesirlerin toplamı, sıralama, yuvarlama |
| bolme | Kesir-bölme ilişkisi, payı paydaya bölme, sonlu ve devirli ondalık gösterim, devir çizgisi |
| kesir | Kesirlerle toplama-çıkarma, doğal sayı ile kesir çarpımı, iki kesrin çarpımı, doğal sayı/kesir bölmeleri, problemler |
| ondalik | Ondalık gösterimlerle dört işlem, 10-100-1000 ile kısa yoldan çarpma-bölme, yüzde, indirim-zam, KDV |
| uzunluk | Uzunluk ölçme birimleri, birim dönüştürme, uygun birim seçme |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır. Kitabın terimleri kullanılır (“ondalık gösterim”, “devirli ondalık gösterim”, “onda birler basamağı”).

Yeni soru türleri için `questions.json` alanları: virgül kaydırma `questionType: "comma_slide"`, `digits`, `start`, `target`, `padLeft`, `padRight`, isteğe bağlı `units`; abaküs `questionType: "abacus"`, `ints`, `decs`, `targetDigits`; adım adım bölme `questionType: "long_division"`, `dividend`, `divisor`, `repeating`; pasta modeli `questionType: "area_model"`, `colsTotal`, `colsTarget`, `rowsTotal`, `rowsTarget`. Metin biçimleri: `{a/b}` kesir, `{w a/b}` tam sayılı kesir, `[[0,1|6]]` devirli gösterim (çizgi `|` sonrasındaki rakamların üstünde).

Kaynak: MEB Matematik 6. Sınıf Ders Kitabı 1. Kitap, 3. Tema (s. 84–161).
