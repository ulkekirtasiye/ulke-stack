# Test Planı Şablonu

Bu şablon, bir özellik, hata düzeltmesi, refactor veya sürümün kalite risklerini planlı biçimde doğrulamak için kullanılır. Köşeli parantez içindeki alanları doldurun. Plan; yalnızca çalıştırılacak testleri değil, kapsanan riski, kanıtı ve yayın kararını da açıklamalıdır.

## 1. Genel Bilgi

- **Başlık:** [Test planının kısa adı]
- **Durum:** [Taslak / İncelemede / Onaylandı / Uygulanıyor / Tamamlandı]
- **Sahip:** [Test sorumlusu]
- **Tarih:** [YYYY-AA-GG]
- **İlgili iş/özellik/sürüm:** [Bağlantı veya kimlik]
- **Test edilecek sürüm/commit:** [Kimlik]
- **Risk seviyesi:** [Kritik / Yüksek / Orta / Düşük]

## 2. Amaç ve Kapsam

### Amaç

[Hangi kullanıcı, iş, veri veya operasyon riskinin doğrulanacağını açıklayın.]

### Dahil Olanlar

- [Etkilenen özellik, bileşen, ekran, API veya veri akışı]
- [İkinci kapsam maddesi]

### Hariç Olanlar

- [Bu planın kapsamadığı alan]
- [Başka plan veya sürümde ele alınacak çalışma]

### Referanslar ve Bağımlılıklar

- **Gereksinim/kabul kriterleri:** [Bağlantı veya özet]
- **Tasarım/ADR:** [Bağlantı veya özet]
- **Dış bağımlılıklar:** [Servis, veri, erişim veya ortam ihtiyacı]
- **Varsayımlar:** [Doğrulanması gereken kabul]

## 3. Risk Değerlendirmesi

| Risk | Olasılık | Etki | Öncelik | Test Yaklaşımı | Sorumlu |
| --- | --- | --- | --- | --- | --- |
| [Yanlış iş davranışı] | [D/O/Y] | [D/O/Y] | [K/O/Y/D] | [Senaryo/katman] | [Rol] |
| [Veri bütünlüğü veya kaybı] | [D/O/Y] | [D/O/Y] | [K/O/Y/D] | [Senaryo/katman] | [Rol] |
| [Yetki veya gizlilik sorunu] | [D/O/Y] | [D/O/Y] | [K/O/Y/D] | [Senaryo/katman] | [Rol] |
| [Entegrasyon/kesinti riski] | [D/O/Y] | [D/O/Y] | [K/O/Y/D] | [Senaryo/katman] | [Rol] |

`D/O/Y`: Düşük / Orta / Yüksek. `K/O/Y/D`: Kritik / Yüksek / Orta / Düşük.

## 4. Test Stratejisi

| Test Katmanı | Amaç | Dahil Senaryolar | Otomasyon | Araç/Ortam |
| --- | --- | --- | --- | --- |
| Birim | [İş kuralları/dönüşümler] | [Senaryolar] | [Evet/Hayır] | [Araç] |
| Entegrasyon | [Veri/API/dosya] | [Senaryolar] | [Evet/Hayır] | [Araç] |
| Uçtan uca/Manuel kabul | [Kritik kullanıcı akışı] | [Senaryolar] | [Evet/Hayır] | [Araç] |
| Regresyon | [Mevcut davranış] | [Senaryolar] | [Evet/Hayır] | [Araç] |
| İşlevsel olmayan | [Performans/erişilebilirlik/güvenlik] | [Senaryolar] | [Evet/Hayır] | [Araç] |

En hızlı ve güvenilir kanıtı sağlayan test katmanını tercih edin. Aynı davranışı gereksiz biçimde birden fazla katmanda kopyalamayın.

## 5. Test Ortamı ve Veri

| Alan | Gereksinim | Hazırlık/Doğrulama |
| --- | --- | --- |
| Ortam | [Geliştirme/Test/Önizleme] | [Sürüm, yapılandırma, erişim] |
| Veritabanı | [Şema ve veri durumu] | [Sentetik/anonim veri, geçiş] |
| Kullanıcı/roller | [Gerekli yetkiler] | [Test hesabı oluşturma] |
| Dış servisler | [Taklit/sandbox/gerçek servis] | [Zaman aşımı, hata senaryosu] |
| Cihaz/tarayıcı | [Gerekli kapsam] | [Sürüm ve çözünürlük] |

- Test verisi kişisel veri, gerçek parola, token veya üretim sırrı içermemelidir.
- Ortam farkları sonucu etkileyebiliyorsa, fark ve gerekçesi açıkça kaydedilmelidir.

## 6. Test Senaryoları

| Kimlik | Alan | Ön Koşul | Adımlar | Beklenen Sonuç | Öncelik | Tür | Durum |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TP-001 | [Akış] | [Koşul] | [Kısa adımlar] | [Gözlemlenebilir sonuç] | [K/O/Y/D] | [Birim/Entegrasyon/E2E/Manuel] | [Planlandı] |
| TP-002 | [Hata yolu] | [Koşul] | [Kısa adımlar] | [Güvenli hata davranışı] | [K/O/Y/D] | [Tür] | [Planlandı] |
| TP-003 | [Sınır/yetki] | [Koşul] | [Kısa adımlar] | [Beklenen sınır davranışı] | [K/O/Y/D] | [Tür] | [Planlandı] |

En az aşağıdaki durumları değerlendirin: başarı akışı, boş/geçersiz/sınır girdi, hata ve zaman aşımı, yetkisiz erişim, veri bütünlüğü, geri uyumluluk ve kritik kullanıcı akışı.

## 7. Otomasyon ve Kalite Kontrolleri

- **Eklenmesi/güncellenmesi gereken testler:** [Liste]
- **Çalıştırılacak komutlar:** [Biçimlendirme, lint, statik analiz, test, paketleme]
- **Kararlılık önlemleri:** [Zaman, ağ, rastgelelik ve dış servis bağımlılığı yaklaşımı]
- **Test bakım notları:** [Fixture, taklit, veri temizliği veya özel kurulum]

Testler bağımsız ve deterministik olmalıdır. Aralıklı başarısızlık görüldüğünde, yeniden çalıştırmak yerine kök neden ve kalıcı düzeltme planı kaydedilmelidir.

## 8. Giriş ve Çıkış Ölçütleri

### Başlama Ölçütleri

- [ ] Kabul kriterleri ve kapsam onaylandı.
- [ ] Test ortamı, erişimler ve test verisi hazır.
- [ ] Bağımlılıklar erişilebilir veya uygun taklitler hazır.
- [ ] Bilinen blokajlar ve risk sahipleri kaydedildi.

### Tamamlama Ölçütleri

- [ ] Kritik ve yüksek öncelikli senaryolar tamamlandı.
- [ ] Engelleyici hata kalmadı; açık hataların etkisi ve kabulü kaydedildi.
- [ ] İlgili otomatik testler ve kalite kontrolleri başarılı.
- [ ] Kapsam dışı veya test edilemeyen riskler belgelenmiş.
- [ ] Yayın öncesi ve sonrası doğrulama adımları hazır.

## 9. Hata Yönetimi ve Raporlama

- Hataları `templates/bug-report.md` şablonuna göre kaydedin.
- Her hata için önem derecesi, yeniden üretim adımı, etki, kanıt ve ilişkilendirilen test senaryosu bulunmalıdır.
- Kritik/yüksek hatalar çözülmeden veya iş sahibi tarafından açıkça kabul edilmeden yayın önerisi vermeyin.
- Günlük test durumunda tamamlanan senaryoları, blokajları, yeni riskleri ve karar ihtiyaçlarını belirtin.

## 10. Yayın Doğrulaması

### Yayın Öncesi

- [ ] Sürüm, yapılandırma, erişim ve veri geçişi kontrol edildi.
- [ ] Geri alma adımları ve yedekleme gereksinimi doğrulandı.
- [ ] Sağlık kontrolü, metrik ve uyarıların izleneceği belirlendi.

### Yayın Sonrası

| Kontrol | Yöntem | Beklenen Sonuç | Sorumlu | Durum |
| --- | --- | --- | --- | --- |
| [Kritik kullanıcı akışı] | [Manuel/Otomatik] | [Sonuç] | [Rol] | [Bekliyor] |
| [Hata oranı/sağlık] | [Gözlemleme] | [Eşik] | [Rol] | [Bekliyor] |
| [Veri/entegrasyon] | [Sorgu/işlem kontrolü] | [Sonuç] | [Rol] | [Bekliyor] |

## 11. Sonuç ve Onay

- **Test özeti:** [Kapsanan alanlar, önemli bulgular ve kanıt]
- **Kalan riskler:** [Açık risk, kabul eden rol ve takip planı]
- **Yayın önerisi:** [Yayınlanabilir / Koşullu yayınlanabilir / Engelleyici sorun var]

| Rol | Ad | Karar | Tarih | Not |
| --- | --- | --- | --- | --- |
| Test | [Ad] | [Onay/Bekliyor] | [YYYY-AA-GG] | [Not] |
| Ürün | [Ad] | [Onay/Bekliyor] | [YYYY-AA-GG] | [Not] |
| Teknik | [Ad] | [Onay/Bekliyor] | [YYYY-AA-GG] | [Not] |
