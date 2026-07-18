# Kod İnceleme İstemi

Bu şablonu, bir değişikliği birleştirme veya yayımlama öncesinde risk odaklı incelemek için kullanın. Köşeli parantez içindeki alanları doldurun. İnceleme, kişisel stil tercihlerinden önce kullanıcı etkisi, veri bütünlüğü, güvenlik ve geri uyumluluğa odaklanmalıdır.

## İstem Şablonu

```text
Aşağıdaki değişikliği üretim kalitesi açısından incele. Kod değiştirme; yalnızca bulguları ve inceleme kararını raporla.

## Değişiklik Bağlamı

- Başlık: [Değişikliğin kısa adı]
- Amaç: [Hangi problemi çözüyor, hangi kullanıcı/iş değeri hedefleniyor?]
- Kapsam: [Değişen dosyalar, bileşenler, API'ler, ekranlar veya veri alanları]
- Kapsam dışı: [Bu incelemede ele alınmayacak alanlar]
- İlgili gereksinimler/kabul kriterleri: [Liste veya bağlantı]
- Risk seviyesi: [Düşük / Orta / Yüksek — gerekçe]

## Doğrulama Kanıtı

- Çalıştırılan testler ve sonuçları: [Liste]
- Manuel doğrulama: [Varsa senaryolar]
- Veri, yapılandırma veya dağıtım etkisi: [Varsa açıklama]
- Bilinen sınırlamalar veya takip maddeleri: [Varsa açıklama]

## Beklenen İnceleme Biçimi

1. Önce `CLAUDE.md`, proje standartları, değişikliğin amacı ve kabul kriterlerini incele.
2. Değişikliğin gerçek kapsamını; çağıranlar, tüketiciler, veri akışları ve dış bağımlılıklarıyla birlikte değerlendir.
3. Öncelikle kritik riskleri araştır: veri kaybı, yetkisiz erişim, gizli bilgi sızıntısı, kesinti, geri uyumsuzluk ve yanlış iş davranışı.
4. Ardından hata yolları, sınır değerler, eşzamanlılık, performans, erişilebilirlik, test kapsamı ve operasyonel etkileri kontrol et.
5. Yalnızca kanıtlanabilir bulguları raporla. Kişisel tercih, isimlendirme veya stil önerilerini engelleyici bulgulardan ayır.
6. Bulgu yoksa bunu açıkça belirt; test edilmemiş veya belirsiz alanları yine de görünür kıl.
7. İncelemeyi aşağıdaki teslim formatıyla, net bir sonuç kararı vererek tamamla.

## İnceleme Kontrol Alanları

- İş davranışı: Kabul kriterleri, başarı/hata akışları, boş/geçersiz/sınır girdiler ve mevcut kullanıcı davranışı.
- Veri: Doğrulama, transaction, şema etkisi, geri alma, eşzamanlılık ve kişisel veri korunması.
- Güvenlik: Kimlik doğrulama, yetkilendirme, sahiplik, giriş doğrulama, sır yönetimi ve günlük kayıtları.
- Mimari: Sorumluluk ayrımı, bağımlılık yönü, dış sözleşme, yapılandırma ve gereksiz karmaşıklık.
- Performans: Sorgu/ağ/dosya maliyeti, kaynak yönetimi, zaman aşımı ve ölçeklenme etkisi.
- Arayüz: Erişilebilirlik, klavye odağı, durum geri bildirimi, responsive davranış ve kullanıcıya gösterilen hata metinleri.
- Test/operasyon: Test kapsamı, regresyon riski, dağıtım, gözlemlenebilirlik, yapılandırma ve geri alma hazırlığı.

## Bulgu Öncelikleri

- Kritik: Veri kaybı, yetkisiz erişim, sır sızıntısı, kalıcı kesinti veya ciddi güvenlik açığı.
- Yüksek: Yaygın hatalı davranış, veri bütünlüğü riski, geri uyumsuzluk veya önemli performans sorunu.
- Orta: Belirli koşullarda hataya yol açan eksik doğrulama, test boşluğu veya bakım/operasyon riski.
- Düşük: İşlevi doğrudan bozmayan tutarlılık, okunabilirlik veya iyileştirme önerisi.

Kritik veya yüksek öncelikli bulgu varsa değişikliği onaylama. Orta/düşük bulgular için kullanıcı etkisini ve takip gereksinimini açıkça belirt.

## Bulgu Yazım Biçimi

Her bulguda şu alanları kullan:

- **[Öncelik] Başlık**
- **Konum:** [Dosya, satır, fonksiyon veya davranış alanı]
- **Kanıt:** [Hangi koşulda ne olur ve neden sorun?]
- **Etki:** [Kullanıcı, veri, güvenlik veya operasyon sonucu]
- **Öneri:** [Çözüm yönü, test veya doğrulama adımı]

## Teslim Formatı

İncelemeyi aşağıdaki sırayla sun:

1. İnceleme kapsamı ve kullanılan kanıtlar.
2. Öncelik sırasına göre bulgular. Bulgu yoksa: “Engelleyici bulgu tespit edilmedi.”
3. Test, veri, güvenlik veya operasyon alanındaki açık doğrulama boşlukları.
4. İnceleme sonucu:
   - **Onay:** Engelleyici bulgu yok.
   - **Düzeltme gerekli:** Kritik veya yüksek öncelikli bulgular çözülmeli.
   - **Ek bilgi gerekli:** Kabul kriteri, davranış veya doğrulama kanıtı yeterli değil.
5. Varsa yayın öncesi gerekli takip adımları.
```

## Kullanım Notları

- İncelenecek fark, commit aralığı veya pull request bağlantısı varsa bağlama ekleyin; inceleme kapsamını tahmine bırakmayın.
- Değişiklik veri şeması, dış API veya yapılandırma içeriyorsa ilgili geçiş ve geri alma planını zorunlu kanıt olarak isteyin.
- Büyük farklarda önce kritik veri/güvenlik yollarını, ardından değişen davranışları inceleyin; tüm dosyaları eşit ayrıntıyla okumaya çalışmayın.
- İnceleme önerilerini somut tutun. “Test ekleyin” yerine hangi senaryonun, neden eksik olduğunu belirtin.
- Kod değişikliği talebiyle inceleme talebini birleştirmeyin; düzeltmeler ayrı çalışma olarak planlanmalıdır.
