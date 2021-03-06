UD12: Bases de dades (II)

# 5. *LibreOffice Base*: Formularis mestre-detall/subformularis

## 馃幆 Objectius

- Concepte de formulari mestre-detall o subformulari.
- Crear i utilitzar subformularis.

---

# 5.1. Formularis mestre-detall/subformularis

Els formularis mestre-detall o subformularis representen formularis que es troben localitzats dins d'altres formularis. Serveixen per a mostrar informaci贸 contextual o addicional d'un o m茅s camps del formulari.

En pr脿ctiques anteriors, ens hav铆em saltat el pas d'afegir subformularis. Ara ha arribat el moment d'utilitzar aquest pas per a crear nostres subformularis.

---

# 馃摑 *Activitat 5: Subformularis*

## Base de dades `Videoclub`

Crearem un formulari fent que, cada vegada que ens movem entre els diferents registres, ens mostre la informaci贸 de totes les pel路l铆cules pertanyents a aqueix g猫nere. Per a aix貌, utilitzarem subformularis.

### Crear subformulari

- Obri la base de dades `Videoclub`.
- Fes clic en el bot贸 `Formularis` de la Barra de dades.
- En la zona superior de `Tasques`, fes clic en l'opci贸 `Crear un formulari utilitzant l'auxiliar...`

#### Pas 1. Selecci贸 de camps

Hem de triar quins camps volem que es mostren en el formulari.

- Tria la taula `GENERE`.
- Selecciona tots els camps.
- Prem `Endavant >`.

#### Pas 2. Configurar un subformulari

Crearem un subformulari basant-nos en la relaci贸 existent entre la taula `GENERE` i `PELICULA`, un g猫nere t茅 moltes pel路l铆cules i una pel路l铆cula pertany a un nom茅s g猫nere.

- Marca la casella `Afig un subformulari`.
- Marca l'opci贸 `Subformulari basat en relaci贸 existent`.
- En l'opci贸 `Quina relaci贸 voleu afegir?` fes clic sobre la taula `PELICULA`.
- Prem `Endavant >`.

#### Pas 3. Afegir camps de subformulari

Hem d'afegir els camps a mostrar en el subformulari.

- Selecciona els camps `Titol`, `Director`, `Any`, `Duracio`, `Suport`, `Argument` i `Genere`.
- Prem `Endavant >`.

#### Pas 5. Organitzeu els controls

En el seg眉ent pas podem triar la distribuci贸 dels camps en el formulari.

- En `Disposici贸 del formulari principal` fes clic en la icona de l'esquerra `En columnes - Etiquetes a l'esquerra`.
- Prem `Endavant >`.

#### Pas 6. Especifiqueu l'entrada de dades

- Deixem les opcions per defecte.
- Prem `Endavant >`.

#### Pas 7. Aplica els estils

Ac铆 triarem un dels estils proposats per *Base*.

- Tria el color i efectes 2D o 3D que vulgues.
- Prem `Endavant >`.

#### Pas 8. Especifiqueu el nom

Finalment guardem el formulari.

- En el camp `Nom del formulari` escriu *`SFGENERE`*. Resta d'opcions per defecte.
- Fes clic a `Finalitza`.

Una vegada finalitzat l'assistent, se'ns obri el formulari per a manipular dades. Si ens fixem, cada vegada que canviem de g猫nere, les dades del subformulari canvien autom脿ticament, mostrant informaci贸 detallada de les pel路l铆cules que pertanyen a aquest g猫nere.

### Personalitzar formulari

- Ve al formulari `SFGENERE`.
- Obri el formulari en mavista de disseny (edita).
- Pot utilitzar-se els efectes i colors que es desitge.
- Canvia el color de fons.
- Redimensiona els elements de la pantalla.
- Inserta un rectangle arredonit 3D. Escriu dins el text *`G脠NERES-DETALL`*.
Per exemple:

![](img/act5_subform1.png)

- 馃捑 Guarda els canvis.
- Tanca el formulari.

---

- 馃捑 Guarda els canvis en la base de dades.
- Tanca la base de dades.

# 馃摑 *Activitat 6: Edici贸 de subformularis*
# Base de dades: `Gimn脿s`

Farem encara m茅s intu茂tiu el formulari FSOCI fent que, cada vegada que ens movem entre els diferents registres, ens mostre la descripci贸 de l'activitat que realitza cada soci. Per a aix貌, utilitzarem subformularis.

### Crear consulta

En primer lloc, necessitem crear una consulta que posteriorment usarem en el nostre subformulari.

- Obri la base de dades `Gimn脿s`.
- Crea una consulta en vista de disseny amb nom *`CSF_activitat`*.
- Tria la taula `ACTIVITAT` i selecciona els camps `Id_activitat` i `Descripcio`.
- 馃捑 Guarda els canvis.
- Tanca la consulta.

### Crear subformulari

- Fes clic en el bot贸 `Formularis` de la `Barra de dades`.
- En la zona superior de `Tasques`, fes clic en l'opci贸 `Crear un formulari utilitzant l'auxiliar...`

#### Pas 1. Selecci贸 de camps

Hem de triar quins camps volem que es mostren en el formulari.

- Tria la taula `SOCI`.
- Selecciona tots els camps.
- Prem `Endavant >`.

#### Pas 2. Configurar un subformulari

Crearem un subformulari basant-nos en la relaci贸 existent entre la taula `SOCI` i `ACTIVITAT`.

- Marca la casella `Afig un subformulari`.
- Marca l'opci贸 `Subformulari basat en selecci贸 manual dels camps`.
- Prem `Endavant >`.

#### Pas 3. Afegiu camps de subformulari

Hem d'afegir els camps a mostrar en el subformulari.

- Tria la consulta `CSF_ACTIVITAT` i selecciona els 2 camps d'aquesta consulta.
- Prem `Endavant >`.

#### Pas 4. Recupereu els camps units

En aquest pas es defineix la relaci贸 existent entre el subformulari i el formulari principal.

- En `Primer camp de subformulari`, selecciona el camp `Id_activitat`.
- En `Primer camp unit de formulari principal`, selecciona el camp `Activitat`.
- Prem `Endavant >`.

#### Pas 5. Organitzeu els controls

En el seg眉ent pas podem triar la distribuci贸 dels camps en el formulari.

- Fes clic en la icona de l'esquerra `En columnes - Etiquetes a l'esquerra`.
- Prem `Endavant >`.

#### Pas 6. Especifiqueu l'entrada de dades

- Deixem les opcions per defecte.
- Prem `Endavant >`.

#### Pas 7. Aplicar els estils

Ac铆 triarem un dels estils proposats per Base.

- Tria el color i efectes 2D o 3D que vulgues.
- Prem `Endavant >`.

#### Pas 8. Especifique el nom

Finalment guardem el formulari.

- En el camp `Nom del formulari` escriu `SFSOCI`. Resta d'opcions per defecte.
- Fes clic a `Finalitza`.

Una vegada finalitzat l'assistent, se'ns obri el formulari per a manipular dades. Si ens fixem, cada vegada que canviem de soci, les dades del subformulari canvien autom脿ticament, mostrant la descripci贸 de l'activitat que realitza el soci actual.

- 馃捑 Guarda els canvis.
- Tanca el formulari.

> 鈿? Com podem observar, s'han perdut tots els canvis que hav铆em fet en el nostre formulari `FSOCI`, ja que ens faltaria incloure la llista desplegable d'activitats i el camp DNI amb m脿scara d'edici贸 de dades. A m茅s, tamb茅 s'han perdut els canvis en el disseny com el color, etc.

## Subformularis en vista de diseny

L'assistent 茅s una forma r脿pida de crear subformularis per貌 t茅 l'inconvenient que perdem tots els canvis efectuats en el formulari principal.

Existeix un **m猫tode alternatiu** per a incloure subformularis sense necessitat de perdre les modificacions realitzades sobre un formulari.

### Formulari `FSOCI`. Disseny

- Fes clic en el bot贸 `Formularis` de la `Barra de dades`.
- Ve al formulari `FSOCI`.
- Obri el formulari en vista de disseny (edita).

#### Crear subformulari

- En la barra d'eines inferior, prem la icona **`Navegador de formularis`**.
- Selecciona el formulari principal *`MainForm`* i amb el bot贸 dret del ratol铆 tria l'opci贸 `Nou` 鈫? `Formulari`.
- Posa com a nom `SFACTIVITAT`.

#### Vincular subformulari

Ara hem d'indicar el vincle que existeix entre el formulari principal i el subformulari creat.

- Fes clic en el subformulari `SFACTIVITAT`.
- Amb el bot贸 dret del ratol铆 tria l'opci贸 `Propietats`, pestanya `Dades`.
- `Tipus de contingut`. Tria `Consulta`.
`Contingut`. Tria la consulta `CSF_activitat`.
- `Enlla莽 als camps mestres`. Fes clic en el bot贸 amb punts suspensius.
- Selecciona el camp `Id_activitat` en la consulta `CSF_activitat` i el camp `Activitat` en la taula `SOCI`.
- Se'ns desplega una finestra on hem d'indicar per quins camps relacionarem tots dos formularis. Nosaltres volem aconseguir que, donat un soci seleccionat en el formulari principal, es mostre la descripci贸 de l'activitat realitzada en un subformulari. En conseq眉猫ncia, triem el camp en com煤 que comparteixen totes dues taules de `SOCI` i `ACTIVITAT`, 茅s a dir, el codi d'activitat.
- Fes clic a `OK`.
- Tanca les propietats del subformulari.

#### Inserir subformulari en formulari `FSOCI`

Ara nom茅s ens falta triar un camp de control que permeta mostrar en el subformulari la descripci贸 de l'activitat.

- Ve al `Navegador de formularis`.
- Selecciona el subformulari `SFACTIVITAT`.
- Prem sobre la icona de la barra esquerra anomenat `M茅s controls`. 
- *Base* ens mostra un quadre amb controls addicionals. Fem clic en la icona `Control de taula`.
- Dibuixa el nou control en el formulari, per exemple al costat del camp `Activitat`. Ens apareix un assistent on triem els camps de `Activitat` i `Descripcio` de la consulta `CSF_ACTIVITAT`.
- Fes clic en el bot贸 `Finalitza`.

Com podem veure, s'ha creat un nou control dins del subformulari.

![](img/act5_subform2.png)

#### Modificar subformulari

Modifiquem les propietats del nou control perqu猫 nom茅s es puga visualitzar el seu contingut.

- Fes doble clic sobre el nou camp de subformulari.
- Selecciona la pestanya `General`. Modifica les seg眉ents propietats:
  - Activat: No.
  - Barra de navegaci贸: No.
  - Marcador de registre: No.
- Tanca la finestra Propietats.
- Tanca el navegador de formularis.
- Tanca el formulari.

#### Formulari FSOCI. Entrada de dades

Fes doble clic sobre el formulari `FSOCI`. Comprova que es mostra la descripci贸 de l'activitat que realitza cada soci.

![](img/act5_subform3.png)

- Tanca el formulari.

---

- 馃捑 Guarda els canvis en la base de dades.
- Tanca la base de dades.
