# Örnek Prompt Şablonları

**İçindekiler**
1. [Loop](#1-loop-örneği)
2. [Goal (hedef)](#2-goal-hedef-örneği)
3. [Skill'i doğrudan çağırma](#3-skilli-doğrudan-çağıran-örnek)
4. [Veri analizi + doğrulama](#4-veri-analizi--doğrulama-örneği)
5. [Artifact — görselleştirme/rapor](#5-artifact-örneği)
6. [Google Drive bağlantısı](#6-google-drive-bağlantısı)
7. [Routine — zamanlanmış hatırlatma](#7-routine-örneği)
8. [Project vs Cowork — hangisi ne zaman](#8-project-vs-cowork--hangisi-ne-zaman)
9. [Claude Code ne zaman kullanılır](#9-claude-code-ne-zaman-kullanılır)
10. [Üçü birden — karar kuralı](#10-üçü-birden--tek-satırlık-karar-kuralı)
11. [Genel prompt yazma formülü (Yap/Yapma)](#11-genel-prompt-yazma-formülü-yapyapma)

---

## 1. Loop örneği
Bir işi belirli aralıklarla otomatik tekrarlatmak için:
```
/loop 30m "şu klasördeki yeni veri dosyalarını kontrol et, yeni bir şey varsa özetle"
```
Not: Senin tez çalışman için genelde gerekmez — sadece nasıl göründüğünü örnek olarak gösteriyorum.

---

## 2. Goal (hedef) örneği
Bir oturuma başlarken büyük resmi netleştirmek için:
```
Hedef: [örn. "Tezin Bölüm 3'ünü Ağustos sonuna kadar bitirmek"]
Şu an neredeyim: [örn. "veri toplama bitti, analiz aşamasındayım"]
Bu oturumda istediğim: [somut, küçük ve net bir adım]
Bu oturum sonunda başarı kriteri: [ne tamamlanmış olmalı]
```

---

## 3. Skill'i doğrudan çağıran örnek
`token-efficient` veya `veri-dogrulama` skill'ini bilerek devreye sokmak istiyorsan:
```
token-efficient skill'ini kullanarak şu kodu incele: [dosya/kod]
```
```
veri-dogrulama skill'ine göre şu hesaplamayı yap ve çapraz kontrol et: [görev]
```
Not: Bu skill'ler zaten uygun bağlamda otomatik devreye giriyor, açıkça çağırmak zorunda değilsin — emin olmak istersen bu şekilde belirtebilirsin.

---

## 4. Veri analizi + doğrulama örneği
```
Bağlam: [konu/bölüm]
Veri: [gerçek veri, değiştirilmeyecek]
Görev: [ne hesaplanacak]
Doğrulama: sonucu bağımsız bir yöntemle çapraz kontrol et,
           varsayım varsa açıkça belirt
Çıktı formatı: [tablo / metin / sadece sayı vb.]
```

---

## 5. Artifact örneği
**Ne işe yarar:** Claude'un ürettiği içeriği (grafik, tablo, rapor sayfası) ayrı, düzenli bir görünümde gösterir — sohbet içine gömülü metin yerine.

**Sen ne zaman kullanırsın:** Bir analiz sonucunu grafikle görmek istediğinde, ya da bulgularını düzenli bir rapor/sayfa halinde görmek istediğinde.
```
[X] verisindeki [Y] dağılımını grafikle göster,
görsel bir rapor/sayfa olarak sun.
```

---

## 6. Google Drive bağlantısı
**Ne işe yarar:** Tezini zaten Google Docs'ta tutuyorsan, Drive'ı bağlarsan Claude dosyayı doğrudan okuyabilir — kopyala-yapıştıra gerek kalmaz.

**Nasıl açılır:** claude.ai → Settings → Connectors → Google Drive → Connect.

**Örnek prompt (bağladıktan sonra):**
```
Google Drive'daki "[dosya adı]" belgesini oku,
[şu bölümü/kısmı] için önerilerini yaz.
```
Not: Bu bağlıysa Claude dosyayı okuyabilir ama **senin izinin olmadan üzerine yazmaz/değiştirmez** — bu zaten CLAUDE.md kuralı.

---

## 7. Routine örneği
**Ne işe yarar:** Belirli bir gün/saatte otomatik olarak sana bir mesaj/hatırlatma gönderir. Loop'tan farkı: Loop kısa aralıklı, teknik/otomatik kontroller için; Routine daha uzun vadeli, planlı hatırlatmalar için (örn. haftalık).

**Sen ne zaman kullanırsın:** Örn. her hafta başı o hafta tezde ne yapman gerektiğini hatırlatması için.
```
Her Pazartesi sabah 9'da bana şunu sor:
"Bu hafta tezde hangi bölüm üzerinde çalışacaksın?"
```
Not: Bunu kurmak istersen bana söyle, ben kurabilirim — kendi kendine otomatik kurmam, senin onayınla.

---

## 8. Project vs Cowork — hangisi ne zaman

| | Project | Cowork |
|---|---|---|
| Ne | Bir konuya ait dosya/bağlamı saklayan "klasör" | Claude'un birden fazla adımı **kendi başına** yürüttüğü çalışma modu |
| Sen ne yaparsın | Konuşursun, sorarsın, birlikte yazarsın — her adımı sen yönlendirirsin | Görevi tarif edersin, Claude arka planda birden fazla adımı senin sürekli müdahalen olmadan yapar |
| Ne zaman kullan | Tez bölümü yazarken, literatür tartışırken, taslak üzerinde ileri-geri konuşurken | "Şu 10 dosyayı tara, ortak temaları bul ve rapor et" gibi çok adımlı, arka planda yapılabilecek işler |

**Pratik kural:**
- Tek dosyayı okuyup tartışacaksan / birlikte yazacaksan → **Project** (normal sohbet).
- Çok sayıda dosyayı tarama/özetleme/karşılaştırma gibi kendi başına yürütülebilecek bir işse → **Cowork** düşünülebilir.

**Uyarı:** Cowork daha bağımsız çalışır, ara adımlarda durup sormaz — "her adımda onay" tercihinle kısmen çelişir. Veri bütünlüğünün kritik olduğu, gerçek veriyle yapılan işlerde Cowork yerine normal Claude Code + adım adım onay akışını tercih et. Cowork'ü daha çok, sonucu kontrol edip sürecini denetlemene gerek duymadığın düşük riskli işlerde kullan.

**Somut örnekler:**

*Project ne zaman:*
- Bir tez bölümünün taslağını tartışmak, fikir geliştirmek (metni sonunda sen `tez/` klasörüne kendin koyarsın)
- Birkaç makaleyi (PDF) doğrudan yükleyip "bunları karşılaştır, tartış" demek — repoya koymaya gerek olmayan, tek seferlik kaynaklar
- Danışmanınla yazışma taslağı, sunum notu gibi bu repoyla ilgisi olmayan işler
- Sürekli dönüp baktığın bir referans konusu (örn. "istatistik terimleri")

*Cowork ne zaman:*
- "İnternette [X] konusunda kaynak bul, başlık+özetlerini bir listeye çıkar" gibi araştırma/toplama işleri
- Kaynakça formatlama, çok sayıda dosyayı yeniden adlandırma gibi tekrarlayan ama **kritik olmayan** işler
- Sonucu görüp kontrol etmenin yeterli olduğu, sürecin nasıl yapıldığının önemli olmadığı işler

---

## 9. Claude Code ne zaman kullanılır

| İş | Nerede |
|---|---|
| Dosyalara/repoya gerçekten dokunmak gerekiyor (veri okumak, script çalıştırmak, `tez/`, `veri/`, `analiz/` klasörlerini düzenlemek) | **Claude Code** |
| Git işlemleri (commit, push) | **Claude Code** |
| Sadece konuşmak, taslak yazmak, fikir tartışmak — dosya sistemine dokunmadan | Normal **Claude sohbeti** (+ Project) |
| Tez metnini repo'da dosya olarak tutup Claude'un doğrudan düzenlemesini istiyorsan | **Claude Code** |
| Tez metnini Google Docs'ta tutuyorsan (Drive bağlantısıyla) | Normal **Claude sohbeti** |

**Kısaca:** Elinde gerçek bir dosya/repo/veri var ve Claude'un ona dokunmasını istiyorsan → Code. Sadece kafa yormak/yazı yazmak istiyorsan → normal sohbet.

---

## 10. Üçü birden — tek satırlık karar kuralı

- **Gerçek veri/hesaplama/repo dosyası** var → **Code**
- **Konuşma/fikir/taslak**, dosyaya dokunmaya gerek yok → **Project**
- **Düşük riskli, çok adımlı** bir toplama/araştırma işi, sonucu kontrol etmen yeterli → **Cowork**

---

## 11. Genel prompt yazma formülü (Yap/Yapma)

Uzun, birleşik cümleler yerine net maddeler kullan — dağınık bir cümlede detay atlanabilir, madde madde yazınca atlanmaz.

**1) Yap / Yapma şeklinde ayır:**
```
Yapılacaklar:
- [net madde]
- [net madde]

Yapılmayacaklar / Dikkat et:
- [kaçınılması gereken şey]
```

**2) Her istekte şu 4 bilgiyi sırayla ver:**
1. **Amaç** — Ne yapmak istiyorsun?
2. **Kapsam** — Hangi dosya/yer değişecek?
3. **İçerik/Detay** — Tam olarak ne olmalı?
4. **Çıktı formatı** — Nasıl sunmamı istiyorsun? (mesaj metni, tablo, kod vb.)

**3) Örnek kalıp:**
```
GÖREV: [ne yapılacak]

ANA MESAJ / İÇERİK:
- [madde 1]
- [madde 2]

EKLENECEK ADIMLAR:
1. ...
2. ...

YAPMA:
- [kaçınılacak şey]
```

Bu formatla yazınca hiçbir detayı atlamadan, tam istediğin gibi yaparım.

---

**Emin olmadığım bir özellik var:** Claude Code arayüzünde "Dispatch (Beta)" diye bir menü öğesi gördüm ama tam olarak nasıl çalıştığından emin değilim. Sana yanlış bilgi vermemek için burada eklemedim — merak edersen birlikte inceleyebiliriz.
