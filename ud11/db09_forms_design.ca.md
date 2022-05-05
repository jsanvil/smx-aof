UD11: Bases de dades (I)

# 9. *LibreOffice Base*: Disseny de formularis

##  🎯 Objectius

- Modificar el disseny de formularis.
- Modificar propietats senzilles de camps.
- Conéixer i utilitzar formats senzills per a mostrar els camps.
- Conéixer alguns controls dels formularis.

---

# 9.1 Disseny d'un formulari

L'auxiliar de formularis crea un disseny per defecte, segons el que hem anat triant en els successius passos. Lògicament, aquest disseny no té perquè adaptar-se als nostres gustos o necessitats, per la qual cosa Base permet canviar el disseny quant a grandària, posició, color, etc.

Una vegada creat el formulari ens poden sorgir multitud d'idees per a millorar-lo; podem afegir més camps, canviar el fons, la grandària i la posició dels camps, l'estil dels caràcters que es mostren i una infinitat de característiques més. En aquesta unitat aprendrem a modificar les propietats dels elements del formulari amb la finalitat d'adaptar-lo a les necessitats dels usuaris.

## 9.1.1 Vista de disseny de formularis

Per a poder modificar els atributs dels camps i el disseny gràfic, hem d'entrar en la vista de disseny de formularis, fent clic en la icona `Editar` de la barra d'eines. Ara entrem en `Vista de disseny de formularis`, per la qual cosa no podem manipular informació de la base de dades, només podem modificar l'aspecte visual del formulari.

> ⚠️ Podem passar de la vista de disseny a la vista de edició de dades i viceversa, fent clic en la icona `Mode de disseny`.

---

# 9.2 Controls d'un formulari

El control més habitual d'un formulari és el `Quadre de text`, o cosa que és el mateix, una etiqueta i un requadre a la dreta per a introduir o editar la informació del camp. Però aquesta no és l'única manera de mostrar les dades en un formulari, existeixen diferents possibilitats depenent de la mena de dades i de la forma que desitgem representar-lo. Tots ells els trobem en la barra lateral.

Per a veure més controls, farem clic en la icona de les fletxes negres i en `Més controls`.

---

# 9.3 Camps amb format

Igual que vam veure amb les taules, aquest tipus de camps serveixen per a mostrar informació en el formulari aplicant un format determinat.

---

# 9.4 Aparença d'un formulari

Fins al moment hem incidit en la part tècnica de la creació i disseny de formularis, sense cuidar excessivament la interfície amb l'usuari. L'aparença és un assumpte summament important, perquè del seu disseny dependrà en gran manera l'adaptació, la utilització i l'acceptació de l'ús d'un determinat formulari.

En conseqüència, ha d'aplicar-se el principi d'ergonomia, de manera que un formulari s'adapte a les nostres necessitats i no al contrari.

## 9.4.1 Elements gràfics

Per a inserir un element gràfic, utilitzarem les icones de la barra d'eines `Dibuix`, situada en la part inferior dreta.

Per a veure més funcionalitats, farem clic en la icona de les fletxes negres.

---

# 9.5 Rètols artístics

La galeria *Fontwork+ conté diferents dissenys de rètols artístics, que al seu torn, podem modificar. Per a inserir un rètol artístic farem clic en la icona de la barra d'eines.

---

# 📝 *Activitat 10: Disseny de formularis*

**Formulari FLIBRO: Disseny**

- Obri la base de dades "biblioteca".
- Fes clic en el botó Formularis de la barra de base de dades.
- Selecciona el formulari *FLIBRO.
- Selecciona la icona Editar de la barra d'eines. Ara entrem en manera Disseny de formularis.

Modificarem les propietats d'alguns camps.

- **Camp `Observacions`**
  - Fes doble clic sobre el camp `Observacions`. En fer doble clic es mostrarà una finestra amb un conjunt de propietats que podrem modificar.
  - Canvia la propietat `Alineació vert` al valor "Superior".

  - Guarda els canvis del disseny del formulari fent clic en la icona `Guardar`. 
  - Tanca el formulari.
  - Fes doble clic sobre el formulari `FLIBRO` i comprova que les observacions es visualitzen correctament:


- **Camp `ID`**

  - Ara canviarem les propietats del camp `ID` perquè no es puga modificar ja que l'`ID` és clau primària.

  - Selecciona el formulari `FLIBRO`.
  - Obri el formulari en vista de disseny.
  - Fes doble clic sobre el camp `ID`. Es mostrarà una finestra de propietats. Canvia la propietat `Activat` al valor *`No`* i la propietat `Alineació` al valor *`Dreta`*.

  - Guarda els canvis del disseny del formulari fent clic en la icona `Guardar`. 
  - Canvia a vista de edició de dades. Fes clic en la icona corresponent.
  - Comprova que no podem editar el valor del camp `ID` (es veurà en un color gris clar) i que el text s'alinea a la dreta.

**Aplicar format camp `Any`**

- Selecciona el formulari `FLIBRO`.
- Obri el formulari en vista de dissen.
- Prem sobre la icona de la barra esquerra anomenat Camp formatat. Dibuixa un nou camp en el formulari al costat del camp `Any`.
- Fes doble clic sobre el nou camp. En la pestanya General, en la propietat Nom escriu *`Any formatat`*.
- Tria la propietat Format. 
- Fes clic en la icona amb punts suspensius. Tria la categoria Data. Fins ara el nostre camp `Any` estava predefinit com DD/MM/AA; és a dir, dues xifres per al dia, dos per al mes i dos per a l'any.
- En el camp Format de codi tecleja AAAA. Després, prem la icona de la dreta Afegir.

- Comprova que s'ha afegit el nou format:


- En la propietat `Activat`, estableix el valor *`No`*.
Ara enllacem el nou camp amb un camp de la nostra base de dades.

- En la pestanya Dades, veu a la propietat Camp de dades i tria el camp `Any`.


- Guarda els canvis.
- Tanca la vista dissenye i comprova el resultat en la vista de dades. Ara tenim un camp amb format que ens mostrarà l'any de publicació del llibre.



**Aplicar format camp `Preu`**

- Selecciona el formulari `FLIBRO`.
- Obri el formulari en vista de disseny. 
- Fes clic en la icona de Més controls .
- En la nova finestra que es mostra, prem sobre la icona anomenada Camp moneda . Dibuixa un nou camp en el formulari al costat del camp “Preu”.
- Fes doble clic sobre el nou camp. En la pestanya General, en la propietat Nom escriu "Preu formatat".
- Tria la propietat Valor predeterminat. Escriu el valor 0.
- En la pestanya Dades, veu a la propietat Camp de dades i tria el camp “Preu”.
- Fes clic en el camp preu antic i esborra'l (tecla *Supr).
- Prem sobre la icona de la barra esquerra anomenat Etiqueta . Dibuixa una nova etiqueta en el formulari a l'esquerra del nou camp “Preu”.
- Tria la propietat Etiqueta. Escriu el text "Preu".
- Guarda els canvis.
- Tanca la vista dissenye i comprova el resultat en la vista de dades. Ara tenim un camp amb format que ens mostrarà l'any de publicació del llibre.





Canviarem l'aparença del disseny del formulari *FLIBRO perquè la interfície resulte agradable i intuïtiva.

Fes clic en el botó Formularis de barra de Base de dades.
Selecciona el formulari *FLIBRO.
Obri el formulari en manera dissenye. 
Pot utilitzar-se els efectes i colors que es desitge.
Desplaçar elements de la pantalla

Anem a redimensiona els elements de la pantalla per a deixar espai per als encapçalats (imatge i títol).

Fes clic en la icona Selecció, situat en la part inferior esquerra de la pantalla.


Selecciona tots els elements del formulari mitjançant el botó esquerre del ratolí.
Situa el ratolí en la vora de la selecció i, quan aparega una creu, arrossega tots els elements cap a la part inferior de la pantalla, per a desplaçar-los més a baix.
Inserir imatge i títol

Inserida un rectangle arredonit 3D en la part superior del formulari i col·loca'l en la part central. Escriu dins el text “BIBLIOTECA”.
Descàrrega del portal la imatge de la icona del llibre. DESCARREGAR
Inserida la imatge descarregada en la part superior del formulari. Menú Inserir → Imatge o icona . Col·loca-la a l'esquerra del rectangle amb el títol.



