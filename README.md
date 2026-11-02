# PDFgear Türkçe Dil Paketi (Resmi Olmayan)

PDFgear programı için topluluk tarafından hazırlanmış, gayrı resmi Türkçe dil paketidir.
PDFgear, Almanca dahil birçok dili desteklediği halde Türkçe içermiyor. Bu depo, programın
Almanca dil kaynaklarından (resource) başlayarak hazırlanan ve İngilizce kaynakla
karşılaştırılarak düzeltilen bir Türkçe çeviriyi içerir.

> ⚠️ Bu proje PDF Gear Tech Pte. Ltd. ile bağlantılı değildir, resmi bir ürün değildir.
> Kullanım tamamen kendi sorumluluğunuzdadır.

## İçerik

Depoda iki seçenek var:

- **`tr/`** — Gerçek bir Türkçe (`tr`) dil paketi. `CommonLib.resources.dll`,
  `PDFgear.resources.dll`, `pdfconverter.resources.dll`, `PDFMonitor.resources.dll`
  dosyalarını içerir.
- **`de_yerine_turkce/`** — Aynı çeviriler, ama Almanca (`de`) dil dosyalarının yerine
  geçecek şekilde paketlenmiş. `tr` klasörü çalışmazsa bu kullanılabilir.

## Kurulum

1. PDFgear'ı tamamen kapatın.
2. PDFgear'ın kurulu olduğu klasörü bulun (genelde `C:\Program Files\PDFgear\`).
   İçinde `de`, `fr`, `es` gibi dil klasörleri görmelisiniz.
3. Bu depodaki **`tr`** klasörünü, o klasörün yanına kopyalayın.
   (`Program Files` için yönetici izni gerekebilir.)
4. PDFgear'ı açın → **Ayarlar (Settings) → Diller (Languages)** listesinden Türkçeyi seçin.
5. Programı yeniden başlatın.

Türkçe seçeneği listede görünmezse `de_yerine_turkce` klasöründeki dosyalarla
`de` klasörünün içeriğini değiştirin (önce yedek alın) ve dili **Deutsch** olarak seçin.

## Nasıl hazırlandı

- Dört dil kaynağı DLL'inin (.NET `ResourceReader` formatı) içindeki Almanca metinler
  programatik olarak çıkarıldı (1664 benzersiz metin).
- Aynı dört exe/dll'in içine gömülü **İngilizce kaynak metinler** doğrudan ayrıştırılarak
  anahtar anahtar (key-by-key) karşılaştırma yapıldı.
- Çeviri Türkçeye çevrildi, yer tutucular (`{0}`, `[br]`, `XXX` vb.) korundu.
- Yeniden paketlenen dosyalar orijinal `.resources.dll` formatına geri yazıldı.

## Katkı

Hatalı veya iyileştirilebilir bir çeviri gördüyseniz lütfen bir **Issue** açın
veya **Pull Request** gönderin.

## Lisans

Bu depodaki çeviri metinleri ve betikler MIT lisansı ile paylaşılmıştır (bkz. `LICENSE`).
PDFgear programının kendisi ve orijinal kaynak dosyaları PDF Gear Tech Pte. Ltd.'e aittir;
bu depo yalnızca değiştirilmiş dil kaynak dosyalarını içerir.
