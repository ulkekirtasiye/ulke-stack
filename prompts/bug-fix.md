# Hata Düzeltme İstemi

Bu şablonu, mevcut bir projedeki davranış hatasını güvenli ve kalıcı biçimde gidermek için kullanın. Köşeli parantez içindeki alanları mevcut kanıtla doldurun. Hata yeniden üretilemiyorsa bunu gizlemeyin; gözlem, günlük kaydı ve ortam farkını açıkça belirtin.

## İstem Şablonu

```text
Mevcut projedeki aşağıdaki hatayı incele ve düzelt.

## Hata Özeti

- Başlık: [Kısa ve kullanıcı etkisini anlatan başlık]
- Etkilenen kullanıcı/alan: [Kim veya hangi sistem etkileniyor?]
- Önem derecesi: [Kritik / Yüksek / Orta / Düşük]
- Ortam ve sürüm: [Geliştirme, test, üretim; sürüm/commit bilgisi]
- İlk gözlem zamanı: [Biliniyorsa tarih/saat]

## Yeniden Üretim Bilgisi

- Ön koşullar: [Gerekli hesap, veri, izin, yapılandırma veya durum]
- Adımlar:
  1. [Adım 1]
  2. [Adım 2]
  3. [Adım 3]
- Beklenen davranış: [Sistemin yapması gereken]
- Gerçekleşen davranış: [Görülen sonuç]
- Kanıt: [Güvenli günlük özeti, hata mesajı, ekran görüntüsü veya test çıktısı]
- Tekrar oranı: [Her zaman / Aralıklı / Bilinmiyor]

## Etki ve Kısıtlar

- Kullanıcı, veri, güvenlik veya operasyon etkisi: [Açıklama]
- Etkilenen bileşenler/dosyalar: [Biliniyorsa liste]
- Son değişiklikler veya bağımlılıklar: [Biliniyorsa açıklama]
- Geçici çözüm: [Varsa açıklama]

## Beklenen Çalışma Biçimi

1. Önce `CLAUDE.md`, ilgili dokümantasyon ve hata kapsamındaki mevcut kodu incele.
2. Hatanın yeniden üretim adımlarını mümkünse bağımsız biçimde doğrula. Üretim verisi veya sır kullanma.
3. Belirtileri, kök nedeni ve tetikleyen koşulları birbirinden ayır. Kanıtlanmamış nedeni kesinmiş gibi sunma.
4. Veri kaybı, güvenlik, yetki veya kesinti riski varsa etkiyi önce sınırla; yıkıcı işlem öncesinde onay iste.
5. Kök nedeni ortadan kaldıran en küçük yeterli düzeltmeyi planla. İlgisiz refactor veya davranış değişikliği yapma.
6. Hatanın tekrarını engelleyen bir regresyon testi ekle veya mevcut testi güncelle.
7. Başarı yolunu, hata yolunu, sınır değerleri ve etkilenen entegrasyonları uygun düzeyde doğrula.
8. Uygun kalite/test kontrollerini çalıştır ve aşağıdaki teslim formatıyla rapor ver.

## Düzeltme Kabul Kriterleri

- Hata, belirtilen veya belgelendiği biçimde artık yeniden üretilemiyor.
- Beklenen davranış, ilgili kullanıcı akışında korunuyor.
- Hatanın tekrarını önleyen otomatik test veya eşdeğer doğrulama mevcut.
- Düzeltme, mevcut veri, yetki, API veya kullanıcı davranışında istenmeyen geri uyumsuzluk yaratmıyor.
- Hata mesajları ve günlük kayıtları gizli bilgi veya kişisel veri ifşa etmiyor.

## Teslim Formatı

Çalışma sonunda şu başlıklarla kısa ve somut bir özet ver:

1. Kök neden: Hatanın neden oluştuğu ve bunu destekleyen kanıt.
2. Düzeltme: Değişen dosyalar ve düzeltmenin davranışı nasıl değiştirdiği.
3. Doğrulama: Yeniden üretim sonucu, eklenen/güncellenen testler ve çalıştırılan kontroller.
4. Etki: Geri uyumluluk, veri, güvenlik ve operasyon değerlendirmesi.
5. Riskler ve takip: Kalan belirsizlik, geçici çözüm veya yayın sonrası izleme gereksinimi.
```

## Kullanım Notları

- Hata yalnızca üretimde görülüyorsa, üretim verisini kopyalamak yerine anonimleştirilmiş veya sentetik veriyle temsilî senaryo oluşturun.
- Aralıklı hatalarda zaman, eşzamanlılık, ağ, kaynak kullanımı ve dış servis yanıtları gibi değişkenleri özellikle kaydedin.
- Kök neden bulunmadan yalnızca semptomu gizleyen çözümü “düzeltildi” olarak işaretlemeyin; geçici önlemse bunu açıkça belirtin.
- Şema geçişi, toplu veri düzeltmesi veya geri döndürülemez işlem gerekiyorsa yedekleme, onay, doğrulama ve geri alma planını ayrıca isteyin.
- Güvenlik açığı şüphesinde istismar ayrıntılarını veya hassas kanıtları isteme eklemeyin; etkiyi sınırlama ve güvenli bildirim sürecini önceliklendirin.
