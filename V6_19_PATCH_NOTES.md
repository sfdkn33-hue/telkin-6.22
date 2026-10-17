# TELKİN v6.19 — Elde Tutulan Nesne Katmanı

## Ana değişiklik
Mahir artık telefon, ses kayıt cihazı, kamera, belge ve fotoğraf/hatıra görevlerinde nesneyi yalnız uzaktan tetiklemiyor. Küçük fiziksel nesne temsili mevcut foto-gerçek Mahir sprite'ının dünya uzayındaki el/göğüs/yüz ankrajına bağlanıyor.

## Akış
- Telefon masadan kaybolup Mahir'in kulağına gelir; işlem bitince yerine döner.
- Ses kayıt cihazı ele alınır; kayıt LED'i elde görünür.
- Kamera görevlerinde sabit inceleme ekranından ayrı küçük kamera gövdesi masada bulunur ve Mahir'in yüz hizasına gelir.
- Belge görevlerinde orta sayfa masadan alınır, göğüs önünde tutulur ve geri bırakılır.
- Hatıra/fotoğraf görevlerinde fotoğraf çerçeveden ayrılıp elde incelenir ve geri döner.
- Alma / tutma / geri bırakma tek bir yumuşak envelope ile çalışır; sahne kaynağı aynı anda küçülerek kopya hissini azaltır.

## Kapsam
Gameplay verisinde bu beş tür toplam 270 fiziksel görev adımıdır. Bölüm 1–2 gibi özel sahnelerde de eldeki temsil, gp nesnesi bulunmasa bile Mahir'in action state'inden çizilir.

## Teknik ilke
- Yeni rig veya sahte iskelet animasyonu yok.
- Save schema 18 değişmedi; elde tutma tamamen transient.
- v6.18 beden koreografisi ve v6.17 çevre kalıcılığı korunur.
- Canlı GitHub değiştirilmedi.
