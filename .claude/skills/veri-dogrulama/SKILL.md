---
name: veri-dogrulama
description: Kullanıcı gerçek verilerle matematiksel, istatistiksel veya sayısal bir hesaplama/analiz istediğinde bu skill'i kullan (örn. ortalama, korelasyon, regresyon, hipotez testi, herhangi bir formül uygulaması). Kullanıcı açıkça "doğrula" demese bile, sonuç yanlış çıkarsa ciddi sonuçları olacağı için (tez/akademik çalışma) her sayısal hesaplamada bu skill'i tetikle.
---

# Veri Doğrulama

## Neden
Bu, gerçek veriyle yapılan ve tez/akademik çalışmaya girecek bir hesaplama. Yanlış bir sonucun sessizce geçmesi, kullanıcının çalışmasına yanlış bilgi olarak girer. Bu yüzden "muhtemelen doğrudur" yeterli değil — hesaplama görülebilir ve çapraz kontrol edilebilir olmalı.

## Yapılacaklar (her sayısal hesaplamada)

1. **Veriyi olduğu gibi kullan.** Girdi veride hiçbir değişiklik (yuvarlama, dışlama, temizleme, örnekleme) yapma — kullanıcı açıkça istemedikçe.
2. **Hesaplama adımlarını göster.** Sadece sonucu değil, ara adımları da yaz (formül, kullanılan değerler, ara sonuçlar).
3. **Bağımsız bir ikinci yöntemle çapraz kontrol et.** Mümkünse farklı bir hesaplama yolu, farklı bir formülasyon veya "ilk sonucu unutup baştan hesapla" mantığıyla ikinci bir geçiş yap.
4. **İki sonuç karşılaştır.**
   - Uyuşuyorsa: sonucu ver, hangi iki yöntemle doğrulandığını kısaca belirt.
   - Uyuşmuyorsa: bunu SUSMA, açıkça söyle, farkın nereden geldiğini araştır, kullanıcıya bildir.
5. **Varsayım yaptıysan açıkça yaz.** ("X dağılımı normal kabul edildi", "eksik veri şu şekilde ele alındı" gibi) — sessizce geçme, kesinmiş gibi sunma.
6. **Karmaşık/kritik hesaplamalarda role bölme öner.** İş büyükse, kullanıcıya "bunu ayrı bir oturumda/promptla bağımsız biri gibi tekrar kontrol ettirebilirim, ister misin?" diye sor.

## Ne yapma
- Sonucu tek bir yöntemle hesaplayıp direkt sunma.
- "Muhtemelen doğrudur" gibi belirsiz ifadelerle geçiştirme — ya doğrula ya da doğrulanmadığını açıkça söyle.
- Veriyi "daha temiz görünsün" diye ufak tefek düzeltme — bu kesinlikle yasak (bkz. kök `CLAUDE.md`).
