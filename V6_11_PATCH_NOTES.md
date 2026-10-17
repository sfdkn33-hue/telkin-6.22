# TELKİN v6.11 — Oyun-İçi QA / Asset Manifest Temizliği

- 94 adet procedural-only mekân paketinde var olmayan `scene.json` için gereksiz ağ isteği engellendi.
- Gerçek dış sahne dosyası yalnız `procedural-pro` paketlerde lazy-load edilir.
- Karakter manifestindeki fiziksel olarak paketlenmemiş 60 duygu/oturma poz yolu kaldırıldı; `poses:{}` + `poseStatus:not-packaged-v6.11` olarak açıkça işaretlendi.
- 11 karakter × 12 yön/yürüyüş karesi korunuyor: 132/132.
- Bölüm 8 Fırın Sokağı özel rotası doğrulandı: spawn→en uzak hedef ~6.13 m; ardışık hedefler en fazla ~3.59 m. 250 m karanlık yürüyüş rotası yok.
- 144 bölüm / 108 mekân eşleşmesi ve mekân chapter listeleri çapraz doğrulandı.
- Canlı GitHub değiştirilmedi.
