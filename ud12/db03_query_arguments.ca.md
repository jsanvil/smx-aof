UD12: Bases de dades (II)

# 3. *LibreOffice Base*: Consultes compostes. Par脿metres i condicions

## 馃幆 Objectius

- Concepte de par脿metre.
- Realitzar consultes amb par脿metres.
- Con茅ixer els operadors de comparaci贸.
- Con茅ixer els operadors de text.
- Realitzar consultes comparatives.

---

# 3.1 Consultes amb par脿metres

Les consultes que hem vist fins ara no permetien la introducci贸 d'elements din脿mics, sin贸 que eren fixats de manera est脿tica en el disseny de la consulta. Existeix la possibilitat que aquests par脿metres canvien de manera din脿mica amb la finalitat d'ampliar les possibilitats de les consultes i flexibilitzar els seus resultats. Com era d'esperar, *Base* permet crear consultes din脿miques que sol路liciten a l'usuari els filtres en temps real.

## 3.1.1 Par脿metres

Els par脿metres s贸n expressions que admeten l'assignaci贸 de valors amb la finalitat d'alterar el comportament d'una consulta. Aquestes expressions permetran a l'usuari la demanda d'un determinat valor cada vegada que s'execute la consulta. Per exemple, podem fer que cada vegada que s'貌briga una consulta sobre la taula `PELICULA`, ens pregunte qu猫 `IDs` desitgem filtrar.

En general, el format dels par脿metres 茅s el seg眉ent:

```text
:nom del par脿metre
```

脡s a dir, consistir脿 en la s铆mbol dos punts seguit del nom del par脿metre.

### *Exemple videoclub:*

`:data` 鈫? Per a indicar una data

`:IDs` 鈫? Per a indicar un identificador

`:any` 鈫? Per a indicar un any

Si pensem en les possibilitats que tenen aquest tipus de consultes ens adonarem que podem combinar diferents par脿metres que flexibilitzaran els resultats. De fet podem posar m茅s d'un par脿metre per a configurar totalment la consulta.

# 3.2 Operadors de comparaci贸

Tal com vam veure en la unitat anterior, les consultes en vista disseny contenen multitud de caracter铆stiques que permeten ampliar les possibilitats de les consultes realitzades amb l'assistent. Una d'aquestes 茅s la de poder introduir operadors de comparaci贸 que filtren els resultats amb els quals ens volem quedar.

Per a qualsevol camp seleccionat en una consulta podem establir condicions. 脡s a dir, podem escriure expressions per a filtrar les dades. Les expressions s'escriuran en la cel路la `Criteri` del camp corresponent de la consulta. Tenim els seg眉ents operadors:

Operador | Significat
-|-
**`<`** | Condici贸 de comparaci贸 `menor que`
**`>`** | Condici贸 de comparaci贸 `major que`
**`<=`** | Condici贸 de comparaci贸 `menor o igual que`
**`>=`** | Condici贸 de comparaci贸 `major o igual que`
**`=`** | Condici贸 de comparaci贸 `igual que`
**`<>`** | Condici贸 de comparaci贸 `diferent que`
`BETWEEN` a `AND` b | Condici贸 per a especificar un interval de valors. *(ENTRE a I b)*
`+`, `-`, `*`, `/` | Els operadors de suma, resta, multiplicaci贸 i divisi贸 poden combinar-se per a efectuar comparacions amb `expressions matem脿tiques`.

---

# 3.3 Operadors de text

Per a qualsevol camp seleccionat en una consulta podem establir condicions. 脡s a dir, podem escriure expressions per a filtrar les dades. Les expressions s'escriuran en la cel路la `Criteri` del camp corresponent de la consulta. Tenim els seg眉ents operadors:

Operador | Significat
-|-
`' '` | Condici贸 de comparaci贸 `igual que`. Amb **cometes simples**.
`*` | Comod铆 que significa qualsevol cadena de car脿cters. S'utilitza juntament amb l'operador `LIKE`.
`?` | Comod铆 que significa `un car脿cter qualsevol` i `nom茅s un`. S'utilitza juntament amb l'operador `LIKE`.
`LIKE` | Condici贸 de comparaci贸 de patrons. Serveix per a especificar un o diversos car脿cters pels quals buscar i, a continuaci贸, buscar registres que comencen o continguen els car脿cters especificats per l'usuari. El camp de dades cont茅 l'expressi贸 indicada. El car脿cter comod铆 (`*`) indica si l'expressi贸 `x` apareix al principi del contingut del camp (`x*`), al final (`*x`) o dins d'aquest (`*x*`).

---

# 3.4 Combinaci贸 d'operadors

Hem vist que existeixen diversos operadors que es poden utilitzar depenent de la mena de camp. A m茅s d'utilitzar-los de manera separada, podem combinar-los amb la finalitat de filtrar encara m茅s els resultats.

## 3.4.1 Complir tots els criteris `(AND)`

La primera opci贸 quan combinem par脿metres i operadors 茅s que es complisquen tots els criteris alhora. En aquest cas, posarem totes les operacions i filtres en la **MATEIXA FILA** del camp `Criteri`.

## 3.4.2 Complir algun dels criteris `(OR)`

Una altra possibilitat 茅s que es complisca, almenys, un dels criteris, 茅s a dir, en lloc que es complisquen tots alhora que puguen fer-ho per separat. En aquest cas, posarem les operacions i filtres en **FILES DIFERENTS** del camp `Criteri`.

---

# 馃摑 *Activitat 3: Consultes compostes. Par脿metres i condicions*

## Consulta amb un par脿metre

Crearem una consulta que ens retorne les pel路l铆cules que tenim d'un g猫nere de cinema determinat.

- Crea una consulta en vista de disseny.
  - Taula: `PELICULA`.
  - Camps a mostrar: Titol, Suport, Duracio, Argument i Genere.
  - Ordena ascendentment per la columna `Titul`.
  - Columna `Genere`. Desmarca la casella `Visible`.
  - En l'apartat `Criteri` escriu el text `:Genere`.
- 馃捑 Guarda la consulta amb nom *`CP_genere_pelis`*.
- Executa la consulta. Apareixer脿 un quadre de di脿leg per a introduir el g猫nere sobre el qual volem consultar.
- En el camp `Valor`, escriu el nom d'un g猫nere de cinema.- - Fes clic a Acceptar. Aix貌 provocar脿 que se seleccionen aquelles pel路l铆cules el camp de les quals `Genere` tinga el valor que hem seleccionat.
- Consulta amb diferents g猫neres i comprova que funciona correctament.
- 馃捑 Guarda els canvis.
- Tanca la consulta.

## Consultes amb diversos par脿metres

Veurem una consulta que ens permeta seleccionar el suport i la duraci贸 mitjan莽ant par脿metres.

- Crea una consulta en vista de disseny.
  - Taula: `PELICULA`.
  - Camps: `Id_pelicula`, `Titol`, `Director`, `Suport` i `Duracio`.
  - En la fila `Criteri` columna `Suport` escriu `:Suport` i en la columna `Duracio` escriu `:Duracio`.
- 馃捑 Guarda la consulta amb nom *`CP_sup_dur_pelis`*.
- Executa la consulta.
- Es mostrar脿, llavors, un quadre de di脿leg per a introduir els par脿metres `Duracio` i `Suport`.
- Introdueix valors que estiguen en la taula (en l'exemple hem utilitzat duraci贸 180 i suport DVD). Aix貌 provocar脿 que se seleccionen aquelles pel路l铆cules els valors de les quals coincidisquen amb els introdu茂ts:
- 馃捑 Guarda els canvis.
- Tanca la consulta.

## Par脿metres i operadors de comparaci贸

### Consulta *`CP_id_entre_pelis`*

Crearem una consulta per a filtrar aquelles pel路l铆cules que es troben entre dues IDs.

- Crea una consulta en vista de disseny.
  - Taula: `PELICULA`.
  - Camps: `Id_pelicula`, `Titol`, `Director` i `Suport`.
  - Columna `Id_pelicula`. Estableix un criteri perqu猫 filtre les pel路l铆cules entre un `ID` inicial i un `ID` final.
- Executa la consulta. Es mostrar脿 el quadre de di脿leg per a introduir els par脿metres.

> Compte amb l'ordre dels par脿metres perqu猫 en aquest cas estan a l'inrev茅s; 茅s a dir, *Base* els demana en ordre invers.

Aix貌 provocar脿 que se seleccionen aquelles pel路l铆cules els valors de les quals coincidisquen amb els introdu茂ts (per exemple, seleccionar 0 i 3)

- 馃捑 Guarda la consulta amb nom *`CP_id_entre_pelis`*.
- Tanca la consulta.

### Consulta *`CP_dur_gen_pelis`*

En el cas dels operadors textuals 煤nicament podrem utilitzar el d'igualaci贸, ja que en introduir el valor, als par脿metres se'ls afigen cometes, amb el que 煤nicament es filtren aquells valors que siguen iguals al valor introdu茂t. Un exemple seria el de seleccionar aquelles pel路l铆cules el director de les quals siga un determinat.

- Crea una consulta sobre la taula `PELICULA` en la qual s'obtinguen els camps `Id_pelicula`, `Titol`, `Director`, `Duracio` i `Genere` de les pel路l铆cules la duraci贸 de les quals siga major a una determinada i el g猫nere de la qual siga un determinat.
- 馃捑 Guarda la consulta amb nom `CP_dur_gen_pelis`.
- Tanca la consulta.

## Operadors de text

- Crea una consulta en vista de disseny.
- Taula: `PELICULA`.
- Camps: `Id_pelicula`, `Titol`, `Director`, `Any`, `Suport`, `Duracio`, `Genere` i `Argument`.
- Estableix un criteri per a obtindre les pel路l铆cules el g猫nere de les quals comence pel text `*A`.
- 馃捑 Guarda la consulta amb nom `CP_gen_A_pelis`.
- Tanca la consulta.

## Combinaci贸 de criteris `AND`

Realitzarem una consulta que retorne les pel路l铆cules amb el suport especificat, amb el g猫nere especificat i amb una duraci贸 entre 2 valors que especifiquem.

- Crea una consulta en vista de disseny.
- Taula: `PELICULA`.
- Camps: `Genere`, `Titol`, `Director`, `Suport`, `Duracio` i `Argument`.
- Ordena ascendentment per `Genere` i `Titol`.
- Estableix els filtres en la fila `Criteri`:
  - Genere: *`:Genere`*
  - Suport: *`:Suport`*
  - Duracio: *`BETWEEN :durmin AND :durmax`*
- Executa la consulta. Comprova que es mostren les pel路l铆cules que compleixen tots els criteris.
- 馃捑 Guarda la consulta amb nom `CP_AND_criteris`.
Tanca la consulta.

## Combinaci贸 de criteris `OR`

Realitzarem una consulta que retorne les pel路l铆cules amb el suport especificat o el t铆tol del qual continga la lletra `"m"` o que tinguen una duraci贸 entre 2 valors que especifiquem.

- Crea una consulta en vista de disseny.
  - Taula: `PELICULA`.
  - Camps: `Genere`, `Titol`, `Director`, `Suport`, `Duracio` i `Argument`.
  - Ordena ascendentment per `Genere` i `Titol`.
  - Estableix els filtres en la fila `Criteri` en diferents files:
    - Genere: *`'LIKE *m*'`*
    - Suport: *`:Suport`*
    - Duracio: *`BETWEEN :durmin AND :durmax`*
- Executa la consulta. Comprova que es mostren les pel路l铆cules que compleixen algun dels criteris.
- 馃捑 Guarda la consulta amb nom `CP_OR_criteris`.
- Tanca la consulta.

---

- 馃捑 Guarda els canvis en la base de dades.
- Tanca la base de dades.
