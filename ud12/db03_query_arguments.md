UD12: Bases de dades (II)

# 3. *LibreOffice Base*: Consultes compostes. Paràmetres i condicions

## 🎯 Objectius

- Concepte de paràmetre.
- Realitzar consultes amb paràmetres.
- Conéixer els operadors de comparació.
- Conéixer els operadors de text.
- Realitzar consultes comparatives.

---

# 3.1 Consultes amb paràmetres

Les consultes que hem vist fins ara no permetien la introducció d'elements dinàmics, sinó que eren fixats de manera estàtica en el disseny de la consulta. Existeix la possibilitat que aquests paràmetres canvien de manera dinàmica amb la finalitat d'ampliar les possibilitats de les consultes i flexibilitzar els seus resultats. Com era d'esperar, *Base* permet crear consultes dinàmiques que sol·liciten a l'usuari els filtres en temps real.

## 3.1.1 Paràmetres

Els paràmetres són expressions que admeten l'assignació de valors amb la finalitat d'alterar el comportament d'una consulta. Aquestes expressions permetran a l'usuari la demanda d'un determinat valor cada vegada que s'execute la consulta. Per exemple, podem fer que cada vegada que s'òbriga una consulta sobre la taula `PELICULA`, ens pregunte què `IDs` desitgem filtrar.

En general, el format dels paràmetres és el següent:

```text
:nom del paràmetre
```

És a dir, consistirà en la símbol dos punts seguit del nom del paràmetre.

### *Exemple videoclub:*

`:data` → Per a indicar una data

`:IDs` → Per a indicar un identificador

`:any` → Per a indicar un any

Si pensem en les possibilitats que tenen aquest tipus de consultes ens adonarem que podem combinar diferents paràmetres que flexibilitzaran els resultats. De fet podem posar més d'un paràmetre per a configurar totalment la consulta.

# 3.2 Operadors de comparació

Tal com vam veure en la unitat anterior, les consultes en vista disseny contenen multitud de característiques que permeten ampliar les possibilitats de les consultes realitzades amb l'assistent. Una d'aquestes és la de poder introduir operadors de comparació que filtren els resultats amb els quals ens volem quedar.

Per a qualsevol camp seleccionat en una consulta podem establir condicions. És a dir, podem escriure expressions per a filtrar les dades. Les expressions s'escriuran en la cel·la `Criteri` del camp corresponent de la consulta. Tenim els següents operadors:

Operador | Significat
-|-
**`<`** | Condició de comparació `menor que`
**`>`** | Condició de comparació `major que`
**`<=`** | Condició de comparació `menor o igual que`
**`>=`** | Condició de comparació `major o igual que`
**`=`** | Condició de comparació `igual que`
**`<>`** | Condició de comparació `diferent que`
`BETWEEN` a `AND` b | Condició per a especificar un interval de valors. *(ENTRE a I b)*
`+`, `-`, `*`, `/` | Els operadors de suma, resta, multiplicació i divisió poden combinar-se per a efectuar comparacions amb `expressions matemàtiques`.

---

# 3.3 Operadors de text

Per a qualsevol camp seleccionat en una consulta podem establir condicions. És a dir, podem escriure expressions per a filtrar les dades. Les expressions s'escriuran en la cel·la `Criteri` del camp corresponent de la consulta. Tenim els següents operadors:

Operador | Significat
-|-
`' '` | Condició de comparació `igual que`. Amb **cometes simples**.
`*` | Comodí que significa qualsevol cadena de caràcters. S'utilitza juntament amb l'operador `LIKE`.
`?` | Comodí que significa `un caràcter qualsevol` i `només un`. S'utilitza juntament amb l'operador `LIKE`.
`LIKE` | Condició de comparació de patrons. Serveix per a especificar un o diversos caràcters pels quals buscar i, a continuació, buscar registres que comencen o continguen els caràcters especificats per l'usuari. El camp de dades conté l'expressió indicada. El caràcter comodí (`*`) indica si l'expressió `x` apareix al principi del contingut del camp (`x*`), al final (`*x`) o dins d'aquest (`*x*`).

---

# 3.4 Combinació d'operadors

Hem vist que existeixen diversos operadors que es poden utilitzar depenent de la mena de camp. A més d'utilitzar-los de manera separada, podem combinar-los amb la finalitat de filtrar encara més els resultats.

## 3.4.1 Complir tots els criteris `(AND)`

La primera opció quan combinem paràmetres i operadors és que es complisquen tots els criteris alhora. En aquest cas, posarem totes les operacions i filtres en la **MATEIXA FILA** del camp `Criteri`.

## 3.4.2 Complir algun dels criteris `(OR)`

Una altra possibilitat és que es complisca, almenys, un dels criteris, és a dir, en lloc que es complisquen tots alhora que puguen fer-ho per separat. En aquest cas, posarem les operacions i filtres en **FILES DIFERENTS** del camp `Criteri`.

---

# 📝 *Activitat 3: Consultes compostes. Paràmetres i condicions*

## Consulta amb un paràmetre

Crearem una consulta que ens retorne les pel·lícules que tenim d'un gènere de cinema determinat.

- Crea una consulta en vista de disseny.
  - Taula: `PELICULA`.
  - Camps a mostrar: Titol, Suport, Duracio, Argument i Genere.
  - Ordena ascendentment per la columna `Titul`.
  - Columna `Genere`. Desmarca la casella `Visible`.
  - En l'apartat `Criteri` escriu el text `:Genere`.
- 💾 Guarda la consulta amb nom *`CP_genere_pelis`*.
- Executa la consulta. Apareixerà un quadre de diàleg per a introduir el gènere sobre el qual volem consultar.
- En el camp `Valor`, escriu el nom d'un gènere de cinema.- - Fes clic a Acceptar. Això provocarà que se seleccionen aquelles pel·lícules el camp de les quals `Genere` tinga el valor que hem seleccionat.
- Consulta amb diferents gèneres i comprova que funciona correctament.
- 💾 Guarda els canvis.
- Tanca la consulta.

## Consultes amb diversos paràmetres

Veurem una consulta que ens permeta seleccionar el suport i la duració mitjançant paràmetres.

- Crea una consulta en vista de disseny.
  - Taula: `PELICULA`.
  - Camps: `Id_pelicula`, `Titol`, `Director`, `Suport` i `Duracio`.
  - En la fila `Criteri` columna `Suport` escriu `:Suport` i en la columna `Duracio` escriu `:Duracio`.
- 💾 Guarda la consulta amb nom *`CP_sup_dur_pelis`*.
- Executa la consulta.
- Es mostrarà, llavors, un quadre de diàleg per a introduir els paràmetres `Duracio` i `Suport`.
- Introdueix valors que estiguen en la taula (en l'exemple hem utilitzat duració 180 i suport DVD). Això provocarà que se seleccionen aquelles pel·lícules els valors de les quals coincidisquen amb els introduïts:
- 💾 Guarda els canvis.
- Tanca la consulta.

## Paràmetres i operadors de comparació

### Consulta *`CP_id_entre_pelis`*

Crearem una consulta per a filtrar aquelles pel·lícules que es troben entre dues IDs.

- Crea una consulta en vista de disseny.
  - Taula: `PELICULA`.
  - Camps: `Id_pelicula`, `Titol`, `Director` i `Suport`.
  - Columna `Id_pelicula`. Estableix un criteri perquè filtre les pel·lícules entre un `ID` inicial i un `ID` final.
- Executa la consulta. Es mostrarà el quadre de diàleg per a introduir els paràmetres.

> Compte amb l'ordre dels paràmetres perquè en aquest cas estan a l'inrevés; és a dir, *Base* els demana en ordre invers.

Això provocarà que se seleccionen aquelles pel·lícules els valors de les quals coincidisquen amb els introduïts (per exemple, seleccionar 0 i 3)

- 💾 Guarda la consulta amb nom *`CP_id_entre_pelis`*.
- Tanca la consulta.

### Consulta *`CP_dur_gen_pelis`*

En el cas dels operadors textuals únicament podrem utilitzar el d'igualació, ja que en introduir el valor, als paràmetres se'ls afigen cometes, amb el que únicament es filtren aquells valors que siguen iguals al valor introduït. Un exemple seria el de seleccionar aquelles pel·lícules el director de les quals siga un determinat.

- Crea una consulta sobre la taula `PELICULA` en la qual s'obtinguen els camps `Id_pelicula`, `Titol`, `Director`, `Duracio` i `Genere` de les pel·lícules la duració de les quals siga major a una determinada i el gènere de la qual siga un determinat.
- 💾 Guarda la consulta amb nom `CP_dur_gen_pelis`.
- Tanca la consulta.

## Operadors de text

- Crea una consulta en vista de disseny.
- Taula: `PELICULA`.
- Camps: `Id_pelicula`, `Titol`, `Director`, `Any`, `Suport`, `Duracio`, `Genere` i `Argument`.
- Estableix un criteri per a obtindre les pel·lícules el gènere de les quals comence pel text `*A`.
- 💾 Guarda la consulta amb nom `CP_gen_A_pelis`.
- Tanca la consulta.

## Combinació de criteris `AND`

Realitzarem una consulta que retorne les pel·lícules amb el suport especificat, amb el gènere especificat i amb una duració entre 2 valors que especifiquem.

- Crea una consulta en vista de disseny.
- Taula: `PELICULA`.
- Camps: `Genere`, `Titol`, `Director`, `Suport`, `Duracio` i `Argument`.
- Ordena ascendentment per `Genere` i `Titol`.
- Estableix els filtres en la fila `Criteri`:
  - Genere: *`:Genere`*
  - Suport: *`:Suport`*
  - Duracio: *`BETWEEN :durmin AND :durmax`*
- Executa la consulta. Comprova que es mostren les pel·lícules que compleixen tots els criteris.
- 💾 Guarda la consulta amb nom `CP_AND_criteris`.
Tanca la consulta.

## Combinació de criteris `OR`

Realitzarem una consulta que retorne les pel·lícules amb el suport especificat o el títol del qual continga la lletra `"m"` o que tinguen una duració entre 2 valors que especifiquem.

- Crea una consulta en vista de disseny.
  - Taula: `PELICULA`.
  - Camps: `Genere`, `Titol`, `Director`, `Suport`, `Duracio` i `Argument`.
  - Ordena ascendentment per `Genere` i `Titol`.
  - Estableix els filtres en la fila `Criteri` en diferents files:
    - Genere: *`'LIKE *m*'`*
    - Suport: *`:Suport`*
    - Duracio: *`BETWEEN :durmin AND :durmax`*
- Executa la consulta. Comprova que es mostren les pel·lícules que compleixen algun dels criteris.
- 💾 Guarda la consulta amb nom `CP_OR_criteris`.
- Tanca la consulta.

---

- 💾 Guarda els canvis en la base de dades.
- Tanca la base de dades.
