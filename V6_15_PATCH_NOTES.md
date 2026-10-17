# TELKİN v6.15 — Yaşayan Çevre / Bağlamsal Etkileşim

## Amaç
v6.14'te görev nesnelerini fiziksel hale getiren yaklaşımı, görev dışı çevreye kontrollü biçimde taşımak. Her nesneyi tıklanabilir yapmak yerine yalnız gündelik hayat hissini güçlendiren birkaç sınıf seçilir.

## Yeni çevre etkileşimleri
- **Işık düğmesi:** duvar düğmesi fiziksel tepki verir; pratik ışık emissive'leri ve iki ana sahne ışığı aç/kapa durumuna tepki verir.
- **Defter:** masa üstündeki seçili defter iki sayfalı fiziksel açılma/kapanma hareketi alır.
- **Perde:** pencere başına seçili perde çifti ray yönünde açılıp kapanır.
- **Dolap / gardırop:** ana gövde ve collision sabit kalır; sonradan eklenen ince kapaklar gerçek dikey menteşe çevresinde açılır.
- **Sabit ekran:** görev ekranlarından bağımsız monitör açılıp kapanabilir; emissive tepki verir.

## Oynanış kuralı
- Bölüm hedefi 2.20 m içindeyse **görev daima önceliklidir**.
- Görev uzaktayken oyuncu 1.48 m içindeki seçili çevre nesnesini kullanabilir.
- Çevre etkileşimi bölüm ilerlemesini, kanıtı, save durumunu veya hikâye koşullarını değiştirmez.
- Bağlamsal nesneler için ayrı mavi görev ışını üretilmez; ekran yalnız yakındayken doğal eylem istemini gösterir.

## Mobil / performans
- Çevre nesneleri sahne kurulurken bir kez indekslenir; her kare bütün sahnede regex taraması yapılmaz.
- Animasyon taban pozdan hesaplanır; drift oluşmaz.
- Dolap kapakları collision listesine eklenmez; mevcut mobilya gövdesi collision'ı korunur.
- Yeni harici görsel/ses asseti eklenmedi.

## Dil
- Işık, defter, perde, dolap ve ekran için TR/EN istemleri eklendi.

## Sürüm
- Staging: v6.15
- Service Worker: `telkin-v6-15-shell-1`
- Canlı GitHub: değiştirilmedi.
