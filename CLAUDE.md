# Proje Kuralları

## Yanıt tarzı
- Kod, komut çıktısı ve teknik işlemlerde kısa ve öz ol. Gereksiz giriş/kapanış cümleleri kullanma ("Elbette!", "Umarım yardımcı olmuştur!" gibi ifadeler yazma).
- Tez metni / akademik yazım isteklerinde bu kural GEÇERLİ DEĞİL — orada detaylı, açıklayıcı, akademik dilde yaz. Kısaltma yapma.
- Kod örneklerine gereksiz yorum satırı ekleme; sadece anlaşılması zor bir kısım varsa tek satır açıklama yaz.

## Veri güvenliği (en önemli kural)
- Hiçbir dosyayı sormadan silme, üzerine yazma veya geri alınamaz şekilde değiştirme.
- `git reset --hard`, `git push --force`, dosya/branch silme gibi geri alınamaz işlemlerden önce her zaman açıkça onay iste.
- Önemli değişiklikleri küçük, açıklayıcı commit'ler halinde kaydet; büyük ve karışık commit yapma.
- Emin olmadığın bir durumda varsayım yapıp devam etme, sor.

## Çalışma düzeni
- Bu depo/klasör birden fazla konu veya tez bölümü içerebilir. Hangi bölüm/konu üzerinde çalışıldığını netleştir, karıştırma.
- Yeni bir konuya geçerken önceki konunun dosyalarına dokunma.

## Veri bütünlüğü ve doğrulama (matematik/analiz işleri)
- Kullanıcı gerçek verilerle karmaşık matematiksel/istatistiksel analizler yaptıracak. Bu tür işlerde:
  - Veriler ASLA değiştirilmez, tahmin edilmez, uydurulmaz veya "düzeltilmez" — kullanıcıdan gelen ham veri neyse odur.
  - Her hesaplama doğrulanmalı: adımlar açıkça gösterilmeli, mümkünse ikinci/bağımsız bir yöntemle çapraz kontrol edilmeli.
  - İş karmaşıksa göreve rol bazlı bölünebilir: bir kısım hesaplamayı yapar, ayrı bir "rol" (ayrı bir prompt/agent) bunu bağımsızca denetler. Kullanıcı bu şekilde bir doğrulama isterse uygulanmalı.
  - Sonuç kesin değilse veya bir varsayım yapıldıysa bu açıkça belirtilmeli, kesinmiş gibi sunulmamalı.

## Tekrarlanan talimatlar → kalıcı kural
- Kullanıcı aynı talimatı/tercihi birden fazla kez söylerse bu geçici bir istek değil, KALICI bir kural adayı sayılır.
- Böyle bir tekrar fark edildiğinde SESSİZCE/OTOMATİK olarak bu dosyaya eklenmez. Önce kullanıcıya "bunu kalıcı kural olarak CLAUDE.md'ye eklemek ister misin?" diye sorulur, kullanıcı onaylarsa eklenir.

## Memory (claude.ai hesap özelliği) hakkında
- Memory, CLAUDE.md'den farklı bir şeydir: CLAUDE.md bu depoya özel, git ile versiyonlanan kurallardır. Memory ise claude.ai hesap ayarlarından (Settings → Capabilities → Memory) açılan, tüm sohbetlerde hatırlanan kişisel bir özelliktir.
- Bu hesap ayarı kullanıcı tarafından açılmalıdır, Claude bunu kullanıcı adına açamaz.

## Sohbet uzunluğu
- Sohbet çok uzayıp yavaşladığında kullanıcıya `/compact` komutunu kullanması önerilmeli.
