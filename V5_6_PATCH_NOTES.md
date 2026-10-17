# TELKİN v5.6 — SES / AMBİYANS MOTORU

Bu sürüm canlı GitHub'a gönderilmemiş staging sürümüdür.

## Yeni ses çekirdeği
- `src/audio/presets.js`: mekân duygu profilleri ve zemin türleri.
- `src/audio/manager.js`: WebAudio tabanlı merkezi ses yöneticisi.
- `audio/manifest.json`: bus, format, voice ve lazy-load politikası.
- `audio/VOICE_NAMING.md`: Türkçe/İngilizce seslendirme dosya standardı.

## Aktif katmanlar
- Ambiyans bus: yağmur, rüzgâr, şehir, su, ateş, oda havası, elektrik/oda hum, mağara ve Doku.
- Mekân değişiminde yumuşak crossfade.
- Zemin türüne göre prosedürel adım sesi: wood/tile/metal/stone/gravel/dust/dirt/concrete/carpet.
- Kapı aç/kapat, zar yuvarlama, kamera glitch, telefon, belge, anomali, Nihyel, UI ve arcade cue API'leri.
- Ses açık/kapalı durumu mevcut save sisteminin `audioOn` alanıyla uyumlu kalır.
- Uygulama arka plana geçtiğinde ses context'i suspend edilir, dönüşte gerekiyorsa resume edilir.

## Seslendirme altyapısı
- `playVoice({lang, character, chapter, cue})` API'si eklendi.
- Örnek yol: `audio/voice/tr/mahir/chapter-001/cue-01.ogg`.
- OGG öncelikli, MP3 fallback.
- Gerçek kayıt yoksa oyun kırılmaz; replik sessiz devam eder.
- Gerçek ses dosyaları henüz eklenmedi; sahte seslendirme paketlenmedi.

## Mevcut motora bağlanan cue'lar
- Yürüyüş/sprint -> zemin tabanlı step.
- Arka kapı -> open / close.
- Bölüm 11 zar mekaniği -> dice roll.
- Arcade kazanma -> win cue.
- Nihyel aç/kapat -> motif cue.
- UI düğmeleri -> hafif click.

## Dürüstlük / sınır
Bu sürüm gerçek stüdyo ambience/SFX/voice kayıtları içermez. İşitsel katmanın çalışan kısmı prosedürel WebAudio'dur ve sonradan gerçek kayıtlarla değiştirilebilecek biçimde tasarlanmıştır.
