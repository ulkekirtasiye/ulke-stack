# Yeni Özellik Geliştirme İstemi

Bu şablonu, mevcut bir projeye yeni özellik eklerken kullanın. Köşeli parantez içindeki alanları proje bağlamına göre doldurun. Eksik bilgi varsa, geri döndürülemez veya kapsamı önemli ölçüde değiştirecek varsayım yapmadan önce netleştirin.

## İstem Şablonu

```text
Mevcut projeye aşağıdaki özelliği ekle.

## Özellik Özeti

- Başlık: [Kısa ve eylem odaklı başlık]
- Problem: [Kullanıcının veya işletmenin yaşadığı sorun]
- Hedef kullanıcı: [Kim kullanacak?]
- Beklenen değer: [Özellik hangi sonucu iyileştirecek?]
- Kapsam: [Dahil olan ekranlar, akışlar, servisler veya veri alanları]
- Kapsam dışı: [Bu çalışmada özellikle yapılmayacaklar]

## Mevcut Bağlam

- İlgili dosyalar/bileşenler: [Biliniyorsa liste]
- Mevcut davranış: [Bugünkü akışın kısa açıklaması]
- Teknik kısıtlar: [Dil, çerçeve, veri, entegrasyon, performans veya dağıtım kısıtları]
- Tasarım/iş kuralı referansları: [Varsa bağlantı veya açıklama]

## Beklenen Çalışma Biçimi

1. Önce mevcut kodu ve ilgili kuralları incele; özellikle `CLAUDE.md` ve proje dokümantasyonunu esas al.
2. Özelliğin kapsamını, etkilenen bileşenleri, veri akışını ve mevcut davranışa etkisini özetle.
3. Belirsizlikler çözümü, veri güvenliğini, maliyeti veya kullanıcı deneyimini anlamlı biçimde etkiliyorsa uygulamadan önce sor.
4. Küçük, sıralı ve geri alınabilir bir uygulama planı sun. Her adımın amacını ve etkilenen dosyaları belirt.
5. Planı uygularken mevcut mimariyi koru; ilgisiz yeniden düzenleme, bağımlılık veya dosya ekleme.
6. Kullanıcı girdilerini, hata yollarını, yetki sınırlarını ve veri bütünlüğünü ele al.
7. Özellik için uygun testleri ekle veya güncelle; ilgili kalite kontrollerini çalıştır.
8. Tamamlandığında aşağıdaki teslim formatıyla rapor ver.

## Kabul Kriterleri

- [Kullanıcı davranışını anlatan, test edilebilir kriter 1]
- [Başarı/hata durumunu anlatan kriter 2]
- [Veri, yetki, performans veya erişilebilirlik kriteri 3]
- [Geri uyumluluk veya entegrasyon kriteri 4]

## Risk ve Operasyon Notları

- Veri etkisi: [Yok / Okuma / Yazma / Geçiş — ayrıntı]
- Güvenlik veya yetki etkisi: [Varsa açıklama]
- Dış servis/bağımlılık etkisi: [Varsa açıklama]
- Yayın veya geri alma gereksinimi: [Varsa açıklama]

## Teslim Formatı

Çalışma sonunda şu başlıklarla kısa ve somut bir özet ver:

1. Yapılan değişiklikler: Değişen dosyalar ve sağlanan davranış.
2. Kabul kriterleri: Her kriterin karşılanma durumu.
3. Doğrulama: Eklenen/güncellenen testler ve çalıştırılan komutların sonucu.
4. Riskler ve sınırlamalar: Kalan riskler, bilinmeyenler veya ertelenen işler.
5. Yayın notu: Yapılandırma, geçiş, izleme veya geri alma için gereken adımlar.
```

## Kullanım Notları

- Kabul kriterlerini “kullanıcı ne yapar, sistem ne olur” biçiminde yazın; teknik çözümü önceden zorunlu kılmayın.
- Özellik büyükse, ilk teslimi kullanıcıya değer sağlayan küçük bir dikey dilime indirgemeyi isteyin.
- Veri yazma, şema değişikliği, ödeme, erişim yetkisi veya canlı trafik etkisi varsa risk bölümünü doldurmak zorunludur.
- Uygulama başlamadan önce plan onayı gerekiyorsa isteme açıkça “Planı sun ve onayımı bekle” cümlesini ekleyin.
- Çalışma sonucunun yalnızca kod değişikliğinden ibaret olmadığını; test, dokümantasyon ve operasyon notlarını da kapsadığını doğrulayın.
