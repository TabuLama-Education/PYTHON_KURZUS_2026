## 1. Feladat: Mozi jegyértékesítő rendszer

Készíts egy programot, amely egy mozi jegyeladási folyamatát szimulálja! A program ellenőrizze a film elérhetőségét, kérje be a kedvezmény típusát, majd számolja ki a fizetendő összeget.

### Adatok

```python
filmek = ["Dűne", "Batman", "Shrek", "Eredet"]
eladott_jegyek = []

alap_ar = 2400  # Ft

```

### A program működése

1. **Adatbekérés és validálás:** - Kérd be a **film címét**. Ha a film **nincs** a `filmek` listában, írd ki: `"A film jelenleg nem játszható."`, és a program **azonnal lépjen ki**.
* Kérd be a **vásárló kategóriáját** (lehetséges értékek: `diak`, `nyugdijas`, `felnott`).


2. **Jegyár számítás:**
* Ha `diak`: 30% kedvezmény jár az alapárból.
* Ha `nyugdijas`: 40% kedvezmény jár az alapárból.
* Ha `felnott`: nincs kedvezmény (teljes ár).
* Ha bármi más kategóriát ad meg, a kedvezmény legyen **0%**, és írja ki: `"Érvénytelen kategória, teljes árú jegyet számolunk."`


3. **Köztes művelet:**
* Add hozzá az `eladott_jegyek` listához a vásárlást `[film_címe, kategoria]` formátumban.


4. **Kimenet:**
* Írd ki a fizetendő összeget Ft-ban.
* Írd ki az aktuális eladási listát.



### Példa futásra (Érvényes kedvezmény)

```text
Melyik filmre kér jegyet? Dűne
Adja meg a kategóriát (diak/nyugdijas/felnott): diak

Sikeres vásárlás!
Fizetendő összeg: 1680 Ft
Eladott jegyek listája: [['Dűne', 'diak']]

```

