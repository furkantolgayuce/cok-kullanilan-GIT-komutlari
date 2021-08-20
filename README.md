# Çok Kullanılan Git Komutları

## Clone

Uzaktayi projeyi clonelamak için vereceğimiz komut:

```
git clone [link]
```



## Remote

Uzakta repo açıp yereldeki klasörle birleştirmek için kullanacağımız komutlar:

* Eğer yereldeki klasörde bir .git dosyası yok ise:
  * `git init`
* Ardından iki repoyu birleştirmek için

```
git remote add origin [link]
```

**Değişikliklerin ardından ilk push komutunu kullanırken:**

* `git push --set-upstream origin master -f` komutunu kullanmalıyız.

## Push

Yaptığımız değişiklikleri uzaktaki repoya göndereceğimiz komutlar:

* Yapılan değişiklikleri tespit etmek için: `git add .`

* Değişikliğin ne olduğunu yorum olarak ekliyoruz `git commit -m "Yorum"`
* Değişiklikleri uzaktaki repoya gönderiyoruz. `git push`

**Özet:**

```
git add .
git commit -m "Yorum"
git push
```



## Pull

Uzaktaki repodaki değişiklikleri almak isterken kullanacağımız komutlar:

* Uzaktaki repodaki değişiklikleri öğrenmek için: `git fetch --all`
* Değişiklikleri almak için: `git pull`

**Özet:**

```
git fetch --all
git pull
```



Eğer daha öncesinde yerelde değişiklik yaptıysak hata verecektir. Yaptığımız değişiklikleri yok saymak için:

**Kullanırken dikkat edin yaptığınız değişiklikleri silecektir.**

```
git stash
```

## Branch Eklemek

Yeni branch oluşturmak için.

`git checkout -b [isim]`

## Commit Seçenekleri
Son commit'in adını değiştirmek veya son değişiklikleri onun içerisine eklemek için

`git commit --amend`

Sadece son commit'in adını değiştirmek istersek ise
`git commit --amend -m "Yeni Commit Adı"`

## Revert
Yaptığımız değişikliği geri almak için kullanabiliriz. Ama yapılan değişikliği de bir adım olarak ekler.

`git revert geri-alacağımız-commit-idsi`

## Reset Hard
Yaptığımız değişikliği silerek geri almak için kullanılır. Revert çok daha güvenli reset kullanıldığı zaman commitler silinir.

`git reset --hard gitmek-istediğiniz-commit-idsi`

## İki commit arasındaki fark
İki commit arasındaki farkı görmek için

`git diff birinci-commitid...ikinci-commitid`

