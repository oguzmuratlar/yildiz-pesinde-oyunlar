# Skor Analisti · Veri Analizi

| Alan | Değer |
|---|---|
| gameId | matematik-8-skor-analisti |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 4. Ünite: Veri Analizi |
| Ekran yönü | Dikey |
| Oyun türü | Spor yayınında canlı analiz masası, karaktersiz. Her görev elle kurulan bir grafik işidir: sütunları ve çizgi noktalarını sürükleyerek grafik kurma, daire grafiğinde dilim sınırlarını sürükleme, grafikte dokunarak seçim, ortalama çizgisini sürükleme, doğru grafiği seçme, grafikten tabloya aktarma, grafik okuyup sonucu tuş takımıyla yazma, bölmeler. Şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "canlı istatistik" bonusu: son üç maçın sayı ortalaması seçilir. Doğruysa +30 📊 ve ekranda ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (📊 puanı yıldızı etkilemez) |
| Soru havuzu | 108 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Karanlık yayın stüdyosu, 3×3 sönük ekran duvarı, sönük "CANLI" lambası, "SKOR ANALİSTİ" tabelası; altta yalnızca "YAYINA GİR" düğmesi.
- **Giriş:** "CANLI" lambası kırmızı yanar, ekranlar sırayla açılıp renkli sütun grafikleri yükselir, alt bantta haber şeridi akar; yeşil parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 ekranlık duvar; doğru görevde ekranda grafik açılır (bonus doğruysa ★), yanlışta karlı parazit.
- **Çıkış:** 5×2 ekran duvarında görevlerin ekranları sırayla açılır (doğrular grafikli, yanlışlar parazitli), "ANALİST KARNESİ x/10 YAYIN" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| bars | Sütun grafiği kur | Tablodaki (ya da çizgi/daire grafiğindeki) veriye göre sütunlar sürüklenir; tek ve çift sütunlu |
| line | Çizgi grafiği kur | Noktalar sürüklenerek çizgi kurulur; tek ve iki çizgili; kaynak tablo ya da sütun grafiği |
| pie | Daire grafiği kur | Dilim sınırları çember üzerinde sürüklenir; dilim açıları canlı görünür |
| pick | Grafikte seç | Koşula uyan sütunlara/noktalara ya da iki değer arasındaki aralıklara dokunulur (en çok artış, ortalamanın üstü, kesişme…) |
| avg | Ortalama çizgisi | Yatay çizgi ortalama değere sürüklenir |
| gkey | Grafik okuma | Grafikten toplam, fark, kat, ortalama, daire dilimi sayısı ya da açısı hesaplanıp tuş takımıyla yazılır |
| match | Doğru grafik | Tabloyu (ya da kaynak grafiği) doğru gösteren A/B/C grafiğine dokunulur |
| tfill | Grafikten tabloya | Daire ya da çizgi grafiğine bakılarak tablo değerleri ayarlanır |
| bin | Bölmeler | Uygun grafik türü, artış/azalış, grafikten çıkarılabilen yargılar, ortalamanın üstü/altı |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| sutun | 22 | Sütun grafiği oluşturma, okuma, ölçek |
| cizgi | 21 | Çizgi grafiği oluşturma, artış/azalış, okuma |
| daire | 23 | Daire grafiği oluşturma, açı ve sayı hesabı |
| donusum | 22 | Tablo, sütun, çizgi ve daire gösterimleri arası dönüşüm; uygun grafik türü |
| yorum | 20 | İki veri grubunu karşılaştırma, çıkarım yapma, ortalama |

Görev türlerinin dağılımı: gkey 25, pick 19, bars 13, match 12, pie 11, line 10, bin 8, avg 6, tfill 4.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (tablo ya da grafik verileri, eksen aralığı ve birimi, daire dilim açıları) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (sütun yükseklikleri, nokta değerleri, dilim açıları, seçilen kategoriler/aralıklar, ortalama çizgisi, seçilen grafik, tablo değerleri, yazılan sayı).
- correctAnswer doğru grafiği ya da sonucu yazar.
- sourceRef: 8. Sınıf Öğretim Programı, 4. Ünite “Veri Analizi”.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
