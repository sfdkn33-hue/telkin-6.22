# TELKİN v6.14 — Fiziksel Görev Etkileşimleri

## Amaç
v6.13 ile başlayan gerçek kapı yaklaşımını bölüm görevlerine yaymak: oyuncu ETKİLEŞ'e bastığında yalnızca ilerleme çubuğu değil, sahnedeki görev nesnesi de eyleme fiziksel bir karşılık verir.

## Yeni fiziksel etkileşim katmanı
- 144 bölümdeki 958 görev adımı yeniden sayıldı.
- 263 konuşma adımı mevcut 3D NPC konuşma sisteminde kalır.
- Kalan 695 görev adımı 12 fiziksel etkileşim türünde görsel hareket alır.

### Tür bazlı hareketler
- `door` (44): görev kapısı menteşe tarafından açılır; kilit/kol parçası kapıyla birlikte döner.
- `phone` (16): telefon gövdeden yükselir, oyuncuya doğru alınır ve ekran/parıltı tepki verir.
- `camera` (35): ekran/kayıt yüzeyi fiziksel odak ve titreşim/parıltı tepkisi verir.
- `audio` (18): kayıt cihazında basma hareketi ve LED ritmi çalışır.
- `document` (163): kâğıtlar masa üzerinde açılarak/fanlanarak okunur.
- `route` (116): rota parçaları sırayla fiziksel/ışıklı tepki verir.
- `memory` (38): fotoğraf/çerçeve hafifçe öne gelir ve vurgulanır.
- `body` (25): test alanı ve direkleri bedensel tepki sırasında hareket/vurgu alır.
- `hazard` (31): bariyer ve ikaz feneri aktif tarama tepkisi verir.
- `anomaly` (8): kristal/halka bileşenleri yükselme, dönüş ve genişleme tepkisi verir.
- `observe` (24): tarayıcı paneli ve ekranı gözlem sırasında hareketlenir.
- `inspect` (177): incelenen artefakt yükselip döner; kaide sabit referans olarak kalır.

## Kamera / karakter yönelimi
- Etkileşim başlarken Mahir görev nesnesine yönelir.
- Kamera yönü sert biçimde koparılmadan hedefe doğru hafifçe toparlanır.

## Ses
- Mevcut prosedürel ses motoru tür bazlı kullanılır: kapı/kilit, telefon, kamera, belge ve anomali özgül ses alır.
- Diğer fiziksel türler `ui_confirm` geri dönüşünü kullanır.
- Yeni harici ses dosyası eklenmedi.

## Güvenlik
- Animasyon her karede taban pozu üzerinden hesaplanır; birikimli konum/rotasyon drift'i oluşmaz.
- Etkileşim iptal edilirse görev nesneleri taban pozuna döner.
- Görev prop'ları collision'a çevrilmedi; oyuncuyu görev hedefinde sıkıştırmama ilkesi korunur.
- v6.13 gerçek arka kapı menteşe/collision sistemi aynen korunur.

## Offline
- Service Worker cache anahtarı `telkin-v6-14-shell-1` olarak yükseltildi.
- Yeni harici asset eklenmediği için shell listesine dosya eklemek gerekmedi.

## Not
- Canlı GitHub değiştirilmedi. Bu sürüm staging paketidir.
