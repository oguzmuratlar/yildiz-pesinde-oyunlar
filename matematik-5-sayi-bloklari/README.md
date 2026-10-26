# Sayı Blokları · Doğru Kapıya Bırak

| Alan | Değer |
|---|---|
| gameId | matematik-5-sayi-bloklari |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 5 (oyun yalnızca 5. sınıf bağlamını kabul eder) |
| Tema | 2. Tema: Sayılar ve Nicelikler (1) — Doğal Sayılar ve İşlemler |
| Ekran yönü | Dikey |
| Oyun türü | Tetris tarzı blok bırakma: her blok bir soru taşır, öğrenci bloğu doğru cevabın kapısına götürüp bırakır. 10 blok, kolaydan zora (3 kolay · 4 orta · 3 zor); blok kendiliğinden düşmez, süre sınırı yok |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ |
| Soru havuzu | 110 görev (83 üç kapılı test, 15 doğru/yanlış, 12 karşılaştırma < = >), index.html içine gömülüdür |

## Oyun

Kuyunun üstünde 3 renkli kapı (doğru/yanlışta 2 kapı) vardır; her kapıda bir cevap yazar. Seçenekler uzunsa kapılarda A, B, C harfleri, seçenekler soru kartında yazılır.

- **Yönlendir:** ◀ ▶ düğmeleri, kuyuda sağa/sola kaydırma, ok tuşları ya da kapıya dokunma ile blok kapılar arasında gezer. Gölge, bloğun nereye ineceğini gösterir.
- **Bırak:** “Bırak” düğmesi, aşağı kaydırma veya seçili kapıya ikinci dokunuş bloğu düşürür.
- **Sonuç:** Doğru blok renkli olarak yerine oturur; yanlış blok gri ve çatlak olur, doğru kapı yeşil çerçeveyle gösterilir. Altta açıklama çıkar.
- **Satır patlatma:** Tamamen dolan satırlar parlayıp silinir, bonus puan verir. Yığın yukarı yaklaşırsa zemin bir satır aşağı kayar; oyun hiçbir zaman bitmez, 10 blok tamamlanır.
- **Sıradaki blok** küçük önizlemede gösterilir. Puan, satır ve seri yalnız oyun içi motivasyondur.

## Soru havuzu

| Grup | İçerik |
|---|---|
| okuma | Çok basamaklı sayıları okuma ve yazma (milyonlar, milyarlar), bölük adları |
| basamak | Basamak adı, basamak değeri, bölükteki sayı, çözümleme |
| kars | Karşılaştırma (< = >), sıralama, rakam kartlarıyla en büyük/en küçük sayı, yuvarlama, tahmin |
| islem | Zihinden ve kısa yoldan çarpma/bölme, eksik terim/çarpan/bölünen/bölen, bölme ve kalan |
| problem | Dört işlem gerektiren gerçek yaşam problemleri, süre hesapları, “en az kaç sefer / kaçıncı saatte” türü kalanlı bölme |

Her oyunda her gruptan 2 görev gelir. Son oynanan 40 görev cihazda hatırlanır.

Kaynak: MEB Matematik 5. Sınıf Ders Kitabı 1. Kitap, 2. Tema (s. 92–137).
