# ULKE STACK — Geliştirme İlkeleri

Bu dosya, ULKE STACK kapsamındaki tüm projelerde insan ve yapay zekâ destekli geliştirme için ortak çalışma standartlarını tanımlar.

## Dil ve İletişim

- Kullanıcıyla her zaman Türkçe iletişim kur.
- Kod içi açıklamaları, dokümantasyonu, hata mesajlarını ve kullanıcıya gösterilen metinleri Türkçe yaz; teknik terimleri gerektiğinde yaygın İngilizce karşılığıyla kullan.
- Önce sonucu, ardından gerekli teknik ayrıntıyı açıkla. Belirsizlik, risk veya kapsam değişikliği varsa uygulamadan önce açıkça belirt.

## Çalışma Akışı

Her değişiklikte şu sırayı izle:

1. Mevcut kodu, mimariyi ve ilgili kuralları incele.
2. Kapsamı, etkilenecek bileşenleri ve olası riskleri belirle.
3. Küçük, geri alınabilir ve amaca doğrudan hizmet eden bir plan oluştur.
4. Uygulamayı mevcut mimari ve adlandırma düzeniyle uyumlu biçimde yap.
5. Değişikliğe uygun testleri çalıştır; başarısız testleri çözmeden işi tamamlanmış sayma.
6. Yapılan değişikliği, doğrulama sonucunu ve bilinen sınırlamaları kısa biçimde raporla.

Mevcut davranışı değiştiren, veri kaybı riski taşıyan veya dış sistemleri etkileyen işlemlerde açık onay al. İlgisiz dosyalara dokunma ve gereksiz soyutlama, bağımlılık veya dosya üretme.

## Kod Kalitesi

- Doğru, okunabilir, bakımı kolay ve test edilebilir kod yaz.
- Sorumlulukları küçük modüllere ayır; tek fonksiyonda birden fazla iş kuralı toplama.
- Anlamlı isimler kullan; kısaltma ve örtük davranışlardan kaçın.
- Tekrar eden iş kurallarını ortak bir noktada topla, ancak erken genelleme yapma.
- Girdi doğrulama, hata yakalama ve kullanıcıya anlaşılır hata mesajları sağla.
- Gizli anahtarları, parolaları ve kişisel verileri kaynak koda, günlük kaydına veya commit'e ekleme.
- Performansı ölçmeden karmaşık optimizasyona gitme; sıcak yolları ve I/O işlemlerini özellikle değerlendir.

## Python Standartları

- Python 3.14'ü hedefle ve standart kütüphaneyi öncelikle değerlendir.
- Tip ipuçlarını herkese açık fonksiyonlarda, sınıf metotlarında ve karmaşık veri akışlarında kullan.
- Kodun modüler kalması için arayüz, iş mantığı, veri erişimi ve altyapı katmanlarını ayır.
- Bağımlılıkları açıkça tanımla; gereksiz paket ekleme.
- Dosya, ağ ve veritabanı işlemlerinde bağlam yöneticileri (`with`) kullan; kaynakların güvenli kapanmasını sağla.
- İstisnaları sessizce yutma. Beklenen hataları özel olarak yakala, bağlam ekle ve gerektiğinde üst katmana ilet.
- Masaüstü uygulamalarında varsayılan arayüz kütüphanesi CustomTkinter'dır. Arayüz olay döngüsünü uzun süren işlerle engelleme.
- Varsayılan kalıcı veri çözümü SQLite'tır. Parametreli sorgu kullan, şema değişikliklerini sürümlendir ve işlem bütünlüğünü koru.

## Arayüz ve Kullanıcı Deneyimi

- Arayüzler sade, tutarlı, erişilebilir ve görev odaklı olmalı.
- Koyu tema desteği ile farklı ekran boyutlarında kullanılabilirlik sağla.
- Form alanlarında doğrulama, yükleme durumlarında geri bildirim ve hata durumlarında yönlendirici mesaj göster.
- Renk, metin boyutu veya yalnızca ikon ile anlam aktarmaya güvenme; yeterli kontrast ve erişilebilir etiket kullan.
- Kullanıcının verisini etkileyen işlemlerde onay, geri alma veya güvenli varsayılanlar sun.

## Test ve Doğrulama

- Yeni davranış için uygun seviyede birim, entegrasyon veya uçtan uca test ekle ya da mevcut testi güncelle.
- Hata düzeltmelerinde, hatayı yeniden üreten bir test eklemeyi önceliklendir.
- Testler deterministik, bağımsız ve okunabilir olmalı; dış servisleri gerektiğinde taklit et.
- Test edilemeyen bir değişiklik varsa nedenini ve uygulanan alternatif doğrulamayı raporla.

## Git ve Dokümantasyon

- Her commit tek bir mantıksal değişikliği içersin ve Türkçe, emir kipinde, açıklayıcı bir başlık taşısın.
- Büyük veya kullanıcıyı etkileyen değişikliklerde `docs/CHANGELOG.md` kaydı oluştur.
- Yeni özellik, önemli mimari kararı veya operasyonel gereksinim için yeterli dokümantasyon ekle.
- Başkasının mevcut değişikliklerini izinsiz silme, geri alma veya yeniden biçimlendirme.

## Dosya Organizasyonu ve Teslim Kriteri

- Her dosya açık bir sorumluluğa sahip olmalı; kaynak kod, test, yapılandırma ve dokümantasyon birbirinden ayrılmalıdır.
- Yeni dosya veya klasör, mevcut proje düzeniyle tutarlı bir konumda oluşturulmalı; geçici çıktılar, yerel veri ve gizli bilgiler sürüm kontrolüne eklenmemelidir.
- Paket veya modül yapısını yalnızca ihtiyaç varsa değiştir; genel amaçlı "utils" dosyaları yerine alanı ifade eden modüller kullan.
- Bir işin tamamlanmış sayılması için kabul kriterleri karşılanmalı, uygun testler veya eşdeğer doğrulama çalışmalı ve etkilenen dokümantasyon güncellenmelidir.
- Test çalıştırılamıyorsa sebebini, riski ve uygulanan alternatif doğrulamayı teslim notunda açıkça bildir.

## Commit Kuralları

- Commit başlığı en fazla 72 karakter, Türkçe, emir kipinde ve tek bir değişikliği anlatacak şekilde yazılır.
- Başlıkta uygun olduğunda tür belirtilir: `docs:`, `test:`, `fix:`, `feat:` veya `chore:`.
- Commit; gereksiz biçim değişikliği, sır, derlenmiş çıktı veya ilgisiz dosya içermemelidir.
- Kırıcı değişikliklerde geçiş notu, veri etkisi ve geri alma yaklaşımı commit veya ilgili dokümantasyonda belirtilmelidir.

## Öncelik Sırası

Kararlar alınırken aşağıdaki sıra gözetilir:

1. Doğruluk
2. Kararlılık ve veri bütünlüğü
3. Güvenlik
4. Performans
5. Okunabilirlik ve sürdürülebilirlik
