# Propunere standardizare tooling

## Scopuri

Tool-urile folosite in cadrul laboratorului de PA dau dovada de o dependenta de tematica care nu permite refolosirea acestora si genereaza un proces de reinventare a rotii in fiecare an. Este un model care duce la concetrarea unei parti mari din concentrare pe rezolvarea de probleme in cod in loc de a scrie probleme mai interesanta.

Scopul tooling-ului ar trebui sa fie usurarea procesului de corectare a temelor, a obtinerii rezultatelor mai rapid pentru a dedica mai mult timp rezolvarii greselilor si de a pierde cat mai putine din greseli pentru a nu lasa studentul cu lacune in gandire si ignorata despre posibile greseli.

## Ideologie de proiectare

In proiectarea tooling-ului putem descrie cateva principii care sa ne ghideze pentru a produce cod folositor cu adevarat:

- Modularizarea codului: codul deja scris ar trebui sa poata fi integrat in alte tool-uri mai usor si fara a trebui modificat
  
- Bine documentat: documentatia buna permite refolosirea codului chiar si dupa ce autorul original inceteaza contributia la acesta
  
- Standardizat: limbaje standard permit integrarea mai usoara a viitoarelor feature-uri, iar o syntaxa standard ne permite intelegerea mai usoara si utilizarea/modificarea a tool-urilor deja scrise
  
- Centralizat: toate tool-urile ar trebui centralizate intr-o sursa a materiei prin copierea acestora. Atfel, un singur tool poate fi folosit mai multe generatii la rand.
  

## Mod de dezvoltare

### Workflow si SDCL

### Limbaje

Se propune separarea posibilului cod in trei posibile scopuri:

- in dezvoltare: codul este in testare din punct de vedere aplicativ. Se testeaza daca poate fi aplicat si daca are un scop.
  
- in utilizare: exista o nevoie pentru un anume tool si acesta este prin urmare dezvoltat pentru utilizare continuua
  
- de interfata: script-uri si mici automatizari care sunt rulate in interiorul altor tool-uri (embedded).
  

Pentru fiecare din acestea se propune folosirea urmatoarelor limbaje, cu posibilitatea ca acestea sa fie modificate/adaugite in cazul in care exista nevoi:

- pentru dezvoltare: Python. Este nevoie de un limbaj usor de scris, pentru care exista destul de mult suport si pachete. In acest moment se testeaza ideea si logica din spatele acesteia
  
- pentru utilizare: C, C++, Nim. Cele trei sunt complet compatibile si se pot compila in cod masina. Dupa acestea pot fi utilizate independent cat si integrate una in cealalta. Codul este reutilizabil si exista suport pentru majoritatea aplicatiilor posibile. (exemple de exceptii -> webapps, dar Nim se poate compila atat in C/C++ cat si Javascript)
  
- de interfata: Lua. Puterea de a da embed usor limbajului in C/C++ permite integrarea acestuia in toate utilitarele menite sa fie utilizate constant
