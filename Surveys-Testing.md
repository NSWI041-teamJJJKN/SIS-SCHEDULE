# Testy pro modul Ankety 


## Test pro Usecase xyz
Vytvořil Pepa Novák

### Test conditions
C1 ... 

C2 ...

C3 ...

C4 ...


### Test cases
||||||
|---|---|---|---|---|
| ID | 1 ||||
| Title | Titulek ||||
| Priority | - ||||
| Preconditions | Vstupní podmínky ||||
| Postconditions | Výstupní podmínky ||||
| Role | Role ||||
| Test data | - ||||
| Covered test conditions | C1, C2 & C3 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Akce 1 | Výsledek 1 ||||
| 2 | Akce 2 | Výsledek 2 ||||
| 3 | Akce 3 | Výsledek 3 ||||
| 4 | Akce 4 | Výsledek 4 ||||


||||||
|---|---|---|---|---|
| ID | 2 ||||
| Title | Titulek ||||
| Priority | - ||||
| Preconditions | Vstupní podmínky ||||
| Postconditions | Výstupní podmínky ||||
| Role | Role ||||
| Test data | - ||||
| Covered test conditions | C4 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Akce 1 | Výsledek 1 ||||
| 2 | Akce 2 | Výsledek 2 ||||
| 3 | Akce 3 | Výsledek 3 ||||
| 4 | Akce 4 | Výsledek 4 ||||

___

## Test pro Usecase Vytvořit specifickou anketu
Vytvořil Štof

### Test conditions
C1 - Učitel se dokáže přihlásit do systému 

C2 - Učitel dokáže otevřít anketní modul

C3 - Systém vypíše všechny učitelem vyučované předměty

C4 - Učitel dokáže zvolit svůj předmět a založit pro něj specifickou anketu

C5 - Učitel dokáže vytvořit číselnou otázku

C6 - Učitel dokáže vytvořit textovou otázku

C7 - Učitel dokáže nastavit otázkám parametry
   - C7a - otázka má zadání
   - C7b - otázka má parametr povinnosti vyplnit
   - C7c - textové otázce lze nastavit filtr zabanovaných slov

C8 - Učitel dokáže anketě parametr - deadline

C9 - Učitel dokáže anketu odeslat ke zpracování

C10 - Systém dokáže ověřit korektnost přijaté ankety
   - C10a - anketa obsahuje alespoň 1 otázku
   - C10b - deadline ankety se nachází v budoucnu
   - C10c - každá otázka má zadání

C11 - Systém vrátí učiteli přijatou nekorektní anketu k opravě

C12 - Systém přijatou korektní anketu zařadí do paměti, a zpřístupní ji k vyplnění zapsaným studentům

<br>

### Test cases
||||||
|---|---|---|---|---|
| ID | 1 ||||
| Title | Vytvoření korektní ankety ||||
| Priority | Normal ||||
| Preconditions | Učitel, jež vyučuje aspoň 1 předmět, je přihlášen v systému a má otevřen modul ankety ||||
| Postconditions | - ||||
| Role | Učitel ||||
| Test data | - ||||
| Covered test conditions | C3, C4, C5, C7a, C8, C9, C10, C12 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Učitel klikne na tlačítko výpis předmětů | Zobrazí se seznam předmětů, jež učitel vyučuje. Díky Preconditions alespoň jeden takový existuje ||||
| 2 | Učitel vybere první předmět v seznamu a stiskne volbu "Vytvořit specifickou anketu" | Zobrazí se prostředí tvorby specifické ankety ||||
| 3 | Učitel vytvoří číselnou otázku, ke které napíše zadání "Test1" | Otázka je přidána ||||
| 4 | Učitel nastaví deadline na zítřejší datum | Parametr deadline je nastaven ||||
| 5 | Učitel stiskne tlačítko odeslání otázky | Otázka je odesílána do systému. Ovládací prvky zešednou ||||
| 6 | Systém provede ověření přijaté ankety | Anketa je ověřena a vyhodnocena jako korektní ||||
| 7 | Systém anketu uveřejní | Učitel je přesměrován zpět na domovskou stránku modulu Ankety. Anketa je uveřejněna v systému ||||


||||||
|---|---|---|---|---|
| ID | 2 ||||
| Title | Vytvoření zcela nekorektní ankety ||||
| Priority | Normal ||||
| Preconditions | Učitel, jež vyučuje aspoň 1 předmět, je přihlášen v systému a má otevřen modul ankety ||||
| Postconditions | - ||||
| Role | Učitel ||||
| Test data | - ||||
| Covered test conditions | C3, C4, C9, C10, C11 ||||
| Test steps |||||
| 1 | Učitel klikne na tlačítko výpis předmětů | Zobrazí se seznam předmětů, jež učitel vyučuje. Díky Preconditions alespoň jeden takový existuje ||||
| 2 | Učitel vybere první předmět v seznamu a stiskne volbu "Vytvořit specifickou anketu" | Zobrazí se prostředí tvorby specifické ankety ||||
| 4 | Učitel stiskne tlačítko odeslání otázky | Otázka je odesílána do systému. Ovládací prvky zešednou ||||
| 5 | Systém provede ověření přijaté ankety | Anketa je ověřena a vyhodnocena jako nekorektní ||||
| 6 | Systém anketu vrátí k opravě | Ovládací prvky se znovu zaktivují a učiteli je vypsána hláška, že anketa neobsahuje žádnou otázku a že nemá nastaven validní deadline ||||