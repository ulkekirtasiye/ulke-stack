# Refactor İstemi

Bu şablonu, dışarıdan görünen davranışı koruyarak kodun okunabilirliğini, test edilebilirliğini, bakımını veya yapısını iyileştirmek için kullanın. Köşeli parantez içindeki alanları proje bağlamına göre doldurun. Refactor, yeni özellik geliştirme veya gizli davranış değişikliği değildir; gerekli davranış değişikliklerini ayrı iş maddesi olarak tanımlayın.

## İstem Şablonu

```text
Mevcut projede aşağıdaki alanı, davranışı koruyarak refactor et.

## Refactor Özeti

- Başlık: [Kısa ve amaç odaklı başlık]
- Problem: [Mevcut kodun bakım, test, karmaşıklık, performans veya güvenlik sorunu]
- Hedef: [İyileştirilmek istenen ölçülebilir sonuç]
- Kapsam: [Modüller, sınıflar, fonksiyonlar veya akışlar]
- Kapsam dışı: [Bu çalışmada değişmeyecek davranışlar/alanlar]
- Mevcut davranış sözleşmesi: [Korunması gereken kullanıcı, API, veri veya entegrasyon davranışı]

## Mevcut Bağlam

- İlgili dosyalar/bileşenler: [Liste]
- Bağımlılıklar ve çağıranlar: [Biliniyorsa liste]
- Mevcut testler: [İlgili testler veya test boşlukları]
- Teknik kısıtlar: [Geri uyumluluk, performans, veri, yayın veya sürüm kısıtları]
- Başarı göstergesi: [Örn. daha küçük sorumluluklar, test kapsamı, tekrarın azalması]

## Beklenen Çalışma Biçimi

1. `CLAUDE.md`, proje standartları, ilgili kod ve testleri incele.
2. Mevcut davranışı, veri akışını, dış sözleşmeleri ve yan etkileri belgeleyerek başlangıç noktası oluştur.
3. Refactor gerekçesini, hedef mimariyi, etkilenen dosyaları ve geri uyumluluk risklerini kısa biçimde açıkla.
4. Davranış değişikliği, şema geçişi, API değişikliği veya kullanıcı akışı etkisi varsa bunu refactor kapsamından ayır; gerekli onayı iste.
5. Küçük, bağımsız ve geri alınabilir adımlardan oluşan plan hazırla. Her adımda korunacak davranışı belirt.
6. Önce güvenlik ağını güçlendir: eksik kritik testleri ekle veya mevcut doğrulama yöntemini açıkça tanımla.
7. Refactor'u gereksiz bağımlılık, geniş dosya taşınması veya ilgisiz biçimlendirme yapmadan uygula.
8. Her önemli adımdan sonra ilgili testleri çalıştır; son aşamada tam kalite kontrolünü uygula.
9. Aşağıdaki teslim formatıyla değişiklik, doğrulama ve kalan riski raporla.

## Korunacak Davranışlar

- [Kullanıcı akışı veya arayüz davranışı]
- [API, komut satırı veya entegrasyon sözleşmesi]
- [Veri şeması, veri biçimi veya sıralama garantisi]
- [Performans, hata mesajı veya yetki davranışı]

## Refactor Kabul Kriterleri

- Dışarıdan gözlemlenen davranış ve belirtilen sözleşmeler korunur.
- Kodun hedeflenen bakım sorunu somut biçimde iyileşir.
- Kritik iş kuralları ve hata yolları test veya eşdeğer doğrulamayla korunur.
- Yeni güvenlik, veri bütünlüğü, performans veya geri uyumluluk riski oluşmaz.
- Değişiklik kapsamı açıklanan sınırı aşmaz; ilgisiz dosyalar değiştirilmez.

## Risk ve Geri Alma Notları

- Veri etkisi: [Yok / Okuma / Yazma / Geçiş — ayrıntı]
- Dış sözleşme etkisi: [Yok / Var — sürümleme veya geçiş notu]
- Yayın riski: [Düşük / Orta / Yüksek — gerekçe]
- Geri alma yaklaşımı: [Commit geri alma, özellik bayrağı, şema geri dönüşü vb.]

## Teslim Formatı

Çalışma sonunda şu başlıklarla kısa ve somut bir özet ver:

1. Gerekçe ve kapsam: Hangi bakım sorununu neden ele aldın?
2. Yapısal değişiklik: Değişen dosyalar, bileşen sınırları ve korunan sözleşmeler.
3. Doğrulama: Çalıştırılan test/kalite kontrolleri ve sonuçları.
4. Davranış değerlendirmesi: Korunan davranışlar ve gözlemlenen farklar.
5. Riskler ve geri alma: Kalan risk, ertelenen iş veya gerekli yayın adımı.
```

## Kullanım Notları

- Kod kokusunu netleştirin: aşırı sorumluluk, tekrar, sıkı bağımlılık, test edilememe veya karmaşık kontrol akışı gibi somut bir neden yazın.
- Test eksikse, geniş refactor öncesinde güvenlik ağı oluşturacak küçük bir test çalışması planlayın.
- Performans refactor'unda başarıyı varsayımla değil, karşılaştırılabilir ölçümle doğrulayın.
- Birden çok bağımsız alanı aynı refactor içinde birleştirmeyin; incelemesi ve geri alınması kolay küçük değişiklikleri tercih edin.
- İsim veya dosya yolu değişikliklerinin dış tüketicileri etkileyip etkilemediğini araştırın; uyumsuz değişiklik gerekiyorsa geçiş notu ekleyin.
