# ULKE Stack

ULKE Stack, Ülke Kitap Kırtasiye projeleri için tekrar kullanılabilir, yapay zekâ destekli geliştirme standartları, rol tanımları ve şablonlar sunan bir depo yapısıdır. Python, web, Cloudflare ve işletme araçları projelerinde tutarlı kalite, güvenlik ve teslimat alışkanlıkları oluşturmayı amaçlar.

## Nedir?

Bu depo bir uygulama ya da kütüphane değildir. Yeni projelerde kullanılacak ortak geliştirme sözleşmesidir: nasıl planlama yapılacağını, hangi kalite kontrollerinin beklendiğini ve uzman rollerin nasıl çalışacağını tanımlar.

## Özellikler

- Ortak kod, test, güvenlik ve dokümantasyon kuralları
- Uzman görevleri için uygulanabilir agent tanımları
- Özellik, hata düzeltme, refactor ve inceleme için hazır promptlar
- Python, web ve masaüstü projeleri için başlangıç şablonları
- Sürüm, değişiklik günlüğü ve yayın kontrol listeleri
- Markdown, bağlantı ve yayın doğrulaması için GitHub Actions

## Klasör Yapısı

```text
agents/       Uzman rol tanımları
docs/         Standartlar, yol haritası ve değişiklik günlüğü
prompts/      Tekrarlanan geliştirme işleri için istemler
templates/    Proje ve süreç şablonları
.github/      GitHub Actions, issue şablonları ve Dependabot ayarları
CLAUDE.md     İnsan ve yapay zekâ destekli geliştirme kuralları
```

## Hızlı Başlangıç

1. Depoyu klonlayın ve hedef projenizin türüne uygun şablonu `templates/` altında inceleyin.
2. Proje köküne `CLAUDE.md` kurallarını ve gerekli şablonları uyarlayın.
3. Yeni işi `prompts/new-feature.md` veya uygun süreç şablonuyla tanımlayın.
4. İlgili agent rolünü kullanarak geliştirmeyi, testleri ve incelemeyi tamamlayın.
5. Yayından önce `templates/release-checklist.md` listesini uygulayın ve `docs/CHANGELOG.md` dosyasını güncelleyin.

## Kurulum

ULKE Stack için paket kurulumu gerekmez. Bu depoyu referans olarak kullanabilir veya içerikleri yeni projenize kopyalayabilirsiniz.

```bash
git clone https://github.com/ulkekirtasiye/ulke-stack.git
cd ulke-stack
```

Şablonların her biri, hedef projede gereken bağımlılıkları ve başlangıç adımlarını kendi içinde açıklar.

## Agent Sistemi

`agents/` klasöründeki her dosya, uzman bir rolün çalışma sınırlarını belirler. Roller; sorumluluk alanı, çalışma biçimi, kalite kontrolleri ve teslim biçimini içerir.

Başlangıç için Python geliştirme işlerinde `agents/python.md` dosyasını kullanın. Mimari kararlar, test, güvenlik, DevOps ve diğer uzmanlık alanları için uygun rol dosyasına başvurun. Agent'lar, `CLAUDE.md` içindeki ortak kuralları tamamlar; onun yerine geçmez.

## Prompt Sistemi

`prompts/` klasörü, işi net ve incelenebilir girdilerle başlatmak için tasarlanmıştır:

- `new-feature.md`: Yeni yetenekler ve kabul kriterleri
- `bug-fix.md`: Hatanın tekrarı, kök neden ve regresyon testi
- `refactor.md`: Davranışı koruyan yapısal iyileştirmeler
- `code-review.md`: Risk, kalite ve güvenlik odaklı inceleme

## Workflow'lar

GitHub Actions, ana dala yapılan gönderimleri ve pull request'leri aşağıdaki kontrollerle doğrular:

- **Markdown Lint:** Markdown biçim kurallarını denetler.
- **Link Checker:** Markdown dosyalarındaki bağlantıları denetler.
- **Release Validation:** `v*` etiketi ya da elle çalıştırma ile yayın için gerekli dosya ve klasörleri doğrular.
- **Dependabot:** GitHub Actions bağımlılıklarını haftalık olarak günceller.

Workflow sonuçları GitHub deposunun Actions sekmesinden izlenmelidir. Yayın doğrulaması yalnızca etiket veya elle tetikleme ile çalıştığından, bir sürüm kesmeden önce ayrıca başlatılmalıdır.

## Proje Şablonları

`templates/` altında özellik tanımı, hata bildirimi, mimari karar kaydı, test planı, yayın kontrol listesi ve proje başlangıç şablonları bulunur. Şablonlar gereksinim, risk, kabul kriteri, test kanıtı ve geri alma bilgisini aynı formatta toplamayı hedefler.

## Roadmap

Yol haritası [docs/ROADMAP.md](docs/ROADMAP.md) dosyasında yer alır. Öncelik sırası; veri güvenliği, mevcut projelere etkisi, tekrar eden işlerin standardizasyonu ve ölçülebilir kalite kazanımıdır. Stack, önce gerçek projelerde doğrulanacak; ardından gözlenen eksikler kalıcı iyileştirmelere dönüştürülecektir.

## Lisans

Bu proje [MIT License](LICENSE) ile lisanslanmıştır.
