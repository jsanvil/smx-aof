# 4. *LibreOffice Base*: Format, edició, validació, ordenació i filtrat de dades

## Objectius
- Conéixer i utilitzar els formats per a mostrar els camps.
- Concepte de camp. Identificar l'estructura d'una taula.
- Concepte de fulla de dades.
- Operacions de manipulació de dades: alta, modificació i esborrat.
- Conéixer i utilitzar la propietat valor per defecte. Conéixer i utilitzar la propietat camp requerit.
- Ordre ascendent i descendent de dades.
- Operacions de filtrat de dades. Operacions de cerca de dades.

---

# 4.1 Propietat Format

Els camps tenen diferents característiques que permeten la seua personalització dins d'un rang determinat de valors. Gràcies a ells podem especificar i afinar el tipus d'element així com la seua estructura.

> La propietat Format determina la manera en què es mostraran les dades en un camp d'una taula, però NO els modifica.

Podem utilitzar l'Assistent per a formats o podem escriure directament la màscara en el camp.

Aquesta propietat és important en molts camps però, possiblement, on més cura cal tindre amb ella és en els camps de tipus "temps" per a no tindre problemes quan introduïm dates i hores.

--- 

# 4.2 Assistent per a formats

L'assistent ens permet triar entre una sèrie de formats preestablits. Per a executar l'assistent anirem al camp i en la propietat `Exemple de format` farem clic en el botó situat a la dreta.

Existeixen diferents tipus entre els quals trobem:

- Text
- Numèric
- Data
- Hora
- Científic
- Moneda
- Percentatge
- Valor booleà
- Fracció

---

## 4.2.1 Tipus Numèric
Totes aquestes màscares estableixen el format amb el qual es visualitzarà el camp numèric. Disposem de les mateixes opcions que en el full de càlcul *Calc*.

- **Decimals**. Indica el nombre de decimals a mostrar.
- **Zeros inicials**. Nombre màxim de zeros davant de la coma decimal.
- **Negatiu en roig**. Els números negatius es visualitzen en color roig.
- **Separador de milers**. Els milers se separen amb punt.

---

## 4.2.2 Tipus Data

Totes aquestes màscares restringeixen l'entrada de dates.

- **Llengua**. En la part superior dreta podem elegir l'idioma. L'elecció d'idioma no és un tema trivial ja que, per exemple, els formats de data predefinits no seran els mateixos per a idiomes de països anglosaxons que per a països europeus continentals.
- **Format**. Existeixen una sèrie de formats predefinits que es mostren en la finestra superior central. Un exemple de com es veuria el format triat es mostra en el rectangle que apareix en el centre de la finestra a la dreta.
- **Codi de format**. Tots els formats predefinits poden ser adaptats per l'usuari i guardats per al seu ús posterior.

---

## 4.2.3 Tipus Hora

Totes aquestes màscares restringeixen l'entrada de temps i són similars a les anteriors.

- **Llengua**. En la part superior dreta podem elegir l'idioma. L'elecció d'idioma no és un tema trivial ja que, per exemple, els formats d'hora predefinits no seran els mateixos per a idiomes de països anglosaxons que per a països europeus continentals.
- **Format**. Existeixen una sèrie de formats predefinits que es mostren en la finestra superior central. Un exemple de com es veuria el format triat es mostra en el rectangle que apareix en el centre de la finestra a la dreta.
- **Codi de format**. Tots els formats predefinits poden ser adaptats per l'usuari i guardats per al seu ús posterior. En l'exemple es mostrarien dos dígits per a les hores, dues per als minuts i dos per als segons.

---

## 4.2.4 Tipus Científic

Totes aquestes màscares restringeixen l'entrada de números en notació científica.

- *Decimals*. Indica el nombre de decimals a mostrar.
Zeros a l'esquerra. Nombre màxim de zeros davant de la coma decimal.
- *Negatiu en roig*. Els números negatius es visualitzen en color roig.
- *Format*. Existeixen una sèrie de formats predefinits que es mostren en la finestra superior central. Únicament existeixen dos, un amb tres números per a l'exponent i un altre per a dos.
- *Format de codi*. Tots els formats predefinits poden ser adaptats per l'usuari i guardats per al seu ús posterior. En l'exemple es mostraria un dígit sencer, dos decimals i dos per a l'exponent.

---

# 📝 *Activitat 2: Formatació de camps*

- Edició de la taula ***LLIBRE***

  - Obri la base de dades "**Biblioteca**".
  - Fes clic en el botó Taules del panell de Base de dades.
  - Selecciona la taula **LLIBRE**.
  - Edita la taula fent clic en la icona Editar de la barra d'eines. 

- Format del camp ***Any de publicació***

  - Selecciona el camp `Any` i en el panell de propietats inferior fes clic en el botó amb punts suspensius del camp `Exemple de format`.
  - Tria la categoria `Data`. Fins ara el nostre camp `Any` estava predefinit com `DD/MM/AA`; és a dir, dues xifres per al dia, dos per al mes i dos per a l'any.
  - En el camp `Codi de format` tecleja `AAAA` (o `YYYY` si tens configurat LibreOffice en anglès). Després, prem la icona de la dreta  `✔️` `Afig`.
  - Comprova que s'ha afegit el nou format.
  - Fes clic en el botó `OK`.

- Format del camp ***Preu***

  - Ara selecciona el camp `Preu` i en el panell de propietats inferior selecciona el botó a la dreta del camp `Exemple de format`.
  - Selecciona la categoria `Moneda`.
  - Fes clic a `OK`.

---
