# TELKİN v5.4 — Mekân Paket Motoru

Bu patch canlı GitHub sürümüne otomatik uygulanmamıştır. Kullanıcı `tamam` dediğinde toplu yayın paketine dahil edilecektir.

## Yeni dosyalar
- `src/data/location-packs.js` — 108 mekân manifesti
- `src/core/location-loader.js` — lazy `scene.json` yükleyici
- `assets/locations/LOCATION_PACK_SPEC.md`
- hero location pack klasörleri ve `scene.json` dosyaları

## Değişen dosyalar
- `index.html` — location manifest/loader scriptleri eklendi
- `src/core/game.js` — v5.4 location pack renderer ve hero set ayrıntıları
- `sw.js` — v5.4 cache ve yeni shell dosyaları
- `README.md`
- `PROJE_DURUMU.md`

## Hero setler
Office, Lab, Home, Hospital, University, Archive, Cafe, Bakery Street, School Night, Station, Management.

## Dürüstlük notu
Bu sürüm gerçek GLB/PBR model importunu henüz yapmaz. `models/` slotları ve lazy loader hazırdır; model yoksa çalışan `procedural-pro` set kullanılır.
