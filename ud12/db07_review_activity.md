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
Província | Text [`VARCHAR`] | 20 | Província
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

> Els camps relacionats no han de tindre els mateixos noms, però han de tindre el mateix tipus de dades i la mateixa grandària. És a dir, han de contindre el mateix tipus d'informació. En la taula `CONTACTE` el camp `Categoria` ha de ser de la mateixa mena de dades que el camp de la taula `CATEGORIA`. El mateix succeeix amb el camp `Provincia` i la taula `PROVINCIA`.

Relaciona les taules `CONTACTE`, `CATEGORIA` i `PROVINCIA` mitjançant els camps corresponents.

- Guarda els canvis.

# Crear formularis 

## Formulari: `FCONTACTE`

Crea un formulari anomenat `FCONTACTE` amb l'auxiliar:
- Taula: CONTACTE
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

- Guarda els canvis i tanca el formulari.

## Províncies

- Obri el formulari `FPROVINCIA`.
- Introdueix les següents dades:

Provincia |
-|
ALBACETE
ALICANTE
BARCELONA
CASTELLO
CONCA
MADRID
MURCIA
TEROL
VALENCIA

- Guarda els canvis i tanca el formulari.

# Disseny de formularis 

Canviarem aspectes estètics del disseny del formulari `FCONTACTE` perquè es mostre millor la fotografia i les observacions de cada contacte.

## Edita el formulari `FCONTACTE`.

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

- Ve al menú `Format` → `Pàgina`, pestanya `Àrea`. Canvia el color pel qual vulgues.
- Guarda els canvis en el disseny del formulari.
- Comprova que ara es visualitza el color seleccionat.

# Campos amb format 

## Camp `Data_aniv`

Ha d'aparéixer en format dia, mes i any `DD/MM/AAAA`: dia, mes i any (4 xifres) en format numèric.

Edita el formulari `FCONTACTE`.
- Prem sobre la icona de la barra esquerra anomenat `Més controls`. 
- Fes clic en la icona `Camp de data`. 
- Dibuixa el camp en el formulari i fes doble clic sobre ell.
- En la pestanya `General`, tria la propietat `Vora`, posa el valor `Vista en 3D`.
- En la propietat Format de data, selecciona la màscara `DD/MM/YYYY`.
- En la propietat Control de format, posa el valor Sí. Ara només deixarà introduir la data amb aquest format.
- Selecciona la pestanya `Dades`. Desplega la llista i tria el camp `Data_aniv`.
- Tanca la finestra de Propietats.

Ara enllacem el nou camp amb un camp de la nostra base de dades.

- Fes clic en el camp antic i prem la tecla `Supr`.
- Col·loca el nou camp en el seu lloc.
- Prem sobre la icona de la barra esquerra anomenat `Etiqueta`. 
- En el formulari, dibuixa una etiqueta a l'esquerra del nou camp. Fes doble clic sobre l'etiqueta.
- En la propietat `Títol` escriu el text `Data aniversari`.
- Tanca el formulari.
- Guarda els canvis.

# Llistes de dades 

Modificarem el formulari perquè els camps de categoria i província siguen llestes desplegables amb els valors que hem introduït anteriorment en les taules.

Camp “Categoria”

Edita el formulari *FCONTACTO.
Prem sobre la icona de la barra esquerra anomenat Llistat. 
Dibuixa el nou control a la dreta del camp categoria.
Apareixerà l'assistent per a guiar-nos en el procés. Seguim els passos corresponents.

Tria la taula *CATEGORIA. Fes clic en Següent.
Selecciona el camp “*Categoria”. Fes clic en Següent.
Tria el camp “*Categoria” tant a l'esquerra com a la dreta. Fes clic a Finalitzar.
Acabem de crear una llista que mostrarà totes les categories de contactes de l'agenda. Ara eliminarem el camp “*Categoria” antic.

Fes clic en el camp “*categoria” i prem la tecla *Supr.
Situa la llista en el mateix lloc que estava el camp antic. Fes més ampla la llista.
Prem sobre la icona de la barra esquerra anomenat Etiqueta . En el formulari, dibuixa una etiqueta a l'esquerra de la llista de categories.
Fes doble clic sobre l'etiqueta. En la propietat Títol escriu el text “Categoria”.
Camp “Província”

Crea la llista desplegable, però en aquest cas amb la taula PROVÍNCIA.
Esborra el camp antic.
Afig l'etiqueta amb el text “Província”.
Tanca el formulari.
1.12. Introducció de dades
Obri el formulari *FCONTACTO mitjançant doble clic.
Introdueix dades de diferents contactes en l'agenda. Pot introduir-se les dades que es desitge.
Tanca el formulari.
Veu a la taula CONTACTE. Obri-la i comprova que s'han guardat totes les dades. Per exemple:


Introduirem les fotos dels nostres contactes en l'agenda.

Descàrrega 5 fotos d'Internet que vulgues. Procura que les fotos no ocupen molt espai per a no superar el límit de grandària a l'hora de pujar al portal la base de dades.
Obri el formulari *FCONTACTO mitjançant doble clic.
Mitjançant el formulari, introdueix una foto per a cada contacte de l'agenda.
1.13. Ordre de tabulació 
Canviarem l'ordre de tabulació perquè siga consecutiu.

Edita el formulari *FCONTACTO.
Primer canviarem de nom tots els camps perquè sapiem quin és quin.

Veu al camp “Aneu_contacte”. Fes doble clic sobre ell. En la propietat Nom, escriu el text “Aneu_contacte”. Tanca les propietats.
Repeteix el mateix procés amb cadascuna de les etiquetes, posant el nom del camp corresponent.
Després establim l'ordre de tabulació correcte.

En la barra d'eines inferior, fes clic en la icona Ordre d'activació. 
Mou els diferents camps perquè quede l'ordre correcte. Utilitza els botons per a desplaçar cap amunt o cap avall. Per exemple:


Guarda els canvis i tanca el formulari.
Fes doble clic en el formulari. Comprova que ara està correcte l'ordre de tabulació. Per a això, passa amb la tecla tabulador d'un camp a un altre.
Tanca el formulari.
1.14. Integritat referencial 
En la relació que hem definit s'impedeix que qualsevol registre relacionat siga modificat o eliminat. Aquesta propietat és el que es coneix com a integritat referencial.

Una vegada establida una relació, comprovarem que és correcta. Per a això només hem d'intentar realitzar alguna operació no permesa i veure que es compleix la integritat referencial.

Cas 1. Esborrar una categoria a la qual pertanyen contactes

Veu a la taula *CATEGORIA.
Elimina una categoria que tinga contactes associats, per exemple “Família”.
Guarda els canvis.
Comprova que Base ens mostra un missatge d'error perquè estem esborrant una categoria a la qual pertanyen contactes relacionats en la taula CONTACTE.
Prem Acceptar. Desfés els canvis.
Tanca la taula *CATEGORIA.
També podem provar des del formulari.

Veu al formulari *FCATEGORIA i fes doble clic sobre ell.
Elimina una categoria que tinga contactes associats, per exemple “Família”. Respon Sí a la pregunta que es formula. Guarda els canvis.
Per exemple:


Tanca el formulari.
Cas 2. Esborrar una província en la qual viuen contactes

Veu a la taula PROVÍNCIA.
Elimina una província que tinga contactes associats, per exemple Madrid o València.
Guarda els canvis.
Comprova que Base ens mostra un missatge d'error perquè estem esborrant una província en la qual viuen contactes relacionats en la taula CONTACTE.
Prem Acceptar. Desfés els canvis.
Tanca la taula PROVÍNCIA.
També podem provar des del formulari.

Veu al formulari *FPROVINCIA i fes doble clic sobre ell.
Elimina una província que tinga contactes associats, per exemple Madrid o València. Respon Sí a la pregunta que es formula. Guarda els canvis.
Per exemple:


Tanca el formulari.
1.15. Consultes
Crea una consulta anomenada "C_contactes_resumeixen": 
Taula: CONTACTE
Que continga els camps "Cognoms", "Nom", "*Telefono", "*Ecorreo" i "*Categoria"
En l'apartat Alias de cada camp escriu "Cognoms", "Nom", "Telèfon", "Correu electrònic" i "Categoria"
Que estiga ordenada ascendentment pel camp "Cognoms" i "Nom"
Crega una consulta anomenada "CP_contacte_*prov", que ens retorne les dades dels contactes d'una província determinada: 
Taula: CONTACTE
Que continga els camps "Cognoms", "Nom", "*Telefono", "*Ecorreo", "*Categoria" i "Província"
En l'apartat Alias de cada camp escriu "Cognoms", "Nom", "Telèfon", "Correu electrònic", "Categoria" i "Província"
Que estiga ordenada ascendentment pel camp "Cognoms" i "Nom"
Que demane la província mitjançant paràmetre
Crega una consulta anomenada "CP_data_*categ", que ens retorne les dades dels contactes que hagen nascut després d'una data determinada i que siguen d'una categoria determinada: 
Taula: CONTACTE
Que continga els camps "Cognoms", "Nom", "*Telefono", "*Ecorreo", "*Categoria" i "Província"
En l'apartat Alias de cada camp escriu "Cognoms", "Nom", "Telèfon", "Correu electrònic", "Categoria" i "Província"
Que estiga ordenada ascendentment pel camp "Cognoms" i "Nom"
Que utilitze un operador de comparació per a la data
Que demane la categoria mitjançant paràmetre
Crega una consulta anomenada *CG_PROVÍNCIA, que mostre el nom de cada província emmagatzemada i el total de contactes que tenim de cada província: 
Taula: CONTACTE
Que continga els camps "Província" i "Aneu_contacte"
En l'apartat Alias de cada camp escriu "Província" i "Total contactes"
Que estiga ordenada ascendentment pel camp "Província"
Que agrupe per província i compte per "Aneu_contacte"
1.16. *Subformularios 
Crear *subformulario *SFPROVINCIA

Crea un *subformulario de nom *SFPROVINCIA fent que, cada vegada que ens movem entre els diferents registres, ens mostre la informació de tots els contactes pertanyents a aqueixa província.
Guarda els canvis.
Tanca el formulari.
Formulari *FCONTACTO. Afegir *subformulario

Modifica el formulari *FCONTACTO per a fer-ho més intuïtiu, de manera que cada vegada que ens movem entre els diferents registres, ens mostre la descripció de la categoria a la qual pertany un contacte.
Guarda els canvis.
Tanca el formulari.

---

- 💾 Guarda els canvis en la base de dades.
- Tanca la base de dades.
