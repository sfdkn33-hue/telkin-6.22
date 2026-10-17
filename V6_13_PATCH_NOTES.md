# TELKİN v6.13 — Gerçek Kapı / Etkileşim Katmanı

## Görsel
- Bölüm 1 odağındaki arka kapı için gerçekçi ahşap kapı görseli runtime WebP varlığına dönüştürüldü.
- Kaynak görsel mobil/WebGL için 512×1162 WebP olarak optimize edildi.
- Menteşe yönü ile görseldeki menteşe/kol tarafı eşleştirildi.
- Kapı artık düz wood küp yerine ince 3D gövde + foto-gerçek ön yüz olarak çiziliyor.

## Animasyon / Etkileşim
- Kapalı konum, ofis duvarındaki gerçek eşik doğrultusuna hizalandı.
- Açılma hareketi gerçek menteşe noktası çevresinde yaklaşık 86° dönüyor.
- Kapı koluna kısa basma hareketi eklendi.
- Var olan kapı açma/kapatma sesleri korunuyor ve yeni animasyonla eşleşiyor.

## Fizik
- Kapı açılırken collision artık bir anda yok olmuyor.
- İlk açılma fazında eşik kapalı kalır; yeterli açıklıktan sonra geçiş serbestleşir.
- Hareket eden kapı yaprağı kendi AABB collision alanını taşır; açık durumda da fiziksel yaprak içinden yürünmez.

## Offline / Cache
- `assets/props/door-wood.webp` service worker shell önbelleğine eklendi.
- Cache anahtarı `telkin-v6-13-shell-1` olarak yükseltildi.

## Not
- Canlı GitHub değiştirilmedi. Bu paket staging sürümüdür.
