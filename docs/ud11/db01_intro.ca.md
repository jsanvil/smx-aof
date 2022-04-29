---
layout: default
title: 1. Introducció a les bases de dades
nav_order: 1
parent: UD11 Bases de dades (I)
has_children: true
---

# 1. Introducció a les bases de dades

## 🎯 Objectius
- Familiaritzar-nos amb el concepte de base de dades.
- Familiaritzar-nos amb el concepte de sistema gestor de base de dades (SGBD).
- Identificar els principals elements de les bases de dades.
- Conéixer els principals usos que reben les bases de dades.

---

La gran quantitat d'informació que manegem en l'actualitat, requereix d'una certa organització que comporta la necessitat d'elements que:

- **Emmagatzemen** la informació de forma organitzada
- Permeten **localitzar** les dades de manera ràpida i senzilla
- **Ordenen** la informació basant-se en criteris
- Realitzen **càlculs** amb les dades numèriques

Per tot això, podem definir una **base de dades** com:
> **Un conjunt de dades que estan organitzats per a un ús determinat**

o, també:

> **Un conjunt d'eines que permeten gestionar informació relacionada d'un tema determinat**.

---

## *Exemple: agenda organitzada*

Si ens fixem en el concepte d'organització podem trobar un exemple bastant clar en la diferència existent entre un munt de números de telèfon i adreces escrits en **trossos de paper** (el que coneixem com a post-it) o tindre'ls organitzats en una **agenda**.
 
En tots dos casos tenim la mateixa informació, però mentre que en el primer trobar un número de telèfon pot portar-nos bastant temps, en el segon cas, el treball es pot reduir a uns pocs segons.

La diferència es troba en la forma en què la informació està emmagatzemada i organitzada.

---

# 1.1. Aplicació pràctica de les bases de dades. Usos

Les bases de dades són un element fonamental que ofereixen multitud d'avantatges a l'hora d'organitzar i emmagatzemar dades. Entre els **usos més habituals** que solen tindre es troben:

- ***Banca***: informació de clients, comptes, transaccions, préstecs, etc.
- ***Transport***: informació de clients, horaris, destins, incidències, trànsit en temps real, sistemes GPS, etc.
- Educació: informació d'estudiants, cursos, matèries (assignatures), horaris, etc.
- ***Forces i cossos de seguretat de l'Estat***: antecedents penals, infraccions, dades personals, DNI electrònic, etc.
- ***Sanitat***: dades de pacients, historials mèdics, dades de centres hospitalaris, dades de proves mèdiques, etc.
- ***Informació personal***: xarxes socials, directoris telefònics, llista de carrers electrònica, agenda de contactes, etc.
- ***Telecomunicacions***: informació de trucades, despeses, saldos, consums, etc.
- ***Internet***: portals i plataformes, blogs, correu electrònic, enciclopèdies digitals, diccionaris, traductors, biblioteques virtuals, etc.

---

# 1.2 Sistemes gestors de bases de dades (*SGBD*)

Anteriorment explicàvem que les bases de dades permeten, entre altres coses, **organitzar els continguts de manera que siguen fàcilment localitzables**.
Per a poder utilitzar les bases de dades necessitem d'un **suport** que permeta introduir, organitzar i recuperar la informació d'aquestes, en definitiva, **administrar-les**, anomenat **sistema gestor de base de dades (*SGBD*)**.

> **Un *SGBD* és un programa informàtic que gestiona una base de dades**.

Existeixen molts tipus diferents de gestors de bases de dades, encara que quasi tots els sistemes moderns emmagatzemen i tracten la informació utilitzant el **model de gestió de bases de dades relacional**. En aquest sistema, les dades s'organitzen en **taules**, les quals es troben **relacionades** d'alguna forma entre elles. Aquestes taules emmagatzemen informació sobre un tema, com poden ser els usuaris d'una xarxa social, els clients d'una empresa, les comandes realitzades per cadascun d'ells o els llibres d'una biblioteca.

[***LibreOffice Base***](https://www.libreoffice.org/discover/base/) és un **sistema gestor de bases de dades relacionals (*SGBDR*)** que permet emmagatzemar i recuperar la informació en les taules d'una base de dades, d'acord amb les relacions que s'hagen establit. A més de ser **lliure**, ofereix diferents versions que permeten adaptar-se als diferents **sistemes operatius existents**.

---

# 1.3 Elements

Pràcticament, en qualsevol base de dades actual, existeixen quatre elements essencials: **taules**, **consultes**, **formularis** i **informes**. Tots són indispensables i necessaris. Aquesta és una definició molt bàsica de cadascun dels elements que formen part d'una base de dades però suficient per a començar a familiaritzar-nos amb aquests conceptes:

Element	       | Funció
---------------|------------------------------------
**Taules**     | Permeten emmagatzemar les dades.
**Consultes**  | Amb les consultes podem accedir a les dades emmagatzemades, ordenar-los i filtrar-los per diferents criteris.
**Formularis** | Faciliten les tasques d'introducció de dades en les taules, de manera que siguen més intuïtives i senzilles per a l'ésser humà.
**Informes**   | Representen la forma més eficaç de presentar les nostres dades, tant per pantalla com per impressora.

---

## 1.3.1 Taules

Dins d'una base de dades, la informació s'emmagatzema i s'organitza en taules, havent-hi en cadascuna d'elles una o diverses sèries de files i columnes. A les files se'ls denomina registres, a les columnes, camps, i a la intersecció d'un registre amb un camp se'n diu dada. L'estructura és similar a un full de càlcul, encara que el funcionament i la nomenclatura difereixen.

 Nom en *full de càlcul* | Nom en *base de dades*
----------------------|---------------------
Fila                  | Registre
Columna               | Camp
Cel·la                | Dades

En la imatge es mostren exemples dels conceptes explicats:

![](https://ioc.xtec.cat/materials/FP/Recursos/fp_smx_m03_/web/fp_smx_m03_htmlindex/WebContent/u5/media/ud1_a1_1.1.png)

---

## 1.3.2 Consultes

Les consultes tenen com a propòsit recuperar la informació emmagatzemada en les taules, és a dir, permeten veure un conjunt de dades d'una taula a partir d'una petició o pregunta que realitzem.

*És similar a aplicar **filtres** en un **full de càlcul**.*

---

## 1.3.3 Formularis

Els formularis ens ajudaran principalment en tasques d'introducció, modificació i esborrat d'informació, ja que mostren les dades de manera diferent al d'una taula, de manera més vistosa i agradable. Quan es tracta d'incloure poques dades podem fer-ho directament sobre les taules però quan el volum és important, aquest mètode es torna poc eficaç. Per a resoldre aquest problema tenim els formularis on la inclusió de dades es fa de forma molt més intuïtiva i senzilla.

*Exemple de formulari:*

![](https://ioc.xtec.cat/materials/FP/Recursos/fp_smx_m03_/web/fp_smx_m03_htmlindex/WebContent/u5/media/1.3.png)

---

## 1.3.4. Informes

Els **informes** tenen com a objectiu proporcionar les eines necessàries per a **obtindre una còpia per pantalla o impresa de les dades existents en una base de dades**.

Habitualment, els informes se solen construir a partir dels resultats obtinguts de l'execució de **consultes**, la qual cosa combina la possibilitat de seleccionar només les dades que volem que ens oferisquen les consultes amb l'avantatge d'imprimir-los, tant per pantalla com en paper.
Aquests poden ser configurats amb diferents estils de manera que es puguen adaptar als diferents usuaris i circumstàncies en les quals siguen requerits.

*Exemple d'informe:*

![](https://ioc.xtec.cat/materials/FP/Recursos/fp_smx_m03_/web/fp_smx_m03_htmlindex/WebContent/u5/media/1.4.png)

---

## *Exemple pràctic: centre educatiu*

A continuació il·lustrarem amb un exemple els elements de les bases de dades amb la finalitat que queden clars tots els conceptes estudiats. Per a això utilitzarem la base de dades d'un centre educatiu:

- **Taules**:
  - professors
  - alumnes
  - matrícules
  - assignatures
  - grups
  - cursos
  - *...*
- **Consultes**:
  - assignatures que té cada alumne
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

Com es pot observar, cada **taula** emmagatzemarà informació de cada element de l'institut, cada **consulta** permetrà obtindre dades que podran ser utilitzats en **informes**, i cada **formulari** permetrà introduir i modificar, de manera senzilla i intuïtiva, la informació d'una o diverses taules.
