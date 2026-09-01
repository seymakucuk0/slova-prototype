# Slova — prototipler

İki sayfa, ikisi de tek dosya, kurulum gerektirmiyor.

| Sayfa | Ne |
|---|---|
| **[A0 ders prototipi](https://seymakucuk0.github.io/slova-prototype/)** | A0'ın 24 node'u, 692 ekran, gezilebilir |
| **[Ekran envanteri](https://seymakucuk0.github.io/slova-prototype/katalog.html)** | Uygulamadaki 6 ders motoru, 112 ekran tipi, hepsi koddan çizildi |

## A0 ders prototipi

24 node × 3 part (Kelimeler · Gramer · Cümle ve diyalog). Haritadan node seçilir,
sağdaki listeden herhangi bir ekrana atlanır.

İçerik `seymakucuk0/curriculum` deposundaki A0 dersinden türetildi. Egzersizler
şu kurallara göre üretiliyor:

- **Çeldirici boşluğa uymaz** — yanlış şık geçerli bir cümle üretmez. Tekliği ya
  görsel (kırmızı araba resmi varsa `blue` gerçeğe aykırıdır) ya da dilbilgisi
  sağlar (`I ___ Leo.` → yalnız `am`).
- **Kümülatif** — öğrencinin henüz görmediği kelime şıkta çıkamaz.
- **Ardışık aynı cümle yok**; aynı hedef kelime kümelenmez.
- **Desen ekranı ancak gerçek bir desen varsa** çıkar; cevap gösterilen satırlarda
  görünüyorsa desen yerine doğru/yanlış egzersizi gelir.
- **Klavye egzersizi** yalnız 2-6 harfli kelimede; bazı kutular dolu gelir,
  kullanıcı en fazla 3 harf yazar.

## Ekran envanteri

Uygulamada gelmiş geçmiş her egzersiz, öğretim ve bağlam ekranı. Her kart ilgili
SwiftUI view'ının kodundan — yazı boyu, köşe yarıçapı, kart yüksekliği gerçek
değerleriyle — yeniden çizildi. Kart altındaki rozet o ekranın bugün kullanılıp
kullanılmadığını söylüyor.

6 sistem: Slides/MicroLesson · Lexicon testleri · Custom Path ders · Beat lesson
(Paths customized) · Quiz & Flashcard · Slide (eski curriculum).

## Not

Bunlar prototip; uygulamanın kendisi ayrı bir depoda. Kelime görsellerinin bir
kısmı henüz üretilmedi, o ekranlarda kesik çizgili "görsel yok" yer tutucusu var.
