# 1. Feladat: Titkos jelszó feltörése

## Feladatleírás

Készítsen programot, amely egy egyszerű belépési rendszert valósít meg! A helyes jelszó legyen:

```python
"python123"
```

A program addig kérje be a jelszót a felhasználótól, amíg a helyes értéket meg nem adja. Hibás próbálkozás esetén jelenjen meg egy hibaüzenet!

### Minta kimenet:

```text
Adja meg a jelszót: alma
Hibás jelszó!

Adja meg a jelszót: 12345
Hibás jelszó!

Adja meg a jelszót: python123
Sikeres belépés!
```

---

# 2. Feladat: Bevásárlás összegének számítása

## Feladatleírás

Egy boltban a vásárló több terméket vásárol. A program kérje be egymás után a termékek árát, és addig folytassa a bekérést, amíg a felhasználó `0` értéket nem ad meg!

A program számolja ki:

* a vásárlás teljes összegét,
* a megvásárolt termékek számát.

### Minta kimenet:

```text
Add meg a termék árát (0 = vége): 1200
Add meg a termék árát (0 = vége): 3500
Add meg a termék árát (0 = vége): 800
Add meg a termék árát (0 = vége): 0

-----------------------
Termékek száma: 3
Fizetendő összeg: 5500 Ft
```

---

# 3. Feladat: Számkitaláló játék

## Feladatleírás

Készítsen programot, amelyben a gép által tárolt szám:

```python
titkos_szam = 7
```

A felhasználónak addig kell próbálkoznia, amíg el nem találja a számot.

A program jelezze:

* ha a tipp túl nagy,
* ha a tipp túl kicsi,
* ha sikerült eltalálni.

### Minta kimenet:

```text
Tippelj egy számot: 3
A keresett szám nagyobb!

Tippelj egy számot: 10
A keresett szám kisebb!

Tippelj egy számot: 7
Eltaláltad!
```

---

# 4. Feladat: ATM pénzfelvétel

## Feladatleírás

Egy bankautomata induló egyenlege:

```python
egyenleg = 50000
```

A program folyamatosan kérje be a felvenni kívánt összeget.

A ciklus addig fusson, amíg:

* a felhasználó `0` értéket nem ad meg,
* vagy nincs elegendő pénz a számlán.

A program minden sikeres pénzfelvétel után írja ki az aktuális egyenleget.

### Minta kimenet:

```text
Aktuális egyenleg: 50000 Ft
Felvenni kívánt összeg: 10000

Sikeres pénzfelvétel!
Új egyenleg: 40000 Ft

Felvenni kívánt összeg: 15000

Sikeres pénzfelvétel!
Új egyenleg: 25000 Ft

Felvenni kívánt összeg: 0

A program véget ért.
```

---

# 5. Feladat: Vizsgaeredmények bekérése

## Feladatleírás

Egy tanár addig rögzíti a diákok pontszámait, amíg `-1` értéket nem ad meg.

A program:

* tárolja az eredményeket egy listában,
* számolja ki az átlagot,
* határozza meg a legmagasabb pontszámot.

### Minta kimenet:

```text
Add meg a pontszámot (-1 = vége): 85
Add meg a pontszámot (-1 = vége): 92
Add meg a pontszámot (-1 = vége): 78
Add meg a pontszámot (-1 = vége): -1

-----------------------
Eredmények: [85, 92, 78]
Átlag: 85.0 pont
Legjobb eredmény: 92 pont
```

---

# 6. Feladat: Ébresztőóra visszaszámlálás

## Feladatleírás

A felhasználó adja meg, hány másodpercről induljon a visszaszámlálás.

A program `while` ciklussal számoljon vissza nulláig, majd írja ki:

```
Ébresztő!
```

### Minta kimenet:

```text
Hány másodpercről induljon? 5

5
4
3
2
1

Ébresztő!
```

---

# 7. Feladat: Menüvezérelt számológép

## Feladatleírás

Készítsen egyszerű számológépet, amely menü alapján működik.

A program ismételten kérje:

```text
1 - Összeadás
2 - Kivonás
3 - Szorzás
0 - Kilépés
```

A ciklus addig fusson, amíg a felhasználó a `0` lehetőséget nem választja.

### Minta kimenet:

```text
1 - Összeadás
2 - Kivonás
3 - Szorzás
0 - Kilépés

Választás: 1

Első szám: 5
Második szám: 8

Eredmény: 13

Választás: 0

Kilépés...
```

---

# 8. Feladat: Pontgyűjtő játék

## Feladatleírás

Egy játékos pontokat gyűjt. A program minden körben bekéri, hány pontot szerzett.

A játék akkor ér véget, ha:

* eléri vagy meghaladja a 100 pontot,
* vagy a játékos `0` pontot ad meg.

A program írja ki a végső pontszámot.

### Minta kimenet:

```text
Szerzett pont: 20
Összpontszám: 20

Szerzett pont: 35
Összpontszám: 55

Szerzett pont: 50
Összpontszám: 105

Gratulálunk, elérted a 100 pontot!
Végső pontszám: 105
```

