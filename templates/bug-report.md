# Hata Raporu Şablonu

Bu şablon, bir hatanın geliştirici veya test ekibi tarafından güvenli biçimde yeniden üretilmesini, önceliklendirilmesini ve doğrulanmasını sağlamak için kullanılır. Köşeli parantez içindeki alanları doldurun. Parola, token, kişisel veri, müşteri kaydı veya üretim sırrı eklemeyin.

## 1. Özet

- **Başlık:** [Kısa, somut ve kullanıcı etkisini anlatan başlık]
- **Durum:** [Yeni / İnceleniyor / Planlandı / Düzeltiliyor / Doğrulanıyor / Kapatıldı]
- **Raporlayan:** [Ad veya rol]
- **Tarih:** [YYYY-AA-GG]
- **İlgili iş/özellik:** [Bağlantı veya kimlik]
- **Öncelik:** [Kritik / Yüksek / Orta / Düşük]
- **Etiketler:** [Bileşen, alan, tür veya ortam etiketi]

## 2. Etki Değerlendirmesi

- **Etkilenen kullanıcılar:** [Kimler, ne kadar yaygın?]
- **İş etkisi:** [İşlem engeli, yanlış sonuç, destek yükü, gelir veya itibar etkisi]
- **Veri etkisi:** [Yok / Okuma / Yanlış yazma / Veri kaybı riski — ayrıntı]
- **Güvenlik veya gizlilik etkisi:** [Yok / Şüphe / Var — güvenli özet]
- **Geçici çözüm:** [Varsa kullanıcı veya destek ekibinin uygulayabileceği güvenli yol]

## 3. Ortam Bilgisi

| Alan | Değer |
| --- | --- |
| Ortam | [Geliştirme / Test / Önizleme / Üretim] |
| Uygulama sürümü/commit | [Sürüm veya kısa commit kimliği] |
| Tarih ve saat | [YYYY-AA-GG SS:DD, zaman dilimi] |
| Kullanıcı rolü | [Rol; kullanıcı kimliği paylaşmayın] |
| İşletim sistemi/tarayıcı | [Sürüm bilgisi] |
| Cihaz/ekran | [Gerekliyse tür ve çözünürlük] |
| Ağ veya dış servis durumu | [Gerekliyse açıklama] |

## 4. Yeniden Üretim

### Ön Koşullar

- [Gerekli yetki, test verisi, yapılandırma veya başlangıç durumu]
- [İkinci ön koşul]

### Adımlar

1. [Başlangıç adımı]
2. [Kullanıcı eylemi]
3. [Kullanıcı eylemi veya sistem koşulu]
4. [Hatanın gözlemlendiği adım]

### Beklenen Davranış

[Sistemin yapması gereken davranışı açık ve ölçülebilir biçimde yazın.]

### Gerçekleşen Davranış

[Görülen sonucu, hata mesajını veya yanlış çıktıyı yazın.]

### Tekrarlanabilirlik

- **Durum:** [Her zaman / Aralıklı / Bir kez görüldü / Yeniden üretilemedi]
- **Sıklık:** [Örn. 5 denemenin 3'ünde]
- **Tetikleyen koşullar:** [Zaman, veri, yetki, ağ, eşzamanlılık veya dış servis koşulu]

## 5. Kanıtlar

- **Ekran görüntüsü/video:** [Güvenli bağlantı veya ek — kişisel verileri maskeleyin]
- **Hata mesajı:** [Gizli bilgi içermeyen tam metin]
- **Günlük/iz kaydı:** [İstek veya işlem kimliği; token ve kişisel veri olmadan]
- **İlgili veri örneği:** [Anonimleştirilmiş/sentetik örnek]
- **Ek bağlam:** [Son değişiklik, zaman çizelgesi veya dış servis olayı]

## 6. İlk Değerlendirme

- **Etkilenen bileşenler:** [Ekran, modül, API, veritabanı veya entegrasyon]
- **Şüphelenilen neden:** [Varsa; kanıtlanmadığını açıkça belirtin]
- **Son değişiklikle ilişkisi:** [Bilinmiyor / Var — bağlantı veya açıklama]
- **Geri uyumluluk riski:** [Varsa açıklama]
- **Önerilen sonraki adım:** [Yeniden üretim, günlük inceleme, test, geri alma vb.]

## 7. Çözüm ve Doğrulama

Bu bölüm, hata çözüldüğünde sorumlu kişi tarafından doldurulur.

- **Kök neden:** [Kanıtlanmış teknik veya iş kuralı nedeni]
- **Düzeltme özeti:** [Değişen davranış ve ilgili dosya/iş kaydı]
- **Regresyon testi:** [Eklenen/güncellenen test ve senaryo]
- **Doğrulama adımları:** [Yeniden üretim adımlarının sonuçları]
- **Yayın/sürüm:** [Sürüm, tarih ve ortam]
- **Kalan risk veya takip:** [Varsa]

## 8. Kapanış Kontrolü

- [ ] Hata güvenli test verisiyle yeniden üretildi veya neden üretilemediği kaydedildi.
- [ ] Beklenen ve gerçekleşen davranış açıkça tanımlandı.
- [ ] Etki ve öncelik değerlendirildi.
- [ ] Kök neden veya geçici önlem belgelendi.
- [ ] Regresyon testi veya eşdeğer doğrulama tamamlandı.
- [ ] Yayın sonrası doğrulama ve kullanıcı etkisi kontrol edildi.
- [ ] Hassas bilgi bulunmadığı doğrulandı.
