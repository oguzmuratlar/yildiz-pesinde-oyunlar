# Geo Akış · Şekil Şekil Kaydır

| Alan | Değer |
|---|---|
| gameId | matematik-5-geo-akis |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 5 (oyun yalnızca 5. sınıf bağlamını kabul eder) |
| Tema | 1. Tema: Geometrik Şekiller |
| Ekran yönü | Dikey |
| Oyun türü | Reels tarzı dikey akış + sağa/sola kaydırmalı karar kartları + Duolingo tarzı seç-kontrol et ve alt geri bildirim şeridi. 10 kart, kolaydan zora (3 kolay · 4 orta · 3 zor); süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 110 görev (70 test, 21 doğru/yanlış kaydırma, 19 iki seçenekli kaydırma), 40'ı oyun içinde çizilen şekille; index.html içine gömülüdür |

## Oyun

Her soru tam ekran bir “reel” kartıdır. Şekil gereken sorularda nokta, doğru, ışın, açı, açıölçer, kesişen/paralel doğrular, çokgen, köşegen, üçgen ve kesişen çember şekilleri SVG ile çizilir.

- **Kaydır ve karar ver:** İki seçenekli kartlar (Doğru/Yanlış, Dar/Geniş açı, Paralel/Kesişen…) parmakla sağa ya da sola fırlatılır. Alttaki iki düğme de aynı işi yapar.
- **Seç ve kontrol et:** Çoktan seçmelide seçenek seçilir, “Kontrol et”e basılır.
- **Geri bildirim:** Alttan yeşil/kırmızı şerit çıkar; doğru cevap ve kısa açıklama gösterilir. “Devam” ya da yukarı kaydırma ile sıradaki kart aşağıdan gelir.
- **Seri ve puan:** Üst üste doğrular 🔥 seriyi büyütür; 3 ve üzeri seride bonus puan gelir. Puan ve seri yalnız oyun içi motivasyondur; uygulamaya giden sonuç yıldız ve doğru sayısıdır.

Yanlış-cevap kaydında şekilli soruların şekli metin olarak da yazılır (ör. “[Şekil: Köşesi O olan, ölçüsü 130° olan bir açı.]”), böylece hata defterinde soru anlaşılır kalır.

## Soru havuzu

| Grup | İçerik |
|---|---|
| temel | Nokta, doğru, doğru parçası, ışın, gösterimler, uzunluk, düzlem, çember-daire, yarıçap-çap, dikme, çizim araçları |
| aci | Derece, dar/dik/geniş/doğru/tam açı, açıölçerle okuma, eş açı, açının elemanları |
| dogru | Kesişen, dik, paralel, çakışık doğrular; ters, komşu, tümler, bütünler açılar; üç doğru; paralel ve kesen |
| cokgen | Çokgen, kenar/köşe/iç açı/dış açı, isimlendirme, köşegen, düzgün çokgen |
| ucgen | Açılarına ve kenarlarına göre üçgenler, iç açılar toplamı, eşkenar/ikizkenar özellikleri, kesişen çemberlerle üçgen inşası |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır.

Kaynak: MEB Matematik 5. Sınıf Ders Kitabı 1. Kitap, 1. Tema (s. 12–91).
