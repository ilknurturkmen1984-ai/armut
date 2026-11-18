# 🍐 Armut · Aile Bütçesi

Aile içi harcamalar, gelirler ve takip edilen ödemeler (sabit giderler, kredi kartı taksitleri, banka kredisi, kurs ücretleri).
YKS-LGS Takip ile aynı düzende çalışır: veriler Google Drive'da tutulur, eşin paylaştığın bağlantıdan görür.

## 1. GitHub'a yükle (bir kez)
1. **armut** deposu → **Add file → Upload files** → bu klasördekilerin hepsini sürükle: `index.html`, `manifest.webmanifest`, `sw.js`, `README.md`, `icons` klasörü → **Commit changes**.
2. **Settings → Pages** → Branch: `main` / `(root)` → **Save**.
3. 1–2 dakika sonra uygulama açılır: `https://ilknurturkmen1984-ai.github.io/armut/`

## 2. İlk açılış (senin telefonunda ya da PC'nde)
1. Uygulamayı aç → **Drive'a bağlan** → YKS-LGS'de kullandığın Google hesabını seç.
   Drive'ında **Armut** klasörü açılır, veriler oraya kaydedilir; her gün otomatik yedek de alınır.
2. **İlk veriyi yükle** → `armut-ilk-veri.json` dosyasını seç. Excel'indeki 2026 rakamları ve ödeme planları gelir.
3. Diğer cihazında (PC ya da telefon) da aynı adresi aç → **Drive'a bağlan**. İki cihaz aynı verileri görür.

## 3. Eşinle paylaş (bir kez)
**Ayarlar → 📲 Eşime bağlantı gönder** → Google API anahtarını yapıştır → **Bağlantıyı oluştur** → WhatsApp ile gönder.
- API anahtarı YKS-LGS'de kullandığınla aynı: eşine gönderdiğin YKS-LGS bağlantısında `k=` işaretinden sonraki kısım (AIza… ile başlar).
- Eşin bağlantıyı açar, ana ekrana ekler. Her açtığında senin son girdiğin verileri görür, değiştiremez.
- Eşinin ekranında "Veri alınamadı (403)" yazarsa: Google Cloud → API anahtarı → Web sitesi kısıtlamalarına `https://ilknurturkmen1984-ai.github.io/*` ekle.

## Nasıl kullanılır
- **+** : harcama ya da gelir gir. Kategori seç, açıklama yaz. Taksit seçersen alışveriş Ödemeler'e plan olarak eklenir.
- **Ödemeler → Bu ay** : aidat, faturalar, kredi, kart taksitleri, Arya'nın kursu. Ödediğine dokun → **Ödendi**. Gider kaydı kendiliğinden eklenir.
- **Ödemeler → Planlar** : yeni sabit gider, taksit, kredi, kurs ya da yıllık ödeme (DASK, emlak vergisi) ekle. Kalan taksit ve tutar görünür.
- **Ödemeler → Borç · Varlık** : banka hesapları, alacaklar, kalan kredi/taksit borcu ve net durum.
- **Rapor** : ay ve yıl özeti, kategori dağılımı, Excel raporu.
- Sağ üstteki düğme: **Drive · güncel** yazıyorsa her şey kayıtlı. **Kaydetmek için dokun** yazıyorsa Google oturumu yenilenmeli; dokunman yeterli.
