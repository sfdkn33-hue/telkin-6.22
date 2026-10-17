# TELKİN v6.16 — Dinamik Collision / Sandalye · Çekmece · Merdiven

## Amaç
v6.15'te başlayan yaşayan çevre katmanını, yalnız görsel hareketten gerçek fizik davranışına taşımak. Hareket eden nesne artık eski yerinde görünmez bir engel bırakmaz ve yeni konumunda içinden geçilemez.

## Yeni fizik katmanı
- **Sandalye:** `achair` ile üretilen sandalye parçaları grup kimliği alır. Bağlamsal olarak seçilen sandalye oturağı, nesnenin güncel konumunu izleyen dinamik footprint kullanır.
- **Bağlamsal sandalye:** kalabalık salonlar dışında sahne başına en fazla bir sandalye geri çekilip yerine itilebilir. Oturak, sırtlık ve dört ayak birlikte hareket eder.
- **Çekmece:** ev tipi `dresser` üzerinde fiziksel çekmece gövdesi, ön yüz ve kulp oluşturulur. Açıldığında çekmece collision'ı dışarı taşınır; kapalıyken gereksiz engel oluşturmaz.
- **Güvenlik kontrolü:** sandalye/çekmece hedef konumu oyuncu veya başka dinamik mobilya tarafından işgal ediliyorsa hareket başlamaz; kullanıcıdan biraz yana geçmesi istenir.
- **Merdiven:** koridor sahnelerinde beş basamak + üst sahanlık oluşturuldu. `groundY()` atlas içinde basamak yüksekliğini okuyarak Mahir/NPC/kamera yüksekliğini gerçek basamaklara bağlar. Yan korkuluk şeritleri fiziksel sınır olarak davranır.

## Görev güvenliği
- Bölüm 1'in merdiven hedefi merdivenin ağzında bırakıldı; görev rotası yeni geometri tarafından kesilmez.
- v6.12 erişilebilir hedef onarımı, v6.14 görev etkileşimi ve v6.15 görev önceliği korunur.
- Görev yakınken çevre nesnesi yine görevi ezmez.

## Performans
- Dinamik collision listesi yalnız gerçekten hareket eden / taşınabilir nesneleri tutar.
- AABB footprint her fizik sorgusunda nesnenin güncel transformundan hesaplanır; sahne yeniden taranmaz.
- Yeni harici görsel/ses asseti eklenmedi.

## Dil
- Sandalye, çekmece ve dolu hareket alanı uyarısı için TR/EN metinleri eklendi.

## Sürüm
- Staging: v6.16
- Service Worker: `telkin-v6-16-shell-1`
- Canlı GitHub: değiştirilmedi.
