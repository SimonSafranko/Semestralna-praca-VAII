CarSellAndCompare – Online autobazár

Meno a priezvisko študenta: Šimon Šafranko  
Študijná skupina: 5ZYI32

Stručný opis projektu

CarSellAndCompare je webová aplikácia fungujúca ako online autobazár, ktorá umožňuje používateľom vyhľadávať a prezerať ponuky automobilov. Používatelia môžu vozidlá filtrovať podľa základných parametrov, ako sú značka, model, cena, rok výroby, počet najazdených kilometrov, typ paliva alebo prevodovka. Pri každom vozidle sú dostupné podrobné informácie, fotografie a údaje o predajcovi.

Hlavnou pridanou hodnotou aplikácie je možnosť porovnávania viacerých vozidiel priamo na stránke. Používateľ si môže vybrať viacero automobilov z dostupných ponúk a následne ich porovnať v prehľadnej tabuľke podľa ich základných parametrov. Registrovaní používatelia môžu zároveň pridávať vlastné ponuky automobilov a komunikovať so záujemcami prostredníctvom správ.

Role v projekte

Návštevník

Návštevník môže používať verejne dostupnú časť aplikácie bez prihlásenia.

- prezerá ponuky automobilov,
- vyhľadáva a filtruje automobily,
- zobrazuje detail automobilu,
- porovnáva automobily,

Registrovaný používateľ

Registrovaný používateľ má prístup k funkciám, ktoré vyžadujú prihlásenie.

- prezerá, vyhľadáva a porovnáva automobily,
- vytvára vlastné ponuky automobilov,
- upravuje a maže vlastné ponuky,
- pridáva fotografie k svojim ponukám,
- komunikuje s ostatnými používateľmi prostredníctvom správ,
- spravuje svoje používateľské údaje.

Administrátor

Administrátor zodpovedá za správu aplikácie a jej obsahu.

- spravuje používateľov,
- spravuje ponuky automobilov,
- upravuje alebo odstraňuje nevhodné ponuky,
- spravuje obsah aplikácie,
- dohliada na komunikáciu a obsah vytvorený používateľmi.

Prípady použitia podľa rolí

Návštevník

- vyhľadá automobil,
- filtruje ponuky automobilov,
- zobrazí zoznam automobilov,
- zobrazí detail automobilu,
- vyberie automobily na porovnanie,
- porovná vybrané automobily,

Registrovaný používateľ

- zaregistruje sa,
- prihlási sa,
- odhlási sa,
- upraví svoje údaje,
- vytvorí ponuku automobilu,
- upraví vlastnú ponuku,
- odstráni vlastnú ponuku,
- pridá fotografie k ponuke,
- zobrazí svoje ponuky,
- odošle správu predajcovi,
- zobrazí prijaté a odoslané správy,
- upraví vlastnú správu,
- odstráni vlastnú správu,
- pridá automobil medzi obľúbené,
- odstráni automobil z obľúbených.

Administrátor

- prihlási sa do administrácie,
- zobrazí zoznam používateľov,
- upraví alebo odstráni používateľa,
- zobrazí všetky ponuky automobilov,
- upraví ponuku,
- odstráni ponuku,
- zobrazí správy,
- odstráni nevhodný obsah.

Plánované entity

Automobil (`Car`)

Hlavná entita aplikácie reprezentujúca automobil ponúkaný na predaj.

Hlavné atribúty:
- ID
- používateľ
- značka
- model
- rok výroby
- cena
- počet najazdených kilometrov
- typ paliva
- prevodovka
- výkon
- objem motora
- typ karosérie
- popis
- dátum vytvorenia

Jeden používateľ môže vytvoriť viac automobilov.

Správa (`Message`)

Reprezentuje komunikáciu medzi používateľmi týkajúcu sa konkrétneho automobilu.

Hlavné atribúty:
- ID
- automobil
- odosielateľ
- príjemca
- text správy
- dátum vytvorenia

Správa je vždy spojená s konkrétnym automobilom.

Fotografia (`Image`)

Obsahuje fotografiu priradenú ku konkrétnemu automobilu.

Hlavné atribúty:
- ID
- automobil
- názov súboru
- cesta k súboru
- dátum vytvorenia

Jeden automobil môže mať viac fotografií.

Obľúbený automobil (`Favorite`)

Slúži na uloženie automobilu medzi obľúbené konkrétneho používateľa.

Hlavné atribúty:
- ID
- používateľ
- automobil
- dátum pridania

Používateľ môže mať viac obľúbených automobilov.

Vzťahy medzi entitami

- Používateľ – Automobil (1:N): Jeden používateľ môže vytvoriť viac ponúk automobilov. Každý automobil patrí používateľovi, ktorý ho vytvoril.

- Automobil – Správa (1:N): Jeden automobil môže mať viac správ od rôznych používateľov. Každá správa sa vzťahuje na jeden konkrétny automobil.

- Automobil – Fotografia (1:N): Jeden automobil môže mať viac fotografií. Každá fotografia patrí ku konkrétnemu automobilu.

- Používateľ – Správa (1:N): Používateľ môže odoslať a prijať viac správ.

- Používateľ – Automobil (M:N cez Obľúbený automobil): Používateľ si môže uložiť viac automobilov medzi obľúbené a jeden automobil môže byť uložený medzi obľúbené viacerými používateľmi.

Hlavné stránky aplikácie

1. Domovská stránka

Úvodná stránka aplikácie s krátkym predstavením CarSellAndCompare a základným vyhľadávaním automobilov.

2. Zoznam automobilov

Zobrazuje dostupné ponuky automobilov. Používateľ môže ponuky vyhľadávať, filtrovať a zoradiť.

3. Detail automobilu

Zobrazuje podrobné informácie o automobile, jeho fotografie, cenu, technické parametre a informácie o predajcovi. Registrovaný používateľ môže z tejto stránky kontaktovať predajcu.

4. Porovnanie automobilov

Zobrazuje vybrané automobily vedľa seba v porovnávacej tabuľke. Používateľ môže porovnať napríklad cenu, rok výroby, počet kilometrov, výkon, palivo a prevodovku.

5. Moje ponuky

Stránka pre registrovaného používateľa, na ktorej môže vytvárať, upravovať a mazať svoje ponuky automobilov a spravovať ich fotografie.

6. Správy

Stránka určená na komunikáciu medzi používateľmi. Zobrazuje prijaté a odoslané správy a umožňuje ich správu.

7. Obľúbené automobily

Zobrazuje automobily, ktoré si používateľ uložil medzi obľúbené.

8. Administrácia

Stránka dostupná administrátorovi na správu používateľov, automobilov a obsahu aplikácie.

Rozdelenie funkcionality

Základné funkcie

- registrácia a prihlásenie používateľa,
- zobrazenie ponúk automobilov,
- vyhľadávanie a filtrovanie automobilov,
- zobrazenie detailu automobilu,
- vytvorenie ponuky automobilu,
- úprava vlastnej ponuky,
- odstránenie vlastnej ponuky,
- pridávanie a správa fotografií,
- porovnávanie automobilov,
- vytváranie a správa správ,
- pridávanie a odstraňovanie obľúbených automobilov,
- administrácia používateľov a ponúk.

Rozširujúce funkcie

- upozornenia na zmenu ceny automobilu,
- história zmien ceny,
- hodnotenie predajcov,
- komentáre k ponukám
