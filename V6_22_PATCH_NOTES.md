# TELKİN v6.22 — Uzun Sürüm Oynanış

## Ana değişiklik
Artık oynanışın kanonik anlatı kaynağı `novel/` altındaki 144 uzun bölüm dosyasıdır. 958 fiziksel görev iskeleti sahne yönlendirmesi olarak korunur; sahne tamamlandığında özet replikler yerine romanın ilgili tam paragraf aralığı açılır.

## Kapsam
- 144 bölüm
- 372 uzun-form sahne
- 318,974 kelime
- 38,677 paragraf
- 0 atlanan paragraf (build-time kapsam doğrulaması)

## Teknik
- Yeni `src/data/long-play.js`: bölüm/sahne -> paragraf aralığı manifesti.
- Yeni `src/novel/playback.js`: lazy-load roman sahne okuyucusu ve mobil sayfalama.
- `advanceChapter()` uzun-form katmanını ana anlatı olarak çağırır.
- Eski kısa sahne sistemi fallback olarak korunur.
- Service Worker: `telkin-v6-22-shell-1`.

## İlk bölüm ince ayarı
Bölüm 1’in altı uzun-form sahnesi, Eren el testi → kapı telkini → Mina telefonu → arka oda → açık kapı → final kilit sesi sırasına göre elle kesim kontrolünden geçirildi.
