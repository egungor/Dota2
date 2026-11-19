# Dota 2

Görsel Dota 2 yama özetleri (web) ve ileride geliştirilecek uygulama için repo.

## Dizin yapısı

```
.
├── docs/                    # Statik web sitesi (GitHub Pages kökü)
│   ├── index.html           # Ana sayfa: yama listesi
│   ├── .nojekyll            # GitHub Pages dosyaları Jekyll'den geçirmeden yayınlasın
│   ├── assets/
│   │   └── img/             # Ortak görseller (logo vb.)
│   └── patches/
│       └── 7.42/
│           ├── index.html   # İngilizce (varsayılan)
│           └── tr.html      # Türkçe
├── data/                    # Web ve uygulamanın ortak kullanacağı yapılandırılmış veri (ileride)
└── app/                     # İleride geliştirilecek uygulama
```

- **`docs/`** sadece yayınlanan statik dosyaları içerir. Derleme adımı yoktur.
- **`data/`** yama verisini (hero, item, neutral değişiklikleri) JSON olarak tutmak için ayrıldı. Böylece web sayfaları ve uygulama aynı veriyi kullanabilir.
- **`app/`** uygulamanın kendi kaynak kodu, bağımlılıkları ve derleme ayarları buraya girer. Web sitesinden bağımsızdır.

## Yayınlama (GitHub Pages)

Settings → Pages → Build and deployment:

- **Source:** Deploy from a branch
- **Branch:** `main` / **Folder:** `/docs`

Site adresi: `https://egungor.github.io/Dota2/`

Tüm bağlantılar göreli (`./`, `../../`) olduğu için site alt dizinde ve özel alan adında aynı şekilde çalışır.

## Yeni yama ekleme

1. `docs/patches/<sürüm>/` klasörü aç (ör. `docs/patches/7.43/`).
2. `index.html` (İngilizce) ve `tr.html` (Türkçe) dosyalarını ekle. 7.42 sayfaları şablon olarak kullanılabilir.
3. `docs/index.html` içindeki yama listesinin en üstüne yeni bir kart ekle.

## Notlar

- Hero bağlantıları dota2.com hero sayfalarına, item bağlantıları Liquipedia'ya gider.
- Resmi hero/item ikonları sayfa açılırken Valve'ın sunucusundan yüklenir; yüklenemezse yerine kısaltma rozeti gösterilir.
- Gayriresmi bir hayran projesidir. Dota 2, Valve Corporation'ın ticari markasıdır.
