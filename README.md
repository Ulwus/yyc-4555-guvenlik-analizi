# YYC 4555 · Safety 4.0 Güvenlik ve Emniyet Analizi

**Yazıcı Makina — YYC 4555 Tam Otomatik Shrink Ambalaj Makinesi**

| Hazırlayan | Öğrenci Numarası | Grup |
| --- | --- | --- |
| Oğuzhan Gündüz | 230541054 | Gündüz 4B |

## Makine ve Projenin Amacı

YYC 4555, ürünleri gruplandırır, PE filmle sarar ve ısı tünelinde ambalajlar. Bu çalışma, uzaktan bakım ve yazılım değişikliklerinin hareket, sıcaklık ve bakım sırasında insan emniyeti üzerindeki etkisini inceler.

> Güvenli bağlantı, güvenli işlem demek değildir. İmzası doğru bir yedek yanlış fiziksel ekseni tarif edebilir; kapanan bakım oturumunun işi yedekte yaşayabilir; yazılım soğuk duruma dönerken metal sıcak kalabilir.

## Teslim Belgeleri (Ana Dizin)

Tüm PDF belgeleri doğrudan deponun ana dizinindedir:

| Belge | Açıklama | Dosya Yolu |
| --- | --- | --- |
| **Makine Anlatımı** | Makinenin görevi, 4 çalışma aşaması ve temel üretici verileri (1 sayfa) | [Makine-Anlatimi.pdf](./Makine-Anlatimi.pdf) |
| **Laboratuvar 1** | Safety Architecture: tehlikeler, emniyet fonksiyonları ve bağımsızlık (1 sayfa) | [Laboratuvar1.pdf](./Laboratuvar1.pdf) |
| **Laboratuvar 2** | IEC 62443 Mini Workshop: bölgeler, veri geçişleri ve erişim kararları (1 sayfa) | [Laboratuvar2.pdf](./Laboratuvar2.pdf) |
| **Laboratuvar 3** | Threat & Risk Matrix: koşullu senaryolar ve risk puanlaması (1 sayfa) | [Laboratuvar3.pdf](./Laboratuvar3.pdf) |
| **Laboratuvar 4** | Secure Remote Access: mevcut senaryo, hedef kontroller ve emniyet köprüsü (1 sayfa) | [Laboratuvar4.pdf](./Laboratuvar4.pdf) |
| **SWOT Analizi** | 24 SWOT maddesi, 6 olay, 8 TOWS stratejisi ve 10 doğrulama kriteri (15 sayfa) | [YYC-4555-SWOT-Analizi.pdf](./YYC-4555-SWOT-Analizi.pdf) |

## Depo Yapısı

```text
.
├── Laboratuvar1.pdf
├── Laboratuvar2.pdf
├── Laboratuvar3.pdf
├── Laboratuvar4.pdf
├── Makine-Anlatimi.pdf
├── README.md
└── YYC-4555-SWOT-Analizi.pdf
```

## Analitik Çerçeve ve Üç Temel Soru

1. **Oturum bittiğinde iş de bitiyor mu?** İptal öncesi yedek devralırsa, kapanmış bakım oturumundan kalan hareket işi yeniden yürütülebilir mi? (`S1` / `C1`)
2. **İmzası doğru dosya doğru fiziksel ekseni mi tarif ediyor?** Bakımda değişen servo eşlemesine eski revizyonun imzalı yedeği yüklenirse, duran motor yanlış mekanizmaya ait sanılabilir mi? (`S2` / `C2`)
3. **Yazılım geçmişe döndüğünde metal soğuyor mu?** Sıcak makinede soğuk duruma ait disk görüntüsü geri yüklendiğinde, sıfırlanan ölçüm yaşı nedeniyle erken erişim izni verilebilir mi? (`S3` / `C3`)

## Kapsam ve Sınırlar

- Üretici beyanları (PLC kontrol, LCD dokunmatik ekran, iki servo, PE film overlap sarma ve ısı tüneli), senaryo varsayımları (SSH bakım erişimi, ana/yedek geçit, iş kuyruğu, imzalı yedek) ve hedef emniyet gereksinimleri birbirinden ayrılmıştır.
- Senaryolar siber-fiziksel bağımlılık analizi kapsamındadır; üreticide bulunmuş güvenlik açığı iddiası veya CE/PL/SIL uygunluk belgesi değildir.

## Kaynaklar

- [Yazıcı Makina — YYC 4555 Ürün Sayfası](https://www.yazicimakina.com.tr/urun/yyc-4555)
- [Yazıcı Makina — Ürün Kataloğu (s. 18–19)](https://www.yazicimakina.com.tr/assets/uploads/8055409397929-986-yazici%20katalog%20144%20dpi%202%20SAYFALI-s%C4%B1k%C4%B1%C5%9Ft%C4%B1r%C4%B1ld%C4%B1.pdf)
- [NIST SP 800-82 Rev. 3 — Guide to Operational Technology Security](https://csrc.nist.gov/pubs/sp/800/82/r3/final)
- [ACSC — Industrial Control Systems: Remote Access Protocol](https://www.cyber.gov.au/publication/industrial-control-systems-remote-access-protocol)
