# data/

Web sitesi (`docs/`) ve uygulama (`app/`) tarafından ortak kullanılacak yapılandırılmış yama verisi için ayrıldı.

Önerilen yapı:

```
data/
└── patches/
    └── 7.42.json   # hero, item, neutral item, mekanik değişiklikleri
```

Şu an 7.42 verisi `docs/patches/7.42/` sayfalarının içinde gömülü duruyor. Uygulama geliştirmeye başlandığında bu veri buraya JSON olarak taşınabilir ve sayfalar da buradan okuyacak şekilde düzenlenebilir.
