# Pasaport Balonu · Dünya Turu

| Alan | Değer |
|---|---|
| gameId | turkce-6-pasaport-balonu |
| Güncel sürüm | 1.0.0 |
| Ders | Türkçe (oyun içi subjectId: turkish; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 6 (oyun yalnızca 6. sınıf bağlamını kabul eder) |
| Tema | 3. Tema: Farklı Dünyalar |
| Ekran yönü | Dikey |
| Oyun türü | Karma görev: kelime atölyesi (harf kutucuklarıyla kelime kurma), hatayı bul (cümlede yanlış yazılan kelimeye dokunma), doğru/yanlış, test, metinli soru. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken kelime atölyesi, hatayı bul ve D/Y görevlerine öncelik verilir; süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 132 görev (72 test, 33 kelime atölyesi, 15 hatayı bul, 12 doğru/yanlış), index.html içine gömülüdür |

## Oyun

Öğrenci sıcak hava balonuyla 10 ülkeyi gezer: Norveç, Danimarka, İspanya, Mısır, Bangladeş, Kazakistan, Özbekistan, Türkmenistan, Çin ve Grönland. Her ülkede bir görev vardır. Doğru cevap pasaporta o ülkenin renkli mührünü basar; yanlış cevapta durağa gri bir bulut mührü düşer. Tur bitince balon Türkiye’ye döner ve öğrenciye mühürlü pasaport sayfası gösterilir.

- **Kelime atölyesi:** “kitap + -ı” gibi bir kök ve ek verilir. Öğrenci harf kutucuklarını sırayla dizerek yeni kelimeyi kurar (kitabı). Kutucuklar arasında ses olayını unutanı yakalayan çeldirici harfler vardır. Konulmuş harfe dokunmak onu geri alır. “Kontrol et” ile cevap verilir.
- **Hatayı bul:** Bir cümle kelime kelime gösterilir. Öğrenci yazımı yanlış kelimeye dokunur, ardından doğru yazılışı görür.
- **D/Y ve test:** Metne dayalı sorularda metnin tamamı ekranda gösterilir.

Hiçbir soru kitaptaki bir metni okumuş olmayı gerektirmez.

## Soru havuzu

| Grup | İçerik |
|---|---|
| ses | Ünsüz yumuşaması, ünsüz benzeşmesi, ünlü düşmesi, ünlü daralması, yardımcı (kaynaştırma) ünsüzler, ünsüz ve ünlü türemesi |
| ek | Yapım eklerinin işlevleri (-cı, -lık, -ca, -cık), tema kelimeleri (göçebe, lehçe, fiyort, muson, antropolog, kültürel miras, ön ayak olmak) |
| yazim | “de/da” bağlacı ve bulunma eki, “ki” bağlacı ve “-ki” eki, “mi” soru eki, ünsüz türemesinin yazıma etkisi, iki nokta |
| anlam | Sebep-sonuç, amaç, zıtlık ve karşılaştırma ifadeleri, nesnel/öznel ve nitel/nicel cümleler, iki noktanın işlevleri |
| metin | Düşünceyi geliştirme yolları (tanımlama, benzetme, karşılaştırma, sayısal veri, tanık gösterme), metin bölümleri, soru sorma stratejisi, çoklu ortam, ekranda verilen kısa metinlerle yüzey ve derin anlam |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır.

Yeni soru türleri için `questions.json` alanları: kelime atölyesi `questionType: "word_building"`, `base`, `suffix`, `tiles`; hatayı bul `questionType: "error_spotting"`, `words`, `wrongIndexes`, `fix`.

Kaynak: MEB Türkçe 6. Sınıf Ders Kitabı 1. Kitap, 3. Tema (s. 116–171).
