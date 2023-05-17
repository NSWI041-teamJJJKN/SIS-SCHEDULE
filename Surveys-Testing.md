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

## Test pro Usecase Vyplnit generickou anketu pro předmět
Vytvořila Nicol

### Test conditions
C1 Anketa sa vytvorila 

C2 Dnesny datum nie je skorsi nez datum vyplnovania

C3 Dnesny datum nie je neskorsi nez datum vyplnovania

C4 student je zapisany na predmet

C5 student je prihlaseny v systeme

C6 spravne sa ukazuju vsetky ankety

C7 filter zonamu ankiet funguje spravne

C8 otvorí sa spravna anketa

C9 anketa sa vsetkym zobrazuje anonymne

C10 Ostatny studenti vidia ankety odkliknute ako viditelne

C11 Ostatny studenti nevidia ankety neodkliknute ako viditelne

C12 anketa sa odoslala

C13 povinne polia ankety su vyplnene 

C14 system spravne zobrazuje uz v minulosti rozpracovanu anketu

C15 chybajuca odpoved v ankete je zvyraznena

C16 vsetky odpovede studenta su zaznamenane

C17 filter neobsahujuci ziadne ankety da oznamenie

C18 odpovede sa zobrazuju vyucujucim

### Test cases
||||||
|---|---|---|---|---|
| ID | 1 ||||
| Title | Student si zobrazuje vsetky zverejnene odpovede k danej ankete ||||
| Priority | High ||||
| Preconditions | Student je prihlaseny do SISu, anketa ma odoslanych niekolko typov odpovedi od inych studentov - niektore su anonymne, neverejne ||||
| Postconditions | Výstupní podmínky ||||
| Role | Student ||||
| Test data | - ||||
| Covered test conditions | C8, C9, C10, C11 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Uzivatel otvori stranku v SISe s anketami | Je nacitana stranka pro ankety ||||
| 2 | Uzivatel klikne na konkretnu anketu ktoru chce zobrazit | Zobrazi sa obsah spravnej ankety ||||
| 3 | Uzivatel stlaci tlacidlo "zobrazit odpovede" | Zobrazi sa zoznam odoslanych odpovedi ktore su verejne a kde niektory autori su anonymny ||||


||||||
|---|---|---|---|---|
| ID | 2 ||||
| Title | Student pri vyplnani ankety nevyplni povinne policko ||||
| Priority | High ||||
| Preconditions | Student je prihlaseny,je obdobie vyplnovania||||
| Postconditions | Výstupní podmínky ||||
| Role | Student ||||
| Test data | - ||||
| Covered test conditions | C13, C14, C15 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Uzivatel otvori stranku pre ankety v sise| Prehlidac otvori pozadovanu stranku a zobrazi zoznam ankiet ||||
| 2 | Uzivatel klikne na konkretnu anketu | Otvori sa mu anketa s otazkami a uz vyplnenymi odpovedmi z minulosti - ak este neboli vyplnene tak bez odpovede ||||
| 3 | Uzivatel ciastocne vyplni anketu a vynecha 1 povinnu odpoved | stranka zobrazuje vsetky jeho odpovede na otazky v ankete ||||
| 4 | Uzivatel odosle odpovede | system ho vrati na anketu obsahujucu odpovede ktore vyplnil pred odoslanim a zvyrazni vynechanu povinnu otazku ||||

___