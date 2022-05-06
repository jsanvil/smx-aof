UD11: Bases de dades (I)

# 5. *LibreOffice Base*: Clau primària. Edició de taules

## 🎯 Objectius

- Conéixer el concepte de clau primària.
- Establir una clau primària en una taula.
- Modificar columnes i tipus de dades.
- Utilitzar el tipus de dades autonumèrico.

---

# 5.1 Clau primària o principal

En apartats anteriors hem vist que les taules estan formades per camps que poden tindre diferents tipus, encara que falta per indicar quin camp és el més important, és a dir, la clau primària. En aquesta unitat aprendrem el concepte de clau primària i com definir-la en cada taula que creem en una base de dades.

La **clau principal o primària** proporciona un valor **únic** per a cada registre de la taula i ens serveix d'identificador de registres de manera que amb aquesta clau podem saber sense cap mena d'equivocació el registre al qual identifica. No podem definir més d'una clau principal, però podem tindre una clau principal composta per més d'un camp. A més, aquesta ens permetrà, en futures unitats, accedir a les dades d'altres taules.

*Per exemple, si tenim una taula amb les dades de contactes dels nostres amics, podríem estar segurs que, usant el seu número del Document Nacional d'Identitat (DNI), cap d'ells tindria el mateix valor en aquest camp. En canvi, el camp nom per als nostres amics podria repetir-se.*

> LA **CLAU PRIMÀRIA** HA DE COMPLIR **3 CONDICIONS**:
>
> - El camp o camps que formen la clau principal d'una taula **no pot contindre valors nuls**. És a dir, sempre ha de prendre un valor per a cada registre de la taula.
>
> - **No poden haver-hi dues registres en la taula amb el mateix valor en el camp o camps de la clau principal**. És a dir, **aquest valor no pot repetir-se en cap registre**.
>
> - Només pot haver-hi **una clau principal per taula**.

> ⚠️ Quan un camp compleix aquestes dues propietats (sense nuls i sense repetits) se'n diu **Clau Primària** o **Clau Principal** i **tota taula ha de tindre una**.

> ⚠️ Quan intentem inserir un nou registre amb valors que infringisquen aquestes dues regles, el sistema no ens deixa crear el nou registre i ens retorna un error.

---

### *Exemple: Clau primària taula ESTUDIANT*

En una taula en la qual es vol emmagatzemar les dades d'un estudiant tenim:

ESTUDIANT          |
-------------------|
Nom                |
Cognoms            |
Edat               |
Curs               |
Número d'expedient |
Grup               |

**Quin camp seleccionaríem com a clau primària?**

- Seleccionaríem `Número d'expedient`, ja que aquest número és únic, no es pot repetir i no pot contindre valors nuls (tot estudiant té un número d'expedient associat).

---

### *Exemple: Clau primària taula LLIBRES*

En una taula en la qual es vol emmagatzemar les dades d'una sèrie de llibres tenim:

LLIBRES   |
----------|
Títol     |
Editorial |
ISBN      |
Any       |
Autor     |

**Quin camp seleccionaríem com a clau primària?**

- Seleccionaríem `ISBN`, ja que aquest número és únic, no es pot repetir i no pot contindre valors nuls (tot llibre publicat té un codi ISBN).

- Què passaria si tenim dos o més exemplars amb el mateix ISBN?

---

# 5.2 Definició de la *clau primària*

Per a assignar una clau principal a un camp, seguirem els següents passos:

- Fer clic sobre el nom del camp que serà clau principal.
- Situar-nos sobre la columna grisa de l'esquerra i amb el botó dret del ratolí triar `Clau principal`.
- A l'esquerra del nom del camp apareixerà una clau indicant-nos que aquest camp és la clau principal de la taula.

---

# 5.3 Edició de taules

Lògicament, *Base* ens permetrà modificar taules, amb l'objectiu d'afegir o eliminar columnes (atributs), o bé, de modificar alguna propietat d'aquestes. Això és important de cara a possibles errors i/o modificacions que es requerisquen fer una vegada establits tots els camps de les taules.

En aquest apartat estudiarem la modificació de les columnes i els tipus de dades, així com un tipus especial de dades molt útil anomenat `Autonumèric`.

---

# 5.4 Modificació de columnes

Les modificacions que es poden realitzar sobre les columnes existents poden ser de dos tipus:

- Canvis de **nom del camp** o de la **descripció** d'aquest.
- Canvi en les **propietats del camp**, des de ser o no clau primària, a canviar el tipus de camp i les propietats associades a aquest tipus de camp.

### 5.4.1 Canvis en el nom o descripció

Per a aquest canvi, n'hi ha prou amb situar-se en el valor que vulguem modificar i canviar el contingut de text. Aquest tipus de modificació **no afecta a les relacions** (elements que es veuran en posteriors unitats) amb el que podem realitzar-les amb tota tranquil·litat.

---

## 5.4.2 Canvis en les propietats de les columnes

Més importants per a la integritat de la taula, i en algun cas més complexes de realitzar, són les operacions que contemplen el canvi de tipus de dades o el canvi de les propietats del camp.

**El canvi en la mena de dades ha de realitzar-se amb cautela**, ja que s'haurà de seleccionar un **tipus de dades compatible** amb els valors ja introduïts (en cas que la taula continga dades).

---

### 5.4.2.1 Canvis en camps de text

Quan canviem entre tipus de dades de text, per exemple, **cal anar amb compte que la grandària** del nou tipus siga prou gran per a contindre els valors prèviament emmagatzemats. Per exemple, si canviem de 40 a caràcters, no passa res, perquè la longitud augmenta. Ara bé, ***si canviem la longitud de 40 caràcters a 20 caràcters, s'esborraran els últims 20 caràcters de cada valor contingut en cada registre.***

---

### 5.4.2.2 Canvis en camps numèrics

Quan canviem entre tipus de dades numèriques, per exemple, ***entre un de tipus real i un altre de tipus sencer cal anar amb compte que la grandària del nou tipus siga prou gran i tindre en compte que només es respectarà la part sencera*** dels valors prèviament emmagatzemats.

---

### 5.4.2.3 Incompatibilitats

**Aquest tipus de conversions no sempre es poden realitzar**. Així, per exemple, encara que seria possible canviar el camp `Data_compra` de tipus `Data` a tipus `Text`, no ens deixarà convertir-ho a un de tipus `Integer`, ja que encara que en el primer pas no és complicat per a *Base* transformar una data a una cadena de text, en el segon cas no és capaç de convertir una data a un número i ens **mostra un avís**.

És a dir, la solució que ens proposa és eliminar per complet aqueixa columna i crear una nova amb el nom que ja tenia i el nou tipus, però perdent els valors que ja teníem introduïts en aqueix camp.

---

# 5.5. Tipus de dades *Autonumèric*

Un canvi molt útil que podem realitzar en la nostra taula és fer que la nostra **clau primària prenga valors automàticament**, per exemple per a posar un codi de referència a un producte o els codis de pel·lícula d'un videoclub. Això es pot fer amb la mena de dades `Autonumèric`, que permet numerar de manera correlativa i automàtica els registres que s'introdueixen en una taula.

---

# 5.6. Eliminació de columnes

Abans d'eliminar una columna de la nostra taula hem de saber que en fer-ho s'esborraran tots els valors que tinguérem donats a aquesta columna en la nostra files pel que, sobretot en el cas de la columna que siga clau primària, cal pensar molt bé si de veritat és convenient eliminar aqueixa columna.

L'eliminació és senzilla i pot ser revocada utilitzant les opcions de `Desfer` i `Refer`.

> ⚠️ **L'eliminació d'una columna es pot desfer només abans de guardar els canvis**. En cas de guardar-los, la columna quedarà eliminada permanentment.

# 📝 *Activitat 6: Clau primària i edició de taules*

**Clau primària**

En el cas de la nostra taula `LLIBRE`, tenim el camp numèric `ID` per a diferenciar un llibre d'un altre ja que, per exemple, podem tindre dos exemplars del mateix llibre, o dos llibres amb el mateix títol o dos llibres amb el mateix autor o dos llibres de la mateixa editorial. El camp `ID` és el que identificarà cadascun dels llibres que s'introduïsquen en la base de dades; és a dir, ens servirà per a distingir un llibre d'un altre inequívocament.

***Podríem triar com a clau primària el codi `ISBN`, ja que és un codi únic que distingeix un llibre d'un altre?***

En aquest cas particular NO. En una biblioteca podem tindre més d'un exemplar del mateix llibre, per la qual cosa no ens serviria, ja que tots els exemplars tindrien el mateix `ISBN` i, per tant, seria un valor repetit. En aquesta situació, seleccionem el camp `ID` perquè és únic.

**Edició de dades**

- Obri la base de dades `Biblioteca`
- Fes clic en el botó `Taules` de la `Barra de Base de dades`.
- Selecciona la taula `LLIBRE`.
- Fes doble clic sobre la taula o clic en la icona, per a entrar en manera edició de dades.
- Inserta un registre duplicat en la taula `LLIBRE`, és a dir, un nou llibre amb el mateix `ID` que un altre. Per exemple:

ID | Títol                    | Cognoms               | Nom        | Suport
---|--------------------------|-----------------------|------------|-------
1  | El Quixot de la Manxa    | De Cervantes Saavedra | Miguel     | Paper
1  | Els contes de l'Alhambra | Irving                | Washington | Paper

- En inserir-ho donaria error perquè ja existeix un llibre amb el mateix `ID`. Si es poguera repetir, crearíem una inconsistència de dades, ja que si ens referim al `ID=1`, no sabríem amb quin llibre es correspon.
- Comprova si es compleixen les restriccions de la clau primària (ha de mostrar-se un missatge d'error de valor duplicat).
- Prem `D'acord`.
- Fes clic a l'esquerra sobre el llapis amb el botó dret del ratolí i tria l'opció `Desfés: entrada de dades`. També pots tancar la taula sense guardar les dades.
- Tanca la taula `LLIBRE`.

**Edició de la taula**

Realitzarem un exemple en el qual canviarem el nom d'alguns camps de la taula `LLIBRE`.

- Obri la taula `LLIBRE` per a edició.
- Canviar nom de camps:
  - Canvia el nom de la columna `Prestable` per `PrestableSN`. Situa't en el camp corresponent i canvia el contingut del text.
  - A continuació modificarem la descripció d'un altre dels camps. Per a això, canviarem la del camp Observacions de `Observacions` a `Observacions (autor, edició, etc.)`.

- 💾 Guarda els canvis.

**Duplicar taula**

Crearem una rèplica de la taula `LLIBRE` amb nom `LLIBRE2`.

- Fes clic amb el botó dret del ratolí sobre la taula `LLIBRE` i selecciona `Copia`.
- Fes clic amb el botó dret del ratolí i selecciona `Apega`.
- En la finestra que es mostra, tria l'opció `Definició i dades` i prem el botó `Crea`.

**Modificar propietats de camps**

- Obri la taula `LLIBRE2` en mode edició.
- Canvia el tipus de camp `PrestableSN` de `Si/No` a `Text [VARCHAR]`.
- Canvia el tipus de camp `Preu` de `Real` a `Enter [INTEGER]`.
- Canvia la longitud del camp `Titol` de `100` a `50`.
- 💾 Guarda els canvis.

**Tipus de dades Autonumèric**

- Edita la taula `LLIBRE2`.
- Ves al camp `ID`.
- Fixa el valor de la columna amb la propietat `Valor Automàtic` a `Sí`.
- 💾 Guarda els canvis.
- Tanca la manera edició.

- A partir d'ara, cada vegada que introduïm una nova fila en la taula `LLIBRE2`, al camp `ID` se li assignarà el major valor assignat fins a aqueix moment incrementat en 1. És a dir, aquest camp es numerarà automàticament i sense repetir els números.

- Obri la taula en manera introducció de dades.
- Introdueix un nou registre amb la informació que vulgues. Comprova que ara el camp `ID` no pot modificar-se, ja que l'assigna el programa automàticament. Per exemple:
  
  - ***LLIBRE 9***
    - ID: NO es pot modificar
    - ISBN: 9788499999999
    - Títol: Els Furs del Regne de València
    - Autor: Jaume I El Conqueridor
    - Editorial: Regne de València
    - Any: 1988
    - Gènere: Historia
    - Suport: Paper
    - Idioma: Valencià
    - Preu: 200 €
    - Web: <http://www.regnedevalencia.es/fueros-furs-reino-regne-valencia/>
    - Observacions: Facsímil de l'edició original
- 💾 Guarda els canvis.

**Eliminació de camps**

- Obri la taula `LLIBRE2` per a edició.
- Selecciona el camp `Portada`. Fes clic en la columna grisa de l'esquerra en el camp seleccionat.
- Fes clic amb el botó dret del ratolí i selecciona l'opció `Suprimeix`.
- 💾 Guarda els canvis.

- 💾 Guarda la base de dades.
- Tanca la base de dades.
- Lliura l'activitat.
