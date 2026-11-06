# Kova

Su aktarma bulmacası. Tek dosyalık, bağımlılıksız bir web prototipi (`index.html`).

## Dünyalar
- **Su:** klasik ölçme bulmacaları. İlk 5 seviye öğretici, 6. seviyeden itibaren hamle limiti, 9. seviyeden itibaren "Bu imkânsız" butonu. 14. seviyeden sonrası sonsuz ve otomatik üretiliyor (seviye numarası sabit tohum, herkeste aynı bulmaca).
- **Su ve yağ:** yağ suyun üstünde durur, dökerken önce üstteki katman akar. 10 seviye, 15 yıldızla açılır.
- **Taş:** taş yer kaplar, dolu kovada suyu taşırır. 5 seviye, 25 yıldızla açılır.
- **Tasarruf (sürdürülebilirlik serisi):** lavabo yok, depo sınırlı, musluk kovayı sadece tamamen doldurur. 8 seviye, 35 yıldızla açılır.

## Ekonomi
- Yıldızlar hem ilerleme hem para birimi. Bir seviyede sadece önceki en iyi sonuca göre fark kazanılır.
- İpucu: günde 3 ücretsiz, sonrası 2 ★.
- Hamle limiti dolunca: +5 hamle (3 ★), baştan başla ya da "Bu imkânsız".
- Ölçülü döküm jokeri: tam 1 L aktarım, 5 ★, seviye başına tek kullanım, en fazla 1 yıldız.
- İmkânsız seviyede ek hamleye harcanan yıldızlar doğru tespitte iade edilir.
- Mağaza (prototip, gerçek ödeme yok): ödüllü reklam, yıldız paketleri, kalıcı Usta paketi.

## Çalıştırma
`index.html` dosyasını tarayıcıda açmak yeterli. İlerleme tarayıcının `localStorage`'ında tutulur.

## Test kısayolları
`#seviye-21`, `#yag-6`, `#tas-1`, `#tasarruf-1` gibi adres sonekleri doğrudan o seviyeyi açar (yayın öncesi kaldırılmalı).

## Çözücü
Her seviyenin en kısa çözümü tarayıcıda BFS ile hesaplanır; yıldızlar, ipuçları, imkânsızlık tespiti ve seviye üretici bu çözücüye dayanır.
