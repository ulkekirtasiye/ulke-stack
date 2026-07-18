# ULKE STACK Uygulama Standartları

Bu belge, ULKE STACK kapsamındaki projelerde uygulanacak asgari üretim standartlarını tanımlar. `CLAUDE.md` ortak çalışma ilkelerinin ana kaynağıdır; bu dosya ise proje teslimatlarında beklenen somut kalite ölçütlerini açıklar. Projeye özgü gerekçeli bir gereksinim bu kurallardan daha sıkıysa, daha sıkı olan kural uygulanır.

## 1. Kapsam ve Karar İlkeleri

- Her değişiklik, açık bir problem tanımı, kapsam ve doğrulanabilir kabul kriteriyle ilişkilendirilmelidir.
- Çözüm, gereksinimi karşılayan en küçük yeterli karmaşıklıkta olmalıdır. Kanıtlanmamış ölçek ihtiyacı için yeni servis, çerçeve veya altyapı katmanı eklenmez.
- Mevcut kullanıcı davranışı, veri veya entegrasyon etkileniyorsa geri uyumluluk, geçiş ve geri alma yaklaşımı belirtilmelidir.
- Veri kaybı, yetki değişikliği, kesinti, yüksek maliyet veya geri döndürülemez işlem riski taşıyan çalışmalar uygulamadan önce onay gerektirir.
- Varsayımlar, açık sorular, bağımlılıklar ve kabul edilen ödünleşimler görünür biçimde kaydedilmelidir.

## 2. Kod ve Mimari

- Kod; arayüz, iş mantığı, veri erişimi ve altyapı sorumluluklarını mümkün olduğunca ayırmalıdır.
- Modül, sınıf ve fonksiyon isimleri alan dilini yansıtmalı; örtük davranış, gizli yan etki ve anlaşılmayan kısaltmalardan kaçınılmalıdır.
- Genel kullanıma açık arayüzlerin girdisi, çıktısı, hata davranışı ve sürüm etkisi açık olmalıdır.
- Tekrarlanan iş kuralları ortaklaştırılmalı; ancak yalnızca olası gelecek kullanım için erken soyutlama yapılmamalıdır.
- Yapılandırma koddan ayrılmalı; ortam bağımlı değerler ve sırlar sabit olarak gömülmemelidir.
- Hata yakalama hedefli olmalı; istisnalar sessizce yutulmamalı ve kullanıcıya güvenli, geliştiriciye tanı koyduracak kadar bağlamlı geri bildirim sağlanmalıdır.
- Kaynaklar (dosya, ağ bağlantısı, veritabanı bağlantısı) belirli bir ömre sahip olmalı ve güvenli biçimde kapatılmalıdır.

## 3. Python Uygulamaları

- Hedef çalışma zamanı Python 3.14'tür. Sürüm uyumluluğu gereksinimi varsa proje dokümantasyonunda açıkça belirtilmelidir.
- Herkese açık fonksiyon, metot ve karmaşık veri akışlarında tür ipuçları kullanılmalıdır.
- Bağımlılıklar kilitlenebilir ve tekrarlanabilir biçimde tanımlanmalı; standart kütüphane yeterliyse ek paket kullanılmamalıdır.
- Dosya, ağ ve veritabanı işlemlerinde zaman aşımı, hata durumu ve kaynak temizliği ele alınmalıdır.
- Uzun süren işlerin ana arayüz döngüsünü veya istek işleme yolunu engellemesi önlenmelidir.
- Günlük kayıtları yapılandırılmış, anlamlı ve gizli bilgi içermeyecek biçimde üretilmelidir.

## 4. Veri ve SQLite

- Varsayılan yerel kalıcı veri çözümü SQLite'tır. Veri erişimi arayüz ve iş mantığından ayrıştırılmalıdır.
- Tabloların birincil anahtarları, ilişkileri, zorunlu alanları ve veri kuralları şema düzeyinde mümkün olduğunca tanımlanmalıdır.
- Tüm değişken SQL değerleri parametreli sorgu ile bağlanmalıdır. Kullanıcı girdisi SQL metniyle birleştirilemez.
- SQLite bağlantılarında yabancı anahtar denetimi etkinleştirilmeli; çok adımlı yazma işlemleri transaction içinde yürütülmelidir.
- Şema ve veri dönüşümleri sürümlü geçişlerle uygulanmalı; ön koşul, yedekleme, doğrulama ve mümkünse geri alma adımı içermelidir.
- Kişisel veya hassas veri yalnızca gerektiği kadar saklanmalı; günlük kayıtları, test verisi ve hata çıktılarında ifşa edilmemelidir.
- Sorgu performansı gerçek kullanım desenlerine göre ölçülmeli; indeksler gerekçe ve yazma maliyeti değerlendirilerek eklenmelidir.

## 5. Güvenlik

- En az yetki ilkesi; kullanıcı, servis hesabı, API belirteci, veritabanı ve altyapı erişimlerinde uygulanmalıdır.
- Parola, token, API anahtarı, sertifika ve kişisel veri kaynak koduna, commit'e, örnek yapılandırmaya veya hata çıktısına eklenemez.
- Dış kaynaklı tüm veri güvenilmez kabul edilmeli; tür, uzunluk, biçim, yetki ve iş kuralı doğrulaması yapılmalıdır.
- Kimlik doğrulama, yetkilendirme ve kayıt sahipliği kontrolleri yalnızca arayüzde değil, işlemi gerçekleştiren katmanda uygulanmalıdır.
- Ağ çağrılarında TLS doğrulaması, zaman aşımı, hata işleme ve yalnızca güvenli/idempotent işlemlerde sınırlı tekrar deneme kullanılmalıdır.
- Dosya işlemlerinde yol aşımı, istenmeyen üzerine yazma ve izin ihlali riskleri kontrol edilmelidir.
- Güvenlik olayı veya şüphesinde önce etkiyi sınırlama, sonra kanıt toplama ve kalıcı düzeltme yaklaşımı izlenmelidir.

## 6. Arayüz ve Erişilebilirlik

- Arayüzler görev odaklı, sade, tutarlı ve Türkçe olmalıdır. Kullanıcıya dönük teknik hata ayrıntıları gösterilmez.
- Web uygulamaları farklı ekran boyutlarında; masaüstü uygulamaları ise farklı pencere/ölçekleme ayarlarında kullanılabilir olmalıdır.
- Koyu tema desteklenmeli; renkler, yüzeyler, metinler ve odak durumu yeterli kontrastla tasarlanmalıdır.
- Tüm temel akışlar klavye ile tamamlanabilmeli; odak sırası görünür ve mantıklı olmalıdır.
- Form alanlarının kalıcı etiketi, doğrulama mesajı ve hata düzeltme yolu bulunmalıdır.
- Boş, yükleniyor, başarı, hata, yetkisiz ve devre dışı durumlar tasarlanmalı ve uygulanmalıdır.
- Silme, gönderme veya mali/veri etkisi olan eylemlerde sonuç, onay ve uygun olduğunda geri alma imkânı açıkça gösterilmelidir.

## 7. Test ve Kalite Kontrolü

- Her yeni veya değişen davranış uygun test seviyesiyle doğrulanmalıdır: birim, entegrasyon, uçtan uca veya manuel kabul testi.
- Hata düzeltmelerinde, mümkün olduğunda hatayı yeniden üreten ve tekrar oluşmasını engelleyen test eklenmelidir.
- Testler bağımsız, deterministik ve gerçek sır/üretim verisinden arındırılmış olmalıdır.
- Başarı akışının yanında boş, geçersiz, sınırda, yetkisiz ve hata durumları doğrulanmalıdır.
- Test edilemeyen değişikliklerde gerekçe, alternatif doğrulama ve kalan risk teslim notunda belirtilmelidir.
- Biçimlendirme, statik analiz ve test araçları proje tanımlarında belgelenmeli; teslim öncesinde ilgili kontroller çalıştırılmalıdır.

## 8. Dağıtım ve Operasyon

- Geliştirme, test, önizleme ve üretim ortamları ayrılmalı; üretim yapılandırması ve sırları farklı ortamlara taşınmamalıdır.
- Dağıtım adımları tekrarlanabilir, izlenebilir ve geri alınabilir olmalıdır. El ile üretim değişikliği istisna olarak ele alınır ve kayda geçirilir.
- Yayın öncesi yapılandırma, veri geçişi, sağlık kontrolü, gözlemleme ve geri alma hazırlığı doğrulanmalıdır.
- Uygulama günlükleri; zaman, seviye, bileşen ve hata bağlamı içermeli, gizli bilgi içermemelidir.
- Kritik hizmetler için sağlık kontrolü, hata oranı, gecikme, kaynak kullanımı ve gerekli iş metrikleri izlenmelidir.
- Veri yedekleri düzenli doğrulanmalı; geri yükleme adımı test edilmeden yedekleme tamamlanmış sayılmamalıdır.

## 9. Dokümantasyon ve Değişiklik Yönetimi

- README veya proje dokümantasyonu; amaç, ön koşullar, yerel kurulum, yapılandırma, çalıştırma, test ve dağıtım bilgilerini içermelidir.
- Önemli mimari kararlar; bağlam, seçenekler, karar gerekçesi ve sonuçlarıyla kaydedilmelidir.
- Kullanıcıyı veya uygulayıcıyı etkileyen önemli değişiklikler `docs/CHANGELOG.md` içinde kayda geçirilmelidir.
- Commit'ler tek mantıksal değişikliği içermeli ve Türkçe, açıklayıcı bir başlık taşımalıdır.
- Kod incelemesinde kritik/yüksek riskli bulgular çözülmeden değişiklik onaylanmamalıdır.
- Dokümantasyon, davranış değişikliğiyle aynı teslimatta güncellenmelidir; tarihçeyi değil güncel gerçeği anlatmalıdır.

## 10. Teslim Öncesi Kontrol

Bir değişiklik tamamlanmadan önce aşağıdaki soruların yanıtı doğrulanmalıdır:

1. Gereksinim ve kabul kriteri karşılandı mı?
2. Veri, güvenlik, geri uyumluluk ve hata yolları değerlendirildi mi?
3. İlgili testler ve kalite kontrolleri çalıştırıldı mı?
4. Yapılandırma, dokümantasyon ve değişiklik günlüğü etkisi gözden geçirildi mi?
5. Dağıtım, izleme ve geri alma gereksinimleri varsa hazır mı?
6. Kullanıcıya veya bakım ekibine aktarılması gereken sınırlama ya da risk açıkça bildirildi mi?
