# Ev Gider Takip

Telefon için optimize edilmiş, aylık ev gelir-gider takip uygulaması.
Oluşturan: **HAKAN KORKMAZ** — Copyright © 2026

## Vercel'e yayınlama

Derleme gerektirmez; saf HTML/CSS/JS (statik site).

**Yöntem 1 – Sürükle bırak:** vercel.com/new → klasörü yükleyin. Framework: *Other*, Build Command ve Output Directory boş kalsın.

**Yöntem 2 – CLI:**
```
npm i -g vercel
cd ev-gider-takip
vercel --prod
```

**Yöntem 3 – GitHub:** klasörü bir repoya yükleyip Vercel'de içe aktarın.

## Dosyalar
- `index.html` – uygulamanın tamamı
- `sw.js` – çevrimdışı çalışma (önce ağ, yoksa önbellek)
- `manifest.webmanifest` + `icons/` – "Ana ekrana ekle" desteği
- `vercel.json` – önbellek ve güvenlik başlıkları

## Notlar
- Veriler yalnızca kullanıcının cihazında (IndexedDB) saklanır; sunucuya gönderilmez. Ayarlar > Veri yönetimi'nden düzenli JSON yedeği alın.
- Fotoğraflar kaydedilirken otomatik küçültülür (en fazla 640 px).
- Yazı stilleri Google Fonts'tan seçildiğinde yüklenir; internet yoksa sistem yazı tipine döner.
- Güncelleme yayınlarken `sw.js` içindeki `CACHE` sürümünü artırmanız önerilir.
