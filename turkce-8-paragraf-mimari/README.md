# Paragraf Mimarı · Paragrafın Yapısı ve Anlatım Biçimleri

| Alan | Değer |
|---|---|
| gameId | turkce-8-paragraf-mimari |
| Güncel sürüm | 1.0.0 |
| Ders | Türkçe (oyun içi subjectId: turkish; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Konu | Paragrafın yapısı, anlatım biçimleri |
| Ekran yönü | Dikey |
| Oyun türü | Şantiye ve vinç, karaktersiz. Her görev bir inşaat işidir: cümle bloklarını vinçle kat kat dizme, yanlış yerdeki iki katın yerini değiştirme, giriş cümlesini temele / sonuç cümlesini çatıya sürükleme, metni ikiye bölen tuğla duvarı örme, eksik katı vinçle indirme, geçiş sözü vidasıyla kirişi bağlama, anlatım biçimi mührünü paftaya basma, bölmeler. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "hangi blok temel olabilir?" bonusu: iki cümleden giriş cümlesi olabilecek olan seçilir. Doğruysa +30 🧱 ve katta ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🧱 puanı yıldızı etkilemez) |
| Soru havuzu | 100 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Mavi gökyüzü, sarı-siyah şantiye şeridi, kule vinç, "PARAGRAF MİMARI" tabelası; altta yalnızca "İNŞAATA BAŞLA" düğmesi.
- **Giriş:** Vincin kolu döner, renkli bloklar tek tek inip üst üste oturur; parlamayla oyuna geçilir.
- **İlerleme:** Üstte giderek yükselen 10 kat bloğu; doğru görevde renkli ✓ (bonus doğruysa ★), yanlışta gri ✕.
- **Çıkış:** 10 kat yukarıdan inip kule olur (doğrular renkli ve numaralı, yanlışlar çatlak gri), "İNŞAAT KARNESİ x/10 KAT" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| stack | Katları diz | Cümle blokları sırayla dokunularak vinçle temelden yukarı katlara konur; en üst kat geri alınabilir |
| swap | Katları değiştir | Yanlış yerdeki iki kata sırayla dokunularak yerleri değiştirilir |
| keystone | Temel / çatı | Giriş cümlesi olabilecek blok temele ya da sonuç cümlesi olabilecek blok çatıya sürüklenir |
| split | Ara duvar | Cümleler arasındaki çizgiye dokunularak metni iki paragrafa ayıran duvar örülür |
| fill | Eksik kat | Paragraftaki boşluğa uygun cümle bloğu vinçle indirilir |
| beam | Kiriş | Vida kutusundan uygun geçiş sözü seçilip iki cümle bağlanır |
| stamp | Proje mührü | Açıklama / Tartışma / Öyküleme / Betimleme mühürlerinden biri paragrafın paftasına basılır |
| bin | Bölmeler | Giriş olabilir/olamaz, giriş–gelişme–sonuç, geçiş sözlerinin görevi, paragrafa uyar/uymaz, anlatım biçimleri |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| sira | 20 | Paragraf oluşturma, cümle sıralaması |
| girsonuc | 20 | Giriş, gelişme ve sonuç cümleleri |
| bolme | 20 | Paragrafı ikiye bölme, geçiş sözleri |
| ekleme | 20 | Paragrafa uygun cümle ekleme |
| anlatim | 20 | Açıklama, tartışma, öyküleme, betimleme |

Görev türlerinin dağılımı: bin 18, fill 14, split 13, keystone 12, beam 12, stamp 12, stack 10, swap 9.

Bütün paragraflar özgündür.

Yanlış-cevap kaydı:
- questionText görevi, paragrafı (numaralı cümlelerle) ve düzeneği (bloklar, bağlayıcılar, mühürler) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (kat sırası, yer değiştirilen katlar, temele/çatıya konan blok, duvarın yeri, indirilen blok, seçilen bağlayıcı, basılan mühür).
- correctAnswer doğru sonucu yazar.
- sourceRef: 8. Sınıf Öğretim Programı, Okuma: Anlam Bilgisi.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
