# Değişiklik Günlüğü

Bu dosya, ULKE STACK'te kullanıcıları, proje uygulayıcılarını veya bakım sürecini etkileyen önemli değişiklikleri kaydeder. Biçim, [Keep a Changelog](https://keepachangelog.com/tr/1.1.0/) yaklaşımını temel alır; sürümler [Semantic Versioning](https://semver.org/lang/tr/) ilkelerine göre değerlendirilir.

## Kayıt Kuralları

- Her sürüm `YYYY-AA-GG` yayımlanma tarihiyle kaydedilir.
- Henüz yayımlanmamış değişiklikler önce `[Yayınlanmadı]` bölümüne eklenir.
- Kullanıcıyı veya uygulayıcıyı etkileyen her değişiklik, kısa ve sonuç odaklı yazılır.
- Bir değişiklik birden fazla kategoriye aitse, en önemli etkisini temsil eden tek kategoriye yazılır.
- Geri uyumsuz değişiklikler `**UYUMSUZ DEĞİŞİKLİK:**` ifadesiyle başlar ve geçiş adımını açıklar.
- Güvenlik düzeltmeleri, hassas ayrıntı veya sır içermeden etki ve gerekli eylemle birlikte kaydedilir.
- Biçim, yazım veya dahili düzenlemeler yalnızca bakım yapanlar için anlamlıysa kayda eklenir.

## Kategoriler

- **Eklendi:** Yeni özellik, şablon, rol veya desteklenen iş akışı.
- **Değiştirildi:** Mevcut davranış, kural veya dokümantasyonda kullanıcıyı etkileyen güncelleme.
- **Kullanımdan Kaldırıldı:** İleride kaldırılacak yapı veya önerilen alternatif.
- **Kaldırıldı:** Artık desteklenmeyen içerik veya davranış.
- **Düzeltildi:** Hatalı veya eksik davranışın düzeltilmesi.
- **Güvenlik:** Güvenlik, erişim veya veri korumaya yönelik iyileştirme.

## [Yayınlanmadı]

### Eklendi

- Değişiklikler yayıma hazır olduğunda buraya eklenir.

### Değiştirildi

- README, hızlı başlangıç, agent, prompt, workflow ve şablon kullanımını açıklayan üretim odaklı bir yapıya getirildi.
- `CLAUDE.md` dosyasına dosya organizasyonu, teslim kriterleri ve commit kuralları eklendi.
- Python agent'ına kanıta dayalı hata giderme yöntemi eklendi.
- Dependabot yalnızca bu depoda mevcut olan GitHub Actions ekosistemi için çalışacak şekilde sınırlandırıldı.

## [0.1.0] - 2026-07-18

### Eklendi

- ULKE STACK için temel depo yapısı oluşturuldu.
- Python otomasyonu, web uygulamaları, masaüstü araçları, Cloudflare ve işletme araçları için ortak hedef tanımlandı.
- Uzman roller, görev istemleri, proje şablonları ve süreç dokümanları için başlangıç klasörleri eklendi.
- Python geliştirme çıktıları, sanal ortamlar, yerel sırlar ve yaygın araç önbellekleri için `.gitignore` yapılandırıldı.

## Sürümleme İlkeleri

- **MAJOR:** Geri uyumsuz kural, şablon veya yapı değişikliği. Geçiş notu zorunludur.
- **MINOR:** Geri uyumlu yeni özellik, rol, şablon veya anlamlı süreç iyileştirmesi.
- **PATCH:** Geri uyumlu hata düzeltmesi, açıklık iyileştirmesi veya küçük bakım değişikliği.

Birden fazla değişiklik tek sürümde yayımlanabilir. Sürüm numarası, en yüksek etkili değişikliğe göre belirlenir.

## Yayın Kontrolü

Yayın oluşturulmadan önce aşağıdaki kontroller tamamlanır:

1. `[Yayınlanmadı]` bölümündeki kullanıcıyı etkileyen maddeler uygun kategoriye taşınır.
2. Sürüm numarası ve tarih eklenir; uyumsuz değişiklikler için geçiş notu doğrulanır.
3. İlgili dokümantasyon, şablon ve referanslar güncel tutulur.
4. Biçim, bağlantı ve gerektiğinde ilgili kalite/test kontrolleri doğrulanır.
5. Yayın notu, değişikliğin faydasını, etkilenen alanları ve kullanıcıdan beklenen eylemi açıklar.
