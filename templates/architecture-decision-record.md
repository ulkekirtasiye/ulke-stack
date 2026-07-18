# Mimari Karar Kaydı (ADR) Şablonu

Bu şablon, sistemin yapısını, güvenliğini, veri modelini, entegrasyonlarını veya operasyonunu anlamlı biçimde etkileyen mimari kararları kaydetmek için kullanılır. Her karar ayrı bir dosyada tutulmalı, karar verildikten sonra geçmişi yeniden yazılmamalıdır. Karar değişirse yeni bir ADR oluşturun ve önceki kayda referans verin.

## ADR-[Sıra No]: [Kısa Karar Başlığı]

- **Durum:** [Taslak / Önerildi / Kabul Edildi / Reddedildi / Kullanımdan Kaldırıldı / Yerine Geçti]
- **Tarih:** [YYYY-AA-GG]
- **Karar sahipleri:** [Rol veya ad]
- **Teknik sorumlu:** [Rol veya ad]
- **İlgili iş/özellik:** [Bağlantı veya kimlik]
- **İlgili ADR'ler:** [ADR numarası veya bağlantı]
- **Gözden geçirme tarihi:** [Varsa YYYY-AA-GG]

## 1. Bağlam ve Problem

[Kararı gerekli kılan durumu açıklayın. İş hedefi, kullanıcı etkisi, mevcut mimari, teknik borç, kısıtlar ve tetikleyen olaylar belirtilmelidir.]

### Karar Sürücüleri

- [Örn. Veri bütünlüğü ve güvenlik]
- [Örn. Yerel kullanımda düşük operasyon maliyeti]
- [Örn. Mevcut Python/SQLite mimarisiyle uyumluluk]
- [Örn. Geri alma ve bakım kolaylığı]

### Kapsam

- **Dahil:** [Bu kararın kapsadığı bileşen, akış veya ortam]
- **Hariç:** [Bu kararın kapsamadığı alan]
- **Varsayımlar:** [Doğrulanması gereken kabuller]
- **Kısıtlar:** [Teknik, mali, yasal, zaman veya ekip kısıtları]

## 2. Karar

[Alınan kararı açık, kısa ve uygulanabilir biçimde yazın. Karar, “Şunu kullanacağız/yapacağız” şeklinde somut olmalıdır.]

### Uygulama İlkeleri

- [Kararın uygulanırken korunması gereken kural]
- [Güvenlik, veri, performans veya operasyon ilkesi]
- [Sürümleme, yapılandırma veya gözlemlenebilirlik gereksinimi]

## 3. Alternatifler ve Değerlendirme

| Alternatif | Faydalar | Maliyetler/Riskler | Karar Sürücülerine Uyum | Sonuç |
| --- | --- | --- | --- | --- |
| [Seçilen yaklaşım] | [Faydalar] | [Maliyetler] | [Yüksek/Orta/Düşük] | Seçildi |
| [Alternatif 1] | [Faydalar] | [Maliyetler] | [Yüksek/Orta/Düşük] | Reddedildi |
| [Alternatif 2] | [Faydalar] | [Maliyetler] | [Yüksek/Orta/Düşük] | Reddedildi |

Alternatifleri yalnızca teknoloji adıyla değil; veri, kullanıcı deneyimi, güvenlik, bakım, maliyet ve operasyon etkisiyle değerlendirin.

## 4. Sonuçlar

### Olumlu Sonuçlar

- [Beklenen fayda]
- [İkinci fayda]

### Bedeller ve Riskler

- [Kabul edilen karmaşıklık, sınırlama veya risk]
- [İzlenmesi gereken varsayım]

### Etkilenen Alanlar

| Alan | Etki | Gerekli Eylem |
| --- | --- | --- |
| Kod/mimari | [Açıklama] | [Eylem] |
| Veri | [Açıklama] | [Eylem] |
| Güvenlik | [Açıklama] | [Eylem] |
| Operasyon | [Açıklama] | [Eylem] |
| Kullanıcı/arayüz | [Açıklama] | [Eylem] |
| Dokümantasyon | [Açıklama] | [Eylem] |

## 5. Uygulama ve Geçiş Planı

### Ön Koşullar

- [Erişim, yapılandırma, veri, tasarım veya onay gereksinimi]

### Aşamalar

1. [Geri alınabilir ilk adım]
2. [Uygulama veya geçiş adımı]
3. [Doğrulama ve yayına alma adımı]

### Geri Uyumluluk

- **Etkilenen sözleşmeler:** [API, veri şeması, dosya biçimi, kullanıcı akışı vb.]
- **Geçiş yaklaşımı:** [Sürümlendirme, uyumluluk katmanı, paralel çalışma veya iletişim]
- **Kullanıcı/entegrasyon sahibi eylemi:** [Varsa]

### Geri Alma

- **Tetikleyiciler:** [Hangi koşullarda geri alınacak?]
- **Adımlar:** [Geri alma sırası]
- **Veri etkisi:** [Geri alınabilirlik, yedekleme veya veri düzeltme notu]
- **Karar sorumlusu:** [Rol veya ad]

## 6. Doğrulama ve İzleme

- **Kabul ölçütleri:** [Kararın doğru uygulandığını gösteren sonuçlar]
- **Test yaklaşımı:** [Birim, entegrasyon, geçiş, performans, güvenlik veya manuel kabul testleri]
- **Operasyonel kontroller:** [Sağlık kontrolü, günlük, metrik, uyarı veya denetim kaydı]
- **Başarı ölçümü:** [Ölçüt, kaynak ve değerlendirme dönemi]
- **Gözden geçirme tetikleyicileri:** [Yük artışı, maliyet, hata oranı, yeni gereksinim veya güvenlik olayı]

## 7. Açık Sorular ve Takip İşleri

| Konu | Açıklama | Sahip | Hedef Tarih | Durum |
| --- | --- | --- | --- | --- |
| [Soru/iş] | [Açıklama] | [Rol] | [YYYY-AA-GG] | [Açık/Tamamlandı] |

## 8. Referanslar

- [Teknik dokümantasyon, iş gereksinimi, tasarım, test sonucu veya ilgili ADR bağlantısı]
- [İkinci referans]

## 9. Karar Geçmişi

| Tarih | Durum | Değişiklik | Sorumlu |
| --- | --- | --- | --- |
| [YYYY-AA-GG] | [Taslak/Onaylandı vb.] | [Kısa açıklama] | [Rol veya ad] |
