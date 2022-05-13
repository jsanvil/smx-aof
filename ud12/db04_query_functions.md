UD12: Bases de dades (II)

# 4. *LibreOffice Base*: Consultes agrupades

## 🎯 Objectius

- Conéixer les funcions d'agrupació.
- Conéixer les funcions de major complexitat.
- Realitzar consultes agrupades.

---

# 4.1 Consultes agrupades

A vegades és necessari realitzar operacions sobre els camps obtinguts. És en aquest moment quan les consultes que hem vist fins ara es queden curtes i hem de recórrer a un determinat tipus que opera sobre els resultats.

Base permet la creació de consultes que inclouen funcions, és a dir, consultes que realitzen operacions sobre els resultats per a calcular, al seu torn, altres camps. Exemples d'aquestes són: sumar tots els valors d'un grup de registres, trobar el valor mitjà, comptar el nombre total de registres o esbrinar el valor màxim i mínim d'un conjunt.

L'ús d'aquestes funcions ve determinat per les consultes denominades d'agrupació. En aquestes consultes els registres es classifiquen segons determinats criteris i a partir d'aquestes classificacions s'apliquen les funcions disponibles. Entre elles trobem:

Funció | Significat
-|-
***Grup*** | Permet agrupar els resultats a mostrar en funció d'un o diversos camps.
***Count*** | Retorna el nombre total de files retornades que continguen algun valor per a aqueix camp.
***Average*** | Per a camps de tipus numèric. Retorna la mitjana dels resultats per a aqueix camp.
***Sum*** | Per a camps de tipus numèric. Retorna la suma dels resultats per a aqueix camp.
***Maximum*** | Per a camps de tipus numèric. Retorna el valor màxim dels resultats per a aqueix camp.
***Minimum*** | Per a camps de tipus numèric. Retorna el mínim dels resultats per a aqueix camp.

---

# 4.2 Funcions complexes

A més de les operacions bàsiques, hauràs observat que el desplegable on se selecciona la funció posseeix més opcions que no hem vist. Aquestes opcions tenen una major complexitat i les estudiarem en aquest punt.

## 4.2.1 Funció `Every` (Tot)

La funció `Every` s'utilitza en el cas de camps de tipus `Boolean`, és a dir, el valor dels quals és `Sí/No`. Aquesta permet saber si tots els valors són `Sí` o hi ha algun que no ho és, de manera que si tots ho són obtindrà un `Sí`, mentre que en cas contrari obtindrà un `No`.

## 4.2.2. Funció `Some` (Algun)

La funció `Some` és similar a l'anterior, però en aquest cas la funció retornarà Sí en cas que algun dels valors siga `Sí` i `No` en cas que tots els valors siguen `No`.

## 4.2.3. Funcions `STDDEV_SAMP` i `VAR_SAMP`

La funció `STDDEV_SAMP` és una funció estadística que retorna la desviació típica d'un grup de números, és a dir, retorna la quantitat que s'han desviat respecte a la mitjana.

La funció `VAR_SAMP` és una funció que retorna la variància d'un grup de números, és a dir, la mesura de dispersió que equival al quadrat de la desviació típica. Els passos per a calcular-la són similars a l'anterior.

---

# 📝 *Activitat 4: Consultes agrupades*

## Consulta `CG_total_genere`

Crearem una consulta que mostre el nom de cada gènere emmagatzemat i el total de pel·lícules que tenim de cada gènere. És a dir, realitzar una consulta sobre la taula `PELICULA` de manera que agrupem les files retornades en funció de cada gènere per a així poder explicar-les i saber el nombre de pel·lícules associades a cadascun d'ells.

- Crea una consulta en vista de disseny.
- Afig la taula `PELICULA`.
- Selecciona els camps `Genere` i `Titol`. Els camps que necessitem són, d'una banda el `Genere`, que és sobre el qual agruparem els resultats retornats i, per un altre, un camp de la taula `PELICULA` que estiguem segurs que sempre tindrà un valor (no estarà buit) per a cada fila de pel·lícules. Per exemple `Titol` o `Id_pelicula`.
- Ordena ascendentment per la columna `Genere`.
- En el camp `Funció` de la columna `Genere` selecciona l'opció `Agrupar`.

En segon lloc, la qual cosa volem és contar les pel·lícules relacionades amb cada gènere.

Ve a la columna `Titol`. En l'apartat `Àlies` escriu *`Total de pel·lícules`*. En l'apartat `Funció` tria l'opció `Comptar` (o *`Count`*).

- 💾 Guarda la consulta com `CG_total_genere`.
- Executa la consulta i comprova que funciona correctament.

Com es pot observar, per a realitzar una operació sobre els camps necessitarem, almenys, un camp sobre el qual realitzar l'agrupació i un altre camp sobre el qual realitzar l'operació. En l'exemple anterior el camp sobre el qual s'agrupa és `Genere`, mentre el camp sobre el qual es realitza l'operació és `Titol`, encara que com hem dit, podria ser també el camp `Id_pelicula`.

De fet, si realitzem la consulta canviant el camp `Titol` per `Id_pelicula` el resultat serà el mateix.

- 💾 Guarda els canvis.
- Tanca la consulta.

## Consulta `CG_mitjana_duracio`

Ara crearem una consulta que calcule la mitjana de duració de les pel·lícules agrupades per `Suport`, és a dir, per a cada suport s'haurà d'obtindre la mitjana de les duracions de les pel·lícules.

- Crea una consulta en vista de disseny.
- Taula: `PELICULA`.
- Camps: `Duracio` i `Suport`. Els camps que necessitem són, d'una banda el `Suport`, que és sobre el qual agruparem els resultats retornats i, per un altre, un camp de la taula `PELICULA` que continga els valors per a realitzar l'operació.
- Ve a la columna `Suport` i estableix un ordre ascendent. En el camp `Funció` selecciona l'opció `Agrupar`.
- Ve a la columna `Duracio`. En l'apartat `Àlies` escriu *`Mitjana de duracions`*. En l'apartat Funció tria l'opció `Average`.
- 💾 Guarda la consulta amb nom `CG_mitjana_duracio`.
- Executa la consulta i comprova que funciona correctament. Per a això pots realitzar la mitjana manualment de les duracions de la taula `PELICULA`.
- 💾 Guarda els canvis.
- Tanca la consulta.

## Consulta `CG_suma_duracio`

També podem realitzar consultes perquè calcule una determinada operació per a tots els registres, és a dir, sense que agrupe per camps. En aquest cas hem de seleccionar el camp sobre el qual volem aplicar la funció i la funció en si.

Realitzarem una consulta en la qual es calcule la suma de totes les duracions.

- Crea una consulta en vista de disseny.
- Taula: `PELICULA`.
- Selecciona el camp `Duracio`, ja que únicament volem aplicar la funció sobre aquest.
- Vee a la columna `Duracio`. En l'apartat `Àlies` escriu *`Suma de duracions`*. En l'apartat `Funció` tria l'opció `Suma`.
- 💾 Guarda la consulta amb nom `CG_suma_duracio`.
- Executa la consulta i comprova que funciona correctament. Per a això pots realitzar la suma manualment de les duracions de la taula `PELICULA`.

Aquest funcionament serveix per a totes les altres funcions i permet obtindre, ràpidament, resultats que poden servir-nos per a realitzar altres càlculs.

- 💾 Guarda els canvis.
- Tanca la consulta.

## Més consultes

Crea les següents consultes en vista de disseny:

- Consulta amb nom `CG_max_genere` sobre la taula `PELICULA` en la qual s'obtinga el màxim de les duracions de cada gènere.
- Consulta amb nom `CG_total_suport` sobre la taula `PELICULA` en la qual s'obtinga el nombre de pel·lícules de cada suport.

## Funció `Every`

Prèviament modificarem la taula `PELICULA` per a inserir un camp Booleà.

### Taula `PELICULA`. Afegir camp

- Obri la taula `PELICULA` en vista de disseny (editar).
- Situa't al final i inserta un camp anomenat `Original`, el tipus del qual serà `Boolean`:

Camp | Tipus | Descripció
-|-|-|-
Original | Sí/No [`BOOLEAN`] | Indica si l'àudio inclou versió original

- 💾 Guarda els canvis.
- Tanca la taula.

### Taula `PELICULA`. Edició de dades

- Obri la taula `PELICULA`.
- Canvia els valors perquè la columna `Original` tinga 3 pel·licules en versió original.
- 💾 Guarda els canvis.
- Tanca la taula.

### Crear consulta

Ara sí que podem realitzar la consulta amb la funció `Every`.

- Crea una consulta en vista de disseny.
- Taula: `PELICULA`.
- Selecciona el camp `Original`.
- Ve a la columna `Original` i en l'apartat `Àlies` escriu *`Totes originals?`*. En l'apartat `Funció` tria l'opció `Every`.
- 💾 Guarda la consulta amb nom `CGC_tot_original`.
- Executa la consulta i comprova que funciona correctament.

Com podem observar, a l'haver diverses d'elles que no són originals, el resultat serà negatiu. Si modifiquem els valors perquè totes siguen originals i tornem a realitzar la consulta el resultat serà verdader.

- 💾 Guarda els canvis.
- Tanca la consulta.

## Funció `Some`

- Crea una consulta en vista de disseny.
- Taula: `PELICULA`.
- Selecciona el camp `Original`.
- Ve a la columna `Original` i en l'apartat `Àlies` escriu *`Alguna original?`*. En l'apartat `Funció` tria l'opció `Some`.
- 💾 Guarda la consulta amb nom `CGC_algun_original`.
- Executa la consulta i comprova que funciona correctament.
- 💾 Guarda els canvis.
- Tanca la consulta.

## Funció `STDDEV_SAMP`

Anem a crear una consulta per a saber la desviació típica de la duració de les pel·lícules.

- Crea una consulta en vista de disseny.
- Taula: `PELICULA`.
- Selecciona el camp `Duracio`.
- Ve a la columna `Duracio` i en l'apartat `Àlies` escriu `Desviació de la duració`. En l'apartat `Funció` tria l'opció `STDDEV_SAMP`.
- 💾 Guarda la consulta amb nom `CGC_desv_duracio`.
- Executa la consulta i comprova que funciona correctament.
- 💾 Guarda els canvis.
- Tanca la consulta.

---

- 💾 Guarda els canvis en la base de dades.
- Tanca la base de dades.
