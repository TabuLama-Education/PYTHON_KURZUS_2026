# Ágazati alapvizsga – gyakorló feladatsor  3

---

## 1. feladat – Poggyászfeladás ellenőrzése

Készítsen Python programot az alábbi leírás alapján!
A feladat végeztével a `.py` kiterjesztésű állományt töltse fel!

1. Kérje be a felhasználótól, hogy milyen típusú jeggyel utazik! A válasz értéke `basic`, `standard` vagy `premium` legyen, és tárolja el egy `jegyTipus` nevű változóban!

2. Kérje be a felhasználótól a feladni kívánt poggyász tömegét kilogrammban, és tárolja el egy `poggyaszTomeg` nevű változóban egész számként!

3. Ha a jegytípus `basic`, és a poggyász tömege legfeljebb `10` kg, akkor írja ki:

```txt
A poggyász feladható basic jeggyel.
```

4. Ha a jegytípus `standard`, és a poggyász tömege legfeljebb `20` kg, akkor írja ki:

```txt
A poggyász feladható standard jeggyel.
```

5. Ha a jegytípus `premium`, és a poggyász tömege legfeljebb `30` kg, akkor írja ki:

```txt
A poggyász feladható premium jeggyel.
```

6. Ha a jegytípus helyes, de a poggyász tömege meghaladja az adott jegytípushoz tartozó határt, akkor írja ki:

```txt
A poggyász túlsúlyos, pótdíjat kell fizetni.
```

7. Minden más esetben írja ki:

```txt
Hibás jegytípus vagy poggyásztömeg.
```

---

## 2. feladat – Beszállókapuk terheltségének elemzése

Készítsen Python programot az alábbi leírás alapján!

A feladat végeztével a `.py` kiterjesztésű állományt töltse fel!

1. Importálja be a `random` modult!

2. Generáljon 16 darab véletlen egész számot, amelyek egy repülőtéren működő beszállókapuknál várakozó utasok számát jelölik!

3. A generálható értékek `0` és `180` közé essenek, a határértékeket is beleértve!

4. A generált értékeket tárolja el egy `utasSzamok` nevű listában, majd írja ki a lista elemeit egymás mellé!

5. Számítsa ki és írja ki a beszállókapuknál várakozó utasok átlagos számát két tizedesjegyre kerekítve!

6. Számolja meg, hány kapunál várakozik kevesebb mint `50` utas, hány kapunál várakozik `50` és `120` közötti utas, valamint hány kapunál várakozik `120` főnél több utas!

7. Határozza meg és írja ki a legterheltebb kapunál várakozó utasok számát, a legkevésbé terhelt kapunál várakozó utasok számát, valamint azt, hogy a legterheltebb kapu hányadik adatként szerepel a listában!

### Minta

```txt
A beszállókapuknál várakozó utasok számai:
34 128 76 12 150 91 43 168 ...

Átlagos utasszám: 88.56 fő
50 fő alatti kapuk száma: 4
50 és 120 fő közötti kapuk száma: 7
120 fő feletti kapuk száma: 5
Legterheltebb kapu utasszáma: 168 fő
Legkevésbé terhelt kapu utasszáma: 12 fő
A legterheltebb kapu helye: 8. adat
```

---

## 3. feladat – Repülőtéri utasok extra díjainak kezelése

Készítsen Python programot az alábbi leírás alapján!

A feladat végeztével a `.py` kiterjesztésű állományt töltse fel!

A programhoz egy `utasok.csv` nevű állomány tartozik. A fájl minden sora egy repülőtéri utas adatait tartalmazza pontosvesszővel elválasztva.

A CSV-fájl szerkezete:

```txt
nev;jaratszam;poggyaszTomeg;elsobbsegiBeszallas
```

1. Készítsen egy saját osztályt `Utas` néven, amely egy repülőtéri utas adatait tárolja!

2. Az osztályban tárolja el az utas nevét, járatszámát, poggyászának tömegét, az elsőbbségi beszállás igénylését, valamint az utas által fizetendő extra díjat!

3. Készítse el az osztály konstruktorát úgy, hogy az paraméterként kapja meg az utas nevét, járatszámát, poggyászának tömegét és az elsőbbségi beszállás értékét!

4. A konstruktorban számítsa ki automatikusan az utas által fizetendő extra díjat! Ha a poggyász tömege legfeljebb `20` kg, akkor poggyászdíjat nem kell fizetni. Ha a poggyász tömege meghaladja a `20` kg-ot, akkor minden többletkilogramm után `2500` Ft pótdíjat kell felszámolni. Amennyiben az utas elsőbbségi beszállást kért, további `6000` Ft díjat kell hozzáadni a fizetendő összeghez.

5. Készítsen egy `UtasokBetoltese` nevű függvényt, amely beolvassa az `utasok.csv` állomány tartalmát, létrehozza az utasokat, majd az elkészült utasobjektumokat egy listában visszaadja!

6. A program írja ki a konzolra az összes utas nevét, járatszámát, poggyászának tömegét, az elsőbbségi beszállás értékét, valamint a hozzá tartozó fizetendő extra díjat!

7. A beolvasott utasadatok alapján végezze el az alábbi feladatokat!

   a) Számítsa ki, hogy az utasoknak összesen mennyi extra díjat kell fizetniük, majd az eredményt írja ki a konzolra!

   b) Határozza meg, hány olyan utas van, akinek a poggyásza meghaladja a `20` kg-ot!

   c) Keresse meg azt az utast, akinek a legmagasabb a fizetendő extra díja!

   d) Írja ki azoknak az utasoknak a nevét és járatszámát, akik elsőbbségi beszállást kértek!

   e) Vizsgálja meg, hogy van-e olyan utas, akinek a poggyásza legalább `30` kg! Az eredményt írja ki a konzolra!

   f) A legtöbbet fizető utas adatait írja ki egy `legtobbet_fizeto_utas.txt` nevű fájlba az alábbi mintának megfelelő formában:

### Minta konzolkimenet

```txt
Repülőtéri utasok adatai:

Név: Tóth Márk
Járatszám: BA415
Poggyász tömege: 31 kg
Elsőbbségi beszállás: igen
Fizetendő extra díj: 33500 Ft

Név: Kovács Anna
Járatszám: LH220
Poggyász tömege: 18 kg
Elsőbbségi beszállás: nem
Fizetendő extra díj: 0 Ft

Név: Nagy Péter
Járatszám: W62213
Poggyász tömege: 24 kg
Elsőbbségi beszállás: igen
Fizetendő extra díj: 16000 Ft

Az utasok által fizetendő extra díjak összege: 49500 Ft
20 kg feletti poggyásszal utazók száma: 2
A legtöbbet fizető utas: Tóth Márk
Elsőbbségi beszállást kérő utasok:
Tóth Márk - BA415
Nagy Péter - W62213
Van olyan utas, akinek a poggyásza legalább 30 kg.
```

### A `legtobbet_fizeto_utas.txt` állomány mintája

```txt
A legtöbbet fizető utas neve: Tóth Márk
Járatszám: BA415
Poggyász tömege: 31 kg
Elsőbbségi beszállás: igen
Fizetendő extra díj: 33500 Ft
```


## csv

```csv
Tóth Márk;BA415;31;igen
Kovács Anna;LH220;18;nem
Nagy Péter;W62213;24;igen
Szabó Lilla;FR839;20;nem
Horváth Bence;KL118;27;nem
Farkas Eszter;AF302;16;igen
Varga Dániel;W62245;34;igen
Molnár Réka;BA415;22;nem
Kiss Gergő;LH220;19;igen
Balogh Zsófia;FR839;29;nem
Németh Ádám;KL118;21;nem
Papp Júlia;AF302;25;igen
```
