# Yönetim paneli tasarım dili önerisi: "Esnaf defteri"

Örnek görüntü: `ana_ekran_esnaf_defteri.html` (tarayıcıda 1920×1080 açılır; PNG bulut oturumundan LFS ile gönderilemediği için repoda yok; harita `Config/iller.json`'dan çizildi). Öneridir; Mustafa onaylamadı, oyun kodu değişmedi.

## Fikir

Oyun babadan kalan bir mahalle dükkânıyla başlıyor. Panel steril bir şirket yazılımı gibi değil, **esnafın masası** gibi görünsün: kareli defter, takvim yaprağı, kasa fişi, dükkân tentesi. Bütün bunlar süs olarak kalır; okunurluk her zaman önce gelir (düz kartlar, net hiyerarşi, rakamlar eşit genişlikte).

## Öğeler

| Öğe | Nesne | Neden |
|---|---|---|
| Tarih | Duvar takvimi yaprağı (kırmızı başlık, büyük gün rakamı, altında günün sözü) | 2011 dükkânının en tanıdık nesnesi; gün geçişi "yaprak koparma" animasyonu olur |
| Para | Kasa fişi (mono rakam, kesik çizgili satırlar, tırtıklı alt kenar) | Kasa, borç, ciro tek bakışta; fiş numarası gün sayısı |
| Yapılacaklar | Çizgili defter sayfası, kırmızı kenar çizgisi, kutucuklar | Tek bildirim yerine "bugün ne yapmalı" listesi; biten iş üstü çizili kalır |
| Bölgeler | Defter ayracı sekmeleri | Harita filtreleri dosya sekmesi gibi |
| Harita | Basılı atlas: deniz adları aralıklı harf, ölçek çubuğu, mağazamız pul/mühür | Oyuncu "imparatorluğunu" kâğıt üstünde büyütür |
| Ana eylem | Yeşil-beyaz çizgili tente (Dükkâna gir) | Markanın imzası; dükkâna dönüşü hep aynı yer gösterir |
| Karakter sesi | Sarı not kartı ("Kadir Bey diyor ki") | Hikâye karakterleri paneli canlı tutar |

## Renk ve yazı

- Kâğıt `#F2ECDF`, kart `#FBF8F1`, mürekkep `#1E2621`, çizgi `#D9CFBB`.
- Miras yeşili `#24704F` (biz, olumlu, ana eylem), takvim kırmızısı `#C2412B` (acil, rakip, borç), hardal `#D49A2A` (uyarı, karakter notu). Başka vurgu rengi eklenmez.
- Yazılar mevcut tema ile aynı (`MarketTheme`): başlık Bricolage Grotesque, metin IBM Plex Sans, rakam IBM Plex Mono.
- Alt menü koyu "tezgâh" şeridi: açık zeminden ayrılır, dükkâna giriş düğmesi orada en göze batan şeydir.

## Dönemle büyüyen panel

Panel şirketle birlikte değişebilir (aynı yerleşim, değişen dokular):

1. **Aile dükkânı (2011–):** kâğıt, takvim yaprağı, kasa fişi (bu örnek).
2. **Şube ağı:** defter yerine klasör/dosya kartları, il haritası ön planda.
3. **Genel merkez / dünya:** daha temiz, koyu temalı "kontrol odası"; ama tente ve Miras yeşili kalır.

Böylece oyuncu ilerlemeyi rakamların yanında ekranın kendisinde de görür.
