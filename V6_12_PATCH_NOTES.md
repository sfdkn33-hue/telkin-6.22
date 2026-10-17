# TELKİN v6.12 — Fiziksel Oynanış / Kamera / Collision QA

- Oyuncu hareketi collision kontrolünde kısa alt-adımlara bölündü (`moveWithCollision`). Ani kare süresi / sprint kombinasyonlarında ince engel atlama ihtimaline karşı fizik güvenliği artırıldı.
- Bölüm hedefi artık yalnızca `boş nokta` kontrolünden geçmiyor; oyuncunun mevcut yürünebilir bölgesinden hedefe yol erişilebilirliği de sınanıyor.
- Bir hedef mobilya/duvar düzeni nedeniyle bağlı yürüyüş bölgesinin dışında kalırsa runtime hedefi aynı bölgede hedefe en yakın yürünebilir noktaya taşıyor ve konsola uyarı bırakıyor.
- Kamera occlusion hesabı döndürülmüş (`ry`) kutuların gerçek dünya AABB genişliğini hesaba katıyor. 90° dönmüş masa/duvar/kapı gibi hacimlerde yanlış kamera yaklaşması / gereksiz görünmezlik azaltıldı.
- Service Worker shell cache `telkin-v6-12-shell-1` olarak yükseltildi.
- Location loader sürüm etiketi `6.12.0` olarak senkronlandı.
- 144 bölüm, 958 görev adımı ve 108 mekân yeniden tarandı: bilinmeyen mekân referansı 0, authored sahne sınırı dışı hedef 0.
- 11 karakter × 12 runtime kare = 132/132; tamamı 384×768 WebP ve mevcut.
- Canlı GitHub değiştirilmedi.
