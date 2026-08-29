# Slova — A0 ders prototipi

Slova'nın A0 seviyesi için ders motoru prototipi. Tek dosya, bağımlılık yok.

**Aç:** https://seymakucuk0.github.io/slova-prototype/

## İçinde ne var

Üç node tamamen oynanabilir. Node uzunlukları sabit değil — içeriğin ne gerektirdiğine göre belirlendi.

| Node | Ekran | Part 1 / 2 / 3 | Neden bu uzunluk |
|---|---|---|---|
| 5 · This is my mother | 33 | 14 / 9 / 10 | Temel uzunluk. Somut isimler, tek ve basit gramer. |
| 6 · Brother and sister | 36 | 18 / 6 / 12 | Kelimeler iki minimal çift (sister↔brother, son↔daughter) — ayırt etme egzersizi Part 1'i uzattı. Gramer node 5'in devamı olduğu için Part 2 kısaldı. |
| 7 · Where are you from | 39 | 12 / 15 / 12 | Kelimelerin üçü soyut, Part 1 kısaldı. Gramer iki yapı taşıyor (düz cümle + devrik soru), Part 2 ikiye katlandı. |

Her node'da en az 4 konuşma, 4 dinleme, 2 harf klavyesi, 3 diyalog egzersizi var. Part 3'te tek kelime egzersizi yok — tamamı cümle ve diyalog.

## 19 egzersiz tipi

`word_card` · `mc_meaning` · `mc_reverse` · `match4` · `image_choice` · `listen_pick` · `listen_write` · `listen_sentence_gap` · `letter_keys` · `fill_blank` · `build_sentence` · `build_translate` · `mc_sentence` · `say_word` · `say_sentence` · `dialog_gap` · `dialog_build` · `dialog_say` · `translate_meaning`

Bunların 14'ünün Slova'da çalışan bir SwiftUI karşılığı var. İkisi yeni:

- **`letter_keys`** — uygulamanın kendi klavyesi. Sadece o kelimede geçen harfler renkli ve basılabilir; harfleri hatırlamak zorunda değilsin, sırayı sen kuruyorsun.
- **`listen_write`** — ses çalar, klavyeyle yazarsın. "Duyamıyorum" bağlantısı egzersizi anlam sorusuna çevirir, böylece sessiz ortamda ders kaybolmaz.

Konuşma egzersizleri tarayıcıda `webkitSpeechRecognition` varsa gerçekten dinler; yoksa simülasyona düşer ve bunu ekranda belirtir. Uygulamada `SpeechRecognitionService` (SFSpeechRecognizer) kullanılıyor.

## Kaynak

Müfredat verisi ayrı ve özel bir repoda tutuluyor: **seymakucuk0/curriculum** — 174 ders, 1392 kelime, 174 gramer noktası, 1276 CEFR can-do kazanımı.

Kazanımlar Avrupa Konseyi'nin CEFR Companion Volume (2018) betimleyicilerinden alınmıştır.
Bu repo yalnızca prototip arayüzünü barındırır; müfredat içeriği burada değildir.
