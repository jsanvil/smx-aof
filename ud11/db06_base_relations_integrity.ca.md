UD11: Bases de dades (I)

# 6. *LibreOffice Base*: Relacions entre taules. Integritat referencial

## 馃幆 Objectius

- Con茅ixer el concepte de relaci贸.
- Con茅ixer el concepte de clau aliena.
- Crear i utilitzar relacions entre taules.
- Concepte d'integritat referencial.
- Comprovaci贸 de la integritat referencial.

---

# 6.1 Bases de dades relacionals

Base, tal com es va comentar amb anterioritat, 茅s un **gestor de base de dades relacional**, entre altres coses, perqu猫 permet establir **vincles o relacions entre les taules** que el componen. L'objectiu d'aquestes relacions ser脿 principalment **evitar la duplicitat d'informaci贸** i en conseq眉猫ncia, **optimitzar el rendiment** de la base de dades.

---

# 6.2 Relacions entre taules

Despr茅s de crear taules diferents en la base de dades, necessitem una manera d'indicar-li a *Base* com ha de combinar aquesta informaci贸.

El primer pas d'aquest proc茅s 茅s definir relacions entre les taules. Una vegada realitzada aquesta operaci贸, podem crear consultes, formularis i informes per a mostrar informaci贸 de diverses taules alhora.

**Una relaci贸 fa coincidir les dades dels camps clau** (normalment un camp amb el mateix nom en totes dues taules). En la majoria dels casos, aquests camps coincidents s贸n la **clau principal** d'una taula, que proporciona un identificador 煤nic per a cada registre, i una **clau aliena o externa** de l'altra taula.

---

## *Exemple pr脿ctic: centre educatiu*

Per a explicar-ho, mostrarem un exemple de base de dades d'un centre educatiu amb dues taules com s贸n `Alumnes` i `Grups`. Inicialment estaran definides de la seg眉ent manera:

 Alumnes       | Grups
 --------------|--------------
 Expedient     | Denominacio
 Nom           | NombreAlumnes
 Cognoms       | Ubicacio
 DataNaixement | Observacions
 Grup          |
 UbicacioGrup  |
 ObservacionsGrup |

En la taula `Alumnes` tenim tota la informaci贸 que necessitem sobre els nostres alumnes com:

- El seu n煤mero d'expedient.
- El seu nom i cognoms.
- La seua data de naixement.
- El grup al qual pertany l'alumne.
- La ubicaci贸 del grup, 茅s a dir, l'aula on estan els alumnes d'aqueix grup *(Primera planta, edifici annex, etc)*.
- Qualsevol tipus de comentari d'inter茅s.

Per a la taula `Grups` tenim:

- Denominaci贸 del grup: *1SMX-D, 2SMX-D, 1ASIR-A, 1DAW-SEMI, etc.*
- Nombre total d'alumnes que t茅 el grup.
- El lloc on est脿 situat: Planta baixa*, Primera planta, Segona planta, etc.*
- Qualsevol altra dada d'inter茅s: *Refor莽, Suport, etc.*

Si ens fixem en les dades podem adonar-nos que, en comprovar les dades incloses en les taules d'Alumnes i Grups, existeix **informaci贸 que es repeteix** en ambdues:

### ALUMNES

Expedient | Nom    | Cognoms      | DataNaixement | Grup        | UbicacioGrup      | ObservacionsGrup
----------|--------|--------------|---------------|-------------|-------------------|------------------
3256      | Jos茅   | P茅rez Garc铆a | 27/07/04      | *1SMX-D*    | **Planta baixa**  | **Refro莽**
3259      | Juan   | S谩nchez Pla  | 17/02/06      | *1SMX-D*    | **Planta Baixa**  | **Refor莽**
3272      | Felipe | Sainz Paso   | 21/09/05      | *2ASIR-A*   | **Segona Planta** | **Taller**
3261      | Mar铆a  | Delgado Vila | 01/10/03      | *1DAW-SEMI* | **Semi**          | **Remot**

### GRUPS

Denominacio | NombreAlumnes | Ubicacio             | Observacions
------------|---------------|----------------------|---------------
1SMX-D      | 24            | ***Planta baixa***   | ***Refro莽***
2SMX-D      | 19            | Segona Planta        | Cap
2ASIR-A     | 20            | ***Segona Planta***  | ***Taller***
1DAW-SEMI   | 27            | ***Semi***           | ***Remot***

Aquesta situaci贸 no 茅s massa favorable quan treballem amb bases de dades on habitualment la quantitat d'informaci贸 que es maneja 茅s important.**La soluci贸 passa per relacionar les taules amb informaci贸 coincident de manera que no existisca duplicitat d'informaci贸**. Tot aix貌, tradu茂t a un llenguatge m茅s natural seria: "Per a qu猫 escriure dues vegades el mateix, si puc fer-ho una sola i treballar de la mateixa manera".

 Alumnes       | Grups
 --------------|------
 Expedient     | Denominacio
 Nom           | NombreAlumnes
 Cognoms       | Ubicacio
 DataNaixement | Observacions
 Grup          |
 *x* *~~UbicacioGrup~~*     |
 *x* *~~ObservacionsGrup~~* |

Tornant al nostre exemple, si relacionem les taules `Alumnes` i `Grups` mitjan莽ant el nom del grup seria suficient amb indicar en la taula `Alumnes` aquest valor per a obtindre el nombre d'alumnes del grup, la seua ubicaci贸 i les possibles observacions:

### `ALUMNES`

Expedient | Nom    | Cognoms      | DataNaixement | *Grup*      | *~~UbicacioGrup~~*  | *~~ObservacionsGrup~~*
----------|--------|--------------|---------------|-------------|---------------------|------------------
3256      | Jos茅   | P茅rez Garc铆a | 27/07/04      | *1SMX-D*    | *~~Planta baixa~~*  | *~~Refro莽~~*
3259      | Juan   | S谩nchez Pla  | 17/02/06      | *1SMX-D*    | *~~Planta Baixa~~*  | *~~Refor莽~~*
3272      | Felipe | Sainz Paso   | 21/09/05      | *2ASIR-A*   | *~~Segona Planta~~* | *~~Taller~~*
3261      | Mar铆a  | Delgado Vila | 01/10/03      | *1DAW-SEMI* | *~~Semi~~*          | *~~Remot~~*

### `GRUPS`

Denominacio | NombreAlumnes | Ubicacio             | Observacions
------------|---------------|----------------------|---------------
1SMX-D      | 24            | ***Planta baixa***   | ***Refro莽***
2SMX-D      | 19            | Segona Planta        | Cap
2ASIR-A     | 20            | ***Segona Planta***  | ***Taller***
1DAW-SEMI   | 27            | ***Semi***           | ***Remot***

---

# 6.3 Tipus de relacions

Les condicions per a establir vincles entre dues taules no s贸n sempre iguals, ja que la manera en qu猫 es relacionen les taules entre si dona lloc a comportaments diferents. En l'estructura de qualsevol base de dades trobem principalment **tres tipus de relacions** que es descriuen de la seg眉ent manera:

- **Un a molts** `(1:N)`
- **Un a un** `(1:1)`
- **Molts a molts** `(N:N)`

## 6.3.1 Relaci贸 `un a molts` `(1:N)`

Aquest tipus es dona quan una fila de la primera taula pot estar relacionada amb moltes files de la segona taula, per貌 una fila de la segona nom茅s est脿 relacionada amb una de la primera.

### *Exemple. Base de dades d'un centre educatiu `(1:N)`*

Si tornem a la base de dades d'un centre educatiu amb dues taules com s贸n `Alumnes` i `Grups`, tenim que:

- Donat `1 alumne`, nom茅s pot pert脿nyer a `1 grup`.
- Donat `1 grup`, pot tindre `molts alumnes`.

### *Altres exemples `(1:N)`*

Altre exemple d'aquesta mena de relacions podria ser entre una taula amb 脿rbitres i una altra amb partits de tennis, ja que:

- Donat `1 脿rbitre`, pot haver arbitrat `molts partits` de tennis.
- Donat `1 partit` de tennis, nom茅s ha sigut arbitrat per `1 脿rbitre`.

## 6.3.2 Relaci贸 `un a un` `(1:1)`

Aquest tipus de relaci贸 apareix amb menys freq眉猫ncia i succeeix quan una fila de la primera taula nom茅s pot estar relacionada amb una fila de la segona i una fila de la segona taula nom茅s pot estar relacionada amb una de la primera.

### *Exemple. Base de dades d'un centre educatiu `(1:1)`*

Si tornem a la base de dades d'un centre educatiu, tenim que un altre exemple seria el d'un tutor amb un grup:

- Cada `grup` nom茅s pot tindre `1 tutor`
- Cada `tutor` nom茅s pot tindre `1 grup`

```text
                       1                      1 
        +------------+                          +-------------+
        |    GRUP    | <----------------------> |    TUTOR    |
        +------------+                          +-------------+
```

### *Altres exemples `(1:1)`*

Altre exemple d'aquesta mena de relacions podria ser entre una taula amb pa茂sos i una altra amb caps de govern:

- Donat `1 pa铆s` nom茅s t茅 `1 cap de govern` *(normalment)*.
- Donat `1 cap de govern`, ho 茅s nom茅s de `1 pa铆s`.

## 6.3.3. Relaci贸 `molts a molts` `(N:N)`

Aquesta classe de relaci贸 ocorre quan una fila de la primera taula pot estar relacionada amb moltes files de la segona taula i una fila de la segona taula pot estar-ho amb moltes files de la primera.

Aquest tipus de relaci贸 nom茅s 茅s possible si **es defineix una tercera taula** (denominada taula d'uni贸) **la clau principal de la qual consta d'almenys dos camps**: ***les claus externes de les Taules `A` i `B`***. Posteriorment tractarem el concepte de clau aliena o externa.

### *Exemple. Base de dades d'un centre educatiu `(N:N)`*

Si tornem a la base de dades d'un centre educatiu, tenim que un altre exemple seria el d'un institut on les taules `PROFESSORS` i `GRUPS` estan relacionades:

- `1 professor` pot impartir classe a `molts grups`
- `1 grup` pot tindre `molts professors`

```text
                         N                           N 
        +--------------+                               +--------------+
        |   PROFESSOR  | <---------------------------> |     GRUP     |
        +--------------+                               +--------------+
```

### *Altres exemples `(N:N)`*

Altre exemple d'aquest tipus el tenim en la relaci贸 entre una taula amb pel路l铆cules i una taula amb int猫rprets (actors) perqu猫:

- Feta `1 pel路l铆cula` en particular, pot tindre `molts actors`
- Donat `1 actor`, aquest pot haver intervingut en `moltes pel路l铆cules`

---

# 6.4 Relacions en la base de dades de "*Biblioteca*"

Si ens fixem en la base de dades `Biblioteca` podem veure que s'est脿 repetint el mateix valor moltes vegades: per exemple, el valor de suport `Paper` apareix en diverses files. 脡s a dir, en introduir el mateix valor de manera redundant s'est脿 possibilitant que en algun moment l'escriguem malament, per exemple, `Papek`, i tinguem un nou suport que no correspon a cap llibre, ja que ni tan sols existeix.

Pot oc贸rrer tamb茅 que tots els t猫cnics de biblioteconomia es posen d'acord i decidisquen que el suport `Paper` no t茅 un nom adequat i que 茅s millor anomenar-lo `Paper-cl脿ssic`. Llavors, en la taula `LLIBRE`, s'ha d'anar un a un canviant el nom i amb cura de no equivocar-se en teclejar. Potser si tenim quatre llibres en aquest suport no ens semble un gran inconvenient fer aquest canvi quatre vegades, per貌 si resulta que 茅s una col路lecci贸 de tres-cents llibres d'aquest suport pot ser que l'esfor莽 semble m茅s important.

La soluci贸 als problemes anteriors est脿 a **separar la informaci贸 que apareix repetida** cont铆nuament en una nova taula `SUPORT` i indicar d'alguna forma en la nostra base de dades que hi ha files de la taula `LLIBRE` i de la taula `SUPORT` que estan relacionades.

---

# 6.5 Establir una relaci贸 `un a molts` `(1:N)`

A l'hora d'establir una relaci贸 un a molts entre dues taules 茅s indispensable que es complisquen **3 CONDICIONS**:

- Totes dues taules han de tindre un **camp en com煤**.
- Tots dos camps hauran de tindre el **mateix tipus** (*INTEGER*, *TEXT*, *SMALL* *INTEGER*, *etc*.) i la **mateixa grand脿ria**.
- Un dels camps haur脿 de ser **clau prim脿ria** en una de les dues taules.

## 6.5.1. Clau aliena o externa

El camp relacionat de la taula `molts` es denomina **Clau `aliena` o `externa`**.

### *Base de dades: Biblioteca*

Segons hem explicat pr猫viament, existeix clarament una relaci贸 entre les taules `LLIBRE` i `SUPORT`. Si considerem (per a simplificar) que *UN LLIBRE NOM脡S POT ESTAR PUBLICAT EN UN SUPORT*, el tipus de relaci贸 que existeix entre la taula `SUPORT` i la taula `LLIBRE` seria del tipus `un a molts` `(1:N)`, ja que:

- Per exemple, el suport `Paper` tindr脿 diversos llibres relacionats que estan en aquest suport.
- Donat un llibre, nom茅s est脿 publicat en una mena de suport.
- I el camp `Suport` de la taula `LLIBRE` ser脿 la `clau aliena` o `externa` que relaciona amb taula `SUPORT`.

Les relacions entre taules 茅s un concepte una miqueta abstracte. No obstant aix貌, si representem gr脿ficament el nostre disseny, el significat queda molt m茅s clar.

```text
                         1                           N 
        +--------------+                               +--------------+
        |    SUPORT    | <---------------------------> |    LLIBRE    |
        +--------------+                               +--------------+
```

On tenim que:

- Cada rectangle es correspon amb una taula.
- Les fletxes indiquen que les dues taules estan relacionades.
- Els n煤meros indiquen la cardinalitat. 脡s a dir:
  - `(N)` Donat un suport (*per ex. "Paper"*), pot haver-hi molts llibres publicats en aqueixa mena de format.
  - `(1)` Donat un llibre, nom茅s est脿 publicat en una mena de suport. Recorda que hem considerat, per a simplificar, que un llibre nom茅s pot estar publicat en un suport.

---

## 6.5.2 Inconsist猫ncia de dades

Abans de definir una relaci贸, hem d'assegurar-nos que les dades s贸n coherents, 茅s a dir, que els camps que estan relacionats contenen la mateixa informaci贸.
En el nostre cas, hem de comprovar que els valors continguts en el camp `Suport` de la taula `LLIBRE` es corresponen amb algun registre de la taula `SUPORT`. Per exemple, si tenim un llibre amb suport "Paper", aquest ha de ser present en la taula `SUPORT` i el text ha de coincidir tant en maj煤scules com min煤scules.

---

# 6.6 Integritat referencial

En la relaci贸 que hem definit en l'apartat anterior, s'**impedeix que qualsevol registre relacionat siga modificat o eliminat**. Aquesta propietat 茅s el que es coneix com a **integritat referencial**.

> 鈿狅笍 Quan existeix una relaci贸 entre 2 taules, qualsevol operaci贸 amb les dades ha de respectar la relaci贸. En cas contrari, no es realitzar脿.

---

# 馃摑 *Activitat 7: Relacions i integritat referencial*

Crearem una nova taula per a emmagatzemar els diferents tipus de suport per als llibres.

## Crear taula `SUPORT`

- Obri la base de dades **biblioteca**.
- `Crea una taula en vista de disseny...`
- Introdueix els camps que s'indiquen a continuaci贸:

Camp   | Tipus            | Longitud | Descripci贸
-------|------------------|----------|------------
Suport | Text [`VARCHAR`] | 20       | Tipus de suport en el qual es troba emmagatzemat (*paper, llibre electr貌nic, MP3, etc.*)

- Una vegada creat el camp, marca'l com a **clau prim脿ria**. Per a aix貌 selecciona la fila i fes clic amb el bot贸 dret del ratol铆 seleccionant l'opci贸 `Clau prim脿ria`.
- 馃捑 Guarda la taula amb el nom `SUPORT`.

## Afegir dades en la taula `SUPORT`

- Fes doble clic amb el ratol铆 per a obrir la taula en vista de dades.
- Inserta les seg眉ents files:

Suport   |
---------|
*Paper*  |
*EBook*  |
*MP3*    |
*PDF*    |
*CD*     |
*DVD*    |

- 馃捑 Guarda els canvis.

## Comprovar consist猫ncia de dades

- Verifica que les dades contingudes en el camp `Suport` de la taula `LLIBRE` s贸n coherents amb les dades de la taula `SUPORT`. En cas necessari, **modifica les dades que corresponga**.

## Relacions. Afegir taules

- Crearem una relaci贸 entre les taules `SUPORT` i `LLIBRE`.
- Tanca totes les taules obertes.

> 鈿狅笍 No 茅s possible establir relacions entre taules obertes, ja que en estar introduint dades o modificant el disseny, aquestes es troben bloquejades.
  
- Ve al men煤 `Eines` 鈫? `Relacions...` Fes clic en la icona Afeg taules.
- Selecciona les taules `LLIBRE` i `SUPORT` amb el bot贸 `Afeg`.

- En el nostre cas, en la taula `LLIBRE` tenim un camp `Suport` que fa refer猫ncia a la mena de suport en qu猫 est脿 publicat el llibre. Per tant, la columna ha de ser de la mateixa mena de dades que la columna que siga clau prim脿ria en l'altra taula i els valors que podr脿 contindre ser脿 qualsevol dels valors que prenga la clau prim脿ria en aquesta taula. En definitiva, en la taula `LLIBRE` el camp `Suport` ha de ser de la mateixa mena de dades que el camp de la taula `SUPORT`.

> 鈿狅笍 Els camps relacionats no tenen perqu猫 tindre els mateixos noms, per貌 han de tindre el mateix tipus de dades i la mateixa grand脿ria. 脡s a dir, han de contindre el mateix tipus d'informaci贸.
  
## Crear relaci贸

- Ara hem d'indicar-li a *Base* expl铆citament que les dues taules estan relacionades i que utilitzarem per a mantindre aquesta relaci贸 la columna `Suport` de la taula `LLIBRE`.

- Arrossega del camp `Suport` de `LLIBRE` al camp `Suport` de `SUPORT`. Base ha creat una relaci贸 un a molts entre les 2 taules:

![](img/base_activitat_7_relacio.png)

- 馃捑 Guarda els canvis.
- Tanca la finestra de relacions

## Verificar integritat referencial

Una vegada establida una relaci贸, comprovarem que 茅s correcta. Per a aix貌 nom茅s hem d'intentar realitzar alguna operaci贸 no permesa i veure que es compleix la integritat referencial.

- **Cas 1. Introduir un llibre amb un suport que no existeix en la taula `SUPORT`**

  - Fes clic en el bot贸 `Taules` de la Barra de dades.
  - Ve a la taula `LLIBRE` i fes doble clic sobre ella.
  - Introdueix un nou registre amb un suport que no existisca en la taula `SUPORT`.
  - 馃捑 Guarda els canvis.
  - Com podem comprovar, *Base* ens **mostra un missatge d'error** perqu猫 estem inserint un registre amb un suport que no existeix en la nostra base de dades.
  - Prem `D'acord`.
  - Fes clic a l'esquerra sobre el llapis amb el bot贸 dret del ratol铆 i tria l'opci贸 `Desf猫s: entrada de dades`.
  - Tanca la taula `LLIBRE`.

- **Cas 2. Modificar un suport que t茅 llibres relacionats**

  - Ve a la taula `SUPORT` i fes doble clic sobre ella.
  - Modifica dades en el registre `Paper` perqu猫 ara siga `Paper1`.
  - 馃捑 Guarda els canvis.
  - Com podem comprovar, *Base* ens **mostra un missatge d'error** perqu猫 estem modificant un registre de suport que cont茅 llibres relacionats en la taula `LLIBRE`.
  - Prem `D'acord`.
  - Fes clic a l'esquerra sobre el llapis amb el bot贸 dret del ratol铆 i tria l'opci贸 `Desf猫s: entrada de dades`.

- **Cas 3. Eliminar un suport que t茅 llibres relacionats**

  - Ve a la taula `SUPORT` i fes doble clic sobre ella.
  - Elimina el registre amb el tipus `Paper`. Fes clic a l'esquerra sobre el triangle amb el bot贸 dret del ratol铆 i tria l'opci贸 `Suprimir les files`.
  - Prem `S铆`.
  - Com podem comprovar, *Base* ens **mostra un missatge d'error** perqu猫 estem eliminant un registre de suport que cont茅 llibres relacionats en la taula `LLIBRE`.
  - Prem `D'acord`.
  - Fes clic a l'esquerra sobre el llapis amb el bot贸 dret del ratol铆 i tria l'opci贸 `Desf猫s: entrada de dades`.

## Tanca la base de dades

- Tanca les taules obertes.
- 馃捑 Guarda la base de dades.
- Tanca la base de dades.
- Lliura l'activitat.
