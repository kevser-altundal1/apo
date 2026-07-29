# Bu Repo Nedir, Nasıl Kullanılır?

Bu repo, tez çalışmamı Claude ile daha düzenli yürütmek için kurduğum bir sistem. İçinde: çalışma kuralları, örnek promptlar ve klasör yapısı hazır — Claude Code'a bağlayınca hepsi otomatik devreye giriyor.

**Repo linki:** https://github.com/kevser-altundal1/apo

## İçinde ne var?

| Dosya/Klasör | Ne işe yarar |
|---|---|
| `README.md` | Repo haritası, nereden başlanacağı |
| `CLAUDE.md` | Claude'un her oturumda otomatik uyduğu kurallar (veri değiştirilmez, kısa/öz yanıt, onay almadan işlem yapmama vb.) |
| `prompt-sablonlari.md` | Kopyala-doldur-kullan örnek promptlar (veri analizi, hedef belirleme, Loop/Cowork/Project ne zaman kullanılır vb.) |
| `.claude/skills/` | Otomatik devreye giren davranışlar (kısa yanıt, veri doğrulama) |
| `tez/`, `veri/`, `analiz/`, `kaynaklar/` | Çalışma klasörleri |

## Claude Code kullanmak istersen, nasıl başlarsın?

1. claude.ai'ye git, giriş yap.
2. Sol menüden **Code** sekmesine tıkla.
3. **New** ile yeni bir session aç.
4. Alt kısımda **"+ Select repo..."** butonuna tıkla.
5. GitHub hesabını bağlaman istenirse bağla, sonra bu repoyu (`kevser-altundal1/apo`) seç — ya da kendi kopyanı/fork'unu oluşturup onu seçebilirsin.
6. Session açıldığı an `CLAUDE.md` otomatik okunur, kurallar devreye girer.
7. Detaylar için repodaki `README.md` ve `prompt-sablonlari.md` dosyalarına bak.

## Kendi çalışman için uyarlamak istersen

Bu yapı benim tez konuma göre kuruldu (veri bütünlüğü, tez yazımı, çoklu bölüm). Kendi işine göre `CLAUDE.md`'deki kuralları değiştirebilir, `.claude/skills/` altına kendi skill'lerini ekleyebilir, klasör yapısını kendi ihtiyacına göre yeniden düzenleyebilirsin — hepsi düz metin dosyası, korkmadan düzenleyebilirsin.
