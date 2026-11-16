# Sözlük Kâşifi · Sözcükte ve Söz Öbeklerinde Anlam

| Alan | Değer |
|---|---|
| gameId | turkce-8-sozluk-kasifi |
| Güncel sürüm | 1.0.0 |
| Ders | Türkçe (oyun içi subjectId: turkish; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Konu | Sözcükte ve söz öbeklerinde anlam (söz varlığı) |
| Ekran yönü | Dikey |
| Oyun türü | Kristal mağarasında keşif, karaktersiz. Her görev bir kâşif işidir: karanlık cümlede sözcükleri fenerle yakma, halatla eşleştirme, kristalleri dizerek deyim/atasözü kurma, boşluğa kristal yerleştirme, keseye kristal toplama, genelden özele sıralama, düşen kristalleri sepete atma, bölmeler. Şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "zıt eşini bul" bonusu: bir sözcüğün zıt anlamlısı iki kristalden seçilir. Doğruysa +30 💎 ve kristal duvarında ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (💎 puanı yıldızı etkilemez) |
| Soru havuzu | 100 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Karanlık kristal mağarası, sönük kristaller, kapalı mor kapaklı sözlük, parlayan "SÖZLÜK KÂŞİFİ" tabelası; altta yalnızca "MAĞARAYA GİR" düğmesi.
- **Giriş:** Fener ışığı mağarayı tarar, kristaller tek tek parlar, sözlüğün kapağı açılır, içinden kristal yükselir; parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 kristallik duvar; doğru görevde kristal renkli parlar ✓ (bonus doğruysa ★), yanlışta gri ✕.
- **Çıkış:** Hazine odasında 10 kristal sırayla belirir (doğrular renkli ve ışıltılı, yanlışlar gri), "KEŞİF KARNESİ x/10 KRİSTAL" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| tapword | Fenerle bul | Cümlenin sözcükleri karanlık taşlardır; istenen sözcük(ler)e dokunulunca yanar (mecaz, yan, terim anlamlı sözcük; deyim, ikileme, yansıma, soyut sözcük) |
| link | Halatla bağla | Sol ve sağ kartlar dokunarak halatla bağlanır (eş/zıt anlamlılar, terim–alan, deyim–anlam, atasözü–durum, çok anlamlı sözcük–anlam) |
| build | Kristal dizme | Kristaller sırayla yuvalara konup deyim ya da atasözü kurulur; fazladan kristaller vardır |
| gapfill | Boşluğa kristal | Cümledeki boşluğa uygun kristal yerleştirilir |
| collect | Keseye topla | İstenen özellikteki bütün kristaller keseye toplanır |
| order | Genelden özele | Kristaller genelden özele doğru yuvalara dizilir |
| rain | Kristal yağmuru | Kristaller tek tek düşer, iki sepetten doğrusuna atılır (süre baskısı yok) |
| bin | Bölmeler | Gerçek/yan/mecaz, terim, eş sesli/çok anlamlı, atasözü konuları, somut/soyut, ikileme/yansıma, genel/özel |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| cokanlam | 20 | Gerçek, yan, mecaz ve terim anlam |
| iliski | 20 | Eş anlam, zıt anlam, eş seslilik |
| deyim | 20 | Deyimler |
| atasozu | 20 | Atasözleri |
| ozellik | 20 | Somut–soyut, genel–özel; ikileme ve yansıma |

Görev türlerinin dağılımı: link 19, gapfill 18, tapword 15, build 13, collect 12, bin 10, order 7, rain 6.

Bütün cümleler özgündür; deyim ve atasözleri halkın ortak söz varlığından alınmıştır.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (cümle, kartlar, kristaller, sepetler) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (yakılan sözcükler, bağlanan çiftler, kurulan söz, yerleştirilen kristal, toplananlar, sıralama, sepet seçimleri).
- correctAnswer doğru sonucu yazar.
- sourceRef: 8. Sınıf Öğretim Programı, Okuma: Söz Varlığı.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
