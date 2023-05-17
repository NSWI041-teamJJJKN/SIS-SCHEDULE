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


## Test pro Usecase Vytvoření generické ankety
Vytvořil Jaroslav Švarc

### Test conditions
C1 - Není zkouškové období

C2 - Je zkouškové období

C3 - Vedoucí katedry je přihlášen do systému

C4 - Vedoucí katedry není přihlášen do systému

C5 - Vedoucí katedry otevře modul anket 

C6 - Vedoucí katedry se přesune do části pro vytváření anket

C7 - Vedoucí katedry vytvoří číselnou otázku

C8 - Vedoucí katedry vytvoří slovní otázku

C9 - Vedoucí katedry nevytvoří žádnou otázku

C10 - U otázky lze zvolit, zda-li je otázka povinná

C11 - U otázky lze nastavit filtrování obsahu

C12 - Anketa obsahuje alespoň jednu otázku 

C13 - Je možné vyřadit některé předměty z ankety

C14 - Systém si uloží generickou anketu

C15 - Na začátku zkouškového období vytvoří systém anketu pro všechny vyučované  předměty, 

C16 - Na začátku zkouškového období zpřístupní nově vytvořenou anketu studentům k vyplnění

C17 - Na začátku zkouškového období přidá velký červený banner do kalendáře deadlinů

C18 - Vedoucí katedry se pokusí ankety zadat po začátku zkouškového období

C19 - Vedoucí katedry se pokusí ankety zadat před začátkem zkouškového období

C20 - Systém nedovolí přistoupit na formulář pro vygenerování generických anket neboť právě probíhají

### Test cases
||||||
|---|---|---|---|---|
| ID | 1 ||||
| Title | Vytvoření ankety s povinnou slovní otázkou ||||
| Priority | - High ||||
| Preconditions | Zkouškové období semestru, pro který chceme vytvořit generické ankety, doposud nezapočalo||||
| Postconditions | Anketa vytvořena||||
| Role | Vedoucí katedry ||||
| Test data | - ||||
| Covered test conditions | C3, C5, C6, C8, C10, C12, C14,  ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Vedoucí katedry se přihlásí do systému  | Vedoucí katedry je přihlášen  ||||
| 2 | Vedoucí katedry otevře modul anket  | Modul je úspěšně otevřen ||||
| 3 | Vedoucí katedry se přesune do části pro vytváření anket | Šablona ankety úspěšně otevřena ||||
| 4 |Vedoucí katedry přidá slovní otázku| Otázka úspěšně přidána ||||
| 5 |Vedoucí katedry označí otazku jako povinnou| Otázka je nastavena jako povinná ||||
| 6 |Vedoucí katedry uloží anketu| Anketa zkontroluje existenci alespoň jedné otázky a anketa je uložena ||||


||||||
|---|---|---|---|---|
| ID | 2 ||||
| Title | Neúspěšné vytvoření ankety ||||
| Priority | - High ||||
| Preconditions | Je zkouškové období a právě probíhají ankety ||||
| Postconditions | Systém nedovolí vytvořit anketu pro současné zkouškové období ||||
| Role | Vedoucí katedry ||||
| Test data | - ||||
| Covered test conditions | C2, C3, C5, C6, C18, C20  ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Vedoucí katedry se přihlásí do systému  | Vedoucí katedry je přihlášen  ||||
| 2 | Vedoucí katedry otevře modul anket  | Modul je úspěšně otevřen ||||
| 3 | Vedoucí katedry se přesune do části pro vytváření anket | Systém zamítne vytvořit anketu pro dané zkouškové období ||||


___