# Yayın Kontrol Listesi Şablonu

Bu şablon, bir sürümün güvenli, izlenebilir ve geri alınabilir biçimde yayımlanmasını sağlamak için kullanılır. Köşeli parantez içindeki alanları doldurun; her kontrolü kanıt veya bağlantıyla destekleyin. Kritik veya yüksek riskli açık madde varsa, açık iş sahibi onayı olmadan yayına devam etmeyin.

## 1. Yayın Bilgisi

- **Sürüm:** [Örn. v1.4.0]
- **Ortam:** [Önizleme / Test / Üretim]
- **Yayın tarihi ve penceresi:** [YYYY-AA-GG SS:DD–SS:DD, zaman dilimi]
- **Yayın sahibi:** [Rol veya ad]
- **Teknik sorumlu:** [Rol veya ad]
- **Test sorumlusu:** [Rol veya ad]
- **İlgili işler/PR'ler:** [Bağlantılar veya kimlikler]
- **Değişiklik günlüğü:** [docs/CHANGELOG.md bağlantısı]
- **Risk seviyesi:** [Düşük / Orta / Yüksek — gerekçe]

## 2. Yayın Kapsamı ve Karar

### Dahil Olan Değişiklikler

- [Özellik, hata düzeltmesi, yapılandırma veya altyapı değişikliği]
- [İkinci değişiklik]

### Hariç Olanlar ve Bilinen Sınırlamalar

- [Ertelenen iş veya kabul edilen sınırlama]

### Yayın Başarı Ölçütleri

- [Kritik kullanıcı akışı başarıyla tamamlanır.]
- [Hata oranı/performans eşiği aşılmaz.]
- [Veri ve entegrasyon kontrolleri beklenen sonucu verir.]

## 3. Yayın Öncesi Doğrulamalar

| Kontrol | Kanıt/Bağlantı | Sorumlu | Durum | Not |
| --- | --- | --- | --- | --- |
| Kapsam ve kabul kriterleri onaylandı | [Bağlantı] | [Rol] | [ ] | [Not] |
| Kod incelemesi tamamlandı | [Bağlantı] | [Rol] | [ ] | [Not] |
| İlgili test planı tamamlandı | [Bağlantı] | [Rol] | [ ] | [Not] |
| Otomatik testler başarılı | [Çıktı] | [Rol] | [ ] | [Not] |
| Biçimlendirme/lint/statik analiz başarılı | [Çıktı] | [Rol] | [ ] | [Not] |
| Paket/artefakt sürümlü ve izlenebilir | [Kimlik] | [Rol] | [ ] | [Not] |
| Dokümantasyon ve değişiklik günlüğü güncel | [Bağlantı] | [Rol] | [ ] | [Not] |
| Açık hata/riskler değerlendirildi | [Bağlantı] | [Rol] | [ ] | [Not] |

## 4. Güvenlik Kontrolleri

| Kontrol | Kanıt/Bağlantı | Sorumlu | Durum | Not |
| --- | --- | --- | --- | --- |
| Sırlar, token'lar ve kişisel veri kaynak kodu/çıktılarda yok | [Kanıt] | [Rol] | [ ] | [Not] |
| Ortam değişkenleri ve secret yönetimi doğrulandı | [Kanıt] | [Rol] | [ ] | [Not] |
| Kullanıcı, servis ve API erişimleri en az yetkiyle sınırlandı | [Kanıt] | [Rol] | [ ] | [Not] |
| Kimlik doğrulama, yetkilendirme ve sahiplik akışları test edildi | [Kanıt] | [Rol] | [ ] | [Not] |
| Girdi doğrulama, hata mesajları ve günlük kayıtları gözden geçirildi | [Kanıt] | [Rol] | [ ] | [Not] |
| Bağımlılık ve çalışma zamanı güvenlik bulguları değerlendirildi | [Kanıt] | [Rol] | [ ] | [Not] |
| TLS, yönlendirme, CORS/WAF veya dış erişim kuralları doğrulandı | [Kanıt] | [Rol] | [ ] | [Not] |

## 5. Veri Yedekleme ve Migration Doğrulaması

### Veri Yedekleme

| Kontrol | Kanıt/Bağlantı | Sorumlu | Durum | Not |
| --- | --- | --- | --- | --- |
| Etkilenen veri ve saklama gereksinimi belirlendi | [Kanıt] | [Rol] | [ ] | [Not] |
| Güncel yedek oluşturuldu | [Konum/Kimlik] | [Rol] | [ ] | [Not] |
| Yedek bütünlüğü doğrulandı | [Kanıt] | [Rol] | [ ] | [Not] |
| Geri yükleme adımı test edildi veya belgeli | [Kanıt] | [Rol] | [ ] | [Not] |

### Migration / Veri Geçişi

| Kontrol | Kanıt/Bağlantı | Sorumlu | Durum | Not |
| --- | --- | --- | --- | --- |
| Şema/değişim geçişleri sürümlü ve sıralı | [Bağlantı] | [Rol] | [ ] | [Not] |
| Ön koşul ve veri hacmi doğrulandı | [Kanıt] | [Rol] | [ ] | [Not] |
| Geçiş temsilî ortam ve veriyle denendi | [Çıktı] | [Rol] | [ ] | [Not] |
| Transaction, hata ve kısmi başarısızlık davranışı test edildi | [Kanıt] | [Rol] | [ ] | [Not] |
| Geçiş sonrası bütünlük sorguları hazır | [Bağlantı] | [Rol] | [ ] | [Not] |
| Geri alma/veri düzeltme planı onaylandı | [Bağlantı] | [Rol] | [ ] | [Not] |

## 6. Performans ve Dayanıklılık Kontrolleri

| Kontrol | Başlangıç/Eşik | Sonuç | Sorumlu | Durum |
| --- | --- | --- | --- | --- |
| Kritik kullanıcı akışı yanıt süresi | [Eşik] | [Ölçüm] | [Rol] | [ ] |
| API/sorgu gecikmesi ve hata oranı | [Eşik] | [Ölçüm] | [Rol] | [ ] |
| Kaynak kullanımı/kapasite | [Eşik] | [Ölçüm] | [Rol] | [ ] |
| Zaman aşımı, tekrar deneme ve dış servis hata davranışı | [Beklenen] | [Sonuç] | [Rol] | [ ] |
| Önbellek/iş kuyruğu/arka plan iş etkisi | [Eşik] | [Sonuç] | [Rol] | [ ] |

Ölçüm yapılmadıysa nedeni, riski ve kabul eden sorumluyu kaydedin; varsayıma dayalı performans onayı vermeyin.

## 7. Rollback Planı

- **Geri alma tetikleyicileri:** [Örn. hata oranı eşiği, veri bütünlüğü sorunu, kritik akış başarısızlığı]
- **Karar sahibi:** [Rol veya ad]
- **Hedef geri dönüş sürümü/artefaktı:** [Kimlik]
- **Azami karar süresi:** [Dakika]

| Adım | Eylem | Sorumlu | Doğrulama | Veri Etkisi |
| --- | --- | --- | --- | --- |
| 1 | [Trafiği/yayını durdur veya sürümü geri al] | [Rol] | [Sağlık kontrolü] | [Açıklama] |
| 2 | [Gerekirse migration geri alma/veri düzeltmesi] | [Rol] | [Bütünlük kontrolü] | [Açıklama] |
| 3 | [Kritik akış ve izleme doğrulaması] | [Rol] | [Kanıt] | [Açıklama] |
| 4 | [Paydaş iletişimi ve olay kaydı] | [Rol] | [Bağlantı] | [Yok] |

## 8. Yayın Adımları

| Sıra | Eylem | Sorumlu | Başlama/Bitiş | Kanıt | Durum |
| --- | --- | --- | --- | --- | --- |
| 1 | [Son ön kontrol ve onay] | [Rol] | [Saat] | [Bağlantı] | [ ] |
| 2 | [Yedek alma veya bakım modu] | [Rol] | [Saat] | [Bağlantı] | [ ] |
| 3 | [Migration/konfigürasyon uygulama] | [Rol] | [Saat] | [Çıktı] | [ ] |
| 4 | [Artefakt dağıtımı] | [Rol] | [Saat] | [Sürüm] | [ ] |
| 5 | [Sağlık kontrolü ve duman testi] | [Rol] | [Saat] | [Kanıt] | [ ] |
| 6 | [Trafik/özellik açma] | [Rol] | [Saat] | [Kanıt] | [ ] |
| 7 | [Yayın duyurusu ve izleme başlangıcı] | [Rol] | [Saat] | [Bağlantı] | [ ] |

## 9. Yayın Sonrası İzleme

### İlk Kontroller

| Kontrol | Beklenen Sonuç/Eşik | İzleme Kaynağı | Sorumlu | Durum |
| --- | --- | --- | --- | --- |
| Uygulama/servis sağlığı | [Eşik] | [Kaynak] | [Rol] | [ ] |
| Kritik kullanıcı akışları | [Başarılı] | [Manuel/Otomatik] | [Rol] | [ ] |
| Hata oranı ve günlükler | [Eşik] | [Kaynak] | [Rol] | [ ] |
| Gecikme ve kaynak kullanımı | [Eşik] | [Kaynak] | [Rol] | [ ] |
| Veri bütünlüğü ve geçiş kontrolü | [Beklenen] | [Sorgu/Kayıt] | [Rol] | [ ] |
| Dış servis/API davranışı | [Beklenen] | [Kaynak] | [Rol] | [ ] |

- **Yoğun izleme süresi:** [Örn. ilk 60 dakika]
- **Takip dönemi:** [Örn. ilk 24 saat]
- **Uyarı/escalation kanalı:** [Kanal ve sorumlu]
- **Kullanıcı/destek iletişimi:** [Duyuru, destek notu veya durum sayfası]

## 10. Nihai Onay ve Kapanış

### Yayın Kararı

- [ ] Yayınlanabilir: Tüm kritik kontroller tamamlandı, engelleyici risk yok.
- [ ] Koşullu yayınlanabilir: Açık riskler kabul edildi ve takip planı belirlendi.
- [ ] Yayın engellendi: Gerekçe ve sonraki adım kaydedildi.

### Onaylar

| Rol | Ad | Karar | Tarih/Saat | Not |
| --- | --- | --- | --- | --- |
| Ürün/İş | [Ad] | [Onay/Bekliyor/Reddedildi] | [YYYY-AA-GG SS:DD] | [Not] |
| Teknik | [Ad] | [Onay/Bekliyor/Reddedildi] | [YYYY-AA-GG SS:DD] | [Not] |
| Test | [Ad] | [Onay/Bekliyor/Reddedildi] | [YYYY-AA-GG SS:DD] | [Not] |
| Operasyon | [Ad] | [Onay/Bekliyor/Reddedildi] | [YYYY-AA-GG SS:DD] | [Not] |

### Kapanış Notu

- **Gerçekleşen yayın zamanı:** [YYYY-AA-GG SS:DD]
- **Sonuç:** [Başarılı / Geri alındı / Kısmi başarı]
- **Açık takip işleri:** [Bağlantılar veya Yok]
- **Olay/öğrenim kaydı:** [Varsa bağlantı]
