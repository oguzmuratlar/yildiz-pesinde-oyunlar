# Eğim Pisti · Doğrusal Denklemler

| Alan | Değer |
|---|---|
| gameId | matematik-8-egim-pisti |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 7. Ünite: Doğrusal Denklemler |
| Ekran yönü | Dikey |
| Oyun türü | Kayak merkezi, karaktersiz. Her görev bir pist ya da harita işidir: denklem terazisi, koordinat düzlemine bayrak dikme, koordinat okuma, tablo doldurma, iki tutamaçla doğru çizme, bitiş bayrağını sürükleyerek eğimli pist kurma, grafikten eğim ölçme, denkleme uyan grafiği seçme, gerçek hayat denklemi kurma, bölmeler, tuş takımı. Şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "hangi pist daha dik?" bonusu: iki pistin eğimi karşılaştırılır. Doğruysa +30 ❄️ ve kapıda ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (❄️ puanı yıldızı etkilemez) |
| Soru havuzu | 100 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Karlı dağ, çam ağaçları, kırmızı-mavi slalom bayrakları, tepede kayakçı ve "EĞİM PİSTİ" tabelası; altta yalnızca "KAYMAYA BAŞLA" düğmesi.
- **Giriş:** Kayakçı bayrakların arasından zikzak çizerek pisti iner; parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 slalom kapısı; doğru görevde kapı bayrağı renklenir ve ✓ (bonus doğruysa ★), yanlışta gri bayrak ve ✕.
- **Çıkış:** Karlı yamaçta 10 kapı zikzak sırayla belirir (geçilenler renkli ✓, kaçırılanlar gri), "PİST KARNESİ x/10 SLALOM KAPISI" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| solve | Denklem terazisi | +, −, ×, ÷ ve sayı/x terimi seçilip iki tarafa birden uygulanır, terazide denklem değişir; sonunda x değeri ayarlanır |
| pts | Bayrak dik | Noktalar sırayla koordinat ızgarasındaki kesişimlere dokunularak yerleştirilir |
| cread | Koordinat oku | Düzlemdeki noktaların x ve y değerleri ayarlanır |
| table | Tablo | y = mx + n için verilen x değerlerinde y değerleri ayarlanır |
| line | Doğru çiz | İki tutamaç denklemi sağlayan noktalara sürüklenir; doğru canlı çizilir |
| ramp | Pist kur | Bitiş bayrağı sürüklenerek istenen eğimde pist kurulur (yatay ve dikey değişim canlı görünür); doğruysa kayakçı iner |
| slope | Eğim ölç | Grafikteki doğrunun eğimi işaret, pay ve paydayla kurulur |
| gmatch | Grafik seç | Denkleme uyan A/B/C grafiğine dokunulur |
| model | Gerçek hayat modeli | Taksi, fidan, yakıt, teleferik, tarife durumları için y = mx + n kurulur |
| bin | Bölmeler | Bölgeler, eksen üstü noktalar, doğrusal mı, eğimin işareti |
| key | Tuş takımı | Denklem çözümü, öteleme, alan, gerçek hayat problemleri |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 9 tür, aynı türden en çok 2).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| denklem | 20 | Birinci dereceden bir bilinmeyenli denklemler |
| koordinat | 20 | Koordinat sistemi, sıralı ikililer, bölgeler, öteleme |
| iliski | 20 | Doğrusal ilişkiler: tablo, grafik, denklem |
| egim | 20 | Eğim, eğimin işareti, grafik ile eğim |
| problem | 20 | Doğrusal ilişki içeren gerçek hayat durumları |

Görev türlerinin dağılımı: solve 15, key 14, table 11, pts 10, ramp 9, model 9, line 8, slope 7, gmatch 7, bin 5, cread 5.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (denklem, noktalar, denklem ve x değerleri, pistin başlangıç noktası, doğrunun geçtiği noktalar, durum) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (x değeri ve uygulanan adımlar, yerleştirilen noktalar, tablo değerleri, tutamaç noktaları, bitiş noktası ve oluşan eğim, kurulan eğim ya da denklem, seçilen grafik).
- correctAnswer doğru sonucu yazar; doğru çizme ve pist kurmada koşulu sağlayan her nokta kabul edilir.
- sourceRef: 8. Sınıf Öğretim Programı, 7. Ünite “Doğrusal Denklemler”.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
