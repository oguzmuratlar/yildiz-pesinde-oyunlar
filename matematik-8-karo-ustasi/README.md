# Karo Ustası · Çarpanlar ve Katlar

| Alan | Değer |
|---|---|
| gameId | matematik-8-karo-ustasi |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 1. Ünite: Çarpanlar ve Katlar |
| Ekran yönü | Dikey |
| Oyun türü | Çini atölyesi, karaktersiz. Her görev elle kurulan bir düzenektir: karolarla dikdörtgen kurma, asal çarpan ağacı ve üslü yazım, sayı kartlarına dokunma, kare karo döşeme, eşit paketleme, bölge (Venn) yerleştirme, zaman şeridinde işaretçi, dikdörtgen karolardan kare pano, aralarında asal kilitleri, tuş takımıyla problem çözümü. Şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "bordür şeridi" bonusu: verilen uzunluktaki şeride kesilmeden ve boşluksuz dizilen karo seçilir (bölünebilme). Doğruysa +30 💎 ve karoda sarı göbek. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (💎 puanı yıldızı etkilemez) |
| Soru havuzu | 101 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Çini atölyesinin duvarında 9 boş karo yuvası, tezgâhta kova ve fırça; üstte lacivert "KARO USTASI" tabelası; altta yalnızca "ATÖLYEYİ AÇ" düğmesi.
- **Giriş:** Çini karolar dönerek uçup yuvalara sırayla oturur, tabela mühür gibi sallanır; mavi parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 karoluk bordür; doğru görevde yıldızlı çini karo (bonus doğruysa sarı göbekli), yanlışta çatlak gri karo.
- **Çıkış:** Görevlerin karoları sırayla panoya oturur (doğrular çini, yanlışlar çatlak), "USTALIK BELGESİ x/10 ÇİNİ KARO" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| rect | Karo dikdörtgenleri | En kaydırıcıyla ayarlanır; n karo tam dikdörtgen olursa kaydedilir, eksik sıra taralı görünür; bütün çarpan çiftleri bulunur |
| tree | Asal çarpan ağacı | Asal sayı karolarına dokunarak sayı dallara ayrılır, sonra ▲▼ ile üsler ayarlanır |
| divs | Sayı kartları | Kurala uyan (çarpan, ortak kat, asal, aralarında asal) bütün kartlara dokunulur |
| tile | Kare karo döşeme | Karo kenarı kaydırılır; zemin canlı döşenir, kesilmesi gereken kenarlar taralı görünür (EBOB) |
| share | Eşit paketleme | Paket sayısı ayarlanır; her paketteki ve artan malzeme görünür (EBOB) |
| venn | Bölgeler | Sayı kartları "yalnız A / ikisi de / yalnız B (/ hiçbiri)" bölgelerine sürüklenir |
| bus | Zaman şeridi | Tekrar eden olayların şeridinde işaretçi ilk birlikte olunan ana sürüklenir (EKOK; saatli görevler var) |
| square | Kare pano | Dikdörtgen karolardan kurulacak karenin kenarı kaydırılır (EKOK) |
| coprime | Kilitler | Sayı çiftleri 🔗 aralarında asal / ✂️ değil olarak işaretlenir; sonuçta EBOB gösterilir |
| key | Tuş takımı | EBOB-EKOK ilişkisi, kalanlı gruplama, karo sayısı problemleri yazılır |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| carpan | 20 | Çarpanlar, çarpan çiftleri, asal çarpanlara ayırma ve üslü yazım |
| ebob | 20 | EBOB, ortak bölenler, karo döşeme ve eşit paylaştırma |
| ekok | 20 | EKOK, ortak katlar, tekrar eden olaylar ve kare oluşturma |
| asal | 20 | Aralarında asal sayılar, asal sayılar, ortak asal çarpanlar |
| problem | 21 | EBOB ve EKOK günlük yaşam problemleri (bahçe, kumaş, gruplar, fenerler, vapurlar, EBOB·EKOK = çarpım) |

Görev türlerinin dağılımı: divs 16, tile 12, bus 12, share 11, venn 11, square 10, tree 8, coprime 8, rect 7, key 6.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (karo sayısı, zemin ve karo ölçüleri, malzeme sayıları, aralıklar ve başlangıç saati, kartlar, sayı çiftleri) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (kaydedilen dikdörtgenler, üslü yazım, seçilen kartlar, karo kenarı, paket sayısı, bölge yerleşimleri, işaretçi zamanı, kare kenarı, kilitler, yazılan sayı).
- correctAnswer doğru çözümü ve EBOB/EKOK değerini yazar.
- sourceRef: 8. Sınıf Öğretim Programı, 1. Ünite “Çarpanlar ve Katlar”.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
