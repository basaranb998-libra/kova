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
- Hamle limiti dolunca: baştan başla ya da "Bu imkânsız". 14. seviyeden (üretilen bulmacaların başından) itibaren ayrıca +5 hamle (3 ★) satın alınabilir.
- Son hamleye gelince uyarı çıkar. Yanlış "Bu imkânsız" tespiti "Çözümü var" kartı açar, 1 hamle sayılır ve o seviyeyi kalıcı olarak en fazla 2 yıldıza düşürür; buton o seviyede bir daha görünmez.
- İmkânsız seviyede ipucu cevabı söylemez, hacimlerin ortak bölenine dikkat çeker. İpucudan sonra doğru tespit 1 yıldız verir.
- Seviye sonu kartı yıldızın neden kısıldığını yazar (ipucu, yanlış tespit, joker).
- İpucu alınamıyorsa (ücretsiz hak bitti, yıldız yok) oyun içinden mağaza açılır.
- Ölçülü döküm jokeri: toplam 10 yıldızla açılır. Tam 1 L aktarım, 5 ★, seviye başına tek kullanım, en fazla 1 yıldız.
- Oyun ekranında üst satırdaki mavi kutu harcanabilir yıldızı gösterir, dokununca mağaza açılır. Altındaki geniş kutuda seviyenin hedefi ve o seviyedeki en iyi yıldız sonucu durur. Bir dünya ya da joker eşiği aşılınca seviye sonu kartından sonra kutlama kartı çıkar.
- İmkânsız seviyede ek hamleye harcanan yıldızlar doğru tespitte iade edilir.
- Mağaza (prototip, gerçek ödeme yok): ödüllü reklam, yıldız paketleri, kalıcı Usta paketi.

## Çalıştırma
`index.html` dosyasını tarayıcıda açmak yeterli. İlerleme tarayıcının `localStorage`'ında tutulur.

## Test kısayolları
`#seviye-21`, `#yag-6`, `#tas-1`, `#tasarruf-1` gibi adres sonekleri doğrudan o seviyeyi açar (yayın öncesi kaldırılmalı).

## Çözücü
Her seviyenin en kısa çözümü tarayıcıda BFS ile hesaplanır; yıldızlar, ipuçları, imkânsızlık tespiti ve seviye üretici bu çözücüye dayanır.
