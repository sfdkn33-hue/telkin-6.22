# TELKİN v6.17 — Kalıcı Çevre Durumu

## Ana değişiklik
Seçici çevre etkileşimleri artık yalnız runtime dekoru değildir; save sistemiyle birlikte yaşar.

### Kaydedilen çevre
- Hub arka kapısı
- Işık düğmesi / ışık durumu
- Defter
- Perde çiftleri
- Dolap/gardırop kapağı
- Sabit monitör
- Seçili sandalye
- Şifonyer çekmecesi

### Tasarım kararı
Atlas durumları `bölüm:mekân` anahtarında tutulur. Böylece oyuncu aynı bölüm içinde geri geldiğinde sahne hafızasını korur; fakat başka bir bölüm aynı mekânı kullandığında eski gündelik pozlar anlatının yeni anını kirletmez.

### Save / migration
- Save schema: 17 → 18
- Eski kayıtlar otomatik normalize edilir.
- Bozuk veya beklenmeyen çevre alanları boolean haritasına filtrelenir.
- Çevre bilgisi olmayan eski kayıtlar varsayılan sahneyle güvenli şekilde devam eder.

### Fizik
Restore edilen sandalye ve çekmece `q/target` durumunu ilk sahne kurulumunda alır. Dinamik collision callback'leri bu restore edilmiş değeri kullandığı için görünmez eski footprint kalmaz.

### GitHub
Canlı GitHub değiştirilmedi; bu paket staging içindir.
