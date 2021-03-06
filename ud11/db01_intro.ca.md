UD11: Bases de dades (I)

# 1. Introducci贸 a les bases de dades

## 馃幆 Objectius

- Familiaritzar-nos amb el concepte de base de dades.
- Familiaritzar-nos amb el concepte de sistema gestor de base de dades (SGBD).
- Identificar els principals elements de les bases de dades.
- Con茅ixer els principals usos que reben les bases de dades.

---

La gran quantitat d'informaci贸 que manegem en l'actualitat, requereix d'una certa organitzaci贸 que comporta la necessitat d'elements que:

- **Emmagatzemen** la informaci贸 de forma organitzada
- Permeten **localitzar** les dades de manera r脿pida i senzilla
- **Ordenen** la informaci贸 basant-se en criteris
- Realitzen **c脿lculs** amb les dades num猫riques

Per tot aix貌, podem definir una **base de dades** com:
> **Un conjunt de dades que estan organitzats per a un 煤s determinat**

o, tamb茅:

> **Un conjunt d'eines que permeten gestionar informaci贸 relacionada d'un tema determinat**.

---

## *Exemple: agenda organitzada*

Si ens fixem en el concepte d'organitzaci贸 podem trobar un exemple bastant clar en la difer猫ncia existent entre un munt de n煤meros de tel猫fon i adreces escrits en **trossos de paper** (el que coneixem com a post-it) o tindre'ls organitzats en una **agenda**.

En tots dos casos tenim la mateixa informaci贸, per貌 mentre que en el primer trobar un n煤mero de tel猫fon pot portar-nos bastant temps, en el segon cas, el treball es pot reduir a uns pocs segons.

La difer猫ncia es troba en la forma en qu猫 la informaci贸 est脿 emmagatzemada i organitzada.

---

# 1.1. Aplicaci贸 pr脿ctica de les bases de dades. Usos

Les bases de dades s贸n un element fonamental que ofereixen multitud d'avantatges a l'hora d'organitzar i emmagatzemar dades. Entre els **usos m茅s habituals** que solen tindre es troben:

- ***Banca***: informaci贸 de clients, comptes, transaccions, pr茅stecs, etc.
- ***Transport***: informaci贸 de clients, horaris, destins, incid猫ncies, tr脿nsit en temps real, sistemes GPS, etc.
- Educaci贸: informaci贸 d'estudiants, cursos, mat猫ries (assignatures), horaris, etc.
- ***Forces i cossos de seguretat de l'Estat***: antecedents penals, infraccions, dades personals, DNI electr貌nic, etc.
- ***Sanitat***: dades de pacients, historials m猫dics, dades de centres hospitalaris, dades de proves m猫diques, etc.
- ***Informaci贸 personal***: xarxes socials, directoris telef貌nics, llista de carrers electr貌nica, agenda de contactes, etc.
- ***Telecomunicacions***: informaci贸 de trucades, despeses, saldos, consums, etc.
- ***Internet***: portals i plataformes, blogs, correu electr貌nic, enciclop猫dies digitals, diccionaris, traductors, biblioteques virtuals, etc.

---

# 1.2 Sistemes gestors de bases de dades (*SGBD*)

Anteriorment explic脿vem que les bases de dades permeten, entre altres coses, **organitzar els continguts de manera que siguen f脿cilment localitzables**.
Per a poder utilitzar les bases de dades necessitem d'un **suport** que permeta introduir, organitzar i recuperar la informaci贸 d'aquestes, en definitiva, **administrar-les**, anomenat **sistema gestor de base de dades (*SGBD*)**.

> **Un *SGBD* 茅s un programa inform脿tic que gestiona una base de dades**.

Existeixen molts tipus diferents de gestors de bases de dades, encara que quasi tots els sistemes moderns emmagatzemen i tracten la informaci贸 utilitzant el **model de gesti贸 de bases de dades relacional**. En aquest sistema, les dades s'organitzen en **taules**, les quals es troben **relacionades** d'alguna forma entre elles. Aquestes taules emmagatzemen informaci贸 sobre un tema, com poden ser els usuaris d'una xarxa social, els clients d'una empresa, les comandes realitzades per cadascun d'ells o els llibres d'una biblioteca.

[***LibreOffice Base***](https://www.libreoffice.org/discover/base/) 茅s un **sistema gestor de bases de dades relacionals (*SGBDR*)** que permet emmagatzemar i recuperar la informaci贸 en les taules d'una base de dades, d'acord amb les relacions que s'hagen establit. A m茅s de ser **lliure**, ofereix diferents versions que permeten adaptar-se als diferents **sistemes operatius existents**.

---

# 1.3 Elements

Pr脿cticament, en qualsevol base de dades actual, existeixen quatre elements essencials: **taules**, **consultes**, **formularis** i **informes**. Tots s贸n indispensables i necessaris. Aquesta 茅s una definici贸 molt b脿sica de cadascun dels elements que formen part d'una base de dades per貌 suficient per a comen莽ar a familiaritzar-nos amb aquests conceptes:

Element        | Funci贸
---------------|------------------------------------
**Taules**     | Permeten emmagatzemar les dades.
**Consultes**  | Amb les consultes podem accedir a les dades emmagatzemades, ordenar-los i filtrar-los per diferents criteris.
**Formularis** | Faciliten les tasques d'introducci贸 de dades en les taules, de manera que siguen m茅s intu茂tives i senzilles per a l'茅sser hum脿.
**Informes**   | Representen la forma m茅s efica莽 de presentar les nostres dades, tant per pantalla com per impressora.

---

## 1.3.1 Taules

Dins d'una base de dades, la informaci贸 s'emmagatzema i s'organitza en taules, havent-hi en cadascuna d'elles una o diverses s猫ries de files i columnes. A les files se'ls denomina registres, a les columnes, camps, i a la intersecci贸 d'un registre amb un camp se'n diu dada. L'estructura 茅s similar a un full de c脿lcul, encara que el funcionament i la nomenclatura difereixen.

 Nom en *full de c脿lcul* | Nom en *base de dades*
----------------------|---------------------
Fila                  | Registre
Columna               | Camp
Cel路la                | Dades

En la imatge es mostren exemples dels conceptes explicats:

![](https://ioc.xtec.cat/materials/FP/Recursos/fp_smx_m03_/web/fp_smx_m03_htmlindex/WebContent/u5/media/ud1_a1_1.1.png)

---

## 1.3.2 Consultes

Les consultes tenen com a prop貌sit recuperar la informaci贸 emmagatzemada en les taules, 茅s a dir, permeten veure un conjunt de dades d'una taula a partir d'una petici贸 o pregunta que realitzem.

*脡s similar a aplicar **filtres** en un **full de c脿lcul**.*

---

## 1.3.3 Formularis

Els formularis ens ajudaran principalment en tasques d'introducci贸, modificaci贸 i esborrat d'informaci贸, ja que mostren les dades de manera diferent al d'una taula, de manera m茅s vistosa i agradable. Quan es tracta d'incloure poques dades podem fer-ho directament sobre les taules per貌 quan el volum 茅s important, aquest m猫tode es torna poc efica莽. Per a resoldre aquest problema tenim els formularis on la inclusi贸 de dades es fa de forma molt m茅s intu茂tiva i senzilla.

*Exemple de formulari:*

![](https://ioc.xtec.cat/materials/FP/Recursos/fp_smx_m03_/web/fp_smx_m03_htmlindex/WebContent/u5/media/1.3.png)

---

## 1.3.4. Informes

Els **informes** tenen com a objectiu proporcionar les eines necess脿ries per a **obtindre una c貌pia per pantalla o impresa de les dades existents en una base de dades**.

Habitualment, els informes se solen construir a partir dels resultats obtinguts de l'execuci贸 de **consultes**, la qual cosa combina la possibilitat de seleccionar nom茅s les dades que volem que ens oferisquen les consultes amb l'avantatge d'imprimir-los, tant per pantalla com en paper.
Aquests poden ser configurats amb diferents estils de manera que es puguen adaptar als diferents usuaris i circumst脿ncies en les quals siguen requerits.

*Exemple d'informe:*

![](https://ioc.xtec.cat/materials/FP/Recursos/fp_smx_m03_/web/fp_smx_m03_htmlindex/WebContent/u5/media/1.4.png)

---

## *Exemple pr脿ctic: centre educatiu*

A continuaci贸 il路lustrarem amb un exemple els elements de les bases de dades amb la finalitat que queden clars tots els conceptes estudiats. Per a aix貌 utilitzarem la base de dades d'un centre educatiu:

- **Taules**:
  - professors
  - alumnes
  - matr铆cules
  - assignatures
  - grups
  - cursos
  - *...*
- **Consultes**:
  - assignatures que t茅 cada alumne
  - alumnes de cada grup
  - grups de cada curs
  - *...*
- **Formularis**:
  - alumnes
  - professors
  - assignatures per alumne
  - grups de cada curs
  - *...*
- **Informes**:
  - professors per grup
  - alumnes matriculats
  - assignatures impartides
  - percentatge d'aprovats
  - *...*

Com es pot observar, cada **taula** emmagatzemar脿 informaci贸 de cada element de l'institut, cada **consulta** permetr脿 obtindre dades que podran ser utilitzats en **informes**, i cada **formulari** permetr脿 introduir i modificar, de manera senzilla i intu茂tiva, la informaci贸 d'una o diverses taules.
