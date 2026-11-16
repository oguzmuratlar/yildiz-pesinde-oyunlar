# Mega Mikro · Üslü İfadeler + Kareköklü İfadeler

| Alan | Değer |
|---|---|
| gameId | matematik-8-mega-mikro |
| Güncel sürüm | 1.0.0 |
| Ders | Matematik (oyun içi subjectId: math; uygulama başka bir değer gönderirse onu kullanır) |
| Sınıf | 8 (oyun yalnızca 8. sınıf bağlamını kabul eder) |
| Ünite | 2. Ünite: Üslü İfadeler ve 3. Ünite: Kareköklü İfadeler (tek oyunda birleşik; her görev kendi ünitesini kaydeder) |
| Ekran yönü | Dikey |
| Oyun türü | Yakınlaştırma (zoom) laboratuvarı, karaktersiz. Her görev elle kurulan bir düzenektir: üs kural makinesi, sıralama kartları, bilimsel gösterimde virgül yerleştirme ve zoom cetveli, basamak çözümleme, sayı doğrusunda karekök, çarpan karolarıyla kökten çıkarma, a√b kurucu (işlem ve geometri), bölmeler, tuş takımı. Şıklı soru yoktur. 10 görev, kolaydan zora (3 kolay · 4 orta · 3 zor), süre sınırı yok |
| Üst katman | Her doğru görevden sonra isteğe bağlı "mercek düellosu" bonusu: iki üslü ya da kareköklü ifadeden büyük olanı seçilir. Doğruysa +30 🔭 ve mercekte sarı halka. Yalnızca oyun içi puanı etkiler, akışı durdurmaz |
| Yıldız | 0–4 doğru 0★ · 5–6 1★ · 7–8 2★ · 9–10 3★ (🔭 puanı yıldızı etkilemez) |
| Soru havuzu | 101 görev, index.html içine gömülüdür |

## Giriş ve çıkış
- **Açılış:** Karanlık laboratuvarda dev mercek; içinde 10²¹ ölçeğinde galaksi; neon "MEGA MİKRO" tabelası; altta yalnızca "MERCEĞİ AÇ" düğmesi.
- **Giriş:** Mercek ölçekten ölçeğe dalar: galaksi 10²¹ → gezegen 10¹² → Dünya 10⁷ → şehir 10³ → insan 10⁰ → karınca 10⁻³ → bakteri 10⁻⁶ → atom 10⁻¹⁰; camgöbeği-pembe parlamayla oyuna geçilir.
- **İlerleme:** Üstte 10 merceklik şerit; doğru görevde parlak mercek (bonus doğruysa sarı halka), yanlışta çatlak gri mercek.
- **Çıkış:** 10¹⁰'dan 10⁻⁸'e iç içe dönerek küçülen 10 çerçeve (doğrular parlak, yanlışlar kesikli), "ZOOM KARNESİ x/10 NET GÖRÜNTÜ" madalyası, sonuç karnesi.

## Görevler (mini oyunlar)
| Tür | Görev | Mekanik |
|---|---|---|
| rule | Kural makinesi | Üslü ifadenin sonucu, verilen tabanın üssü ▲▼ ile ayarlanarak kurulur (çarpma, bölme, üssün üssü, negatif üs, taban değiştirme) |
| order | Sıralama | Kartlara küçükten büyüğe sırayla dokunulur (üslü sayılar, bilimsel gösterim, kareköklü ifadeler) |
| sci | Bilimsel gösterim | Anlamlı rakamlar arasına dokunarak virgül konur, üs zoom cetvelinde işaretçi sürüklenerek ya da ▲▼ ile ayarlanır; işlem sonucu da bu biçimde kurulur |
| place | Çözümleme | Rakam karoları 10'un kuvvetlerinin yanındaki yuvalara sürüklenir |
| line | Sayı doğrusu | Karekök kartı onda birlik çentikli sayı doğrusunda yerine sürüklenir (yaklaşık değer) |
| simp | Kökten çıkarma | Çarpan çifti karolarından tam kare içereni seçilerek kök dışına çıkarılır; a√b bulunana kadar sürdürülür |
| calc | Kök işlemleri | Katsayı ve kök içi kaydırıcılarıyla a√b sonucu kurulur |
| geo | Kareler ve dikdörtgen | Alanı verilen karelerin toplam genişliği ya da çevresi, dikdörtgenin alanı a√b biçiminde kurulur |
| bin | Bölmeler | Kartlar bölmelere ayrılır (tam kare, karekökü tam sayı, iki tam sayı arası, rasyonel/irrasyonel) |
| key | Tuş takımı | Üs ya da kök içindeki bilinmeyen yazılır |

Her deste kurulurken her konudan 2 görev seçilir; görev türleri olabildiğince farklı tutulur (destede en az 8 tür).

## Soru havuzu
| Grup | Görev | İçerik |
|---|---|---|
| uslu | 20 | Tam sayıların tam sayı kuvvetleri, üslü ifadelerle işlemler ve karşılaştırma |
| bilimsel | 21 | 10'un kuvvetleri, ondalık gösterimin çözümlenmesi, bilimsel gösterim ve bilimsel gösterimle işlemler |
| karekok | 20 | Tam kare sayılar, karekök tahmini, a√b biçimi |
| kokislem | 20 | Kareköklü ifadelerle çarpma, bölme, toplama, çıkarma ve karşılaştırma |
| gercek | 20 | Ondalık ifadelerin karekökü, rasyonel/irrasyonel sayılar, kareköklü ifadelerle geometri problemleri |

Görev türlerinin dağılımı: calc 14, line 13, rule 12, sci 12, geo 11, order 9, simp 8, bin 8, key 7, place 7.

Yanlış-cevap kaydı:
- unit alanı göreve göre "2. Ünite: Üslü İfadeler" ya da "3. Ünite: Kareköklü İfadeler" olur; sourceRef de ilgili üniteyi gösterir.
- questionText görevi ve düzeneği (ifade, kartlar, anlamlı rakamlar, basamaklar, sayı doğrusu aralığı, çarpan çiftleri, kare alanları) metin olarak içerir.
- studentAnswer öğrencinin kurduğunu yazar (üs, sıra, a × 10^n, çözümleme, sayı doğrusundaki konum, a√b, bölmeler, yazılan sayı).
- correctAnswer doğru sonucu yazar.

Teknik notlar:
- Uygulamadan oyuna mesaj: `window.YildizPesindeGame.receiveMessage(json)`
- En düşük WebView: iOS 15.4, Android System WebView 98
- Harici ağ isteği, analitik veya reklam yoktur (Content-Security-Policy ile kapatılmıştır).

Tarayıcıda doğrudan açıldığında oyun "Deneme modu"nda çalışır ve sonuç kaydetmez.
