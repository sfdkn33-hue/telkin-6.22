# TELKİN v6.18 — Fiziksel Beden / Nesne Kullanımı

## Ana değişiklik
Mahir artık etkileşim sırasında yalnız hedefe bakmıyor; üretim sprite'ı korunarak beden taşıyıcısı eyleme göre eğiliyor, alçalıyor, nesneye yaklaşıyor ve kamera bu beden hareketini takip ediyor.

### Bağlanan eylemler
- Hub ahşap kapısında kola uzanma koreografisi
- Işık düğmesi / ekran: kısa uzanma-dokunma
- Dolap / perde: uzanma
- Çekmece: alçak uzanma
- Defter ve belge sınıfı: eğilip inceleme
- Kamera / ses / telefon: dokunma
- Bölüm içindeki fiziksel görevlerde tür bazlı Mahir beden pozu
- Sandalye: çek → otur → kalk + yerine it döngüsü

### Sandalye
Sandalye geri çekildikten sonra ikinci etkileşim Mahir'i oturtur. Otururken hareket kilitlenir fakat ETKİLEŞ düğmesi çalışır; üçüncü etkileşimde Mahir kalkar ve sandalye otomatik olarak yerine itilir. Oturma hâli save'e yazılmaz; sandalyenin fiziksel konumu v6.17 çevre kaydıyla korunur.

### Görsel ilke
Eski primitif 3D Mahir production renderına geri alınmadı. v6.18, kabul edilen foto-gerçek yönlü sprite sistemini korur; beden kullanımı billboard taşıyıcısının kontrollü dönüşüm/kamera koreografisiyle verilir.

### GitHub
Canlı GitHub değiştirilmedi; paket staging içindir.
