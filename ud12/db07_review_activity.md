UD12: Bases de dades (II)

# 馃摑 *Activitat 7: Exercici de recopilaci贸. Agenda electr貌nica*

# Crear base de dades

- Crea una nova base de dades anomenada `Agenda`.
- Deixa les opcions que estan seleccionades per defecte.

# Crear taules

Una vegada creada la base de dades, crearem les taules necess脿ries.

## Taula: `CONTACTE`

Crea la taula de contactes de l'agenda electr貌nica amb els seg眉ents camps i propietats:

Camp | Tipus | Longitud | Descripci贸
-|-|-|-
Id_contacte | Enter [`INTEGER`] | *Per defecte* | Identificador (clau prim脿ria)
Nom | Text [`VARCHAR`] | 25 | Nom del contacte
Cognoms | Text [`VARCHAR`] | 50 | Cognoms del contacte
DNI | Text [`VARCHAR`] | 10 | DNI
Telefon | Text [`VARCHAR`] 12 | Tel猫fon
Email | Text [`VARCHAR`] | 50 | Correu electr貌nic
Data_aniv | Data [`DATE`] | *Per defecte* | Data d'aniversari
Adreca | Text [`VARCHAR`] | 50 | Adre莽a
Poblacio | Text [`VARCHAR`] | 50 | Poblaci贸
Provincia | Text [`VARCHAR`] | 20 | Prov铆ncia
CP | Text [`VARCHAR`] | 5 | Codi postal
Categoria | Text [`VARCHAR`] | 20 | Codi de categoria (classificaci贸)
Foto | Imatge [`LONGVARBINARY`] | *Per defecte* | Foto del contacte
Observacions | Nota [`LONGVARCHAR`] | *Per defecte* | Observacions diverses

- Fixa com a clau prim脿ria el camp `Id_contacte`.
- Guarda la taula amb el nom `CONTACTE`.

## Taula: `CATEGORIA`

Introdueix els camps que s'indiquen a continuaci贸:

Camp | Tipus | Longitud | Descripci贸
-|-|-|-
Categoria | Text [`VARCHAR`] | 20 | Codi de la categoria de classificaci贸 de contactes
Descripcio | Text [`VARCHAR`] | 50 | Descripci贸 de la categoria

- Fixa com a clau prim脿ria el camp `Categoria`.
- Guarda la taula amb el nom `CATEGORIA`.

## Taula: `PROVINCIA`

Introdueix els camps que s'indiquen a continuaci贸:

Camp | Tipus | Longitud | Descripci贸
-|-|-|-
Provincia | Text [`VARCHAR`] | 20 | Prov铆ncia

- Fixa com a clau prim脿ria el camp `Provincia`.
- Guarda la taula amb el nom `PROVINCIA`.

# Establir propietats de camps

## Taula `CONTACTE`. Format de dades

- Camp `Data_aniv`. Estableix un nou format: tria la categoria Data, format *`DD/MM/AAAA`*.

## Taula `CONTACTE`. Valor requerit

- Camp `Nom`. Estableix el camp com requerit.
- Camp `Cognoms`. Estableix el camp com requerit.
- Camp `Categoria`. Estableix el camp com requerit.

D'aquesta manera, per a cada registre ser脿 obligatori introduir el nom, cognoms i codi de categoria del contacte.

# Edici贸 de taules

## Taula `CONTACTE`. Tipus de dades *Autonum猫ric*

- Camp `Id_contacte`. Estableix la propietat `Valor Autom脿tic` a *`S铆`*.

A partir d'ara, cada vegada que introdu茂m una nova fila en la taula `CONTACTE`, el camp `Id_contacte` prendr脿 el major valor assignat fins a aqueix moment incrementat en 1.

## Relacions

Despr茅s del disseny de taules, podem comprovar que la taula de contactes t茅 camps en com煤 amb la taula de categories i la taula de prov铆ncies. Per tant, hem de relacionar les taules mitjan莽ant aqueixos camps en com煤.

Els n煤meros indiquen la cardinalitat. 脡s a dir:

## Relaci贸 categoria-contacte

- `(N)` Donada una categoria, pot haver-hi molts contactes que pertanguen a ella.
- `(1)` Donat un contacte, nom茅s pot pert脿nyer a una categoria de classificaci贸.

## Relaci贸 categoria-prov铆ncia

- `(N)` Donada una prov铆ncia, pot tindre molts contactes que visquen en ella.
- `(1)` Donat un contacte, nom茅s pot viure en una prov铆ncia.

# Establir una relaci贸 un a molts `(1:N)`

En el nostre cas, en la taula `CONTACTE` tenim un camp `Categoria` que fa refer猫ncia a la classificaci贸 del contacte: *amic, fam铆lia, conegut, etc.* Per tant, la columna ha de ser de la mateixa mena de dades que la columna que siga clau prim脿ria en l'altra taula i els valors que podr脿 contindre ser脿 qualsevol dels valors que prenga la clau prim脿ria en aquesta taula.

De la mateixa manera, en la taula `CONTACTE` tenim un camp `Provincia` que fa refer猫ncia a la prov铆ncia en qu猫 viu el nostre contacte.

> 鈿? Els camps relacionats no han de tindre els mateixos noms, per貌 han de tindre el mateix tipus de dades i la mateixa grand脿ria. 脡s a dir, han de contindre el mateix tipus d'informaci贸. En la taula `CONTACTE` el camp `Categoria` ha de ser de la mateixa mena de dades que el camp de la taula `CATEGORIA`. El mateix succeeix amb el camp `Provincia` i la taula `PROVINCIA`.

Relaciona les taules `CONTACTE`, `CATEGORIA` i `PROVINCIA` mitjan莽ant els camps corresponents.

- 馃捑 Guarda els canvis.

# Crear formularis

## Formulari: `FCONTACTE`

Crea un formulari anomenat `FCONTACTE` amb l'auxiliar:

- Taula: `CONTACTE`
- Que continga tots els camps de la taula
- L'organitzaci贸 ser脿 `En columnes - Etiquetes a l'esquerra`
- L'estil el que m茅s t'agrade

## Formulari: `FCATEGORIA`

Crea un formulari anomenat `FCATEGORIA` amb l'auxiliar:

- Taula: `CATEGORIA`
- Que continga tots els camps de la taula
- L'organitzaci贸 ser脿 `Full de dades`
- L'estil el que m茅s t'agrade

## Formulari: `FPROVINCIA`

Crea un formulari anomenat `FPROVINCIA` amb l'auxiliar:

- Taula: `PROVINCIA`
- Que continga tots els camps de la taula
- L'organitzaci贸 ser脿 `Full de dades`
- L'estil el que m茅s t'agrade

# Introducci贸 de dades

## Categories

- Obri el formulari `FCATEGORIA`.
- Introdueix les seg眉ents dades:

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

- 馃捑 Guarda els canvis i tanca el formulari.

## Prov铆ncies

- Obri el formulari `FPROVINCIA`.
- Introdueix les seg眉ents dades:

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

- 馃捑 Guarda els canvis i tanca el formulari.

# Disseny de formularis

Canviarem aspectes est猫tics del disseny del formulari `FCONTACTE` perqu猫 es mostre millor la fotografia i les observacions de cada contacte.

## Edita el formulari `FCONTACTE`

### Camp `Foto`

La foto dels contactes es mostra xicoteta i no es pot apreciar b茅.

- Mou-ho a la dreta del formulari. Fes-lo m茅s gran.

### Camp `Observacions`

Ens assegurarem que les observacions de cada contacte es puguen llegir b茅.

- Mou-ho a l'esquerra del formulari.
- Canvia la propietat `Alineaci贸 vert` al valor *`Superior`*.
- Canvia la propietat `Entrada en l铆nies m煤ltiples` al valor *`S铆`*.
- Comprova que ara es visualitza tot correctament.

### Color de fons

Anem canviar el color de fons del formulari de contactes.

- Ve al men煤 `Format` 鈫? `P脿gina`, pestanya `脌rea`. Canvia el color per el que vulgues.
- 馃捑 Guarda els canvis en el disseny del formulari.
- Comprova que ara es visualitza el color seleccionat.

# Camps amb format

## Camp `Data_aniv`

Ha d'apar茅ixer en format dia, mes i any `DD/MM/AAAA`: dia, mes i any (4 xifres) en format num猫ric.

Edita el formulari `FCONTACTE`.

- Prem sobre la icona de la barra esquerra anomenat `M茅s controls`.
- Fes clic en la icona `Camp de data`.
- Dibuixa el camp en el formulari i fes doble clic sobre ell.
- En la pestanya `General`, tria la propietat `Vora`, posa el valor `Vista en 3D`.
- En la propietat Format de data, selecciona la m脿scara `DD/MM/YYYY`.
- Selecciona la pestanya `Dades`. Desplega la llista i tria el camp `Data_aniv`.
- Tanca la finestra de Propietats.

Ara enllacem el nou camp amb un camp de la nostra base de dades.

- Fes clic en el camp antic i prem la tecla `Supr`.
- Col路loca el nou camp en el seu lloc.
- Prem sobre la icona de la barra esquerra anomenat `Etiqueta`.
- En el formulari, dibuixa una etiqueta a l'esquerra del nou camp. Fes doble clic sobre l'etiqueta.
- En la propietat `Etiqueta` escriu el text `Data aniversari`.
- Tanca el formulari.
- 馃捑 Guarda els canvis.

# Llistes de dades

Modificarem el formulari perqu猫 els camps de categoria i prov铆ncia siguen llestes desplegables amb els valors que hem introdu茂t anteriorment en les taules.

## Camp `Categoria`

- Edita el formulari `FCONTACTE`.
- Prem sobre la icona de la barra esquerra anomenat `Llistat`.
- Dibuixa el nou control a la dreta del camp categoria.
- Apareixer脿 l'assistent per a guiar-nos en el proc茅s. Seguim els passos corresponents.
- Eliminarem el camp 鈥?*Categoria鈥? antic.

## Camp `Provincia`

- Crea la llista desplegable, per貌 en aquest cas amb la taula `PROVINCIA`.
- Esborra el camp antic.
- Tanca el formulari.

# Introducci贸 de contactes

- Obri el formulari `FCONTACTE` mitjan莽ant doble clic.
- Introdueix dades de 5 contactes en l'agenda. Pots introduir les dades que desitges.
- Introdueix les fotos dels contactes en l'agenda.
- Tanca el formulari.

# Ordre de tabulaci贸

Canviarem l'ordre de tabulaci贸 perqu猫 siga consecutiu.

- Edita el formulari `FCONTACTE`.

Primer canviarem de nom tots els camps perqu猫 sapiem quin 茅s quin.

- Ve al camp `Id_contacte`. Fes doble clic sobre ell.
- En la propietat `Nom`, escriu el text `Id_contacte`.
- Tanca les propietats.

- Repeteix el mateix proc茅s amb cadascuna de les etiquetes, posant el nom del camp corresponent.

Establirem l'ordre de tabulaci贸 correcte.

- En la barra d'eines inferior, fes clic en la icona `Ordre d'activaci贸`.
- Mou els diferents camps perqu猫 quede l'ordre correcte. Utilitza els botons per a despla莽ar cap amunt o cap avall.
- 馃捑 Guarda els canvis i tanca el formulari.
- Fes doble clic en el formulari. Comprova que ara est脿 correcte l'ordre de tabulaci贸. Per a aix貌, passa amb la tecla tabulador d'un camp a un altre.
- Tanca el formulari.

# Consultes

## Crea una consulta anomenada `C_contactes_resum`:

- Taula: `CONTACTE`
- Que continga els camps `Cognoms`, `Nom`, `Telefon`, Email i `Categoria`
- En l'apartat `脌lies` de cada camp escriu *`Cognoms`*, *`Nom`*, *`Tel猫fon`*, *`Correu electr貌nic`* i *`Categoria`*
- Que estiga ordenada ascendentment pel camp `Cognoms` i `Nom`

## Crea una consulta anomenada `CP_contacte_prov`, que ens retorne les dades dels contactes d'una prov铆ncia determinada

- Taula: `CONTACTE`
- Que continga els camps `Cognoms`, `Nom`, `Telefon`, `Email`, `Categoria` i `Provincia`
- En l'apartat `脌lies` de cada camp escriu *`Cognoms`*, *`Nom`*, *`Tel猫fon`*, *`Correu electr貌nic`*, *`Categoria`* i *`Prov铆ncia`*
- Que estiga ordenada ascendentment pel camp `Cognoms` i `Nom`
- Que demane la prov铆ncia mitjan莽ant par脿metre

## Crea una consulta anomenada `CP_data_categ`, que ens retorne les dades dels contactes que hagen nascut despr茅s d'una data determinada i que siguen d'una categoria determinada

- Taula: `CONTACTE`
- Que continga els camps `Cognoms`, `Nom`, `Telefon`, `Email`, `Categoria` i `Provincia`
- En l'apartat `脌lies` de cada camp escriu *`Cognoms`*, *`Nom`*, *`Tel猫fon`*, *`Correu electr貌nic`*, *`Categoria`* i *`Prov铆ncia`*
- Que estiga ordenada ascendentment pel camp `Cognoms` i `Nom`
- Que demane la data i utilitze un operador de comparaci贸
- Que demane la categoria mitjan莽ant par脿metre

## Crea una consulta anomenada `CG_PROVINCIA`, que mostre el nom de cada prov铆ncia emmagatzemada i el total de contactes que tenim de cada prov铆ncia

- Taula: `CONTACTE`
- Que continga els camps `Provincia` i `Id_contacte`
- En l'apartat `脌lies` de cada camp escriu *`Prov铆ncia`* i *`Total contactes`*
- Que estiga ordenada ascendentment pel camp `Provincia`
- Que agrupe per prov铆ncia i compte per `Id_contacte`

# Subformularis

## Crear subformulari `SFPROVINCIA`

- Crea un subformulari de nom `SFPROVINCIA` fent que, cada vegada que ens movem entre els diferents registres, ens mostre la informaci贸 de tots els contactes pertanyents a aqueixa prov铆ncia.
- 馃捑 Guarda els canvis.
- Tanca el formulari.

## Formulari `FCONTACTE`. Afegir subformulari

- Modifica el formulari `FCONTACTE` per a fer-ho m茅s intu茂tiu, de manera que cada vegada que ens movem entre els diferents registres, ens mostre la descripci贸 de la categoria a la qual pertany un contacte.
- 馃捑 Guarda els canvis.
- Tanca el formulari.

---

- 馃捑 Guarda els canvis en la base de dades.
- Tanca la base de dades.
