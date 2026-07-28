# apo — Tez Çalışma Deposu

Bu repo, doktora tezi ve ilgili kod/analiz çalışmaları için kullanılıyor.

## Klasör yapısı

| Klasör/Dosya | Ne için |
|---|---|
| `tez/` | Tez metni, bölüm bölüm |
| `veri/` | Ham veri — değiştirilmez |
| `analiz/` | Kod, script, analiz dosyaları |
| `kaynaklar/` | Makale özetleri, literatür notları |
| `CLAUDE.md` | Tüm çalışma kuralları (Claude bunu her oturumda otomatik okur) |
| `prompt-sablonlari.md` | Kopyala-doldur-kullan örnek prompt kalıpları |
| `.claude/skills/` | Otomatik devreye giren yardımcı davranışlar (token-efficient, veri-dogrulama) |

## Nereden başlarım?

1. `CLAUDE.md`'yi oku (kurallar orada, kısa).
2. Tez metni yazacaksan → normal claude.ai sohbeti + o bölüm için bir Project aç.
3. Kod/analiz yapacaksan → Claude Code ile bu repo üzerinde çalış.
4. `prompt-sablonlari.md`'den uygun kalıbı kopyala, doldur, gönder.
5. Konu değişince `/clear`, sohbet uzayınca `/compact`.

Detaylı gerekçeler ve tüm kurallar için: `CLAUDE.md`.
