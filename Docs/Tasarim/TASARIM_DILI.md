# Yönetim paneli tasarım dili

> **05.10.2026, Mustafa:** "Holding patronu gibi hissetsin; dopamin salgılatsın; 'şuraya da bakayım' desin, incelerken zevk alsın." Seçilen yön aşağıdaki **Holding**. Önceki öneriler (Esnaf defteri, Kontrol odası, Masa oyunu) karşılaştırma için altta duruyor.

## Seçilen yön: Holding (`ana_ekran_holding.html`)

Örnek an: 6. yıl, 47 mağaza, 8 il (veriler uydurma). Dosya tarayıcıda açılınca hareketlidir: rakamlar sayarak artar, ışıklar parlar, kamyon hatları akar, haber bandı kayar.

**His:** gece, yüksek kattaki ofis. Koyu lacivert-siyah zemin, şampanya altını (servet, biz, ana eylem), zümrüt yeşili (büyüme, rekor), soluk mavi (rakip), kırmızı yalnız düşüş ve acil için. Cam gibi yarı saydam paneller, yumuşak parıltı.

**Bakınca keyif veren (dopamin) ilkeleri:**

1. **Büyük rakam, canlı rakam.** Şirket değeri ekranın en büyük şeyi, altın renkte; açılışta sayarak artar. Yanında "Bugün +184.250 ₺" nabız gibi atar.
2. **Harita = imparatorluk.** Gece uydu görüntüsü: her mağaza bir ışık, sahip olunan iller altın parlar, depodan mağazalara kamyon hatları akar, rakipler soluk mavi noktalar. Oyuncu ışıkların çoğalmasını izlemek ister.
3. **Merak kancaları.** Haritada küçük etiketler: "Bursa rekor +%34", "İstanbul: pay %0,2, fırsat büyük". Her biri tıklanınca ilgili sayfaya gider.
4. **Neredeyse bitti çubuğu.** "Bir üstteki rakibi geçmene %87" gibi hedefler hep görünür, dolarken parlar.
5. **Sıralama.** Türkiye ligi: oyuncu kendi satırını altın çerçevede, ▲3 ile görür; bir üstteki rakip hep adıyla yazılı. Sonra dünya ligi.
6. **Ödüller.** Bu hafta açılan rozetler parlayarak gelir ("YENİ"); kilitli olanın altında "3 kaldı" yazar.
7. **Kutlama kartı.** Önemli an (yeni mağaza, rekor, kilit) üstte kısa bir kartla kutlanır, sonra kaybolur.
8. **Haber bandı.** Altta borsa bandı gibi akan şirket haberleri: rekorlar, rakip hamleleri, fiyat değişimleri.
9. **Kilit açıldı kartı.** "Yurt dışı seni bekliyor" gibi büyük eşikler altın çerçeveli, tek düğmeli kartla gelir.
10. **Unvan.** Başlıkta "Çınar Holding · Yönetim Kurulu Başkanı". Unvan şirketle büyür: Market sahibi → Genel müdür → Holding başkanı.

**Dikkat:** kötü haber de net görünmeli (Kadıköy −%3 kırmızı); panel yalnız överse güven kaybolur. Parıltı ve animasyon kısa ve seyrek olmalı; her şey parlarsa hiçbir şey parlamaz.

**Tek dükkânda:** aynı dil, daha sade. Harita tek ışıkla başlar, lig satırı "listede değilsin, ilk 50'ye girmene X kaldı" der (M53), unvan "Market sahibi". Işıklar çoğaldıkça ekran zenginleşir.

---

# Önceki öneri: "Esnaf defteri"

Örnek görüntü: `ana_ekran_esnaf_defteri.html` (tarayıcıda 1920×1080 açılır; PNG bulut oturumundan LFS ile gönderilemediği için repoda yok; harita `Config/iller.json`'dan çizildi). Öneridir; Mustafa onaylamadı, oyun kodu değişmedi.

Dosyalar: `ana_ekran_esnaf_defteri.html`, `baslangic_esnaf_defteri.html` (başlangıç ekranı), karşılaştırma için `ana_ekran_kontrol_odasi.html` ve `ana_ekran_masa_oyunu.html` (aşağıda).

Örnekteki oyuncu: Ayşe Demir, Türkiye, Eskişehir, "Çınar Market", Normal. Rakamlar örnek.

## Fikir

Oyuncu, yıllardır tek şubeli küçük bir market işleten ailenin dükkânını devralıyor; sonrasını kendi kararları yazıyor. Panel steril bir şirket yazılımı gibi değil, **esnafın masası** gibi görünsün: kareli defter, takvim yaprağı, kasa fişi, dükkân tentesi. Süs okunurluğun önüne geçmez (düz kartlar, net hiyerarşi, eşit genişlikte rakamlar).

Hazır hikâye ve karakter yok; panelin "sesi" oyuncunun kendi verisidir: market adı, şehri, ilkleri, hatıraları, rekorları.

## Öğeler

| Öğe | Nesne | Not |
|---|---|---|
| Tarih | Duvar takvimi yaprağı: kırmızı başlıkta ay ve "1. yıl · 1. hafta", büyük gün rakamı | Gerçek yıl yazılmaz. Alt satırda mevsim, bayrama kalan gün, ekonomik dönem. Gün geçişi yaprak koparma |
| Para | Kasa fişi: kasa, işletme borcu (faizsiz, soluk renkte, kırmızı değil), bina (varlık), mağaza | Borç tehdit gibi gösterilmez; istenince ödenen bir kalem |
| Yapılacaklar | Çizgili defter sayfası, kırmızı kenar çizgisi, kutucuklar | Her satırda çözen düğme; biten iş üstü çizili kalır. İlkler de buraya düşer ("Dükkânı devraldın") |
| İlerleme | "Sıradaki eşik" kartı: Hipermarket ve toptan → mağaza 1/8, il 1/2; sonra yurt dışı → 25 mağaza, 5 il | Bölüm yerine şirket büyüklüğü |
| Bölgeler | Defter ayracı sekmeleri | Ülke paketinden gelir (M52); Türkiye'ye özel değil |
| Harita | Basılı atlas: deniz adları aralıklı harf, ölçek çubuğu, mağazamız market adının yazılı olduğu mühür | Ana il koyu yeşil, komşu iller hafif koyu, rakip yoğunluğu soluk kırmızı daire |
| Ana eylem | Çizgili tente (Dükkâna gir) | Tente rengi oyuncunun seçtiği market rengi olabilir (başlangıç ekranına bir seçim) |
| Not kartı | Sarı kart: "Sıradaki ilk", rekor, hatıra | Karakter sözü yerine oyuncunun kendi geçmişi |
| İmza | Sol altta market adı, oyuncu adı, şehir, yıl | Oyun adı değil, oyuncunun markası |

## Renk ve yazı

- Kâğıt `#F2ECDF`, kart `#FBF8F1`, mürekkep `#1E2621`, çizgi `#D9CFBB`.
- Marka yeşili `#24704F` (biz, olumlu, ana eylem; oyuncu rengi seçerse bunun yerine geçer), takvim kırmızısı `#C2412B` (acil, rakip), hardal `#D49A2A` (uyarı, not kartı). Başka vurgu rengi eklenmez.
- Yazılar mevcut tema ile aynı (`MarketTheme`): başlık Bricolage Grotesque, metin IBM Plex Sans, rakam IBM Plex Mono.
- Alt menü koyu "tezgâh" şeridi; dükkâna giriş düğmesi orada en göze çarpan şeydir.

## Şirketle büyüyen panel

Aynı yerleşim, şirket büyüdükçe değişen dokular (yıl değil, büyüklük eşikleri):

1. **Tek dükkân:** kâğıt, takvim yaprağı, kasa fişi (bu örnek).
2. **Şube ağı (8 mağaza, 2 il ile hipermarket/toptan):** defter yerine klasör ve dosya kartları, il haritası ön planda.
3. **Yurt dışı (25 mağaza, 5 il) ve dünya:** daha temiz, koyu temalı "kontrol odası"; dünya haritası. Tente ve marka rengi kalır.

Oyuncu ilerlemeyi rakamların yanında ekranın kendisinde de görür.

## Başlangıç ekranı (örnek: `baslangic_esnaf_defteri.html`)

Sol: spiralli "devir teslim" defteri. Adın, marketin adı (tabela ve özel marka), ülke (paketten; şimdilik 4, "+6 yakında"), şehir (küçük harita + kısa karakter: nüfus, rakip, kira, müşteri), zorluk (Rahat/Normal/Zor kartları), market rengi (6 renk). Sağ: seçimlerle canlı değişen dükkân önü (tabela, tente, vitrin), altında devralınan durum (kasa, bina, faizsiz borç, mağaza) ve "Anahtarı al" düğmesi.

## Karşılaştırma: iki farklı yön

Aynı içerik, farklı tarz. Mustafa henüz seçmedi.

| | Esnaf defteri | Kontrol odası (`ana_ekran_kontrol_odasi.html`) | Masa oyunu (`ana_ekran_masa_oyunu.html`) |
|---|---|---|---|
| His | Sıcak, nostaljik, küçük işletme | Ciddi yönetim simülasyonu, borsa ekranı | Neşeli, oyuncak gibi, rahat |
| Zemin | Kâğıt, kareli defter | Koyu yeşil-siyah, ızgara | Mavi masa, kalın siyah çerçeveli kartlar |
| Bilgi yoğunluğu | Orta | Yüksek (olay akışı, grafik, rakip tablosu, göstergeler) | Düşük (büyük düğme, az rakam) |
| Güçlü yanı | Oyunun kimliği; tente/tabela marka olur | Büyük şirkette çok veri rahat okunur | Yeni oyuncuya en kolay; uzaktan bile okunur |
| Zayıf yanı | Şirket büyüyünce "kâğıt" fazla gelebilir | Soğuk; tek dükkânda boş ve iddialı durur | Ciddi ekonomi kararlarında çocuksu kaçabilir |
| Kime | Hikâyeyi seven, yavaş oynayan | Excel seven, optimizasyoncu | Gündelik oyuncu |

Karma öneri: tek dükkânda "Esnaf defteri" ile başla, şirket büyüdükçe panel "Kontrol odası"na doğru evrilsin (yukarıdaki "Şirketle büyüyen panel").
