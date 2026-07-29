# Bu Repo Nedir? (Örnek/Öğretici Amaçlı)

Bu benim kişisel tez reposu — burada senin çalışmanı önermem. Bunu sana, "Claude'u düzenli nasıl kullanırım" için bir **örnek/şablon** olsun diye gönderiyorum. Buradan sadece işine yarayan fikri al, kendi sistemini kur.

**Repo linki (bakmak için):** https://github.com/kevser-altundal1/apo

## Buradan ne öğrenirsin?

| Dosya/Klasör | Ne öğretir |
|---|---|
| `CLAUDE.md` | Claude'a kalıcı kural nasıl yazılır (örn. "veriye dokunma", "kısa cevap ver") |
| `.claude/skills/` | Bir "skill" (otomatik devreye giren davranış) nasıl yazılır |
| `prompt-sablonlari.md` | Hangi durumda Project / Cowork / Claude Code kullanılır, örnek promptlar |
| `README.md` | Bir repoyu nasıl kendine göre haritalandırırsın |

## Kendi sistemini nasıl kurarsın

1. Kendi bilgisayarında (ya da Drive'ında) boş bir klasör aç.
2. Bu repodan işine yarayan dosyaları (`CLAUDE.md`, `.claude/skills/`, `prompt-sablonlari.md`) kopyala, kendi klasörüne koy, kendi konuna göre düzenle.
3. Claude Code'u nasıl kullanacağına karar ver:
   - **Tarayıcıdan** (claude.ai → **Code** sekmesi): hiçbir şey indirmene gerek yok. Klasörünü GitHub'a repo olarak koyarsın, oradan seçip bağlarsın.
   - **Terminalden** (CLI): bilgisayarına kurman gerekir. Terminale şunu yaz: `npm install -g @anthropic-ai/claude-code`. Kurulum bitince klasörüne git, `claude` yaz, başlar.
4. Claude'a klasörünü/reponu bağla, konuş — ihtiyacına göre kuralları (`CLAUDE.md`) ve skill'leri sen yazarsın.

## Not

Buradaki bilgilerin çoğu zaten Claude'un genel dokümantasyonunda var. Ben sadece kendi ihtiyacım için basitçe, tek yerde toplu hale getirdim. Sen de kendi konuna göre böyle bir sistem kurabilirsin — buradaki dosyalar sana sadece "nasıl bir şey" olduğunu göstermek için.
