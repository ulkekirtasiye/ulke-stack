# Özellik Tanımı Şablonu

Bu şablon, yeni bir özelliğin iş hedefini, kapsamını, teknik etkilerini ve yayın hazırlığını ortak bir kaynakta toplamak için kullanılır. Köşeli parantez içindeki alanları doldurun. Bilinmeyen alanları varsayımla kapatmak yerine `Açık Sorular` bölümünde kaydedin.

## 1. Genel Bilgi

- **Başlık:** [Özelliğin kısa ve açık adı]
- **Durum:** [Taslak / İncelemede / Onaylandı / Geliştirmede / Yayına Hazır / Yayınlandı]
- **Sahip:** [Ürün veya teknik sorumlu]
- **Oluşturulma tarihi:** [YYYY-AA-GG]
- **Son güncelleme:** [YYYY-AA-GG]
- **İlgili iş/issue:** [Bağlantı veya kimlik]
- **Hedef sürüm:** [Varsa sürüm veya kilometre taşı]

## 2. Problem ve İş Hedefi

### Problem Tanımı

[Hangi kullanıcı veya iş problemi çözülüyor? Mevcut durum, kanıt ve etkiyi açıklayın.]

### Hedef Kullanıcılar

- [Kullanıcı türü 1 ve ihtiyacı]
- [Kullanıcı türü 2 ve ihtiyacı]

### Beklenen Değer

[Kullanıcı ve işletme için beklenen sonucu açıklayın.]

### Başarı Ölçütleri

| Ölçüt | Başlangıç Değeri | Hedef | Ölçüm Kaynağı | Ölçüm Dönemi |
| --- | --- | --- | --- | --- |
| [Örn. işlem tamamlama süresi] | [Değer] | [Hedef] | [Kaynak] | [Dönem] |
| [Örn. hata oranı] | [Değer] | [Hedef] | [Kaynak] | [Dönem] |

## 3. Kapsam

### Dahil Olanlar

- [Kullanıcı akışı, ekran, API, veri veya entegrasyon kapsamı]
- [İkinci kapsam maddesi]

### Kapsam Dışı Alanlar

- [Bu teslimde yapılmayacak çalışma]
- [Sonraki aşamaya bırakılan ihtiyaç]

### Varsayımlar ve Bağımlılıklar

- **Varsayımlar:** [Doğrulanması gereken kabul]
- **Teknik bağımlılıklar:** [Servis, kütüphane, altyapı veya veri kaynağı]
- **İş bağımlılıkları:** [Tasarım, içerik, erişim, onay veya dış ekip ihtiyacı]

## 4. Kullanıcı Deneyimi ve İş Akışı

### Kullanıcı Senaryoları

1. **[Senaryo adı]:** [Kullanıcı], [amacı] için [eylemi] yapar; sistem [beklenen sonucu] sağlar.
2. **[Hata/istisna senaryosu]:** [Koşul] gerçekleştiğinde sistem [güvenli ve anlaşılır davranışı] gösterir.

### Akış Açıklaması

[Başlangıç, karar noktaları, başarı/hata/iptal yolları ve sonuç ekranlarını adım adım açıklayın.]

### Arayüz Etkileri

- **Etkilenen ekranlar/bileşenler:** [Liste]
- **Yeni veya değişen durumlar:** [Boş, yükleniyor, başarı, hata, yetkisiz vb.]
- **Erişilebilirlik:** [Klavye, odak, etiket, kontrast ve hata geri bildirimi gereksinimleri]
- **Responsive/koyu tema:** [Etkiler ve doğrulama yaklaşımı]
- **Kullanıcı metinleri:** [Yeni metinler, ton ve çeviri gereksinimi]

## 5. Teknik Tasarım

### Tasarım Özeti

[Bileşenler, sorumluluklar, veri akışı ve dış sistem sınırlarını açıklayın. Gerekirse diyagram veya bağlantı ekleyin.]

### Etkilenen Bileşenler

| Bileşen | Değişiklik | Gerekçe | Geri Uyumluluk Etkisi |
| --- | --- | --- | --- |
| [Modül/servis/ekran] | [Ekle/Değiştir/Kaldır] | [Neden] | [Yok/Var — açıklama] |

### İş Kuralları

- [Kural 1: giriş, koşul ve beklenen sonuç]
- [Kural 2: yetki, sınır veya hata davranışı]

### Yapılandırma ve Operasyon

- **Ortam değişkenleri/sırlar:** [Gerekli değerler; sırların saklanma yöntemi]
- **Gözlemlenebilirlik:** [Günlük, metrik, sağlık kontrolü veya uyarı]
- **Performans/kapasite:** [Beklenen yük, zaman aşımı, sorgu veya kaynak etkisi]

## 6. Veri Modeli

### Veri Etkisi

- **Etkilenen tablolar/varlıklar:** [Liste]
- **İşlem türü:** [Yok / Okuma / Yazma / Şema değişikliği / Veri geçişi]
- **Veri sınıflandırması:** [Genel / Dahili / Kişisel / Hassas]
- **Saklama ve silme:** [Varsa yaşam döngüsü gereksinimi]

### Şema ve Geçiş Tasarımı

| Nesne | Değişiklik | Bütünlük Kuralı | Geçiş/Geri Alma Notu |
| --- | --- | --- | --- |
| [Tablo/alan/indeks] | [Açıklama] | [NOT NULL, FK, UNIQUE vb.] | [Açıklama] |

### Veri Güvenliği

- [Yetkilendirme, sahiplik, doğrulama veya maskeleme gereksinimi]
- [Yedekleme, transaction veya veri dönüşümü gereksinimi]

## 7. API ve Entegrasyon Etkileri

| Sözleşme/Entegrasyon | Değişiklik | İstek/Yanıt veya Olay Etkisi | Sürümleme ve Geçiş |
| --- | --- | --- | --- |
| [API, Worker, dış servis] | [Açıklama] | [Açıklama] | [Uyumlu/Uyumsuz — plan] |

- **Kimlik doğrulama ve yetki:** [Etkiler]
- **Hata ve zaman aşımı davranışı:** [Etkiler]
- **Dış servis kesintisi davranışı:** [Etkiler]

## 8. Kabul Kriterleri

- [ ] [Kullanıcının yapabildiği, gözlemlenebilir davranış]
- [ ] [Başarı, hata veya sınır durumuna ait kriter]
- [ ] [Veri bütünlüğü, yetki veya güvenlik kriteri]
- [ ] [Arayüz/erişilebilirlik veya performans kriteri]
- [ ] [Geri uyumluluk, entegrasyon veya operasyon kriteri]

Her kriterin testle, manuel kabul adımıyla veya üretim gözlemiyle nasıl doğrulanacağı `Test Planı` bölümünde belirtilmelidir.

## 9. Test Planı

| Test Alanı | Senaryo | Doğrulama Yöntemi | Beklenen Sonuç | Sorumlu |
| --- | --- | --- | --- | --- |
| Birim | [İş kuralı] | [Otomatik test] | [Sonuç] | [Rol] |
| Entegrasyon | [Veri/API akışı] | [Otomatik veya kontrollü test] | [Sonuç] | [Rol] |
| Arayüz | [Kritik kullanıcı yolu] | [Manuel/E2E] | [Sonuç] | [Rol] |
| Regresyon | [Mevcut davranış] | [Test paketi] | [Sonuç] | [Rol] |
| Operasyon | [Sağlık/izleme/geri alma] | [Kontrol] | [Sonuç] | [Rol] |

## 10. Riskler ve Önlemler

| Risk | Olasılık | Etki | Önleme/Azaltma | Sorumlu | Geri Alma Yaklaşımı |
| --- | --- | --- | --- | --- | --- |
| [Risk açıklaması] | [Düşük/Orta/Yüksek] | [Düşük/Orta/Yüksek] | [Önlem] | [Rol] | [Adım] |

Özellikle veri kaybı, yetkisiz erişim, geri uyumsuzluk, kesinti, maliyet ve dış servis bağımlılığı risklerini değerlendirin.

## 11. Yayın Planı

### Yayın Öncesi

- [ ] Kabul kriterleri ve test planı tamamlandı.
- [ ] Yapılandırma, sırlar, izinler ve veri geçişi doğrulandı.
- [ ] Yedekleme ve geri alma adımları gözden geçirildi.
- [ ] İzleme, sağlık kontrolü ve destek iletişimi hazırlandı.

### Yayın Sırası

1. [Aşama 1]
2. [Aşama 2]
3. [Aşama 3]

### Yayın Sonrası Doğrulama

- [ ] [Kritik kullanıcı akışı]
- [ ] [Hata oranı, gecikme veya iş metriği]
- [ ] [Veri ve entegrasyon kontrolü]

### Geri Alma

[Geri alma tetikleyicisi, uygulanacak adımlar, veri etkisi ve karar sorumlusu]

## 12. Açık Sorular ve Kararlar

| Tarih | Konu | Karar veya Açık Soru | Sahip | Son Tarih |
| --- | --- | --- | --- | --- |
| [YYYY-AA-GG] | [Konu] | [Açıklama] | [Rol] | [YYYY-AA-GG] |

## 13. Onaylar

| Rol | Ad | Durum | Tarih | Not |
| --- | --- | --- | --- | --- |
| Ürün | [Ad] | [Bekliyor/Onaylandı] | [YYYY-AA-GG] | [Not] |
| Teknik | [Ad] | [Bekliyor/Onaylandı] | [YYYY-AA-GG] | [Not] |
| Test | [Ad] | [Bekliyor/Onaylandı] | [YYYY-AA-GG] | [Not] |
