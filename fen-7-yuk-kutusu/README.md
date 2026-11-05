# Yük Kutusu · Elektriklenme

| Alan | Değer |
|---|---|
| gameId | fen-7-yuk-kutusu |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Ünite | 6. Ünite: Elektriklenme |
| Ekran yönü | Dikey |
| Oyun türü | Kutu açmalı TV yarışması. Her turda 10 kutudan biri seçilir; kutudan etkileşimli bir deney düzeneği çıkar (sürtme, sürükleme, dokundurma, fırlatma, yerleştirme). Deney başarılıysa kutunun ödülü kasaya girer, başarısızsa ödül yanar. 3., 6. ve 9. görevden sonra bankacı arar: VARIM (teklifi al) ya da YOKUM (sonraki kutu ×2). Test ve şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (⚡ kasa puanı ve bankacı teklifleri yalnızca oyun içi eğlencedir, yıldızı etkilemez) |
| Soru havuzu | 100 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:**
  1. TV stüdyosu: sallanan spot ışıkları, sahne zemini ve "YÜK ⚡ KUTUSU" tabelası.
  2. "ŞOVU BAŞLAT" denince 10 altın kutu tek tek sahneye düşer.
  3. Tabelaya yıldırım çarpar, kutular sallanır, alkış sesiyle oyuna geçilir.
- **İlerleme:** Üstte 10 mini kutu vardır. Doğru görevde kutu yeşile döner (⚡), yanlışta söner (✕). Kutu panosunda açılan kutuların ödülü, yananlar ✕ ile görünür.
- **Çıkış:**
  1. Stüdyoda kasa toplamı belirir.
  2. 10 kutu sırayla açılır.
  3. "ŞOV ŞAMPİYONU x/10 KUTU" madalyası basılır, sonuç "YARIŞMA KARNESİ" olarak açılır.

## Görevler (deney düzenekleri)
| Tür | Görev | Mekanik |
|---|---|---|
| hang | Asılı küreler | Kilitsiz kürelere dokunarak yük (+ / − / nötr) verilir; serbest bırakınca küreler gerçekten iter/çeker, hedefler tek tek kontrol edilir |
| rub | Sürtünme tezgâhı | Çubuk (plastik/cam) ve kumaş (yün/ipek) seçilir, çubuk parmakla kumaşın üstünde sağa-sola sürtülür; elektron aktarımı canlandırılır. Zor görevlerde iki tezgâh kurularak çekecek/itecek çubuk çifti hazırlanır |
| touch | Dokunma tezgâhı | Nötr metal top sürüklenip pozitif ya da negatif küreye dokundurulur; ardından test küresi itme/çekme ya da elektroskop yaprakları sonucu gösterir |
| induce | Etki ile elektriklenme | Yüklü çubuk küreye sürüklenir; kürenin yakın ve uzak yarısına yük yerleştirilir, sonra elektronların kayması izlenir |
| paint | Boya hattı | Sprey tabancanın ya da gövdenin yükü ayarlanır; boya tanecikleri yüzeye yapışır ya da itilip saçılır |
| tech | Teknoloji avı | Evdeki araçlardan elektriklenmeden yararlananlar işaretlenir; toz bulutu yalnızca bunlara çekilir |
| storm | Fırtına | Paratonerin yeri ve telin bağlanacağı yer seçilir; şimşek/yıldırım kayıtları ayırt edilir; yolcu yıldırımdan korunacağı yere (metal gövdeli araç, Faraday kafesi) konur |
| straw | Pipet dengesi | Yüklü/yüksüz pipeti istenen yönde hareket ettirecek çubuk seçilir ve pipete yaklaştırılır |
| swipe | Hızlı tur | Kartlar sola ya da sağa fırlatılır (parmakla kaydırma ya da düğmeler) |

Her deste kurulurken her konudan 2 görev seçilir. Görev türleri olabildiğince farklı tutulur.

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| yuk | 20 | Pozitif, negatif, nötr cisimler; + ve − yük sayıları; aynı yüklerin itmesi, zıt yüklerin çekmesi, yüklü-nötr çekim |
| surt | 17 | Sürtünme ile elektriklenme; plastik–yün, cam–ipek; elektron aktarımı |
| dokun | 22 | Dokunma ile ve etki (temassız) ile elektriklenme, elektroskop, pipet deneyleri |
| tekno | 23 | Elektrik süpürgesi, boyama, baca filtresi, parmak izi, lazer yazıcı, klima; boyamada eşit kaplama |
| doga | 18 | Şimşek ve yıldırım, paratoner, Faraday kafesi; Thales, Gilbert, Cabeo, Franklin, Faraday, Tesla |

Görev türlerinin dağılımı: hang 14, rub 14, storm 14, swipe 13, paint 11, tech 10, touch 8, induce 8, straw 8.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneğin durumunu (kilitli yükler, hedefler, yük sayıları, kartlar, araçlar) metin olarak içerir.
- studentAnswer öğrencinin kurduğu düzeneği yazar (seçilen çubuk ve kumaş, dokundurulan küre, yerleştirilen yükler, paratoner yeri, fırlatılan kartlar).
- correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 7. Sınıf Ders Kitabı (2. kitap), 6. Ünite (s. 104–128).

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
