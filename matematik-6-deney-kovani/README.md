# Deney Kovanı · Deney, Sıklık, Deneysel Olasılık

| Alan | Değer |
|---|---|
| gameId | matematik-6-deney-kovani |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 6 (oyun yalnızca 6. sınıf bağlamını kabul eder) |
| Tema | 2. Tema: Veriden Olasılığa |
| Ekran yönü | Dikey |
| Oyun türü | Sanal deney yapma (para, sayı küpü, çark, torba) + çetele tablosu + sıklığı / göreli sıklığı / yüzdeyi bal peteği gözlerini doldurarak gösterme + test + doğru/yanlış. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken deney ve petek görevlerine öncelik verilir; süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 107 görev (59 test, 18 bal peteği, 15 deney, 15 doğru/yanlış), index.html içine gömülüdür |

## Oyun

Ekranın üstünde 10 gözlü bir kovan vardır. Her doğru görevde bir göz balla dolar ve yanına bir arı gelir; yanlış görevde göz gri ve çatlak kalır. Oyun sonunda arılar uçuşur (hareketi azaltma açıksa uçuşmaz).

- **Deney yap:** Öğrenci “1 kez at / 5 kez at” (çarkta “çevir”, torbada “çek”) düğmeleriyle deneyi 10 ya da 20 kez kendisi yapar. Sonuçlar gerçekten rastgeledir ve her denemede çetele tablosuna işlenir (beşli çetele çizgisi + sayı). Sorulan olayın çıktıları tabloda yeşil satırla gösterilir. Deney bitince öğrenci:
  - olayın **sıklığını**, **deneysel olasılığını (kesir)** ya da **yüzde** olarak deneysel olasılığını petekte gösterir, veya
  - deneyine göre deneysel olasılığı **en fazla** olan çıktıyı seçer (eşitlikte en çok gelen çıktıların hepsi doğru sayılır).
  Doğru cevap öğrencinin kendi deney sonuçlarından hesaplanır.
- **Bal peteği:** Petekte deney sayısı kadar göz (kesir ve sıklık) ya da 100 göz (yüzde) vardır. Bal alttan dolar: öğrenci balın ulaşacağı göze dokunur, − / + ile ince ayar yapar. Göstergede kesir, yüzde ya da “… kez” yazar. Yüzde görevlerinde öğrenci kesri paydası 100 olacak şekilde düşünüp gözleri doldurur (ör. 7/20 → 35 göz → %35).
- **Test ve D/Y:** Seçeneğe dokunulur. Tablo, sütun grafiği, nokta grafiği ve ham veri listesi gereken sorularda ekranda çizilir.

Yanlış-cevap kaydında petekte doldurulan değer, deney görevlerinde öğrencinin bütün deney sonuçları (ör. “Yazı 12, Tura 8”) ve bu sonuçlara göre doğru değer yazılır.

## Soru havuzu

| Grup | İçerik |
|---|---|
| kavram | Deney, çıktı, olay; çift/asal sayı gelme olaylarının çıktıları; çekip geri koyma; olasılık 0–1 aralığı |
| siklik | Sıklık, sıklık tablosu, sütun ve nokta grafiği okuma, ham veriden sayma, eksik sıklık bulma |
| goreli | Göreli sıklık = sıklık ÷ deney sayısı, deneysel olasılığı kesirle gösterme, deney yapıp hesaplama |
| yuzde | Deneysel olasılığı yüzde ile ifade etme (penaltı, okçu, otobüs, sıcaklık, balıkçı problemleri) |
| karar | Deneysel olasılıkları karşılaştırma, farklı deney sayılarında oran karşılaştırma, eksik değer bulma, deney sayısının etkisi |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır. Kesirler metinde `{pay/payda}` biçimiyle yazılır ve oyunda kesir çizgisiyle gösterilir; yanlış-cevap kaydına `pay/payda` olarak düz metin gider.

Yeni soru türleri için `questions.json` alanları: bal peteği `questionType: "honey_fill"`, `mode` (`sayi` / `kesir` / `yuzde`), `trials`, `cells`, `targetCells`; deney `questionType: "experiment"`, `device` (`kind`: `coin` / `die` / `spinner` / `bag`, `outcomes`, `colors`), `trials`, `event`, `ask` (`sayi` / `kesir` / `yuzde` / `mode`), `cells`. Veri gereken sorularda `figure` (`table` / `bar` / `dot` / `raw`) ve düz metin karşılığı `figureText` vardır.

Kaynak: MEB Matematik 6. Sınıf Ders Kitabı 1. Kitap, 2. Tema (s. 60–83).
