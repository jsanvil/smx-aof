UD11: Bases de dades (I)

# 8. *LibreOffice Base*: Formularis simples. Manipulació de dades

## 🎯 Objectius

- Concepte de formulari.
- Conéixer els elements principals d'un formulari.
- Crear formularis senzills de manera automàtica.
- Manipular dades des d'un formulari.
- Treballar i manipular camps de tipus objecte.

---

# 8.1 Formularis

*Base* ofereix, a més de les taules i les consultes, un element molt potent per a gestionar la informació de les bases de dades: els formularis. En aquesta unitat aprendrem a crear formularis senzills amb els quals modificar les dades de manera visual i còmoda, i així evitar l'edició directa de les taules amb els problemes que això pot comportar.

**Els formularis són objectes** que *Base* proporciona **per a veure, introduir o imprimir dades d'una o diverses taules**. Es tracta de la presentació de la informació continguda en les taules a través de la pantalla de l'ordinador amb un disseny intuïtiu i agradable.

Per mitjà dels formularis l'usuari visualitza la informació continguda en les taules, examina els resultats d'una consulta i altera el seu contingut introduint, modificant o eliminant informació en els camps. És a dir, ofereix les mateixes funcions de la Full de Dades o les Consultes aportant una millor presentació de cara a l'usuari final.

En definitiva, **les taules emmagatzemen la informació i els formularis s'encarreguen de recollir-la**. **En tancar o guardar els formularis, les taules s'actualitzen**.

# 8.2 Crear formularis amb l'auxiliar

L'Auxiliar per a crear formularis és l'eina que ens facilita la creació de tota mena de formularis de la manera més senzilla possible. Això no significa que l'Auxiliar per a formularis siga l'única forma que podem utilitzar per a crear els formularis, però sí la més còmoda i la que recomanem. Per a això, l'assistent formula preguntes detallades sobre els orígens de registres, camps, disseny i format que desitgem i crega un formulari basat en les nostres respostes.

# 8.3 Formularis. Manipulació de dades

Després de crear un formulari i obrir-lo en pantalla podem intuir el fàcil que resulta treballar amb ell. Doncs bé, aquesta senzillesa és una dels seus principals característiques, les quals ens facilitaran molt la labor a l'hora de gestionar les dades. De fet, per a utilitzar un formulari n'hi ha prou amb usar els diferents camps que el componen per a afegir, modificar o visualitzar les dades de les nostres taules. En aquesta unitat aprendrem a manipular les dades mitjançant formularis.

## 8.3.1 Elements del formulari

Quan obrim un formulari per a modificar les dades es mostrarà una pantalla amb els següents elements:

- **Barra de Menús**. Té els mateixos menús que mostra el processador de textos *Writer, si bé és cert que dins d'ells apareixen algunes opcions específiques dels formularis.
- **Barra d'eines Estàndard**. Igual que els menús, conté els mateixos botons que observem quan estem escrivint qualsevol document en *Writer.
- **Barra d'eines Disseny de formularis**. Només es troba activa quan editem un formulari o quan el creguem en manera dissenye. Els seus diferents botons els veurem més endavant.
- **Barra d'eines Navegació de formularis**. És la barra que tenim activa quan treballem amb les dades en un formulari qualsevol i en ella trobem botons per a moure'ns pels diferents registres, botons per a filtrar les dades del formulari, botons per a ordenar els registres per diferents camps, etc.
- **Barra d'Estat**. Ens ofereix tipus d'informació específica alhora que ens permet modificar determinats paràmetres.

### 8.3.1.1 Barra navegació de formularis

Segons hem comentat anteriorment, un formulari ens permet interactuar amb la informació d'una taula però de forma molt més intuïtiva i còmoda. Tots els canvis que fem des d'un formulari s'aplicaran en la taula corresponent.

Base disposa d'una barra de navegació de formularis amb totes les funcions per a afegir, modificar o eliminar dades.

Els diferents botons d'aquesta barra no ens serveixen per a navegar pels camps que integren un formulari, sinó per a navegar pels diferents registres que utilitza aquest formulari. A continuació s'especifica quines accions realitzen alguns d'aquests botons:

- **Registre actual**: indica el número de registre en el qual ens trobem. Podem editar-lo per a anar directament a un determinat registre.
- **Total**: indica el nombre total de registres de la taula. Al principi indicarà un número seguit d'un asterisc, el qual indicarà que existeixen més registres, encara que a mesura que anem passant cap avant, el número s'anirà modificant fins a arribar al màxim real.
- **Moure's entre registres**: aquest conjunt de botons permet desplaçar-nos entre els registres:

Botó | Funció
-|-
⏪| Desplaçar-se al primer registre.
⬅|Desplaçar-se al registre anterior.
➡|Desplaçar-se al registre posterior.
⏩|Desplaçar-se a l'últim registre.

- **Inserir nou registre**: si fem clic sobre aquest botó mostrarà el formulari amb tots els camps buits i el cursor intermitent en el primer d'ells perquè comencem a introduir les dades d'un nou registre.
- **Guardar canvis**: aquest botó podem usar-lo per a guardar les dades que hàgem introduït en un registre nou o en un que estiguem modificant. Els registres també es guarden automàticament quan premem Entrar (Intro) estant en l'últim camp del formulari. Hem de tindre en compte que per a guardar un registre no és necessari emplenar tots els camps del formulari, bastarà que emplenem aquells que siguen obligatoris.
- **Desfer última acció**: aquest botó, igual que en qualsevol altra aplicació, elimina els canvis que hàgem realitzat, bé siga modificant dades o introduint dades noves en el registre actual. Aquesta opció és vàlida en l'edició de dades.
- **Eliminar registre actual**: permet eliminar el contingut del registre que ens mostra el formulari. Aquesta acció elimina les dades de la taula que els conté i ja no podrem recuperar-los, per la qual cosa convé tindre molt clar que volem esborrar les dades.

# 8.4 Modificació de dades en un formulari

La modificació de les dades d'un formulari es realitzarà utilitzant la barra del punt anterior. Per a entendre-ho millor l'explicarem amb exemples.

## 8.4.1 Camp tipus Imatge

En cas que el formulari continga camps de tipus imatge, per a poder editar-la tenim 2 opcions:

- Fer doble clic.
- Fer clic amb el botó dret del ratolí i seleccionar l'opció `Insereix una imatge des de...`

# 📝 *Activitat 9: Formularis*

**Crear formulari `FLIBRO`**

- Obri la base de dades `Biblioteca`.
- Fes clic en el botó **Formularis** de la Barra de **Base de dades**.
En la zona superior de **Tasques**, fes clic en l'opció `Crear un formulari utilizant l'auxiliar...`
- A continuació es desplegarà un assistent que ens guiarà pas a pas per a crear el nostre formulari.
- **Pas 1. Selecció de camp**
  - Hem de triar quins camps volem que es mostren en el formulari i de quines taules. Les taules apareixeran en la part superior mentre que els camps es mostraran en la part inferior. Per a això:
  - Selecciona la taula `LLIBRE`.
  - Selecciona tots els camps utilitzant els botons (un a un) o (tots).
  - Prem `Endavant >`

- **Pas 2. Configurar un subformulari**
  - Aquest pas es tractarà en blocs posteriors de nivell més avançat, per la qual cosa farem clic en `Endavant >`.

- **Pas 5. Organitzeu controls**
  - En el següent pas podem triar la distribució dels camps en el formulari.
  - Fes clic en la icona de l'esquerra "En columnes - Etiquetes a l'esquerra".
  - Prem `Endavant >`

- **Pas 6. Establir entrada de dades**
  - Deixem les opcions per defecte i premem `Endavant >`

- **Pas 7. Aplicar estils**
  - Ací seleccionarem un dels estils proposats per Base.
  - Tria el color i els efectes 2D o 3D que vulgues.
  Prem `Endavant >`

- **Pas 8. Establir nom**
  - Finalment guardem el formulari.
  - En el camp Nom del formulari escriu *`FLIBRO`*. Deixa la resta d'opcions per defecte.
  - Fes clic a `Finalitza`

- Una vegada finalitzat l'assistent, se'ns obri el formulari per a introduir o modificar dades.
- 💾 Guarda els canvis.

---

**Formulari `FLIBRO`. Afegir, esborrar i modificar dades**

- Fes clic en el botó `Formularis` de la barra de `Base de dades`.
- Obri el formulari `FLIBRO` fent doble clic.
- Inserirem un nou llibre. Prem el botó d'afegir registre de la barra navegació de formularis, que està situat en la part inferior de la pantalla.
- Ara els camps es fixaran a un valor buit i/o amb el seu valor per defecte.

> ⚠️ Les màscares de format aplicades als camps en les taules, no es transfereixen automàticament als camps del formulari (per exemple en el camp d'any i preu). Posteriorment veurem com se soluciona aquest problema.

- Descàrrega la següent imatge:
![](img/act_9_portada.jpg)
- Introdueix els valors del nou registre (si l'identificador ID de llibre ja existeix, introdueix un valor numèric de 10 o superior).

  - `ID`: 10
  - `ISBN`: 9788400000000
  - `Titol`: La última legión
  - `Cognoms_autor`: Massimo Manfredi
  - `Nom_autor`: Valerio
  - `Editorial`: SPQR
  - `Anyo`: 01/01/07
  - `Genere`: Historia
  - `Suport`: Paper
  - `Idioma`: Espanyol
  - `Preu`: 9,45
  - `Web`: <https://es.wikipedia.org/wiki/La_última_legión>
  - `Portada`: [act_9_portada.jpg](img/act_9_portada.jpg)
- Inserir la imatge descarregada en el camp de la portada.
- Per a acabar, prem el botó de guardar canvis perquè aquests queden fixats en la taula.

---

**Més dades**

- Per a cadascun dels registres de la taula `LLIBRE`, descàrrega d'Internet una imatge de la portada i afig aquesta imatge en el camp `Portada`. **Procura que les fotos no ocupen molt espai per a no superar el límit de grandària a l'hora de pujar al portal la base de dades**.
- 💾 Guarda els canvis.
- Tanca el formulari.

---

- 💾 Guarda la base de dades.
- Tanca la base de dades.
- Lliura l'activitat.
