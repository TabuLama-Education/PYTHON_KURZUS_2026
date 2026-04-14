# Feladat – Banki hitelminősítés

Készíts programot, amely egy ügyfél alapadatai alapján eldönti, hogy kaphat-e hitelt.

A program kérje be a felhasználótól az alábbi adatokat:

* életkor
* havi nettó jövedelem
* meglévő havi törlesztőrészletek összege
* munkaviszony hossza hónapban
* szerepel-e negatív státusszal a KHR-listán (`igen` vagy `nem`)

A program a következő szabályok alapján minősítse az ügyfelet:

* Ha az ügyfél életkora kisebb mint 18, akkor **nem hitelképes**
* Ha az ügyfél negatív KHR-listán szerepel, akkor **nem hitelképes**
* Ha a havi nettó jövedelme kisebb mint 250000 Ft, akkor **nem hitelképes**
* Ha a munkaviszonya rövidebb mint 6 hónap, akkor **nem hitelképes**
* Ha a meglévő havi törlesztőrészletek összege meghaladja a nettó jövedelem 40%-át, akkor **nem hitelképes**
* Ha minden feltétel megfelelő, akkor:

  * ha a jövedelem legalább 600000 Ft **és** a munkaviszony legalább 24 hónap, akkor **kiemelten hitelképes**
  * egyébként **hitelképes**

A program a végén írja ki az ügyfél minősítését.

---


# Expected output – példák

## 1. eset – Nem hitelképes (életkor miatt)

**Bemenet:**

```
Add meg az életkort: 16
Add meg a havi nettó jövedelmet Ft-ban: 300000
Add meg a meglévő havi törlesztőrészletek összegét Ft-ban: 50000
Add meg a munkaviszony hosszát hónapban: 12
Szerepel negatív KHR-listán? (igen/nem): nem
```

**Kimenet:**

```
Minősítés: nem hitelképes
```

---

## 2. eset – Nem hitelképes (KHR miatt)

**Bemenet:**

```
Add meg az életkort: 30
Add meg a havi nettó jövedelmet Ft-ban: 400000
Add meg a meglévő havi törlesztőrészletek összegét Ft-ban: 50000
Add meg a munkaviszony hosszát hónapban: 12
Szerepel negatív KHR-listán? (igen/nem): igen
```

**Kimenet:**

```
Minősítés: nem hitelképes
```

---

## 3. eset – Nem hitelképes (túl magas törlesztés)

**Bemenet:**

```
Add meg az életkort: 35
Add meg a havi nettó jövedelmet Ft-ban: 300000
Add meg a meglévő havi törlesztőrészletek összegét Ft-ban: 150000
Add meg a munkaviszony hosszát hónapban: 12
Szerepel negatív KHR-listán? (igen/nem): nem
```

**Kimenet:**

```
Minősítés: nem hitelképes
```

---

## 4. eset – Hitelképes

**Bemenet:**

```
Add meg az életkort: 28
Add meg a havi nettó jövedelmet Ft-ban: 350000
Add meg a meglévő havi törlesztőrészletek összegét Ft-ban: 50000
Add meg a munkaviszony hosszát hónapban: 12
Szerepel negatív KHR-listán? (igen/nem): nem
```

**Kimenet:**

```
Minősítés: hitelképes
```

---

## 5. eset – Kiemelten hitelképes

**Bemenet:**

```
Add meg az életkort: 40
Add meg a havi nettó jövedelmet Ft-ban: 700000
Add meg a meglévő havi törlesztőrészletek összegét Ft-ban: 100000
Add meg a munkaviszony hosszát hónapban: 36
Szerepel negatív KHR-listán? (igen/nem): nem
```

**Kimenet:**

```
Minősítés: kiemelten hitelképes
```

---

