# Sayı Akvaryumu · Çarpan, Kat, Bölünebilme, Asal

| Alan | Değer |
|---|---|
| gameId | matematik-6-sayi-akvaryumu |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 6 (oyun yalnızca 6. sınıf bağlamını kabul eder) |
| Tema | 1. Tema: Sayılar ve Nicelikler (1) |
| Ekran yönü | Dikey |
| Oyun türü | Kurala uyan sayıların baloncuklarını patlatma (çoklu seçim) + çarpan ağacını (mercan) adım adım kurma + test + doğru/yanlış. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken baloncuk ve çarpan mercanı görevlerine öncelik verilir; süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 102 görev (43 test, 34 baloncuk patlatma, 15 doğru/yanlış, 10 çarpan mercanı), index.html içine gömülüdür |

## Oyun

Ekranın üstünde boş bir akvaryum vardır. Her doğru görevde akvaryuma rengârenk bir balık gelir; yanlış görevde dibe gri bir taş düşer. Oyun sonunda balıklar yüzer (hareketi azaltma açıksa yüzmez).

- **Baloncuk patlat:** 8–14 baloncukta sayılar (ya da 0–9 rakamları) vardır. Öğrenci kurala uyan bütün baloncuklara dokunur (ör. “36'nın bölenleri”, “3 ile kalansız bölünenler”, “14▢ sayısı 3'e bölünüyorsa ▢ yerine gelebilecek rakamlar”, “8 ile aralarında asal olanlar”). Tekrar dokunulan baloncuk geri gelir. Kontrolde doğru seçimler yeşil, kurala uymayan seçimler kırmızı, kaçırılanlar yeşil kesikli gösterilir. Görevin doğru sayılması için bütün doğru baloncuklar seçilmeli, yanlış hiçbiri seçilmemelidir.
- **Çarpan mercanı:** Kök sayı (12, 20, 28, 30, 36, 45, 52, 72, 84, 90) mercanın tepesindedir. Parlayan sayıya dokunulur; asal değilse sunulan çarpan çiftlerinden biri seçilir (aralarında çarpımı tutmayan bir çeldirici ve 1 x n vardır), asalsa “Asal ✓” seçilir. Hangi çarpan çiftiyle başlanırsa başlansın kabul edilir. Bütün yapraklar asal olunca asal çarpanlara ayırma (ör. 72 = 2 x 2 x 2 x 3 x 3) yazılır. Herhangi bir hata görevi yanlış sayar ama ağaç tamamlatılır; hata nedeni (ör. “4 x 10 = 40, 36 değil.”) anında gösterilir.
- **Test ve D/Y:** Seçeneğe dokunulur.

Yanlış-cevap kaydında baloncuktaki bütün sayılar, öğrencinin seçtikleri, kurala uymayan seçimleri ve kaçırdıkları; çarpan mercanında yapılan hatalar ve doğru asal çarpan ayrımı yazılır.

## Soru havuzu

| Grup | İçerik |
|---|---|
| carpan | Çarpan, bölen, en küçük/en büyük çarpan, çarpan sayısı, bölenlerin toplamı, dikdörtgen ve eşit paylaştırma problemleri |
| kat | Katlar, en küçük kat, katların sonsuzluğu, kumbara, mola, asansör problemleri |
| bolunebilme | 2, 3, 4, 5, 6, 9 ve 10 ile kalansız bölünebilme; eksik rakam bulma |
| asal | Asal sayı, 1 ve 2'nin durumu, asal çarpanlar, çarpan ağacı |
| ortak | Ortak kat, ortak bölen, aralarında asal sayılar, otobüs-fener-kütüphane ve demet problemleri |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır. Ders kitabındaki gibi “EBOB/EKOK” terimleri kullanılmaz; “ortak katların en küçüğü”, “ortak bölen” denir.

Yeni soru türleri için `questions.json` alanları: baloncuk `questionType: "bubble_select"`, `numbers`, `targets`; çarpan mercanı `questionType: "factor_tree"`, `root`, `primeFactors`.

Kaynak: MEB Matematik 6. Sınıf Ders Kitabı 1. Kitap, 1. Tema (s. 12–59).
