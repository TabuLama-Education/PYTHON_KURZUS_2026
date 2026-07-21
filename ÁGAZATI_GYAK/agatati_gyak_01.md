# Ágazati alapvizsga – próba feladatsor

## 1. feladat – Rendezvénybelépő ajánló

Készítsen egy Python programot az alábbi leírás alapján!

A feladat végeztével a `.py` kiterjesztésű állományt töltse fel!

1. Kérje be a felhasználótól konzolon keresztül, hogy milyen típusú rendezvényre szeretne menni: `koncert`, `színház` vagy `sport`.

2. A bekért értéket tárolja el egy `rendezvenyTipus` nevű változóban!

3. Kérje be a felhasználótól, hogy mennyi pénzt szán a belépőre, és tárolja el egy `keret` nevű változóban egész számként!

4. Ha a felhasználó `koncert` rendezvényt választott, és a keret legalább `12000`, akkor írja ki:

```txt
Prémium koncertjegyet ajánlunk.
```

5. Ha a felhasználó `színház` rendezvényt választott, és a keret legalább `8000`, akkor írja ki:

```txt
Jó helyre szóló színházjegyet ajánlunk.
```

6. Ha a felhasználó `sport` rendezvényt választott, és a keret legalább `6000`, akkor írja ki:

```txt
Sporteseményre szóló belépőt ajánlunk.
```

7. Minden más esetben írja ki:

```txt
A megadott keret vagy rendezvénytípus alapján nem tudunk megfelelő ajánlatot adni.
```

---

## 2. feladat – Okosvárosi hőmérsékletmérés

Készítsen egy Python programot az alábbi leírás alapján!

A feladat végeztével a `.py` kiterjesztésű állományt töltse fel!

1. Importálja be a `random` modult!

2. Generáljon 30 darab véletlen egész számot, amelyek egy városi hőmérsékletmérő napi méréseit jelképezik!

3. A generálható értékek `-5` és `38` közé essenek, a határértékeket is beleértve!

4. A generált értékeket tárolja el egy `meresek` nevű listában, majd írja ki a lista elemeit egymás mellé!

5. Számítsa ki és írja ki a mérések átlagát két tizedesjegyre kerekítve!

6. Számolja meg, hány mérés volt fagypont alatti, hány mérés volt `0` és `25` fok közötti, valamint hány mérés volt `25` fok feletti!

7. Határozza meg és írja ki a legmagasabb hőmérsékletet, a legalacsonyabb hőmérsékletet, valamint azt, hogy a legmagasabb érték hányadik mérésként szerepelt a listában!

### Minta

```txt
A mért hőmérsékletek:
12 18 -2 25 31 7 ...

Átlaghőmérséklet: 16.43 °C
Fagypont alatti mérések száma: 3
0 és 25 fok közötti mérések száma: 19
25 fok feletti mérések száma: 8
Legmagasabb hőmérséklet: 38 °C
Legalacsonyabb hőmérséklet: -5 °C
A legmagasabb érték helye: 14. mérés
```

---

## 3. feladat – Csomagautomata-kezelő rendszer

Készítsen egy Python programot az alábbi leírás alapján!

A feladat végeztével a `.py` kiterjesztésű állományt töltse fel!

A programhoz egy `csomagok.csv` nevű állomány tartozik. A fájl minden sora egy csomag adatait tartalmazza pontosvesszővel elválasztva.

A CSV-fájl szerkezete:

```txt
azonosito;tomeg;tavolsag;prioritas
```

Példa:

```txt
PKG001;4;12;normal
PKG002;2;35;express
PKG003;8;7;normal
PKG004;1;50;express
```

1. Készítsen egy saját osztályt `Csomag` néven!

2. Az osztály rendelkezzen az alábbi tulajdonságokkal:

```txt
azonosito
tomeg
tavolsag
prioritas
szallitasiDij
```

3. Készítse el az osztály konstruktorát, amely paraméterként megkapja az `azonosito`, `tomeg`, `tavolsag` és `prioritas` értékeket!

4. A konstruktor számítsa ki automatikusan a szállítási díjat az alábbi szabály szerint:

```txt
alapdíj = tomeg * 500 + tavolsag * 80
```

Ha a csomag prioritása `express`, akkor a szállítási díj legyen az alapdíj kétszerese. Egyéb esetben a szállítási díj maradjon az alapdíj értéke.

5. Készítsen egy `CsomagokBetoltese` nevű függvényt, amely beolvassa a `csomagok.csv` fájlt, létrehozza a csomagokat, majd azokat egy listában visszaadja!

6. Készítsen egy `LegdragabbCsomag` nevű függvényt, amely paraméterként megkapja a csomagok listáját, és visszaadja azt a csomagot, amelynek a legmagasabb a szállítási díja!

7. A legdrágább csomag adatait írja ki egy `legdragabb_csomag.txt` nevű fájlba az alábbi adatokkal:

```txt
A legdrágább csomag azonosítója: PKG004
Tömeg: 1 kg
Távolság: 50 km
Prioritás: express
Szállítási díj: 9000 Ft
```
