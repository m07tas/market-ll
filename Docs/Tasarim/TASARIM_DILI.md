# Yönetim paneli tasarım dili önerisi: "Esnaf defteri"

Örnek görüntü: `ana_ekran_esnaf_defteri.html` (tarayıcıda 1920×1080 açılır; PNG bulut oturumundan LFS ile gönderilemediği için repoda yok; harita `Config/iller.json`'dan çizildi). Öneridir; Mustafa onaylamadı, oyun kodu değişmedi.

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
