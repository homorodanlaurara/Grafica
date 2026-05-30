# Cimitirul de Tehnologie Veche (Mini-Scena 3D)

## Descrierea Proiectului
Acest proiect reprezinta o mini-scena 3D construita pentru a ilustra o tema post-apocaliptica. Scena infatiseaza ramasitele unei tehnologii uitate – un monitor CRT stricat si o unitate PC rasturnata, abandonate in intuneric. 

Pentru a da viata scenei, am implementat un efect dinamic: ecranul monitorului palpaie neregulat (flicker effect), emitand o lumina verde care interactioneaza cu mediul inconjurator.

## Tehnologii Utilizate
* **HTML/CSS:** Pentru structura de baza si afisarea canvas-ului pe tot ecranul (fullscreen).
* **JavaScript:** Limbajul principal folosit pentru logica aplicatiei.
* **Three.js (WebGL):** Libraria principala pentru randarea graficii 3D in browser.
* **OrbitControls.js:** Un modul din Three.js folosit pentru a permite utilizatorului sa interactioneze cu scena (rotire cu click-stanga, zoom cu scroll).

## Elemente Tehnice Implementate
1. **Geometrii si Grupuri:** Am folosit `BoxGeometry` si `Group` pentru a construi monitorul din mai multe piese distincte (carcasa si ecran). Pentru pietre/ruine am folosit `DodecahedronGeometry` pentru a obtine un aspect "low-poly".
2. **Iluminare:** * `AmbientLight` pentru o vizibilitate de baza.
   * `DirectionalLight` care simuleaza lumina lunii si genereaza umbre (`castShadow`).
   * `PointLight` atasat de monitor pentru lumina verde care se rasfrange pe pamant.
3. **Materiale:** Am utilizat `MeshStandardMaterial` deoarece reactioneaza la lumina. Proprietatea `emissive` a fost folosita pentru a face ecranul sa lumineze singur.
4. **Generare Procedurala:** Ruinele sunt generate si imprastiate aleatoriu in scena folosind `for` si functii trigonometrice (`Math.cos`, `Math.sin`).

## Imagine
<img width="1871" height="944" alt="miniscena" src="https://github.com/user-attachments/assets/359c4e11-38ea-4d24-93db-a86f5ab3efd4" />
<img width="1734" height="707" alt="miniscena2" src="https://github.com/user-attachments/assets/6610ad13-f2bc-43fd-86d4-1e722f35d2b0" />
