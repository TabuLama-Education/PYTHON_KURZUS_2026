# Ágazati alapvizsga – próba feladatsor

## 1. feladat – Jelszóerősség ellenőrzése

Készítsen egy Python programot az alábbi leírás alapján!

A feladat végeztével a `.py` kiterjesztésű állományt töltse fel!

1. Kérjen be a felhasználótól egy jelszót, és tárolja el egy `jelszo` nevű változóban!

2. Vizsgálja meg, hogy a jelszó legalább `8` karakter hosszú-e!

3. Vizsgálja meg, hogy a jelszó tartalmaz-e legalább egy számjegyet!

4. Vizsgálja meg, hogy a jelszó tartalmaz-e legalább egy nagybetűt!

5. Vizsgálja meg, hogy a jelszó tartalmaz-e legalább egy különleges karaktert az alábbiak közül: `!`, `?`, `#`, `@`.

6. Ha a jelszó mind a négy feltételnek megfelel, akkor írja ki:

```txt
A megadott jelszó erős.
```

7. Ha a jelszó valamelyik feltételnek nem felel meg, akkor írja ki, hogy a jelszó nem elég erős, majd külön sorokban jelezze, melyik feltétel nem teljesült!

### Minta

```txt
Add meg a jelszót: Almafa12

A megadott jelszó nem elég erős.
Hiányzik belőle a különleges karakter.
```

---

## 2. feladat – Moziterem ülőhelyeinek vizsgálata

Készítsen egy Python programot az alábbi leírás alapján!

A feladat végeztével a `.py` kiterjesztésű állományt töltse fel!

1. Hozzon létre egy `ulohelyek` nevű listát, amely egy moziterem egyik sorának foglaltságát tartalmazza! A listában a `0` érték szabad helyet, az `1` érték foglalt helyet jelentsen!

2. A lista legalább `20` darab elemet tartalmazzon!

3. Írja ki a képernyőre az ülőhelyek állapotát úgy, hogy a szabad helyek helyén `szabad`, a foglalt helyek helyén `foglalt` szöveg jelenjen meg!

4. Számolja meg, hány szabad ülőhely van a sorban!

5. Számolja meg, hány foglalt ülőhely van a sorban!

6. Vizsgálja meg, hogy van-e legalább három egymás melletti szabad ülőhely a sorban!

7. Az eredményeket írja ki a képernyőre a minta szerint!

### Minta

```txt
Ülőhelyek állapota:
1. hely: szabad
2. hely: foglalt
3. hely: szabad
...

Szabad helyek száma: 9
Foglalt helyek száma: 11
Van legalább három egymás melletti szabad hely.
```

---

## 3. feladat – Állatorvosi rendelő kezelése

Készítsen egy Python programot az alábbi leírás alapján!

A feladat végeztével a `.py` kiterjesztésű állományt töltse fel!

A programhoz egy `allatok.csv` nevű állomány tartozik. A fájl minden sora egy állatorvosi rendelőben nyilvántartott állat adatait tartalmazza pontosvesszővel elválasztva.

A CSV-fájl szerkezete:

```txt
nev;faj;eletkor;oltas;kezelesAra
```

1. Készítsen egy saját osztályt `Allat` néven!

2. Az osztály rendelkezzen az alábbi tulajdonságokkal: `nev`, `faj`, `eletkor`, `oltas`, `kezelesAra`, `idosAllat`.

3. Készítse el az osztály konstruktorát, amely paraméterként megkapja a `nev`, `faj`, `eletkor`, `oltas` és `kezelesAra` értékeket!

4. A konstruktor állítsa be az `idosAllat` tulajdonság értékét `True` értékre, ha az állat életkora legalább `10`, egyébként pedig `False` értékre!

5. Készítsen egy `AllatokBetoltese` nevű függvényt, amely beolvassa az `allatok.csv` fájlt, létrehozza az állatokat, majd azokat egy listában visszaadja!

6. A program írja ki a konzolra az összes állat adatát, majd külön írja ki azoknak az állatoknak a nevét és faját, amelyek nem rendelkeznek oltással!

7. A program számítsa ki az összes kezelés árát, számolja meg az idős állatokat, keresse meg a legdrágább kezeléshez tartozó állatot, majd az eredményeket írja ki egy `rendelo_osszefoglalo.txt` nevű fájlba!

### Minta kimenet a fájlban

```txt
Állatorvosi rendelő összefoglaló

Összes kezelés ára: 87500 Ft
Idős állatok száma: 2
Legdrágább kezeléshez tartozó állat: Bodri
Faj: kutya
Kezelés ára: 22000 Ft
```

---

## A 3. feladathoz tartozó `allatok.csv` állomány tartalma

```txt
Bodri;kutya;12;igen;22000
Mici;macska;4;nem;13500
Luna;nyúl;2;igen;8000
Max;kutya;8;nem;17500
Csipesz;hörcsög;1;igen;6000
Cirmi;macska;14;nem;20500
```

