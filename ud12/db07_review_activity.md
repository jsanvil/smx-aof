UD12: Bases de dades (II)

# 📝 *Activitat 7: Exercici de recopilació. Agenda electrònica*

# Crear base de dades

- Crea una nova base de dades anomenada `Agenda`.
- Deixa les opcions que estan seleccionades per defecte.

# Crear taules

Una vegada creada la base de dades, crearem les taules necessàries.

## Taula: `CONTACTE`

Crea la taula de contactes de l'agenda electrònica amb els següents camps i propietats:

Camp | Tipus | Longitud | Descripció
-|-|-|-
Id_contacte | Enter [`INTEGER`] | *Per defecte* | Identificador (clau primària)
Nom | Text [`VARCHAR`] | 25 | Nom del contacte
Cognoms | Text [`VARCHAR`] | 50 | Cognoms del contacte
DNI | Text [`VARCHAR`] | 10 | DNI
Telefon | Text [`VARCHAR`] 12 | Telèfon
Email | Text [`VARCHAR`] | 50 | Correu electrònic
Data_aniv | Data [`DATE`] | *Per defecte* | Data d'aniversari
Adreca | Text [`VARCHAR`] | 50 | Adreça
Poblacio | Text [`VARCHAR`] | 50 | Població
Provincia | Text [`VARCHAR`] | 20 | Província
CP | Text [`VARCHAR`] | 5 | Codi postal
Categoria | Text [`VARCHAR`] | 20 | Codi de categoria (classificació)
Foto | Imatge [`LONGVARBINARY`] | *Per defecte* | Foto del contacte
Observacions | Nota [`LONGVARCHAR`] | *Per defecte* | Observacions diverses

- Fixa com a clau primària el camp `Id_contacte`.
- Guarda la taula amb el nom `CONTACTE`.

## Taula: `CATEGORIA`

Introdueix els camps que s'indiquen a continuació:

Camp | Tipus | Longitud | Descripció
-|-|-|-
Categoria | Text [`VARCHAR`] | 20 | Codi de la categoria de classificació de contactes
Descripcio | Text [`VARCHAR`] | 50 | Descripció de la categoria

- Fixa com a clau primària el camp `Categoria`.
- Guarda la taula amb el nom `CATEGORIA`.

## Taula: `PROVINCIA`

Introdueix els camps que s'indiquen a continuació:

Camp | Tipus | Longitud | Descripció
-|-|-|-
Provincia | Text [`VARCHAR`] | 20 | Província

- Fixa com a clau primària el camp `Provincia`.
- Guarda la taula amb el nom `PROVINCIA`.

# Establir propietats de camps

## Taula `CONTACTE`. Format de dades

- Camp `Data_aniv`. Estableix un nou format: tria la categoria Data, format *`DD/MM/AAAA`*.

## Taula `CONTACTE`. Valor requerit

- Camp `Nom`. Estableix el camp com requerit.
- Camp `Cognoms`. Estableix el camp com requerit.
- Camp `Categoria`. Estableix el camp com requerit.

D'aquesta manera, per a cada registre serà obligatori introduir el nom, cognoms i codi de categoria del contacte.

# Edició de taules

## Taula `CONTACTE`. Tipus de dades *Autonumèric*

- Camp `Id_contacte`. Estableix la propietat `Valor Automàtic` a *`Sí`*.

A partir d'ara, cada vegada que introduïm una nova fila en la taula `CONTACTE`, el camp `Id_contacte` prendrà el major valor assignat fins a aqueix moment incrementat en 1.

## Relacions

Després del disseny de taules, podem comprovar que la taula de contactes té camps en comú amb la taula de categories i la taula de províncies. Per tant, hem de relacionar les taules mitjançant aqueixos camps en comú.

Els números indiquen la cardinalitat. És a dir:

## Relació categoria-contacte

- `(N)` Donada una categoria, pot haver-hi molts contactes que pertanguen a ella.
- `(1)` Donat un contacte, només pot pertànyer a una categoria de classificació.

## Relació categoria-província

- `(N)` Donada una província, pot tindre molts contactes que visquen en ella.
- `(1)` Donat un contacte, només pot viure en una província.

# Establir una relació un a molts `(1:N)`

En el nostre cas, en la taula `CONTACTE` tenim un camp `Categoria` que fa referència a la classificació del contacte: *amic, família, conegut, etc.* Per tant, la columna ha de ser de la mateixa mena de dades que la columna que siga clau primària en l'altra taula i els valors que podrà contindre serà qualsevol dels valors que prenga la clau primària en aquesta taula.

De la mateixa manera, en la taula `CONTACTE` tenim un camp `Provincia` que fa referència a la província en què viu el nostre contacte.

> ⚠ Els camps relacionats no han de tindre els mateixos noms, però han de tindre el mateix tipus de dades i la mateixa grandària. És a dir, han de contindre el mateix tipus d'informació. En la taula `CONTACTE` el camp `Categoria` ha de ser de la mateixa mena de dades que el camp de la taula `CATEGORIA`. El mateix succeeix amb el camp `Provincia` i la taula `PROVINCIA`.

Relaciona les taules `CONTACTE`, `CATEGORIA` i `PROVINCIA` mitjançant els camps corresponents.

- 💾 Guarda els canvis.

# Crear formularis

## Formulari: `FCONTACTE`

Crea un formulari anomenat `FCONTACTE` amb l'auxiliar:

- Taula: `CONTACTE`
- Que continga tots els camps de la taula
- L'organització serà `En columnes - Etiquetes a l'esquerra`
- L'estil el que més t'agrade

## Formulari: `FCATEGORIA`

Crea un formulari anomenat `FCATEGORIA` amb l'auxiliar:

- Taula: `CATEGORIA`
- Que continga tots els camps de la taula
- L'organització serà `Full de dades`
- L'estil el que més t'agrade

## Formulari: `FPROVINCIA`

Crea un formulari anomenat `FPROVINCIA` amb l'auxiliar:

- Taula: `PROVINCIA`
- Que continga tots els camps de la taula
- L'organització serà `Full de dades`
- L'estil el que més t'agrade

# Introducció de dades

## Categories

- Obri el formulari `FCATEGORIA`.
- Introdueix les següents dades:

Categoria | Descripcio
----------|------------
AMICS     | Millors amics
CONEGUTS  | Coneguts
DIVERSIO  | Companys de festa
FAMILIA   | Familiar
FRIKI     | Personatjes frikis
NEGOCIS   | Contactes comercials
TREBALL   | Companys de treball
VIP       | Contacte important

- 💾 Guarda els canvis i tanca el formulari.

## Províncies

- Obri el formulari `FPROVINCIA`.
- Introdueix les següents dades:

Provincia |
----------|
ALBACETE  |
ALACANT   |
BARCELONA |
CASTELLO  |
CONCA     |
MADRID    |
MURCIA    |
TEROL     |
VALENCIA  |

- 💾 Guarda els canvis i tanca el formulari.

# Disseny de formularis

Canviarem aspectes estètics del disseny del formulari `FCONTACTE` perquè es mostre millor la fotografia i les observacions de cada contacte.

## Edita el formulari `FCONTACTE`

### Camp `Foto`

La foto dels contactes es mostra xicoteta i no es pot apreciar bé.

- Mou-ho a la dreta del formulari. Fes-lo més gran.

### Camp `Observacions`

Ens assegurarem que les observacions de cada contacte es puguen llegir bé.

- Mou-ho a l'esquerra del formulari.
- Canvia la propietat `Alineació vert` al valor *`Superior`*.
- Canvia la propietat `Entrada en línies múltiples` al valor *`Sí`*.
- Comprova que ara es visualitza tot correctament.

### Color de fons

Anem canviar el color de fons del formulari de contactes.

- Ve al menú `Format` → `Pàgina`, pestanya `Àrea`. Canvia el color per el que vulgues.
- 💾 Guarda els canvis en el disseny del formulari.
- Comprova que ara es visualitza el color seleccionat.

# Camps amb format

## Camp `Data_aniv`

Ha d'aparéixer en format dia, mes i any `DD/MM/AAAA`: dia, mes i any (4 xifres) en format numèric.

Edita el formulari `FCONTACTE`.

- Prem sobre la icona de la barra esquerra anomenat `Més controls`.
- Fes clic en la icona `Camp de data`.
- Dibuixa el camp en el formulari i fes doble clic sobre ell.
- En la pestanya `General`, tria la propietat `Vora`, posa el valor `Vista en 3D`.
- En la propietat Format de data, selecciona la màscara `DD/MM/YYYY`.
- Selecciona la pestanya `Dades`. Desplega la llista i tria el camp `Data_aniv`.
- Tanca la finestra de Propietats.

Ara enllacem el nou camp amb un camp de la nostra base de dades.

- Fes clic en el camp antic i prem la tecla `Supr`.
- Col·loca el nou camp en el seu lloc.
- Prem sobre la icona de la barra esquerra anomenat `Etiqueta`.
- En el formulari, dibuixa una etiqueta a l'esquerra del nou camp. Fes doble clic sobre l'etiqueta.
- En la propietat `Etiqueta` escriu el text `Data aniversari`.
- Tanca el formulari.
- 💾 Guarda els canvis.

# Llistes de dades

Modificarem el formulari perquè els camps de categoria i província siguen llestes desplegables amb els valors que hem introduït anteriorment en les taules.

## Camp `Categoria`

- Edita el formulari `FCONTACTE`.
- Prem sobre la icona de la barra esquerra anomenat `Llistat`.
- Dibuixa el nou control a la dreta del camp categoria.
- Apareixerà l'assistent per a guiar-nos en el procés. Seguim els passos corresponents.
- Eliminarem el camp “*Categoria” antic.

## Camp `Provincia`

- Crea la llista desplegable, però en aquest cas amb la taula `PROVINCIA`.
- Esborra el camp antic.
- Tanca el formulari.

# Introducció de contactes

- Obri el formulari `FCONTACTE` mitjançant doble clic.
- Introdueix dades de 5 contactes en l'agenda. Pots introduir les dades que desitges.
- Introdueix les fotos dels contactes en l'agenda.
- Tanca el formulari.

# Ordre de tabulació

Canviarem l'ordre de tabulació perquè siga consecutiu.

- Edita el formulari `FCONTACTE`.

Primer canviarem de nom tots els camps perquè sapiem quin és quin.

- Ve al camp `Id_contacte`. Fes doble clic sobre ell.
- En la propietat `Nom`, escriu el text `Id_contacte`.
- Tanca les propietats.

- Repeteix el mateix procés amb cadascuna de les etiquetes, posant el nom del camp corresponent.

Establirem l'ordre de tabulació correcte.

- En la barra d'eines inferior, fes clic en la icona `Ordre d'activació`.
- Mou els diferents camps perquè quede l'ordre correcte. Utilitza els botons per a desplaçar cap amunt o cap avall.
- 💾 Guarda els canvis i tanca el formulari.
- Fes doble clic en el formulari. Comprova que ara està correcte l'ordre de tabulació. Per a això, passa amb la tecla tabulador d'un camp a un altre.
- Tanca el formulari.

# Consultes

## Crea una consulta anomenada `C_contactes_resum`:

- Taula: `CONTACTE`
- Que continga els camps `Cognoms`, `Nom`, `Telefon`, Email i `Categoria`
- En l'apartat `Àlies` de cada camp escriu *`Cognoms`*, *`Nom`*, *`Telèfon`*, *`Correu electrònic`* i *`Categoria`*
- Que estiga ordenada ascendentment pel camp `Cognoms` i `Nom`

## Crea una consulta anomenada `CP_contacte_prov`, que ens retorne les dades dels contactes d'una província determinada

- Taula: `CONTACTE`
- Que continga els camps `Cognoms`, `Nom`, `Telefon`, `Email`, `Categoria` i `Provincia`
- En l'apartat `Àlies` de cada camp escriu *`Cognoms`*, *`Nom`*, *`Telèfon`*, *`Correu electrònic`*, *`Categoria`* i *`Província`*
- Que estiga ordenada ascendentment pel camp `Cognoms` i `Nom`
- Que demane la província mitjançant paràmetre

## Crea una consulta anomenada `CP_data_categ`, que ens retorne les dades dels contactes que hagen nascut després d'una data determinada i que siguen d'una categoria determinada

- Taula: `CONTACTE`
- Que continga els camps `Cognoms`, `Nom`, `Telefon`, `Email`, `Categoria` i `Provincia`
- En l'apartat `Àlies` de cada camp escriu *`Cognoms`*, *`Nom`*, *`Telèfon`*, *`Correu electrònic`*, *`Categoria`* i *`Província`*
- Que estiga ordenada ascendentment pel camp `Cognoms` i `Nom`
- Que demane la data i utilitze un operador de comparació
- Que demane la categoria mitjançant paràmetre

## Crea una consulta anomenada `CG_PROVINCIA`, que mostre el nom de cada província emmagatzemada i el total de contactes que tenim de cada província

- Taula: `CONTACTE`
- Que continga els camps `Provincia` i `Id_contacte`
- En l'apartat `Àlies` de cada camp escriu *`Província`* i *`Total contactes`*
- Que estiga ordenada ascendentment pel camp `Provincia`
- Que agrupe per província i compte per `Id_contacte`

# Subformularis

## Crear subformulari `SFPROVINCIA`

- Crea un subformulari de nom `SFPROVINCIA` fent que, cada vegada que ens movem entre els diferents registres, ens mostre la informació de tots els contactes pertanyents a aqueixa província.
- 💾 Guarda els canvis.
- Tanca el formulari.

## Formulari `FCONTACTE`. Afegir subformulari

- Modifica el formulari `FCONTACTE` per a fer-ho més intuïtiu, de manera que cada vegada que ens movem entre els diferents registres, ens mostre la descripció de la categoria a la qual pertany un contacte.
- 💾 Guarda els canvis.
- Tanca el formulari.

---

- 💾 Guarda els canvis en la base de dades.
- Tanca la base de dades.
