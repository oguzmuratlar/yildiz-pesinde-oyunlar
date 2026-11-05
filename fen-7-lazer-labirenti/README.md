# Lazer Labirenti · Işığın Kırılması ve Mercekler

| Alan | Değer |
|---|---|
| gameId | fen-7-lazer-labirenti |
| Güncel sürüm | 1.0.0 |
| Ders | Fen Bilimleri (oyun içi subjectId: science; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 7 (oyun yalnızca 7. sınıf bağlamını kabul eder) |
| Ünite | 4. Ünite: Işığın Kırılması ve Mercekler |
| Ekran yönü | Dikey |
| Oyun türü | Lazerli kaçış odası temalı ışık ve mercek simülasyonları. Öğrenci karakteri yoktur; kapıdaki 10 kilit ilerlemeyi gösterir. Test ve doğru/yanlış sorusu yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (💎 puanı yalnızca oyun içi eğlence içindir) |
| Soru havuzu | 100 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Giriş:**
  1. Karanlık oda, zeminde ızgara, odayı kesen kırmızı lazer çizgileri, 10 kilitli çelik kapı, titreyen neon "LAZER LABİRENTİ" tabelası.
  2. "LAZERLERİ AÇ" denince lazer ızgarası söner, beyaz ışık prizmaya girer ve gökkuşağı yelpazesine ayrılır, kilitler parlar.
  3. Yeşil tarama çizgisi ekranı süpürür, oyuna geçilir.
- **İlerleme:** Üstte 10 kilit vardır. Doğru görevde kilit açılır (🔓), yanlışta kilitli (🔒) kalır.
- **Çıkış:**
  1. Kapıdaki kilitler doğru görev sayısı kadar tek tek açılır.
  2. 5 ve üzeri doğruda kapı ardındaki ışığa doğru aralanır.
  3. "KAÇIŞ USTASI x/10 KİLİT" madalyası basılır, sonuç "KAÇIŞ RAPORU" olarak açılır.

## Görevler (simülasyonlar)
| Tür | Görev | Mekanik |
|---|---|---|
| refract | Lazer yönlendirme | İki saydam ortam (yoğunlukları belirtili) arasında lazerin izleyeceği yol üç aday ışından seçilir; lazer ateşlenir, gerçek kırılma çizilir |
| apparent | Görünür konum | Havadan suya ya da sudan havaya bakan gözlemcinin cismi gördüğü konum (A/B/C) seçilir; ışınlar ve uzantıları çizilir |
| prism | Prizma tüneli | Prizmadan çıkan renkler kırmızıdan başlayarak sıralanır; beyaz ışık renklere ayrışır |
| angles | Kırılma haritası · Mercek haritası | Diyagramdaki numaralı parçalara (normal, gelen/kırılan ışın, açılar, ortamlar; asal eksen, optik merkez, odak noktası, odak uzaklığı) adlar yerleştirilir |
| lens | Mercek tezgâhı | Mercek kesitleri ve sembolleri İNCE / KALIN KENARLI olarak etiketlenir; paralel ışınlar odakta toplanır ya da dağılır |
| tools | Gözlükçü rafı · Optik vitrin | Araçlar mercek türüne ya da işlevine (netleştirir, büyütür, büyütüp yansıtır) göre etiketlenir |
| fire | Orman devriyesi | Ormana atılmış atıklardan güneş ışığını toplayıp yangına yol açabilecekler işaretlenir |
| sort | Kasa | Kırılma kanunları, ışığın hızı, görüntüler, mercek özellikleri, araç işlevleri, OPMER, bilim insanları |
| calc | Sayı çarkı | Gelme ve kırılma açısı (normal 90°), kırılma sayısı, odak uzaklığı, bilim insanlarının yılları |

Her deste kurulurken her konudan 2 görev seçilir. Görev türleri olabildiğince farklı tutulur.

## Soru havuzu

| Grup | Görev | İçerik |
|---|---|---|
| kirilma | 21 | Kırılma tanımı, kırılma kanunları, dik gelen ışın, ışığın hızı ve yoğunluk |
| gorunum | 21 | Balıkçı–dalgıç, sudaki balık ve taş, prizma ve gökkuşağı, Mîrim Çelebi, İbnü’l-Heysem, el-Fârisî |
| kavram | 19 | Normal, gelen/kırılan ışın, gelme/kırılma açısı, asal eksen, optik merkez, odak noktası ve uzaklığı, İbn Sehl, Young |
| mercek | 19 | İnce kenarlı (yakınsak) ve kalın kenarlı (ıraksak) mercekler, sembolleri, ışın yolları |
| kullanim | 20 | Büyüteç, okuma ve uzak gözlüğü, dış kapı dürbünü, mikroskop, teleskop, projeksiyon, orman yangını riski, OPMER |

Görev türlerinin dağılımı: sort 17, refract 14, angles 14, lens 12, calc 10, apparent 10, tools 10, fire 7, prism 6.

Yanlış-cevap kaydı:
- questionText görevi, ortamları ve yoğunluklarını, konumları, parçaları, mercekleri ya da araçları metin olarak içerir.
- studentAnswer öğrencinin seçtiği yolu, konumu, etiketleri, sıralamayı ya da girdiği sayıyı yazar.
- correctAnswer doğru çözümü yazar.

Kaynak: MEB Fen Bilimleri 7. Sınıf Ders Kitabı (2. kitap), 4. Ünite (s. 12–35).

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
