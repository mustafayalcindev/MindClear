# Yok Et / Yaşat

Karanlık temalı, tek sayfalık bir dijital ritüel uygulaması. Seni yoran bir düşünceyi yaz ve farklı araçlarla yok et; ya da değer verdiğin bir şeyi yaz ve büyüt. Hiçbir şey sunucuya gönderilmez, hiçbir şey kalıcı olarak saklanmaz — her şey sadece senin tarayıcında, o oturum boyunca yaşar.

> Bu proje tamamen [Claude](https://claude.ai) ile, tek bir `index.html` dosyası üzerinde, adım adım sohbet ederek geliştirildi.

<!-- 
Buraya bir ekran görüntüsü veya kısa bir GIF eklemek repo'yu çok daha çekici gösterir:
![önizleme](./screenshot.png)
-->

## ✨ Özellikler

### Yok Et
- Yazdığın düşünce ekranda büyük bir kelimeye dönüşüyor.
- Üç farklı **yok etme aracı** arasından seçim yapabiliyorsun:
  - 🔨 **Balyoz** — tıkladıkça çatlıyor, 5. tıklamada cam gibi kırılıp parçalanıyor.
  - 🔥 **Alev Makinesi** — basılı tuttukça ekrana gerçek anlamda alev püskürtüyor, kelime küle dönüşüyor.
  - 🌀 **Kara Delik** — her tıklamada büküp küçülterek kendi içine çekiyor, sonunda bir tekilliğe çöküyor.
- Her vuruşta haptik titreşim, ekran sarsıntısı ve katmanlı, sentezlenmiş ses efektleri (Web Audio API ile, hiçbir ses dosyası kullanılmadan).
- Yok etmenin ardından **7 saniyelik gerçek bir nefes molası** — senkronize nefes sesi ve yükselen yeşil ışıklarla.

### Yaşat
- Değer verdiğin, büyütmek istediğin bir şeyi yaz; yumuşak bir "filizlenme" animasyonuyla büyüyor.
- Her eklediğin şey, hafifçe rastgele açılarla döndürülmüş küçük kartlardan oluşan bir **kolaja** (bahçene) ekleniyor.
- İstemediğin bir öğeyi bahçenden kaldırabiliyorsun.

### Genel
- Alt gezinme çubuğuyla iki mod arasında geçiş (Yok Et / Yaşat).
- Her iki tarafın sayılarını birleştiren tek bir istatistik çubuğu.
- Belirli kilometre taşlarında (5, 10, 25, 50...) küçük kutlama anları.
- Ne yazacağını bilemeyenler için hazır öneri etiketleri.
- Uygulamanın renkleriyle tasarlanmış, indirilebilir/paylaşılabilir bir **özet kartı** (Canvas API ile anlık oluşturuluyor).
- Yerel paylaşım menüsü desteği (Web Share API), yoksa panoya kopyalama veya dosya indirme.
- Ekranda ara sıra gezinen, tıklayınca ürken küçük bir hayalet figürü.
- Tam klavye erişilebilirliği, ekran okuyucu etiketleri, `prefers-reduced-motion` desteği.
- Duyarlı (responsive) tasarım, mobil güvenli alan (safe-area) desteği.

## 🧱 Teknoloji

Harici hiçbir framework veya kütüphane yok — tamamen **vanilla HTML / CSS / JavaScript**, tek dosyada:

- Ses tasarımı: [Web Audio API](https://developer.mozilla.org/docs/Web/API/Web_Audio_API) (tüm efektler kod ile sentezleniyor)
- Titreşim: [Vibration API](https://developer.mozilla.org/docs/Web/API/Vibration_API)
- Paylaşım: [Web Share API](https://developer.mozilla.org/docs/Web/API/Navigator/share)
- Özet kartı: [Canvas API](https://developer.mozilla.org/docs/Web/API/Canvas_API)
- Google Fonts: Archivo Black, Inter

## 🚀 Kullanım

### GitHub Pages ile yayınlama
1. Bu repo'yu fork'la veya klonla.
2. GitHub'da **Settings → Pages** kısmından `main` dalını (branch) kaynak olarak seç.
3. Birkaç dakika içinde `https://<kullanıcı-adın>.github.io/<repo-adı>/` adresinde canlı olur.

### Yerelde çalıştırma
Herhangi bir derleme/kurulum adımı yok. `index.html` dosyasını doğrudan tarayıcıda açman yeterli:

```bash
git clone https://github.com/<kullanıcı-adın>/<repo-adı>.git
cd <repo-adı>
open index.html   # macOS
# veya dosyaya çift tıkla
```

## 🔒 Gizlilik

Uygulamanın bir sunucu tarafı (backend) yok. Yazdığın hiçbir şey hiçbir yere gönderilmiyor veya kalıcı olarak saklanmıyor; sayfayı yenilediğinde oturum sıfırlanır.

## 📄 Lisans

[MIT](./LICENSE)
