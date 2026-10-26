# Kazı'nın Tünelleri · Tam Sayılar, Rasyonel Sayılar ve İşlemler

| Alan | Değer |
|---|---|
| gameId | matematik-7-kazi-tunelleri |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Tema | 1. Tema: Sayılar ve Nicelikler (1) |
| Ekran yönü | Dikey |
| Oyun türü | Karakterli yeraltı macerası: madenci köstebek Kazı + 10 odalı tünel kesiti (yer yüzeyi 0, aşağısı negatif) + kristal sayacı ve 🔥 seri. Görevler: maden asansörüyle dikey sayı doğrusunda konum bulma, taş ayıklama (iki gruba ayırma), kristal kulesinde sıralama, işaret + değer kristaliyle işlem sonucu kurma, matkapla çok adımlı işlemi katman katman çözme, test ve doğru/yanlış. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor); deste kurulurken oyun görevlerine öncelik verilir ve türler dengelenir (bir oyunun 8–10 görevi etkileşimli); süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 123 görev (26 asansör, 22 işaret + değer, 13 matkap, 12 kristal kulesi, 10 taş ayıklama, 20 test, 20 doğru/yanlış), index.html içine gömülüdür |

## Oyun

Rehber karakter **Kazı**, baretli ve fenerli bir köstebektir; konuşma balonuyla görevi anlatır, doğru cevapta patilerini kaldırıp zıplar, 3 doğru üst üste gelince coşar, yanlışta üzülüp cesaret verir. Ekranın üstünde toprağın kesiti vardır: yer yüzeyi 0, aşağısı −1, −2 diye işaretlidir. Doğru görevde bir tünel odasında kristal parlar, yanlışta oda taşlarla dolar.

- **Maden asansörü:** Dikey sayı doğrusunda (yukarı pozitif, aşağı negatif; gerekirse her birim eş parçalara bölünmüş) asansör düğmelerle ya da sürüklenerek götürülür. 🚩 başlangıç noktasıdır. Konum bulma (deniz seviyesi, zemin kat, sıcaklık), rasyonel sayıyı gösterme, tam sayılarla ve rasyonel sayılarla toplama/çıkarma, en yakın tam sayı görevleri bu türdedir. Ekranda sayısal konum yazmaz.
- **Taş ayıklama:** Üstten grup seçilir, o gruba giren taşlara dokunulur (doğal sayı/değil, pozitif/negatif, mutlak değer, tam sayı/değil, rasyonel/tanımsız, sonlu/devirli ondalık).
- **Kristal kulesi:** Kristallere dokunarak kule alttan (küçükten büyüğe) ya da yukarıdan (büyükten küçüğe) doldurulur; yanlış yerleşen kristal geri alınabilir.
- **İşaret + değer:** Ekrandaki işlemin sonucu için önce işaret (pozitif/negatif), sonra değer kristali seçilir; işaret kuralı ile değer ayrı ayrı değerlendirilir.
- **Matkap:** Çok adımlı işlem ya da problem katmanlara bölünür; her katmanda o adımın sonucu seçilir (devirli ondalığı a/b'ye çevirme, işlem önceliği, problem adımları).
- **Test ve D/Y:** Renkli seçenekler.

Kesirler ekranda alt alta (pay/payda), devirli ondalık gösterimler devir çizgisiyle yazılır; kayıtlarda düz metin kullanılır ("−5/8", devreden basamaklar parantezde: "0,1(7)").

## Soru havuzu

| Grup | İçerik |
|---|---|
| tamsayi | Tam sayılarla gerçek yaşam durumları, dikey/yatay sayı doğrusu, doğal sayı–tam sayı ilişkisi, mutlak değer |
| rasyonel | Rasyonel sayı tanımı, tanımsız ifade, sayı doğrusunda gösterme, tam sayıların rasyonel sayı olması, sonlu ve devirli ondalık gösterim, devirli gösterimi a/b'ye çevirme |
| siralama | Tam sayıları ve rasyonel sayıları karşılaştırma ve sıralama, en yakın tam sayılar, iki rasyonel sayı arasındaki sayılar |
| tamislem | Tam sayılarla toplama, çıkarma, çarpma, bölme ve problemler (kat, sıcaklık, bakiye, kalori, dalış, saat dilimi) |
| rasislem | Rasyonel sayılarla dört işlem, işlem özellikleri, üslü ifadeler, çok adımlı işlemler ve problemler |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır.

Yeni soru türleri için `questions.json` alanları: `number_lift` (`low`, `high`: tam sayı aralığı, `parts`: bir birimin eş parça sayısı, `scale`: bir birimin değeri, `startStep`, `targetStep`: parça cinsinden konum, `zeroLabel`), `rock_sort` (`bins`, `items[].label`, `items[].bin`), `crystal_order` (`items` küçükten büyüğe, `descending`: dolum yönü), `sign_value` (`expression`, `sign`, `magnitudes` — ilk değer doğrudur), `drill_steps` (`steps[].prompt`, `steps[].options` — ilk seçenek doğrudur). Metinlerde `{a/b}` kesir, `[[A|B]]` devirli ondalık gösterimdir (B devreder).

Kaynak: MEB Matematik 7. Sınıf Ders Kitabı 1. Kitap, 1. Tema (s. 14–116).
