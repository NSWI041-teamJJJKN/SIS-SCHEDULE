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

## Test pro Usecase "Zobrazit výsledky specifických anket učiteli"
Vytvořil Jan Jevčák

### Test conditions
C1 Anketa je vytvořena

C2 Anketa není vytvořena

C3 Učitel se úspěšně přihlásí do systému

C4 Učiteli se nepodaří přihlásit do systému

C5 Otevření modulu anket

C6 Zobrazení všech anket

C7 Zovrazení jedné ankety použitím filtrování

C8 Zovbrazení více anket použitím filtrování

C9 Zobrazení odpovědí pro anketu


### Test cases
||||||
|---|---|---|---|---|
| ID | 1 ||||
| Title | Zobrazení ankety jednoho předmětu ||||
| Priority | - ||||
| Preconditions | Anketa je vytvořena ||||
| Postconditions | - ||||
| Role | Učitel ||||
| Test data | - ||||
| Covered test conditions | C3, C5, C7 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Uživatel načte v prohlížeči stránku SISu | Systém zobrazí domovskou obrazovku SISu ||||
| 2 | Uživatel zadá své přihlašovací jméno a heslo, klikne na tlačítko [Přihlásit] | Systém uživatele přihlásí ||||
| 3 | Uživatel klikne na tlačítko [Anketa] | Systém zobrazí seznam dostupných anket ||||
| 4 | Uživatel vyhledá anketu pro předmět [Úvod do softwarového inženýrství] | Systém zobrazí výsledky vyhledávání. ||||
| 5 | Uživatel zkontroluje vyhledané výsledky. | Systém zobrazil jeden výsledek - předmět "Úvod do sofwarového inženýrství" ||||


||||||
|---|---|---|---|---|
| ID | 2 ||||
| Title | Zobrazení výsledků ankety ||||
| Priority | - ||||
| Preconditions | Existuje jedna anketa s dvěma odpověďmi studentů ||||
| Postconditions | - ||||
| Role | Učitel ||||
| Test data | - ||||
| Covered test conditions | C3, C5, C6, C9 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Uživatel načte v prohlížeči stránku SISu | Systém zobrazí domovskou obrazovku SISu ||||
| 2 | Uživatel zadá své přihlašovací jméno a heslo, klikne na tlačítko [Přihlásit] | Systém uživatele přihlásí ||||
| 3 | Uživatel klikne na tlačítko [Anketa] | Systém zobrazí seznam dostupných anket ||||
| 4 | Uživatel zkontroluje zobrazené ankety | Je zobrazena jedna anketa ||||
| 5 | Uživatel klikne na první zobrazenou anketu | Systém zobrazí odpovědi pro danou anketu ||||
| 6 | Uživatel zkontroluje odpovědi pro danou anketu | Daná anketa obsahuje právě 2 odpovědi ||||

___

## Test pro Usecase Vytvořit specifickou anketu
Vytvořil Štof

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
