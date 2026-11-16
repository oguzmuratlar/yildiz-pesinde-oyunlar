# Yük Sınırı · Eşitsizlikler

| Alan | Değer |
|---|---|
| gameId | matematik-8-yuk-siniri |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 8. Ünite: Eşitsizlikler |
| Ekran yönü | Dikey |
| Oyun türü | Karayolu, kantar ve köprü; karaktersiz. Her görev bir yol işidir: sayı doğrusunda yolu işaretleme (uç noktayı sürükleme, boş/dolu daire, yön), gösterimden levha asma, durumdan eşitsizlik kurma, kantar terazisinde eşitsizlik çözme (negatif sayıyla çarpma ve bölmede yön değişir), çözüm olan tam sayıları seçme, gösterim seçme, kamyona koli yükleyip kantardan geçirme, bölmeler, tuş takımı. Şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "hangi kamyon geçer?" bonusu: köprü kuralı (x < L ya da x ≤ L) verilir, iki kamyondan kuralı sağlayan seçilir. Doğruysa +30 📦 ve bariyerde ★. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (📦 puanı yıldızı etkilemez) |
| Soru havuzu | 101 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Tepeler, nehir, köprüye giden yol, kantar göstergesi, "EN ÇOK 20 t" levhası, kapalı bariyer ve "YÜK SINIRI" tabelası; altta yalnızca "YOLA ÇIK" düğmesi.
- **Giriş:** Kamyon kantara çıkar, gösterge 0 t'dan 18 t'a sayar, onay sesiyle bariyer kalkar, kamyon kornayla köprüden geçer; parlamayla oyuna geçilir.
- **İlerleme:** Üstte yol üzerinde 10 bariyer; doğru görevde bariyer yeşil kalkar ve ✓ (bonus doğruysa ★), yanlışta kırmızı kalır ve ✕.
- **Çıkış:** 10 şerit sırayla açılır; geçen kamyonlar şeritte ilerler (✓), kalanlar gri ve 🚧 ile durur. "SEFER KARNESİ x/10 SEFER" madalyası basılır, sonuç karnesi açılır.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| nline | Yolu işaretle | Uç nokta(lar) sayı doğrusunda sürüklenir, daireye dokunularak boş/dolu yapılır, tek koşulda yön (sola/sağa) seçilir |
| nread | Levha as | Sayı doğrusundaki gösterimin eşitsizliği işaret düğmeleri ve sayı ayarlarıyla kurulur |
| write | Durumdan eşitsizlik | Gerçek hayat durumu için x ile eşitsizlik kurulur (en az / en çok / -den az / -den fazla) |
| isolve | Kantar terazisi | +, −, ×, ÷ ve sayı seçilip iki tarafa uygulanır; negatif sayıyla çarpma/bölmede işaret döner; sonunda çözüm kurulur |
| member | Kamyonları geçir | Eşitsizliği sağlayan bütün tam sayılara dokunulur |
| imatch | Yolu seç | Eşitsizliğe uyan A/B/C sayı doğrusu gösterimine dokunulur |
| truck | Kantardan geç | Koli sayısı ayarlanır, kamyon kantardan geçer ya da durur (en çok / aralık koşulu) |
| bin | Bölmeler | İfade–işaret eşleme, çözüm mü değil mi, yön değişir mi, çıkarım doğru mu |
| key | Tuş takımı | En büyük/en küçük tam sayı çözüm, çözüm sayısı, gerçek hayat problemleri |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| dogru | 21 | Eşitsizlikleri sayı doğrusunda gösterme ve okuma |
| yazma | 20 | Gerçek hayat durumlarına uygun eşitsizlik yazma |
| cozum | 20 | Birinci dereceden bir bilinmeyenli eşitsizlikleri çözme |
| kume | 20 | Eşitsizliği sağlayan tam sayılar |
| problem | 20 | Eşitsizliklerle gerçek hayat problemleri |

Görev türlerinin dağılımı: key 18, write 17, isolve 14, truck 12, nline 11, member 11, nread 8, imatch 6, bin 4.

Yanlış-cevap kaydı:
- questionText görevi ve düzeneği (eşitsizlik, sayı doğrusu gösterimi, durum, kamyon ve köprü verileri) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (uç noktalar, boş/dolu daireler ve yön; kurulan eşitsizlik ve terazi adımları; seçilen tam sayılar; seçilen gösterim; koli sayısı ve toplam kütle).
- correctAnswer doğru sonucu yazar; aralık koşullu kamyon görevinde koşulu sağlayan her koli sayısı kabul edilir.
- sourceRef: 8. Sınıf Öğretim Programı, 8. Ünite “Eşitsizlikler”.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
