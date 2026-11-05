# Tartışmalı Pozisyon arşivi

Süper Lig tartışmalı pozisyon yorumları (Trio / F.A / D.A.B / B.G / M.Ç / D.Ç).

Claude veya başka AI: bu repo **public**; dosyaları raw URL ile kendin çek.

## Claude için ana dosya
- Maç özeti (markdown): [`matches/tp-pozisyon-kasimpasa-besiktas-2026-11-01.md`](matches/tp-pozisyon-kasimpasa-besiktas-2026-11-01.md)
- Raw: https://raw.githubusercontent.com/korhanckc/tp-pozisyon-arsivi/main/matches/tp-pozisyon-kasimpasa-besiktas-2026-11-01.md
- Yapılandırılmış JSON: [`matches/2026-11-01-kasimpasa-besiktas.json`](matches/2026-11-01-kasimpasa-besiktas.json)
- Index: [`index.json`](index.json)
- Trabzonspor–Gaziantep (1 Kas): [`matches/tp-pozisyon-trabzonspor-gaziantep-2026-11-01.md`](matches/tp-pozisyon-trabzonspor-gaziantep-2026-11-01.md) — raw: https://raw.githubusercontent.com/korhanckc/tp-pozisyon-arsivi/main/matches/tp-pozisyon-trabzonspor-gaziantep-2026-11-01.md

## Anahtarlar
| Kod | Kaynak |
|-----|--------|
| Trio | Trio |
| F.A | Fırat Aydınus |
| D.A.B | Deniz Ateş Bitnel |
| B.G | Bünyamin Gezer |
| M.Ç | Mustafa Çulcu |
| D.Ç | Deniz Çoban |

Her dolu yorumcu satırı `Karar · https://…` biçimindedir. `[A]` = otomatik altyazı / konuşmacı belirsizliği. `[özet alıntı]` = @tartismalar özet tweetindeki atıf. `Hak.` = diğer adlı hakem alıntısı.
`@tartismalar` yalnızca başka hakemlerin alıntılı teyitleri için kullanılır; hesap sahibinin şahsi yorumu yok sayılır.

## Hakem / VAR atamaları (`atamalar/`)

Pozisyon dosyalarına dokunulmaz. Süper Lig saha + VAR/AVAR atamaları:

- Klasör: [`atamalar/`](atamalar/)
- Hafta dosyası: `atamalar/super-lig-2026-27-hafta-NN.json` (tek dosya; VAR gelince aynı dosya güncellenir)
- 11. hafta: [`atamalar/super-lig-2026-27-hafta-11.json`](atamalar/super-lig-2026-27-hafta-11.json)
- Claude raw: https://raw.githubusercontent.com/korhanckc/tp-pozisyon-arsivi/main/atamalar/super-lig-2026-27-hafta-11.json

Kaynak kuralı: yalnızca açıklanmış TFF/MHK (veya aktaran haber) + `kaynaklar` linki. Açıklanmamış alan `null` / yardımcılar `[]`.

