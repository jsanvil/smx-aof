**UD11: Bases de dades (I)**

# 7. *LibreOffice Base*: Consultes. Criteris d'ordenaci贸 i selecci贸. Informes

## 馃幆 Objectius

- Con茅ixer el concepte de consulta de dades.
- Utilitzar l'assistent per a crear consultes senzilles.
- Crear consultes senzilles en vista dissenye.
- Crear consultes sobre diverses taules.
- Crear consultes amb criteris d'ordenaci贸.
- Crear consultes amb criteris de selecci贸.
- Concepte d'informe.
- Crear informes usant l'assistent.

---

# 7.1. Consultes de dades

De res serveix tindre la nostra informaci贸 perfectament estructurada en taules, si no existeix la possibilitat de recuperar les dades. Per a tal fi, els Sistemes Gestors de Bases de dades i, m茅s concretament *Base*, disposen d'un tipus predeterminat d'objecte denominat **Consultes**. En aquest apartat aprendrem a crear consultes mitjan莽ant l'ajuda de l'assistent, amb el que la seua generaci贸 ser脿 molt senzilla.

Les **consultes** s贸n **objectes que permeten formular preguntes a *Base* sobre el contingut d'una o de diverses taules**; 茅s a dir, s贸n objectes que utilitzarem per a visualitzar part de la informaci贸 continguda en les nostres bases de dades. Gr脿cies a les consultes tindrem la possibilitat d'obtindre tota la informaci贸 continguda en les taules afegint interessants funcionalitats:

- Filtrar la informaci贸 per a recuperar nom茅s aquelles dades que ens interessen en cada cas.
- Ordenar la informaci贸 recuperada utilitzant tants criteris com necessitem.
- Utilitzar diverses taules per a obtindre dades combinades d'elles. Sens dubte, nom茅s per aquest motiu ja tenen sentit les bases de dades, i m茅s concretament les consultes.

El **resultat d'una consulta** es denomina **Full de Dades** i presenta aspecte de taula; no obstant aix貌, les consultes no creen noves taules, sin贸 que mostren part de la taula o les taules sobre les quals es realitza la consulta.

En *Base* les consultes es poden crear de tres maneres diferents: en mode Disseny, utilitzant l'assistent o utilitzant *SQL*.

---

# 7.2. Consultes amb l'assistent

L'Assistent per a consultes crea consultes senzilles que recuperen dades dels camps especificats en una o m茅s taules o consultes. Si es desitja, l'assistent tamb茅 pot sumar, comptar i obtindre la mitjana dels valors de grups de registres o de tots els registres i pot calcular el valor m铆nim o m脿xim d'un camp.

---

# 7.3. Consultes en vista disseny

En l'apartat anterior hem utilitzat l'assistent per a crear consultes senzilles; no obstant aix貌, *Base* disposa d'un editor per a dissenyar consultes de forma m茅s completa. En aquesta unitat aprendrem a utilitzar l'editor i a con茅ixer el potencial que es pot obtindre gr脿cies a la llibertat d'edici贸 de les consultes.

---

## 7.3.1. Consultes sobre una taula

Comen莽arem amb consultes senzilles sobre les dades d'una sola taula per a posteriorment elaborar consultes m茅s complexes. En el seg眉ent exemple crearem una consulta sobre la taula `LLIBRE` mostrant 4 camps.

---

***Exemple pr脿ctic: taula `LLIBRE`***

Fes clic en el bot贸 `Consultes` de la Barra de Base de dades.
En la zona superior de Tasques, fes clic en l'opci贸 `Crear una consulta en vista de disseny...`
Apareixer脿 el quadre de di脿leg Agregar taula o consulta.

Selecciona la taula `LLIBRE` i fes clic en el bot贸 `Afegir` (o doble clic sobre l'objecte).

En aquest moment apareixer脿 la finestra de disseny. En la zona superior d'aquesta finestra es mostra les taules o consultes agregades. En la zona inferior podem seleccionar les diferents columnes i aplicar filtres.

En la quadr铆cula inferior s'especifiquen els camps de la taula que intervenen en la consulta. S'han d'especificar els camps que desitgem que apareguen com a resultat de la consulta i els camps sobre els quals s'estableixen les condicions en la consulta.

La quadr铆cula est脿 dividida en files i columnes. Cada columna correspon amb un camp. Cada fila espec铆fica una caracter铆stica del camp.

Entre les propietats del camp trobem:

- **Camp**: Espec铆fica els camps que intervenen en la consulta.
- **脌lies**: El valor que s'escriga es mostrar脿 en la cap莽alera de la columna de resultats en lloc del nom del camp que t茅 la taula.
- **Taula**: Mostra el nom de la taula d'on procedeixen els camps.
- **Ordenaci贸**: Estableix l'ordre en el qual apareixeran els registres resultants de la consulta en mostrar la fulla de dades.
- **Visible**: Indica quins camps, dels quals es troben en zona inferior, es mostraran en la fulla de dades.
- **Funci贸**: Aquest caracter铆stica s'explicar脿 m茅s endavant.
- **Criteri**: Permet establir la condici贸 o condicions que ha de complir un camp perqu猫 el registre corresponent aparega en la fulla de dades.

-
Una vegada vistos els elements de la finestra de disseny estem en disposici贸 d'afegir els camps a la consulta. Per a aix貌 seleccionarem els camps d'una de les dues formes possibles:

- Fent doble clic sobre el camp de la taula
- Fent clic sobre el camp i arrossegant-lo fins a la taula fins a una de les columnes de la part inferior

Selecciona els camps `Titol`, `Cognoms_autor`, `Nom_autor`, `Suport` i `Editorial`:

![Base: Diseny de consulta simple](img/base_query_design_simple.png)

A continuaci贸 executa la consulta amb el bot贸 `Executa la consulta (F5)`, la qual cosa far脿 que es mostren els resultats corresponents a aquesta.

Per a acabar, tanca la consulta sense guardar els canvis.

---

## 7.3.2. Consultes sobre diverses taules

Les taules de les bases de dades tenen relacions i, a vegades, interessa que les consultes oferisquen informaci贸 de m茅s d'una taula.

La manera de crear la consulta en aquest cas 茅s similar a la que acabem de veure en el punt anterior.

---

# 7.3. Criteris d'ordenaci贸

Les consultes poden complicar-se amb la introducci贸 d'operadors, seleccions i/o ordenacions amb la finalitat de tindre dades m茅s filtrades i ordenats. En aquesta unitat aprendrem a crear consultes que utilitzen aquests elements que ens ajudaran a afinar en les cerques i a presentar les dades d'una manera millor a la qual hav铆em vist.

Els resultats de la consulta poden ser ordenats utilitzant un o diversos criteris. Veurem els passos a seguir mitjan莽ant un exemple.

---

***Exemple pr脿ctic: Biblioteca***

Fes clic en el bot贸 `Consultes` de la Barra de Base de dades.
En la zona superior de Tasques, fes clic en l'opci贸 `Crear una consulta en vista de disseny...`
Selecciona i afig la taula `LLIBRE` i `SUPORT`.
Agrega els camps `Titol`, `Cognoms_autor` i `Nom_autor` de la taula `LLIBRE`, aix铆 com el camp `Suport` de la taula `SUPORT`.
El seg眉ent pas ser脿 fer clic sobre el desplegable `Ordenaci贸` del camp que es vulga ordenar i seleccionar el tipus d'ordenaci贸 (ordenarem la consulta ascendentment per t铆tol):

![Base: Diseny de consulta. Ordenaci贸](img/base_query_design_order.png)

A continuaci贸 executa la consulta amb el bot贸 `Executa la consulta (F5)`, la qual cosa far脿 que es mostren els resultats corresponents a aquesta.

Per a acabar, tanca la consulta sense guardar els canvis.

# 7.4. Criteris de selecci贸

Altra de les opcions que ens ofereix Base 茅s la de poder seleccionar registres que complisquen una determinada condici贸, de manera que es mostren nom茅s aquells el valor dels quals coincidisca amb el que fixem. Per a aix貌 haurem d'inserir els criteris en la fila `Criteri` en aquelles columnes en les quals vulguem realitzar el filtre.

---

## 7.4.1. Compliment d'un criteri de selecci贸

***Exemple pr脿ctic: Biblioteca***

Sobre la taula `LLIBRE` seleccionar els camps `Titol`, `Cognoms_autor` i `Nom_autor` el suport del qual siga *`Paper`*

![Base: Diseny de consulta. Criteri](img/base_query_design_where.png)

Si ens fixem, el camp `Suport` s'utilitza per a la consulta per貌 no es mostra en executar la consulta (casella `Visible` desmarcada).

## 7.4.2 Compliment de diferents criteris simult脿niament (operador I l貌gic) (*AND*)

Tamb茅 podem utilitzar m煤ltiples criteris o filtres de selecci贸 amb la finalitat que es complisquen varis alhora.

---

***Exemple pr脿ctic: Biblioteca***
Sobre la taula `LLIBRE` seleccionar els camps `Titol`, `Cognoms_autor` i `Nom_autor` el suport del qual siga '*Paper*' i editorial siga '*Regne de Val猫ncia*'

![Base: Diseny de consulta. Criteri AND](img/base_query_design_where_and.png)

---

## 7.4.3. Compliment de, almenys, un dels criteris (operador O l貌gic) (*OR*)

脡s possible que es vulga que es complisca, almenys, algun dels criteris i que no siga necessari que es complisquen tots alhora.
Per a aix貌 utilitzarem la fila de criteri i la fila immediatament inferior (la fila `O`), de manera que se seleccionaran aquells registres que complisquen la condici贸 de la fila criteri o de les files inferiors.

---

***Exemple pr脿ctic: Biblioteca***

Sobre la taula `LLIBRE` seleccionar els camps `Titol`, `Cognoms_autor` i `Nom_autor` el suport del qual siga *`Paper`* o *`EBook`*

![Base: Diseny de consulta. Criteri OR](img/base_query_design_where_or.png)

---

# 7.5. Informes

**Els informes permeten presentar en pantalla o paper les dades que estan emmagatzemats en les taules o consultes**. Encara que 茅s possible imprimir els formularis i els fulls de dades, els informes permeten un major control sobre l'aparen莽a final de la presentaci贸 de les dades i la possibilitat de presentar subtotals i resums de totals per categories d'informaci贸, aix铆 com calcular el percentatge que representa cada categoria sobre el total.

*Base* utilitza *Writer* com a suport per a la generaci贸 d'informes. Aix貌 suposa un gran avantatge a l'hora de dissenyar els nostres informes per tractar-se d'una eina coneguda i de gran versatilitat.

Un informe 茅s la manera de recuperar i presentar la informaci贸 emmagatzemada en una base de dades de manera clara i atractiva, encara que no es pot utilitzar per a modificar la informaci贸 de la taula o consulta en la qual estan basats.

Per a entendre'ns, diguem que un informe d'una base de dades es compon d'una s猫rie d'apartats que permeten presentar la informaci贸 de manera ordenada facilitant la interpretaci贸 de la mateixa per part del lector. Aquest pot comptar al comen莽ament del mateix amb una cap莽alera en la qual s'inclou el t铆tol d'aquest informe aix铆 com les cap莽aleres de les columnes que contenen la informaci贸. Davall de les cap莽aleres apareixen les l铆nies que contindran les dades que volem mostrar, 茅s el cos de l'informe, i al final del mateix pot apar茅ixer el peu de l'informe en el qual es poden realitzar c脿lculs sobre les dades que mostra el cos de l'informe.

---

# 7.6. Crear un informe amb l'auxiliar

L'Assistent per a crear informes 茅s l'eina que ens facilita la creaci贸 de tota mena d'informes de la manera m茅s senzilla possible. Aix貌 no significa que aquest assistent siga l'煤nica forma que podem utilitzar per a crear-los, per貌 s铆 la m茅s c貌moda i la que recomanem. Per a aix貌, l'assistent formula preguntes detallades sobre els or铆gens de registres, camps, disseny i format que desitgem i crega un informe basat en les nostres respostes.

# 馃摑 *Activitat 8: Consultes i informes*

## Crear consulta amb l'auxiliar

- Obri la base de dades `Biblioteca`.
- Fes clic en el bot贸 `Consultes` de la Barra de `Base de dades`.
- En la zona superior de `Tasques`, fes clic en l'opci贸 `Crea una consulta utilitzant l'auxiliar...`

- A continuaci贸 es desplegar脿 un assistent que ens guiar脿 pas a pas per a crear la nostra consulta.

- **Pas 1. Selecci贸 de camps**
  - Hem de triar quins camps volem que es mostren en la consulta.
  - En el camp `Taules`, tria la taula `LLIBRE`.
  - En `Camps disponibles`, selecciona els camps `Titol`, `Cognoms_autor`, `Nom_autor`, `Suport` i `Idioma` utilitzant els botons per a passar un a un els camps.
  - Prem `Endavant >`.
- **Pas 2. Ordre de classificaci贸**
  - A continuaci贸, podem triar si volem que es mostren ordenats en funci贸 dels valors d'un o diversos camps.
  - Selecciona que s'ordenen alfab猫ticament pel camp `Titol`.
  - Prem `Endavant >`.
- **Pas 3. Condicions de la busca**
  - En el seg眉ent pas podem triar si volem indicar un o diversos criteris de cerca; 茅s a dir, si volem que les files que es mostren complisquen alguna condici贸 en particular.
  - Com en el nostre cas l'objectiu 茅s mostrar nom茅s els llibres en format `Paper`, hem d'indicar que per al camp `Suport` nom茅s volem aquells que continguen el valor `Paper`.
  - Prem `Endavant >`.
- **Pas 7. 脌lies**
  - A continuaci贸, podem triar amb quin nom (脿lies) es visualitzaran en mostrar el resultat de la consulta, les cap莽aleres de les columnes dels camps que hem triat.
  - Com els noms dels camps s贸n bastant clars, deixem les opcions per defecte.
  - Prem `Endavant >`.
- **Pas 8. Resum**
  - Per a finalitzar, se'ns mostra un resum amb totes les opcions triades i 茅s on hem d'indicar el nom amb el qual es guardar脿 la consulta. A m茅s podem triar si en finalitzar volem que es mostre el resultat de la consulta o s'貌briga la consulta en vista de Disseny per a afinar i detallar millor la consulta.
  - En el camp `Nom de la consulta` escriu `CATALOG_PAPER`. Deixem per defecte l'opci贸 `Mostrar consulta` perqu猫 es mostre el resultat.
  - Prem `Finalitza`.
- Una vegada acabada, s'executar脿 la consulta oferint una s猫rie de resultats ordenats alfab猫ticament per t铆tol-
- Si tanquem la consulta veurem que, en l'apartat de consultes, s'ha creat amb el nom que li hem donat.

## Crea una consulta anomenada `LLIBRE_CASTELLA`

- Taula: `LLIBRE`
- Que continga els camps `Titol`, `Cognoms_autor`, `Nom_autor`,`Idioma`, `Suport`, `Editorial` i `Any`
- Que estiga ordenada ascendentment per `Cognoms_autor`
- Que el camp `Idioma` siga igual a *`Espanyol`*
- Els 脿lies deixa'ls com estan
- 馃捑 Guarda els canvis.

## Crea una consulta anomenada `LLIBRE_BASICA`

- Taula: `LLIBRE`
- Que continga els camps `Titol`, `Cognoms_autor`, `Nom_autor`,`Idioma`, `Observacions`, `Any` i `Suport`
- Ordena la consulta ascendentment pel camp `Titol`.
- 馃捑 Guarda els canvis.

## Crear consulta amb diverses taules

- Fes clic en el bot贸 `Consultes` de la Barra de Base de dades.
En la zona superior de Tasques, fes clic en l'opci贸 `Crear una consulta en vista de disseny...`
- Apareixer脿 el quadre de di脿leg Agregar taula o consulta. Selecciona la taula `LLIBRE` i fes clic en el bot贸 Afegir (o b茅 fes doble clic sobre l'objecte).
- Repeteix el proc茅s i afig la taula `SUPORT`.
- En la finestra de disseny es mostraran totes dues taules ja relacionades autom脿ticament, estant en disposici贸 d'afegir els camps a la consulta.
- Selecciona els camps `ID`, `Titol`, `Cognoms_autor`, `Nom_autor`, `Suport`.
- La fila Taula cont茅 les dues taules sobre les quals hem realitzat la consulta, 茅s a dir, `LLIBRE` i `SUPORT`.
- Ordena la consulta ascendentment pel camp `Titol`. Guarda els canvis.
- 馃捑 Guarda la consulta com a `LLIBRE_RESUM`.

## Crear una consulta anomenada `INFO_PREU_ORD`

- Taula: `LLIBRE`
- Que continga els camps `Titol`, `Preu`, `Editorial`, `Any` i `Observacions`
- Que estiga ordenada ascendentment per `Preu`
- 馃捑 Guarda els canvis.

## Crear una consulta anomenada `INFO_EDITORIAL_ORD`

- Taula: `LLIBRE`
- Que continga els camps `Titol`, `Editorial`, `Any` i `Suport`
- Que estiga ordenada ascendentment per `Editorial`
- 馃捑 Guarda els canvis.

## Crea una consulta anomenada `LLIBRES_PAPER_MP3`

- Taula: `LLIBRE`
- Que continga els camps `Titol`, `Cognoms_autor`, `Nom_autor` i `Suport`.
- Que el camp `Suport` siga igual a *`Paper`* o *`MP3`*.
- 馃捑 Guarda els canvis.

## Crea una consulta anomenada `LLIBRES_EDREINO`

- Taula: `LLIBRE`
- Que continga els camps `Titol`, `Cognoms_autor`, `Nom_autor`, `Idioma` i `Editorial`.
- Marca `Editorial` com **no visible**.
- Que el camp `Editorial` siga igual a *`Regne de Val猫ncia`* i l'`Idioma` del qual siga *`Valenci脿`*.
- 馃捑 Guarda els canvis.

## Crear un informe amb l'auxiliar

- Fes clic en el bot贸 `Informes` de la Barra de Base de dades.
- En la zona superior de `Tasques`, fes clic en l'opci贸 `Crear un informe utilitzant l'auxiliar...`
- A continuaci贸 es desplegar脿 un assistent que ens guiar脿 pas a pas per a crear la nostra consulta.

- **Pas 1. Selecci贸 de camps**
Hem de triar quins camps volem que es mostren en l'informe i de quines taules. Les taules apareixeran en la part superior mentre que els camps es mostraran en la part inferior.
  - Selecciona la taula LLIBRE.
  - Selecciona els camps `ISBN`, `Titol`, `Cognoms_autor`, `Nom_autor`, `Suport` i `Idioma`.
  ![Base: Auxiliar d'informes Pas 1. Selecci贸 de camps](img/base_report_wizard_1.png)
  - Prem `Endavant >`.

- **Pas 2. Etiquetatge dels camps**
  - A continuaci贸, podem triar amb quin nom (脿lies), es mostraran les cap莽aleres de les columnes dels camps que hem triat en mostrar el resultat de l'informe. Per defecte l'assistent utilitzar脿 el nom propi de cada camp en la taula o consulta.
  - Com els noms dels camps s贸n bastant clars, deixem les opcions per defecte.
  ![Base: Auxiliar d'informes Pas 2. Etiquetatge dels camps](img/base_report_wizard_2.png)
  - Prem `Endavant >`.

- **Pas 3. Agrupaci贸**
  - Aquest pas permet triar un nivell d'agrupament de les dades, de manera que es mostre la informaci贸 resumida segons l'agrupaci贸, podent tindre aquesta un m脿xim de quatre camps.
  - Per a entendre-ho millor suposem que fem una llista de llibres de tres idiomes. Aquesta llista l'organitzem en primer nivell per l'idioma i en segon nivell per l'autor. En aquest cas, l'informe crear脿 un primer nivell d'agrupament per a cada idioma i dins d'ell crear脿 un grup per a cada autor dins del qual apareixeran els llibres que ha escrit.
  - Continuarem amb l'exercici.
  - Agrupa pel camp `Idioma`.
  ![Base: Auxiliar d'informes Pas 3. Agrupaci贸](img/base_report_wizard_3.png)
  - Prem `Endavant >`.

- **Pas 4. Opcions d'ordenaci贸**
  - En aquest pas seleccionarem el criteri d'ordenaci贸 de camps de l'informe en funci贸 de l'agrupament que h脿gem triat. Podem ordenar per un m脿xim de quatre camps i en ordre ascendent o descendent. Recorda que els camps agrupats nom茅s es poden ordenar dins de cada grup.
  - Ordena els camps ascendentment per Idioma i *descendentemente per Cognoms autor.
  ![Base: Auxiliar d'informes Pas 4. Opcions d'ordenaci贸](img/base_report_wizard_4.png)
  - Prem `Endavant >`.

- **Pas 5. Triar un format**
  - En aquest pas hem de triar l'aspecte extern de l'informe. Per a aix貌 comptem amb el quadre de llista Disseny de dades en el qual es mostra un bon nombre de plantilles predeterminades. A m茅s, podem observar com en seleccionar qualsevol dels dissenys d'aquesta llista es reflecteix a l'instant en l'informe.
  - Una vegada decidit el disseny per a les dades, utilitzarem el quadre de llista Disseny d'encap莽alats i peus de p脿gina per a localitzar el model que m茅s ens agrade per a la presentaci贸 dels peus i les cap莽aleres de l'informe. Igual que ocorre amb els dissenys de dades, amb els encap莽alats i peus de p脿gina tamb茅 podem comprovar el resultat en la p脿gina de l'informe.
  - L'煤ltima decisi贸 que hem de prendre en aquest pas 茅s l'orientaci贸 de l'informe: vertical o horitzontal. La utilitzaci贸 de l'una o l'altra dependr脿 fonamentalment de la quantitat de columnes que tinga el nostre informe.
  - Selecciona la distribuci贸 "Tabular" i orientaci贸 "Horitzontal".
  ![Base: Auxiliar d'informes Pas 5. Triar un format](img/base_report_wizard_5.png)
  - Prem `Endavant >`.

- **Pas 6. Crear informe**
  - Per a finalitzar, se'ns mostra un resum amb totes les opcions triades i 茅s on hem d'indicar el nom amb el qual es guardar脿 l'informe. A m茅s, podem triar si en finalitzar volem que es mostre el resultat de l'informe o s'貌briga en manera Disseny per a afinar i detallar millor l'informe.
  - Fixa el valor del camp T铆tol de l'informe a "INFORME_IDIOMA_AUTOR".
  - Deixa l'opci贸 Crear informe ara perqu猫 es mostre el resultat.
  ![Base: Auxiliar d'informes Pas 6. Crear informe](img/base_report_wizard_6.ca.png)
  - Prem `Finalitza`.

- A continuaci贸 s'executar脿 l'informe:
![Base: Auxiliar d'informes final](img/base_report_wizard_7.ca.png)

- 馃捑 Guarda la base de dades.
- Tanca la base de dades.
- Lliura l'activitat.
