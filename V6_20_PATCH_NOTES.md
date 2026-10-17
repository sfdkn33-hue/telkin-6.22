# TELKİN v6.20 — Aktif Nesne Kullanımı

## Ana değişiklik
v6.19'da Mahir'in eline gelen nesneler artık yalnız taşınmıyor; orta etkileşim fazında gerçekten kullanılıyor.

## Telefon
- Ekran etkileşim sırasında canlanır.
- Bağlantı durumu noktası ve konuşma/seviye çizgileri görünür.
- Arama bağlanma anında ayrı procedural bağlantı sesi çalar.

## Ses kayıt cihazı
- REC ışığı yanıp söner.
- Dört küçük VU seviye göstergesi kayıt boyunca hareket eder.
- Kayıt başlama anında ayrı kısa REC sesi çalar.

## Kamera
- Deklanşör düğmesi fiziksel olarak basılır.
- Lens/aperture kısa süre kapanır.
- Çekim anında gerçek kısa flaş görünür.
- Yeni procedural deklanşör sesi eklendi.

## Belge / fotoğraf
- Belgede üst sayfa orta fazda fiziksel olarak çevrilir; basit metin satırları elde okunabilirlik hissi verir.
- Fotoğraf/hatıra elde hafifçe çevrilip incelenir.
- Sayfa ve fotoğraf için ayrı hafif kâğıt sesleri vardır.

## Teknik
- Tüm kullanım hareketleri q/progress tabanlıdır; FPS değişiminde birikimli drift üretmez.
- Kullanım sesi tek seferlik latch ile korunur; render döngüsünde tekrar tetiklenmez.
- Save schema 18 değişmez; aktif kullanım transient kalır.
- TELKIN_UNIVERSE runtime sürüm etiketi de 6.20'ye çekildi; eski 5.4 title flash kaldırıldı.
- Canlı GitHub değiştirilmedi.
