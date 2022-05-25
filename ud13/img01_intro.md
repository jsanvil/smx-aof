UD13: Imatge digital

# 1 Formats i resolució d'imatges

## 🎯 Objectius

- Conéixer els conceptes bàsics utilitzats en el tractament digital de la imatge.
- Conéixer els tipus d'imatges digitals.
- Elements d'una imatge digital: resolució, grandària, profunditat de color i modes de color.
- Familiaritzar-se amb l'entorn de treball de *GIMP*. Aprendre a personalitzar l'entorn al nostre gust.
- Identificar els principals elements de la interfície d'usuari.
- Localitzar el sistema d'ajuda del programa.

---

# 1.1 Tractament digital d'imatges

En l'actualitat, el desenvolupament tecnològic ha possibilitat un enorme avanç en el món de la fotografia. Les càmeres digitals, els ordinadors i els programes de retoc fotogràfic permeten un ventall de possibilitats impensable tan sols fa uns pocs anys.

El tractament o processament digital correspon al conjunt de tècniques aplicades a les imatges digitals amb l'objectiu de millorar la qualitat, afegir efectes, realitzar muntatges o facilitar la cerca d'informació.

En aquesta unitat introduirem alguns dels conceptes bàsics que s'han de conéixer per a començar a treballar en el món del tractament d'imatges. En els següents apartats definirem conceptes com a píxel, mapa de bits, imatge vectorial i els elements d'una imatge digital.

---

# 1.2 Elements bàsics. Píxel

Wikipedia ens diu: “Un píxel o pixel (acrònim de l'anglés *picture element*, "element d'imatge") és la menor unitat homogènia en color que forma part d'una imatge digital, ja siga aquesta una fotografia, un fotograma de vídeo o un gràfic. Ampliant prou una imatge digital (zoom), per exemple en la pantalla d'un ordinador, poden observar-se els píxels que componen la imatge. Els píxels apareixen com a xicotets quadrats o rectangles en color, en blanc o en negre, o en matisos de gris. Les imatges es formen com una matriu rectangular de píxels, on cada píxel forma una àrea relativament xicoteta respecte a la imatge total”.

En definitiva, la imatge d'una pantalla d'ordinador és com un mosaic amb un número de *pixels* en horitzontal i en vertical. Quan es diu que la pantalla té una resolució de 800 x 600 o 1024 x 768, la primera xifra indica el número de *pixels* en horitzontal que tindrà l'escriptori i la segona xifra els *pixels* en vertical.

Pixelat en fer zoom:

![Exemple de pèrdua de qualitat en ampliar un detall de la imatge rasteritzada](https://upload.wikimedia.org/wikipedia/commons/2/2b/Pixel-example.png)

# 1.3. Tipus d'imatges

Podem dividir els tipus d'imatges digitals en dues: imatges de mapa de bits i imatges vectorials. Abans de veure els tipus d'imatges, introduirem el concepte de píxel, fonamental per a entendre el funcionament de la fotografia digital.

![Raster vs Vector](https://upload.wikimedia.org/wikipedia/commons/6/6b/Bitmap_VS_SVG.svg)

---

## 1.3.1. Imatges de mapa de bits

Normalment, els arxius de les imatges es guarden en forma de mapa de bits (mapa de bits en anglés) o mosaic de píxels. Per exemple, els escàners i càmeres digitals creen imatges en aquest format. Aquest tipus d'imatges estan formades per una matriu de punts o raster (una forma quadrangular amb un nombre de píxels en horitzontal i en vertical). Cada píxel guarda la informació de color de la part d'imatge que ocupa.

El principal inconvenient que presenten aquesta classe d'arxius és el de l'ampliació: quan un arxiu s'amplia molt, es distorsiona la imatge, mostrant-se el mosaic amb els *píixels* i una degradació en els colors arribant a aquest efecte *pixelació* a causa de la deformació de la fotografia.

![The Gunk](https://upload.wikimedia.org/wikipedia/commons/7/71/The_Gunk_699px.png)

---

## 1.3.2. Imatges vectorials

Wikipedia ens indica que és una “imatge digital formada per objectes geomètrics independents (segments, polígons, arcs, etc.), cadascun d'ells definit per diferents atributs matemàtics de forma, de posició, de color, etc. Per exemple, un cercle de color roig quedaria definit per la posició del seu centre, el seu radi, el gruix de línia i el seu color”. Dit d'una altra manera, es tracta d'imatges formades per multitud de vectors que guarden la seua informació mitjançant expressions matemàtiques.

El principal avantatge d'aquestes imatges és que es poden reduir i ampliar sense perdre qualitat perquè els traços es redibuixen en canviar de grandària. Per tant, es poden moure, estirar, retorçar, etc., de manera senzilla amb les aplicacions que treballen aquest tipus de gràfics. A més, aquesta classe d'arxius ocupen molta menys memòria que les imatges de mapa de bits.

Dibuix vectorial:

![Tux](https://upload.wikimedia.org/wikipedia/commons/3/35/Tux.svg)

---

# 1.4. Propietats de la imatge

## 1.4.1. Resolució

La resolució representa la quantitat de detall que pot observar-se en una imatge, bé siga obtinguda mitjançant escàner, càmera de fotos o impresa. Aquesta quantitat es mesura en ppp (píxels o punts per polzada) o en anglés *dpi* (*dots per inch*). Lògicament, tindre major resolució es tradueix a obtindre una imatge amb més detall o qualitat visual.

![Image dpi](https://upload.wikimedia.org/wikipedia/commons/f/f2/Resolution_illustration.png)

>Recordem que 1 polzada = 2,54 cm.

Per a les imatges digitals emmagatzemades com a mapa de bits, la convenció és descriure la resolució de la imatge amb dos nombres enters, on el primer és la quantitat de columnes de píxels (quants píxels té la imatge a l'ample) i el segon és la quantitat de files de píxels (quants píxels té la imatge a l'alt). Per exemple:

![Image resolution](img/UD13_ImageResolution.png)

---

### 1.4.1.1. Resolució de pantalla

Representa el nombre de píxels per polzada (ppp) que és capaç de mostrar un monitor d'ordinador. La resolució de pantalla ve donada pel producte de l'ample per l'alt, mesurats tots dos en píxels, amb el que s'obté una relació, anomenada relació d'aspecte. Aquesta relació d'aspecte pot variar, ja que està d'acord a la forma del monitor i de la targeta gràfica. Per això, es poden diferenciar dues grandàries de pantalla:

![Resolució de pantalla](https://upload.wikimedia.org/wikipedia/commons/e/e5/Vector_Video_Standards2.svg)

Grandària absoluta: l'amplària i altura de la finestra del monitor, mesurat generalment en polzades. Depén del monitor.
Resolució o grandària relativa: ve determinada pel nombre de píxels que es mostren en la finestra del monitor. Depén de la targeta gràfica.

---

### 1.4.1.2. Resolució d'una càmera digital

La qualitat de resolució de les càmeres digitals s'expressa en **Megapíxels**. Per exemple, una càmera de 12MP pot prendre una fotografia amb 12 milions de píxels. Per a saber quina és la resolució d'una càmera digital hem de conéixer els píxels d'ample x alt als quals és capaç d'obtindre una imatge.

*Exemples:*

Píxels | Resolució
-|-
1600 x 1200 | 1600x1200 = 1.920.000 píxels, és a dir 2 MP
2816x2112 | 2816x2112 = 5.947.392 píxels, és a dir 6 MP

---

### 1.4.1.3. Resolució d'impressió

En una impressora, es refereix al nombre de punts per polzada (ppp) als quals es pot imprimir una imatge digital de qualitat. A partir de 200ppp podem dir que la resolució d'impressió és bona, i si volem assegurar-nos, hem d'aconseguir els 300ppp perquè moltes vegades l'òptica de la càmera, la neteja de l'objectiu o el processador d'imatges de la càmera digital disminueixen la qualitat.

---

### 1.4.1.4. Resolució d'escanejat

Depén dels components de l'escàner i dels paràmetres als quals volem escanejar. El mínim solen ser imatges escanejades amb una resolució per defecte de 200ppp.

---

## 1.4.2. Grandària

Tipus | Significat
-|-
**Grandària digital** | La grandària digital és el **nombre de píxels** (ample x alt) que formen una imatge digital. S'expressa en Megapíxels (milions de píxels).
**Grandària física** | És la grandària física d'una **imatge impresa**; és a dir, són les dimensions reals en termes d'amplària i altura una vegada impresa. Se sol expressar en centímetres o polzades.
**Grandària d'arxiu** | Fa referència a la quantitat de **memòria física** necessària per a guardar una imatge digital en un suport informàtic d'emmagatzematge (disc dur, memòria USB, memòria RAM, etc.).

---

## 1.4.3. Profunditat de color

La profunditat de color es refereix al nombre de bits necessaris per a codificar i guardar la informació de color de cada píxel en una imatge. Com més gran siga la profunditat de color en bits, la imatge disposarà d'una paleta de colors més àmplia i, en conseqüència, es representarà millor.

Un bit és una posició de memòria que pot tindre el valor 0 o 1. En la taula següent podem comprovar el nombre de colors possibles segons el nombre de bits de profunditat de color.

Profunditat (bits) | Núm. de colors
---|---
1  | 2 (blanc i negre) (0=color negre, 1= color blanc)
2  | 4 (00=color negre, 01=color X, 10=color I, 11=color blanc)
4  | 16
8  | 256
16 | 65536
24 | 16,7 milions
32 | 4294 milions

---

# 1.5. Modes de color

Els modes de color defineixen el sistema que utilitzem per a descriure els colors en un entorn determinat. Un model de colors és un model matemàtic abstracte que permet representar els colors en forma numèrica, utilitzant típicament tres o quatre valors o components cromàtics.

Els modes de color més comuns són: escala de grisos, indexat, *RGB*, *HSV* i *CMYK*.

---

## 1.5.1. Escala de grisos

Una escala de grisos és una escala emprada en la imatge digital en la qual el valor de cada píxel posseeix un valor equivalent a una graduació de grisa. Les imatges representades d'aquest tipus estan compostes d'ombres de grisos.

![Grayscale](https://upload.wikimedia.org/wikipedia/commons/f/fa/Grayscale_8bits_palette_sample_image.png)

---

## 1.5.2. Indexat

En aquest model, podem especificar els colors amb els quals treballarem amb un màxim de 256 colors. Utilitza un canal de color indexat de 8 bits.

![Indexed color](https://upload.wikimedia.org/wikipedia/commons/c/ce/Screen_color_test_VGA_16colors.png)

---

## 1.5.3. RGB

RGB (sigles en anglés de *Red, Green, Blue*, en valencià RVA "roig, verd i blau") és un model de color basat en la síntesi additiva, amb el qual és possible representar un color mitjançant la mescla per addició dels tres colors de llum primaris.

![RGB](https://upload.wikimedia.org/wikipedia/commons/c/ce/Barn_grand_tetons_rgb_separation.jpg)

La intensitat de cadascuna de les components es mesura segons una escala que va del 0 al 255 i cada color és definit per un conjunt de valors escrits entre parèntesis (corresponents a valors "R", "G" i "B") i separats per comes.

D'aquesta manera, el roig s'obté amb (255,0,0), el verd amb (0,255,0) i el blau amb (0,0,255), obtenint, en cada cas un color resultant monocromàtic. L'absència de color, és a dir el color negre, s'obté quan les tres components són 0: (0,0,0).

![RGB](https://upload.wikimedia.org/wikipedia/commons/1/12/RGB_sliders.svg)

---

## 1.5.4. HSV/HSB

El model ***HSV*** (de l'anglés *Hue, Saturation, Value*), també anomenat ***HSB*** (*Hue, Saturation, **Brightness***), defineix un model de color en termes dels seus components. Està basat en la manera en què l'ull humà percep el color, per tant es tracta del mode més "natural".

***Hue*** (Tonalitat). És el valor del color: roig, blau, verd, etc. Es representa com un grau d'angle els valors possibles del qual van de 0 a 360° (encara que per a algunes aplicacions es normalitzen del 0 al 100%). Cada valor correspon a un color. Exemples: 0 és roig, 60 és groc i 120 és verd.

***Saturation*** (Saturació). Es refereix a la puresa del color i va del 0% al 100%. Quant menor siga la saturació d'un color, major tonalitat grisenca hi haurà i més descolorit estarà.

***Value******Brightness*** (Lluminositat). Referència la intensitat de llum del color, és a dir, la quantitat de negre o blanc que conté. Els valors possibles van del 0 al 100%. 0 sempre és negre. Depenent de la saturació, 100 podria ser blanc o un color més o menys saturat.

![HSV](https://upload.wikimedia.org/wikipedia/commons/1/1b/Triangulo_HSV.png)

---

## 1.5.5 CMYK

***CMYK*** (sigles de *Cyan*, *Magenta*, *Yellow* i *Key*) és un model de color sustractiu que s'utilitza en la impressió d'imatges en colors. És la versió moderna i més precisa de l'antic model tradicional de coloració (RYB), que s'utilitza encara en pintura i arts plàstiques. Permet representar una gamma de colors més àmplia que aquest últim, i té una millor adaptació als mitjans industrials.

Aquest model es basa en la mescla de pigments dels següents colors per a crear altres més:

![CMYK](https://upload.wikimedia.org/wikipedia/commons/4/4c/CMYK_color_swatches.svg)

C = *Cyan* (Cian). M = *Magenta* (Magenta). I = *Yellow* (Groc). K = *Black* o *Key* (Negre).

![CMYK Image](https://upload.wikimedia.org/wikipedia/commons/3/3c/SubtractiveColorSynthesis_CMYK_2.jpg)

---

## 1.5.6. Usos i colors

Els modes *RGB* (roig, verd i blau), escala de grisos i indexat estan indicats per a imatges el destí de les quals siga una pantalla d'ordinador. Per contra, en el cas que una imatge vaja a ser impresa, podem utilitzar la manera *CMYK*, que és la manera de color utilitzat per les impressores.

Un *pixel* solament pot ser d'un color; quan diem que una imatge és de 256 colors, això indica que un píxel pot tindre un d'aquests 256 colors. Perquè una imatge tinga més de 256 colors ha de treballar en mode *RGB* en el qual un píxel pot ser la combinació d'un dels 256 nivells de roig, 256 nivells de blau i 256 nivells de verd (256 x 256 x 256 = 16.777.216 colors; per això es diu que una imatge *RGB* pot tindre milions de colors). Quants més colors tinga una imatge més ocuparà l'arxiu que la conté.

En general, els programes de retoc fotogràfic treballen en mode *RGB*, perquè s'adapta bé a la pantalla. No obstant això, és possible convertir la imatge a escala de grisos o al mode indexat, però cal tindre present que si una imatge es guarda en escala de grisos o indexat ja no es poden recuperar tots els colors en revertir-la al mode *RGB*. És aconsellable mantindre una còpia del treball en mode *RGB*.

---

# 1.6 Programa de retoc d'imatges de GNU - *GIMP*

![Wilber](https://docs.gimp.org/2.10/en/images/using/wilber.png)

El *GIMP* és una eina de retoc fotogràfic multiplataforma. El *GIMP* és un acrònim de ***GNU Image Manipulation Program***. Al *GIMP* es poden dur a terme tota mena de tasques de retoc d'imatges, incloent-hi el retoc fotogràfic, la composició i la creació d'imatges.

El *GIMP* té moltes capacitats. Es pot usar com un senzill programa de pintura, un programa de retoc fotogràfic professional, un sistema en línia de procés per lots, un generador d'imatges per a producció en sèrie, un convertidor de formats d'imatges, etc.

El *GIMP* és ampliable i extensible. Està dissenyat per ampliar-se amb connectors i extensions. La interfície avançada de scripts permet automatitzar des de les tasques més simples fins als procediments més complexos de manipulació d'imatges.

Un dels punts forts del *GIMP* és la seva lliure disponibilitat des de diverses fonts per a molts sistemes operatius. Gairebé totes les distribucions de GNU/Linux inclouen el *GIMP* com una aplicació estàndard. El *GIMP* també està disponible per a altres sistemes operatius com *Microsoft Windows™* o *Mac OS X™(Darwin)* d'*Apple*. El *GIMP* és una aplicació de programari lliure coberta per la Llicència Pública General [GPL](https://www.gnu.org/licenses/gpl-3.0.html). La GPL ofereix als usuaris la llibertat d'accedir i modificar el codi font amb què es construeixen els programes.

📄 [Documentació oficial GIMP](https://docs.gimp.org/2.10/ca/)

---

## 1.6.1 [Finestres principals](https://docs.gimp.org/2.10/ca/gimp-concepts-main-windows.html)

![Finestres principals](https://docs.gimp.org/2.10/ca/images/using/single-window.png)

---

## 1.6.2 El sistema d'ajuda del *GIMP*

L'Equip de Documentació del *GIMP* i altres usuaris us proporcionen la informació necessària per entendre com usar el *GIMP*. El manual d'usuari és una part important d'aquest document. La versió actual es troba en el lloc web de l'Equip de Documentació [GIMP-DOCS](https://www.gimp.org/docs/) en format *HTML*. La versió *HTML* també està disponible com a ajuda contextual mentre es fa servir el *GIMP* prement la tecla `F1`. Es pot accedir a l'ajuda d'elements específics del menú prement `F1` mentre el punter del ratolí enfoca en aquest element.

# Activitat 1: Introducció a GIMP

Per a treballar en classe descarregarem una versió portable de *GIMP*

- [Descàrrega GIMP 2.10.25 AppImage](https://github.com/aferrero2707/gimp-appimage/releases/download/continuous/GIMP_AppImage-git-2.10.25-20210610-x86_64.AppImage)

- Guarda l'arxiu a l'escriptori i dona-li permiso d'execució.

Per a poder seguir les pràctiques usarem la versió 2.10 de *GIMP* i l'idioma en anglés. Com som usuaris avançats utilitzarem la *GIMP* en anglés, ja que la majoria de recursos i tutorials d'Internet utilitzen aquest llenguatge

- Obri *GIMP*, fent doble clic en el fitxer descarregat.
- Ve a `Edit` > `Preferences`, en Interface en l'apartat `Language` posa `English [en_US]`. Haurem de reinicia l'aplicació.

Modo ventana única.  En les últimes versions, per defecte la manera "Finestra única" que integra tots els panells d'eines i edició en una sola finestra.
Però si tenim una configuració antiga emmagatzemada en el nostre perfil d'usuari, pot ser que ens apareguen els panells en finestres separades.

- Ve a `Windows` i comprova que l'opció `Wingle-Window mode` està marcada.

Ara canviarem l'opció de comentari per a posar el nostre nom en les nostres imatges.

- Ve a `Edit` > `Preferences`, en `Default Image` canvia el paràmetre `Comment` i posa el teu **nom i cognoms**.

---

- Descarrega la següent imatge:

![Tower Bridge 4k](img/Tower_Bridge_4K.jpg)

La imatge té unes dimensions de `3840x2160`, aquest tipus d'imatges es diuen ***4k*** perquè la seua amplària està pròxima als 4000 *pixels*.

Anem a canviar la mida de la imatge a 640x360.

- Ve a Image > Scale image... i posa en *Width:* `640` i en *Height:* `360`, la resta d'opcions per defecte.
- Fes clic en `Scale` i espera que termine el process.

Ara la imatge es veurà molt xicoteta, però podem adaptar el zoom.
Podem gastar diverses opcions:

- Tecla `1` per a 100%
- Tecles `+` i `-`
- Usar la roda del ratolí amb la tecla `Ctrl`.
- Anar al menú `View` > `Zoom...`

Ara transformarem la imatge voltejant-la horitzontalment.

- `Image` > `Transform` > `Flip Horizontally`

Guarda els canvis.
- `File` > `Save As...` i posa-li el nom `ud13_act1.xcf`

Exporta la imatge al format `jpg`
- `File` > `Export As...` posa-li el nom `ud13_act1.jpg`
- En `Quality` posa `55`
- En `Comment` posa el teu nom i cognoms

Exporta la imatge al format `png`
- `File` > `Export As...` posa-li el nom `ud13_act1.png`
- Deixa les opcions per defecte.

Lliura els arxius `xcf`, `jpg` i `png` creats.
