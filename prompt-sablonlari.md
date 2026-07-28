# Örnek Prompt Şablonları

## 1. Loop örneği
Bir işi belirli aralıklarla otomatik tekrarlatmak için:
```
/loop 30m "şu klasördeki yeni veri dosyalarını kontrol et, yeni bir şey varsa özetle"
```
Not: Senin tez çalışman için genelde gerekmez (bkz. CLAUDE.md / genel rehber) — sadece nasıl göründüğünü örnek olarak gösteriyorum.

## 2. Goal (hedef) örneği
Bir oturuma başlarken büyük resmi netleştirmek için:
```
Hedef: [örn. "Tezin Bölüm 3'ünü Ağustos sonuna kadar bitirmek"]
Şu an neredeyim: [örn. "veri toplama bitti, analiz aşamasındayım"]
Bu oturumda istediğim: [somut, küçük ve net bir adım]
Bu oturum sonunda başarı kriteri: [ne tamamlanmış olmalı]
```

## 3. Skill'i doğrudan çağıran örnek
`token-efficient` skill'ini bilerek devreye sokmak istiyorsan:
```
token-efficient skill'ini kullanarak şu kodu incele: [dosya/kod]
```
veya
```
Bu görevi token-efficient skill kurallarına göre yap: [görev]
```
Not: Bu skill zaten kod/teknik işlerde otomatik devreye giriyor, açıkça çağırmak zorunda değilsin — ama emin olmak istersen bu şekilde belirtebilirsin.

## 4. Veri analizi + doğrulama örneği (önceki rehberden)
```
Bağlam: [konu/bölüm]
Veri: [gerçek veri, değiştirilmeyecek]
Görev: [ne hesaplanacak]
Doğrulama: sonucu bağımsız bir yöntemle çapraz kontrol et,
           varsayım varsa açıkça belirt
Çıktı formatı: [tablo / metin / sadece sayı vb.]
```
