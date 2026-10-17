# TELKİN v6.21 — Sinematik Nesne Odağı

## Ana değişiklik
v6.20'de aktif olarak kullanılan eldeki nesneler artık etkileşim sırasında ayrı bir sinematik okuma katmanı kazanır.

## Sinematik kamera
- Telefon, kayıt cihazı, kamera, belge ve hatıra kullanımında kamera kısa süreliğine Mahir'in omuz hattına yaklaşır.
- Kamera yönü Mahir'in baktığı yöne yumuşakça karışır; oyuncunun kamera yönü kalıcı olarak değiştirilmez.
- FOV etkileşim ortasında hafifçe daralır, başlangıç ve bitişte normal değere döner.
- Yaklaşım q/progress tabanlıdır; FPS değişiminde drift üretmez.
- Mevcut kamera occlusion çözümü yakın planda da korunur.

## Kamera / viewfinder
- Kamera kullanırken ekran üstünde gerçek bir viewfinder çerçevesi belirir.
- REC, merkez odak işareti ve mevcut görev hedefi kadraj etiketi olarak görünür.

## Telefon
- Telefon kullanımında ayrı arama HUD'ı açılır.
- Mevcut sahne repliklerinden güvenli biçimde karşı taraf adı bulunabiliyorsa kişi adı gösterilir (örn. MİNA); bulunamazsa HAT/LINE fallback kullanılır.
- Bağlantı anı BAĞLANIYOR → BAĞLANTI AKTİF olarak değişir.

## Belge / hatıra
- Belge ve hatıra kullanımında okunabilir bir yakın plan kartı görünür.
- Kart, henüz oynanmamış anlatı cümlelerini spoiler olarak açmaz; yalnız mevcut görev etiketi/hedefini gösterir.

## HUD davranışı
- Sinematik kullanım sırasında görev kartı, görev rehberi ve bölüm kimliği geri plana çekilir.
- Overlay pointer-events:none olduğundan mobil/masaüstü kontrolleri kilitlemez.
- prefers-reduced-motion desteği korunur.

## Teknik
- Save schema 18 değişmez; sinematik overlay transient'tir.
- Gameplay verisi değişmedi.
- Canlı GitHub değiştirilmedi.
