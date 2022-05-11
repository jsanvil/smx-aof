UD11: Bases de dades (I)

# 📝 *Activitat 11: Exercici de recopilació. Gimnàs*

## 🎯 Objectius

- Crear la base de dades d'un gimnàs.
- Repassar tots els conceptes vistos anteriorment.

# Base de dades: Gimnàs

El gimnàs *TotGym S.L.* pretén crear una base de dades automatitzada de tots els seus clients, així com de les activitats que es realitzen. Per a això contracta els serveis d'una empresa de serveis informàtics.

En l'exercici es donaran les directrius però seràs tu el que hauràs de realitzar tots els passos, tal com s'han vist en la teoria.

# 0. Crear base de dades

- Crea una nova base de dades anomenada `Gimnàs`.
- Deixa les opcions per defecte que hagen seleccionades.

---

# 1. Crear taules

Una vegada creada la base de dades, crearem les taules necessàries.

## Taula: `SOCI`

- Crea la taula de socis del gimnàs amb els següents camps i propietats:

Camp             | Tipus                    | Longitud      | Descripció
-----------------|--------------------------|---------------|------------
**Id_soci**      | Enter [`INTEGER`]        | *Per defecte* | Identificador (**clau primària**)
**Nom**          | Text [`VARCHAR`]         | 25            | Nom del soci
**Cognoms**      | Text [`VARCHAR`]         | 50            | Cognoms del soci
**DNI**          | Text [`VARCHAR`]         | 10            | DNI
**Telefon**      | Text [`VARCHAR`]         | 12            | Telèfon de contacte
**Adreca**       | Text [`VARCHAR`]         | 50            | Adreça
**Quota**        | Real [`REAL`]            | *Per defecte* | Import de la quota mensual
**Activitat**    | Text [`VARCHAR`]         | 20            | Codi d'activitat que realitza
**Horari**       | Hora [`TIME`]            | *Per defecte* | Horari de l'activitat
**Foto**         | Imatge [`LONGVARBINARY`] | *Per defecte* | Foto grandària carnet del soci
**Observacions** | Nota [`LONGVARCHAR`]     | *Per defecte* | Observacions diverses

- 🔑 Estableix com a **clau primària** el camp `Id_soci`.
- 💾 Guarda la taula amb el nom ***`SOCI`***

---

# 2. Establir propietats de camps

## Format de dades

- Camp `Horari`. Estableix un nou format: tria la categoria Hora, format `HH:MM`.
- Camp `Quota`. Estableix un nou format: tria la categoria `Moneda`.

## Valor predeterminat (per defecte)

- Camp `Quota`:
  - Estableix `0` com a valor predeterminat.
  - Entrada requerida

- Camp `Nom`:
  - Estableix el camp com a entrada requerida.

- Camp `Cognoms`:
  - Estableix el camp com a entrada requerida.

D'aquesta manera, per a cada registre serà obligatori introduir el nom i cognoms del soci.

---

# 3. Edició de taules

## Tipus de dades `Autonumèric`

Un canvi molt útil que podem realitzar en la nostra taula de socis, és fer que la nostra clau primària prenga valors automàticament.

- Camp `Id_soci`:
  - Estableix la propietat `Valor automàtic:` a *`Sí`*.

A partir d'ara, cada vegada que introduïm una nova fila en la taula `SOCI`, el camp `Id_soci` prendrà el major valor assignat fins a aqueix moment incrementat en `1`.

---

# 4. Introducció de dades

- Obri la taula `SOCI`
- Inserita les següents dades:

Id_soci | Nom | Cognoms | DNI | Telefon | Adreca | Quota | Activitat | Horari | Foto | Observacions
-|-|-|-|-|-|-|-|-|-|-
0 | Quim | Daurat Chico | 77406349-X | 999999999 | C/ Quintaro, 1 | 30,00 € | Natacio2D | 16:00 | OBJECT | No sap nadar
1 | Joan | Peris Vila | 76871019-G | 888888888 | Avda. Encisams, 34 | 39,00 € | Aerobic2D | 18:00 | OBJECT | Antecedents de reuma
2 | Enriqueta | Sanchis Mollar | 75942691-L | 777777777 | C/ Reina, 20 | 15,00 € | Aerobic2D | 17:00 | OBJECT | Ve amb bicicleta
3 | Llum | Ferris Alfons | 72345678-H | 111111111 | C/ Torrent, 27 | 40,00 € | Boxing3D | 12:00 | OBJECT | No té guants
4 | Leroy | Jenkins | X7654333-C | 222222222 | C/ Tomatoes, 3 | 27,50 € | Aerobic2D | 15:00 | OBJECT | Només parla anglés

---

# 5. Consultes

- Crea una consulta anomenada *`Activitats_socis`* amb l'auxiliar:
  - Taula: `SOCI`
  - Que continga els camps `Id_soci`, `Cognoms`, `Nom`, `Activitat`, `Horari` i `Quota`
  - Que estiga ordenada ascendentment pel camp `Cognoms`
- Crega una consulta anomenada *`Activitats_30`* en vista de disseny:
  - Taula: `SOCI`
  - Que continga els camps `Id_soci`, `Cognoms`, `Nom`, `Activitat`, `Horari` i `Quota`
  - Que estiga ordenada ascendentment pel camp `Cognoms`
  - Que el camp `Quota` siga `major o igual` a `30 euros`.

---

# 6. Crear formularis

## Formulari: FSOCI

- Crea un formulari anomenat *`FSOCI`* amb l'auxiliar:
  - Taula: `SOCI`
  - Que continga tots els camps de la taula
  - L'organització serà En columnes - Etiquetes a l'esquerra
  - L'estil el que més t'agrade

- Introduirem les fotos dels nostres socis del gimnàs.
  - Descàrrega 5 fotos d'Internet que vulgues. ***Procura que les fotos no ocupen molt espai per a no superar el límit de grandària a l'hora de pujar al portal la base de dades***.
  - Mitjançant el formulari, introdueix una foto per a cada soci del gimnàs.

---

# 7. Disseny de formularis

Canviarem aspectes estètics del disseny del formulari `FSOCIO` perquè es mostre millor la fotografia i les observacions de cada soci.

## Camp `Id_soci`

- Canvia la propietat `Habilitat` a *`No`*

## Camp `Foto`

- Camp `Foto`. Mou-ho a la dreta del formulari.
- Camp `Observacions`. Mou-lo a l'dreta del formulari.

## Camp `Observacions`

- Fes doble clic en el camp `Observacions`.
- Canvia la propietat `Alineació vert` al valor *`Centre`*.
- Canvia la propietat `Entrada de línies múltiples` al valor *`Sí`*.

![](img/base_activitat_11_formulari.png)

---

# 8. Relacions

Si ens fixem en la base de dades, podem veure que s'està repetint el mateix valor moltes vegades, per exemple, *`Aerobic2D`* apareix en diverses files. És a dir, en introduir el mateix valor de manera redundant s'està possibilitant que en algun moment l'escriguem malament, per exemple, *`Aerobic2D`*, i tinguem una nova activitat que no és realitzada per cap soci, ja que ni tan sols existeix. La solució als problemes anteriors està a separar la informació que apareix repetida contínuament en una nova taula `ACTIVITAT` i indicar d'alguna forma en la nostra base de dades que hi ha files de la taula `SOCI` i de la taula `ACTIVITAT` que estan relacionades.

## 8.1. Crear taules

### Taula: `ACTIVITAT`

- Crea la taula d'activitats realitzades en el gimnàs amb els següents camps i propietats:

Camp | Tipus | Longitud | Descripció
-|-|-|-
Id_activitat | Text [`VARCHAR`] | 20 | Codi d'activitat
Descripcio | Text [`VARCHAR`] | 50 | Descripció
Dilluns | Sí/No [`BOOLEAN`] | *Per defecte* | Dia dilluns
Dimarts | Sí/No [`BOOLEAN`] | *Per defecte* | Dia dimarts
Dimecres | Sí/No [`BOOLEAN`] | *Per defecte* | Dia dimecres
Dijous | Sí/No [`BOOLEAN`] | *Per defecte* | Dia dijous
Divendres | Sí/No [`BOOLEAN`] | *Per defecte* | Dia divendres
Dissabte | Sí/No [`BOOLEAN`] | *Per defecte* | Dia disabte
Diumenge | Sí/No [`BOOLEAN`] | *Per defecte* | Dia diumenge

- 🔑 Fixa com a clau primària el camp `Id_activitat`.
- 💾 Guarda la taula amb el nom `ACTIVITAT`.

## 8.2. Introducció de dades

Introdueix diversos registres amb les diferents activitats del gimnàs.

Id_activitat | Descripcio | Dilluns | Dimarts | Dimecres | Dijous | Divendres | Dissabte | Diumenge
-|-|-|-|-|-|-|-|-
Aerobic2D | Aeròbic dos dies a la setmana  | Sí | No | No | Sí | No | No | No
Boxing3D  | Boxa tres dies a la setmana     | No | No | No | No | Sí | Sí | Sí
Fitness2D | Fitnes dos dies a la setmana   | No | Sí | No | Sí | No | No | No
Fitness3D | Fitnes tres dies a la setmana  | Sí | No | Sí | No | Sí | No | No
Natacio2D | Natació dos dies a la setmana  | No | Sí | No | Sí | No | No | No
Natacio3D | Natació tres dies a la setmana | Sí | No | Sí | No | Sí | No | No
Recupera1D| Exercicis de recuperació       | Sí | No | No | No | No | No | No
Spinning1D| Spinning cap de setmana        | No | No | No | No | No | Sí | No

## 8.3. Inconsistència de dades

Abans de definir una relació, hem d'assegurar-nos que les dades són coherents, és a dir, que els camps que estan relacionats contenen la mateixa informació.
En el nostre cas, hem de comprovar que els valors continguts en el camp `Activitat` de la taula `SOCI` es corresponen amb algun registre de la taula `ACTIVITAT`.
*Per exemple, si tenim un soci que realitza l'activitat `Aerobic2D`, aquesta ha de ser present en la taula `ACTIVITAT` i el text ha de coincidir tant en majúscules com minúscules.*

### Comprovar consistència de dades

- Verifica que les dades contingudes en el camp `Activitat` de la taula `SOCI` són coherents amb les dades de la taula `ACTIVITAT`. En cas necessari, modifica les dades que corresponga.

## 8.4. Identificar la relació

Existeix clarament una relació del tipus un a molts `(1:N)` entre les taules `SOCI` i `ACTIVITAT`. Si considerem que un soci només pot realitzar una activitat, aquest seria el tipus de relació que existeix entre la taula `ACTIVITAT` i la taula `SOCI` ja que, per exemple, l'activitat *`Natacion2D`* serà realitzada per diversos socis, però donat un soci només realitzarà una activitat.

> ⚠ Simplificarem la realitat i suposem que un soci només pot realitzar una activitat. Posteriorment tractarem les relacions molts a molts `(N:N)`, ja que presenten major complexitat.

### Interpretació de la relació

Les relacions entre taules és un concepte una miqueta abstracte. No obstant això, si representem gràficament el nostre disseny, el significat queda molt més clar.

```text
                        1                           N 
        +-------------+                               +----------+
        |  ACTIVITAT  | <---------------------------> |   SOCI   |
        +-------------+                               +----------+
```

On tenim que:

- Cada rectangle es correspon amb una taula.
- Les fletxes indiquen que les 2 taules estan relacionades.
- Els números indiquen la cardinalitat. És a dir:
  - `(N)` Donada una activitat, pot haver-hi molts socis que la realitzen.
  - `(1)` Donat un soci, només pot realitzar una activitat.

---

# 9. Establir una relació un a molts `(1:N)`

En el nostre cas, en la taula SOCI tenim un camp “Activitat” que fa referència a l'activitat que realitza el soci. Per tant, la columna ha de ser de la mateixa mena de dades que la columna que siga clau primària en l'altra taula (`Id_activitat`) i els valors que podrà contindre serà qualsevol dels valors que prenga la clau primària en aquesta taula.

> ⚠ Els camps relacionats no tenen perquè tindre els mateixos noms, però han de tindre el mateix tipus de dades i la mateixa grandària. És a dir, han de contindre el mateix tipus d'informació. En la taula `SOCI` el camp “Activitat” ha de ser de la mateixa mena de dades que el camp `Id_activitat` de la taula `ACTIVITAT`.

## Crear relació

- Tanca totes les taules obertes.
- Relaciona el camp `Activitat` de `SOCI` amb el camp `Id_activitat` d'`ACTIVITAT`.
- 💾 Guarda els canvis.

---

# 10. Informe

## Crea un informe anomenat *`Inf_socis`* amb l'assistent

- Taula: `SOCI`
- Que continga tots els camps de la taula
- S'ordenarà pel camp `Nom` de manera ascendent
- El disseny el que més t'agrade

---

# Lliurar l'activitat

- 💾 Guarda tots els canvis.
- Tanca la base de dades `Gimnàs`.
- Liura la base de dades `Gimnàs.odb`.
