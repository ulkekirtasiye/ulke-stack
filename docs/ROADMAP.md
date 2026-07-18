# ULKE STACK Yol Haritası

Bu yol haritası, ULKE STACK'in Ülke Kitap Kırtasiye projelerinde kullanılacak güvenilir, tekrar kullanılabilir ve üretim odaklı bir AI geliştirme standardı haline gelmesi için planlanan çalışmaları tanımlar. Tarihler yerine bağımlılık ve hazır olma ölçütleri kullanılır; öncelikler iş ihtiyacı, risk ve geri bildirime göre güncellenir.

## Vizyon

Farklı proje türlerinde tutarlı kalite sağlayan; gereksinim toplama, tasarım, geliştirme, test, dağıtım ve bakım süreçlerini açık kurallarla destekleyen bir çalışma çerçevesi oluşturmak.

## Başarı Ölçütleri

- Yeni bir proje, ilgili şablon ve kurallar kullanılarak tekrar edilebilir biçimde başlatılabilir.
- Uzman rol tanımları gerçek görevlerde net sorumluluk, doğrulama adımı ve teslim biçimi sağlar.
- Yeni özellik, hata düzeltme, refactor ve inceleme süreçleri için uygulanabilir istemler bulunur.
- Kalite, güvenlik, veri bütünlüğü ve operasyon riskleri proje yaşam döngüsünün erken aşamalarında ele alınır.
- Dokümantasyon güncel, kısa ve kullanıcıların karar vermesine yardımcı olacak niteliktedir.

## Aşama 1 — Temel Standartların Oluşturulması

**Amaç:** Tüm projelerde geçerli ortak kuralları ve uzmanlık alanlarını tanımlamak.

Kapsam:

- Ana geliştirme ilkelerini `CLAUDE.md` içinde netleştirmek.
- Mimari, Python, veritabanı, tasarım, test, DevOps, Cloudflare, SEO, inceleme ve proje yönetimi uzman rollerini tamamlamak.
- Kod kalitesi, güvenlik, erişilebilirlik, test ve Git beklentilerini ortak bir dilde toplamak.

Tamamlanma ölçütleri:

- Her rolün sorumluluk alanı, çalışma akışı, kontrol noktaları ve teslim biçimi tanımlıdır.
- Roller arasında çelişen veya tekrarlayan kurallar ayıklanmıştır.
- Üretim ortamını etkileyen işlemler için onay, doğrulama ve geri alma beklentisi belirtilmiştir.

## Aşama 2 — Süreç ve Dokümantasyon Şablonları

**Amaç:** Sık yapılan geliştirme işlerini tutarlı girdiler ve çıktılarla yürütmek.

Kapsam:

- Yeni özellik, hata düzeltme, refactor ve kod inceleme istemlerini hazırlamak.
- Standartlar, değişiklik günlüğü, issue ve pull request şablonlarını tanımlamak.
- Gereksinim, kabul kriteri, risk, test kanıtı ve geri alma notu için ortak alanlar belirlemek.

Tamamlanma ölçütleri:

- Her şablon kendi amacına uygun, kısa ve uygulanabilir yönergeler içerir.
- Şablonlar iş, teknik, test ve operasyonel bilgileri birbirinden ayırır.
- Yeni bir iş maddesi veya değişiklik, ek açıklamaya ihtiyaç duymadan incelemeye hazırlanabilir.

## Aşama 3 — Proje Başlatma Şablonları

**Amaç:** Python, web ve masaüstü projeleri için güvenli başlangıç noktaları sunmak.

Kapsam:

- Python otomasyon, web uygulaması ve CustomTkinter masaüstü projesi şablonlarını hazırlamak.
- Klasör yapısı, yapılandırma, bağımlılık, test, kalite araçları ve dokümantasyon başlangıçlarını tanımlamak.
- SQLite, ortam değişkeni, gizli bilgi yönetimi ve dağıtım notları için varsayılanları belirlemek.

Tamamlanma ölçütleri:

- Her şablon tek komut veya açık adımlarla yerel geliştirme ortamında çalıştırılabilir.
- Temel kalite kontrolleri ve örnek testler çalışır durumdadır.
- Şablonlar örnek sır veya üretim verisi içermez; güvenli varsayılanlarla gelir.

## Aşama 4 — Uygulama ve Geri Bildirim Döngüsü

**Amaç:** Standartları gerçek projelerde doğrulamak ve gereksiz karmaşıklığı azaltmak.

Kapsam:

- Her proje kullanımında eksik, belirsiz veya çakışan kuralları kaydetmek.
- Şablonların başlatma süresi, bakım maliyeti ve kalite etkisine dair geri bildirim toplamak.
- Tekrarlanan hataları ilgili rol, istem veya şablonda kalıcı iyileştirmeye dönüştürmek.

Tamamlanma ölçütleri:

- Geri bildirimler somut örnek, etki ve öneriyle kayıt altındadır.
- Değişiklikler gerekçeli, gözden geçirilmiş ve `CHANGELOG.md` içinde izlenebilir durumdadır.
- Kullanılmayan veya değer üretmeyen içerik kaldırılmak üzere işaretlenmiştir.

## Aşama 5 — Operasyonel Olgunluk

**Amaç:** Stack'in uzun vadeli bakımını, sürümleme disiplinini ve güvenilir kullanımını sağlamak.

Kapsam:

- Sürümleme, değişiklik günlüğü, sahiplik ve periyodik gözden geçirme sürecini işletmek.
- Güvenlik, bağımlılık, yedekleme ve erişim uygulamalarını düzenli olarak değerlendirmek.
- Kritik şablon ve süreçlerin güncelliğini gerçek proje ihtiyaçlarına göre doğrulamak.

Tamamlanma ölçütleri:

- Önemli değişiklikler kullanıcı etkisi ve geçiş notlarıyla yayımlanır.
- Dokümantasyonun sorumlusu, gözden geçirme aralığı ve güncelleme tetikleyicileri tanımlıdır.
- Kritik süreçlerde geri alma veya güvenli varsayılan yaklaşımı belgelenmiştir.

## Önceliklendirme İlkeleri

Yol haritasındaki işler aşağıdaki sırayla değerlendirilir:

1. Veri güvenliği, kullanıcı etkisi ve operasyonel risk azaltma.
2. Mevcut projelerin teslimatını veya bakımını doğrudan kolaylaştıran iyileştirmeler.
3. Tekrarlanan işleri standartlaştıran şablonlar ve otomasyonlar.
4. Ölçülebilir kalite veya performans kazanımı sağlayan geliştirmeler.
5. Kanıtlanmış ihtiyaç olmadan önerilen deneysel veya geniş kapsamlı çalışmalar.

## Yol Haritası Güncelleme Kuralları

- Her yeni madde; problem, beklenen değer, kapsam, bağımlılık, risk ve tamamlanma ölçütü içermelidir.
- Tamamlanan işler `docs/CHANGELOG.md` içinde kullanıcı/ekip etkisiyle birlikte kaydedilir.
- Tarih taahhüdü yalnızca kapasite, bağımlılık ve kabul kriterleri doğrulandıktan sonra verilir.
- Kapsam veya öncelik değiştiğinde, ertelenen iş ve gerekçesi görünür biçimde güncellenir.
- Bu dosya bir görev listesi değildir; ayrıntılı işler proje takip sisteminde tutulur.
