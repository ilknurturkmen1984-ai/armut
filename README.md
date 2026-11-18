# 🍐 Armut · Aile Bütçesi

Aile içi alışverişler ve gelir–gider takibi. Telefona uygulama gibi kurulur (Android ve iPhone).

## Yükleme (bir kez)

1. GitHub'da **armut** deposunu aç → **Add file → Upload files**.
2. Bu klasördeki her şeyi sürükle: `index.html`, `manifest.webmanifest`, `sw.js`, `README.md` ve `icons` klasörü → **Commit changes**.
3. **Settings → Pages** → Source: *Deploy from a branch*, Branch: `main` / `(root)` → **Save**.
4. 1–2 dakika sonra uygulama şu adreste açılır: `https://KULLANICI-ADIN.github.io/armut/`

> ⚠️ `armut-ilk-veri.json` dosyasını GitHub'a **yükleme**. Bu dosyada Excel'deki rakamlar şifresiz duruyor. Yalnızca uygulamanın içinden yüklenir.

## Yönetici anahtarı (token), yalnız senin için

Verilerin depoya kaydedilebilmesi için GitHub'da bir anahtar oluşturman gerekiyor:

1. GitHub → sağ üst profil → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**
2. Name: `armut` · Expiration: 1 yıl
3. Repository access: **Only select repositories → armut**
4. Permissions → Repository permissions → **Contents: Read and write**
5. **Generate token** → çıkan `github_pat_…` metnini kopyala.

## İlk açılış

**Sende (yönetici):** Yönetici → aile şifresi (eşinle paylaşacağın, en az 10 karakter) → token → Başla.
Sonra **Ayarlar → Yedek / ilk veri dosyası yükle** ile `armut-ilk-veri.json` dosyasını seç. Excel'deki 2026 aylık toplamları ve borç/varlık/alacak tablosu uygulamaya gelir.

**Eşinin telefonunda:** aynı adresi aç → **Aile üyesi (izleyici)** → aynı aile şifresi → Başla.
Eşin tüm ekranları görür ve Excel raporu indirebilir, ama kayıt değiştiremez.

**Ana ekrana ekleme:** Android/Chrome'da ⋮ → *Ana ekrana ekle*. iPhone/Safari'de Paylaş → *Ana Ekrana Ekle*.

## Güvenlik

- Veriler depoda `data/armut.enc.json` dosyasında **AES-256 ile şifreli** durur. Depo herkese açık olsa da aile şifresini bilmeyen kimse içeriği okuyamaz.
- Aile şifresi hiçbir yere gönderilmez. **Şifreyi unutursan veri açılmaz.** Ayarlar → Yedek indir ile ara sıra yedek al.
- Token yalnız senin cihazlarında saklanır. Eşine token verme.

## Neler var

- **Ana Sayfa:** bu dönemin harcaması, gelir, kalan, bütçe çubuğu, en çok harcanan 5 kategori, son kayıtlar
- **+ Yeni kayıt:** gider/gelir, kategori, kimin için, ödeme şekli, taksit (taksitler aylara otomatik bölünür)
- **Sabit giderler:** aidat, faturalar, kredi gibi aylık kalemler tek ekrandan, geçen ayın tutarı önerilerek eklenir
- **Ekstreden yapıştır:** Excel'deki Tarih · Açıklama · Tutar sütunlarını kopyala-yapıştır yap. Kategoriler anahtar kelimeyle otomatik seçilir (Migros → Online Market, Bilyoner → Şans Oyunu …) ve aynı kayıt iki kez eklenmez
- **Rapor:** dönem ve yıl görünümü, kategori dağılımı, günlük mutfak maliyeti, önceki aya göre değişim, kategori×ay tablosu, **Excel raporu**
- **Durum:** varlıklar, borçlar, alacaklar ve net durum
- **Ayarlar:** bütçe, dönem başlangıç günü (kart kesim günü), aile üyeleri, kategoriler, sabit giderler, kurallar
