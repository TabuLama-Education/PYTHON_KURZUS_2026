
# Ágazati alapvizsga – próba feladatsor
## 1. feladat – Iskolai büfé fizetés ellenőrzése
Készítsen egy Python programot az alábbi leírás alapján!
A feladat végeztével a `.py` kiterjesztésű állományt töltse fel!
1. Kérje be a felhasználótól, hogy milyen típusú vásárló érkezett a büfébe! A válasz értéke `diak`, `tanar` vagy `vendeg` legyen, és tárolja el egy `vasarloTipus` nevű változóban!
2. Kérje be a felhasználótól a vásárlás összegét forintban, és tárolja el egy `osszeg` nevű változóban egész számként!
3. Ha a vásárló `diak`, és a vásárlás összege legalább `1500` Ft, akkor írja ki:
```txt
A diákkedvezmény jár, a vásárló 10% kedvezményt kap.
```
4. Ha a vásárló `diak`, de a vásárlás összege `1500` Ft alatt van, akkor írja ki:
```txt
A vásárlás összege nem éri el a diákkedvezmény határát.
```
5. Ha a vásárló `tanar`, és a vásárlás összege legalább `2000` Ft, akkor írja ki:
```txt
A tanári kedvezmény jár, a vásárló 15% kedvezményt kap.
```
6. Ha a vásárló `vendeg`, akkor írja ki:
```txt
Vendég vásárló esetén nem jár kedvezmény.
```
7. Minden más esetben írja ki:
```txt
Hibás vásárlótípus vagy vásárlási összeg.
```
---
## 2. feladat – Futóverseny eredményeinek elemzése
Készítsen egy Python programot az alábbi leírás alapján!
A feladat végeztével a `.py` kiterjesztésű állományt töltse fel!
1. Importálja be a `random` modult!
2. Generáljon 20 darab véletlen egész számot, amelyek egy futóverseny résztvevőinek célba érési idejét jelölik percben!
3. A generálható értékek `25` és `90` közé essenek, a határértékeket is beleértve!
4. A generált értékeket tárolja el egy `idok` nevű listában, majd írja ki a lista elemeit egymás mellé!
5. Számítsa ki és írja ki a versenyzők átlagos célba érési idejét két tizedesjegyre kerekítve!
6. Számolja meg, hány versenyző ért célba `40` percen belül, hány versenyző teljesített `40` és `60` perc között, valamint hány versenyzőnek kellett `60` percnél több idő!
7. Határozza meg és írja ki a leggyorsabb időt, a leglassabb időt, valamint azt, hogy a leggyorsabb eredmény hányadik helyen szerepel a listában!
### Minta
```txt
A versenyzők célba érési idejei:
34 58 71 42 29 65 ...
Átlagos idő: 52.35 perc
40 percen belüli teljesítések száma: 5
40 és 60 perc közötti teljesítések száma: 9
60 perc feletti teljesítések száma: 6
Leggyorsabb idő: 29 perc
Leglassabb idő: 88 perc
A leggyorsabb eredmény helye: 5. adat
```
---
## 3. feladat – Szállodai szobafoglalások kezelése
Készítsen egy Python programot az alábbi leírás alapján!
A feladat végeztével a `.py` kiterjesztésű állományt töltse fel!
A programhoz egy `foglalasok.csv` nevű állomány tartozik. A fájl minden sora egy szobafoglalás adatait tartalmazza pontosvesszővel elválasztva.
A CSV-fájl szerkezete:
```txt
vendegNev;ejszakakSzama;szobaTipus;reggeli
```
Példa:
```txt
Kovács Anna;3;standard;igen
Nagy Péter;2;premium;nem
Szabó Lili;5;standard;igen
Tóth Márk;1;premium;igen
```
1. Készítsen egy saját osztályt `Foglalas` néven!
2. Az osztály rendelkezzen az alábbi tulajdonságokkal:
```txt
vendegNev
ejszakakSzama
szobaTipus
reggeli
vegosszeg
```
3. Készítse el az osztály konstruktorát, amely paraméterként megkapja a `vendegNev`, `ejszakakSzama`, `szobaTipus` és `reggeli` értékeket!
4. A konstruktor számítsa ki automatikusan a foglalás végösszegét az alábbi szabály szerint:
- A `standard` szoba ára `18000` Ft éjszakánként.
- A `premium` szoba ára `28000` Ft éjszakánként.
- A reggeli ára `3500` Ft éjszakánként, ha a `reggeli` értéke `igen`.
5. Készítsen egy `FoglalasokBetoltese` nevű függvényt, amely beolvassa a `foglalasok.csv` fájlt, létrehozza a foglalásokat, majd azokat egy listában visszaadja!
6. Készítsen egy `LegnagyobbFoglalas` nevű függvényt, amely paraméterként megkapja a foglalások listáját, és visszaadja azt a foglalást, amelynek a legmagasabb a végösszege!
7. A legnagyobb értékű foglalás adatait írja ki egy `legnagyobb_foglalas.txt` nevű fájlba az alábbi adatokkal:
```txt
A legnagyobb értékű foglalás vendége: Szabó Lili
Éjszakák száma: 5
Szobatípus: standard
Reggeli: igen
Végösszeg: 107500 Ft
```