# Braț Robotic Universal Robots: Construire Piramidă și Vopsire Cub

Acest proiect implică programarea unui braț robotic Universal Robots (UR5) pentru a executa două sarcini complexe și distincte: construirea unei piramide din cuburi și vopsirea suprafeței superioare a cubului final al acestei piramide. Proiectul demonstrează controlul precis al mișcărilor robotului, utilizarea unui gripper, gestionarea coordonatelor și implementarea unei logici programatice modulare, fiind dezvoltat și testat în simulatorul URSim.

---

## Scopul Proiectului

Scopul principal al acestui proiect este de a dezvolta un program robust și modular pentru un braț robotic UR5, capabil să execute sarcini de manipulare (construirea unei structuri) și sarcini de proces (vopsirea unei suprafețe). Obiectivele vizează explorarea capacităților de programare a roboților industriali, gestionarea preciziei mișcărilor, optimizarea traiectoriilor și asigurarea siguranței operaționale, toate acestea fiind demonstrate și validate într-un mediu de simulare.

---

## Descriere Generală și Funcționalități

Programul robotului UR5 oferă următoarele funcționalități cheie:

- Construire Piramidă Modulară: Robotul preia succesiv cuburi și le plasează în locații precise pentru a construi o piramidă pe mai multe straturi (de ex., 3 straturi).
- Vopsirea Suprafaței Superioare: După construirea piramidei, robotul preia un marker și vopsește o traiectorie predefinită (ex., o spirală sau un pătrat) pe suprafața superioară a cubului final.
- Manipulare Obiecte cu Gripper: Utilizează un gripper (simulator) pentru a prelua și plasa cuburile și markerul cu precizie.
- Mișcări Precise și Controlate: Toate mișcările robotului sunt programate pentru a fi fluide, evitând coliziunile și asigurând stabilitatea structurii.
- Structură Modulară a Programului: Codul este organizat în subprograme distincte pentru fiecare fază (construire, vopsire, poziționare inițială), facilitând dezvoltarea și depanarea.
- Simulare Completă: Întregul proces este simulat în mediul URSim pentru validare și ajustări înainte de implementarea pe un robot fizic.

---

## Tehnologii și Instrumente Utilizate

Acest proiect a fost dezvoltat și testat folosind:

- URSim (Universal Robots Simulator): Un simulator software esențial pentru Universal Robots, care permite dezvoltarea și testarea programelor fără a necesita un robot fizic. Rulează într-un mediu virtual.
- Brațul Robotic Universal Robots (UR5): Robotul industrial real (sau modelul simulat al acestuia) pentru care a fost conceput programul.
- Limbajul Polyscope / Script UR: Limbajul de programare specific Universal Robots, utilizat pentru a scrie logica de control și secvențele de mișcare ale robotului.
- Oracle VirtualBox: Platforma de virtualizare folosită pentru a rula mediul URSim.

---

## Logica Programului și Realizarea Proiectului

Proiectul este structurat modular pentru a facilita gestionarea complexității. Logica programului este împărțită în subprograme distincte:

1. move_to_home(): Subprogram pentru poziționarea inițială și sigură a brațului robotic
2. build_pyramid(): Secvență complexă pentru construirea piramidei:
Calculează dinamic coordonatele de preluare și plasare pentru fiecare cub, pe fiecare strat
Include mișcări de siguranță (pre-pick, post-place) pentru a evita coliziunile
Gestionarea gripper-ului (deschidere/închidere) pentru a prinde și elibera cuburile
3. paint_cube(): Secvență pentru vopsirea suprafeței superioare a cubului final:
Mișcări precise pentru a prelua markerul
Traiectorie definită (ex: spirală sau linii) pentru a acoperi suprafața
Mișcări de siguranță pentru a repoziționa markerul
Programul principal apelează aceste subprograme într-o ordine logică pentru a executa sarcina completă

---

## Simulare și Validare

Întregul program a fost testat și validat extensiv în simulatorul URSim. Acest proces a fost crucial pentru:

- Ajustarea Coordonatelor: Determinarea precisă a punctelor de preluare și plasare pentru fiecare cub, asigurând stabilitatea piramidei
- Verificarea Logicii: Asigurarea că secvențele de construire și vopsire rulează corect și fără erori
- Prevenirea Coliziunilor: Testarea mișcărilor robotului în spațiul de lucru pentru a evita orice coliziune cu mediul sau cu structura construită
- Sincronizare Mișcări-Gripper: Asigurarea unei sincronizări perfecte între mișcările brațului robotic și acțiunile gripper-ului
- Simulările au confirmat funcționalitatea și robustețea soluției propuse, pregătind programul pentru o eventuală rulare pe un robot fizic

---

## Rulare și Utilizare

Pentru a rula și testa programul robotului în simulator:

1. Instalați Oracle VirtualBox: Descărcați și instalați VirtualBox de pe site-ul oficial.
2. Instalați URSim: Descărcați imaginea URSim (de la Universal Robots) și configurați o mașină virtuală în VirtualBox.
3. Porniți URSim: Lansați mașina virtuală URSim.
4. Descărcați fișierele Proiectului: Clonați acest repository sau descărcați fișierele proiectului (în special fișierul .script) în mașina virtuală URSim.
5. Încărcați Programul: În interfața Polyscope a URSim, navigați la secțiunea "Program" și încărcați fișierul .script al proiectului (e.g., [nume_program_robot.script]).
6. Rulați Simularea: Asigurați-vă că mediul de simulare este setat corect (cu cuburi, marker etc.) și apoi rulați programul pentru a observa comportamentul robotului.

---

## Capturi

Mai jos sunt câteva capturi de ecran din simulatorul URSim, ilustrând etapele de construire a piramidei și secvența de vopsire.

Spațiul de lucru al simulatorului URSim:

![vedere_ursim](https://github.com/user-attachments/assets/6f9e650d-82f7-465c-a571-9752eabed9d2)


Robotul în timpul construirii piramidei:

![piramida](https://github.com/user-attachments/assets/a7a21897-9d93-4d64-8702-b7b1bab86177)


Secvența de vopsire a cubului final:

![vopsire](https://github.com/user-attachments/assets/19f2da57-9d27-4a35-bcff-ce68b9ca85da)

---

## Realizat de

Proiect realizat de [bogdanch7](https://github.com/bogdanch7)

An universitar 2024–2025

---

## Licență

Acest proiect este creat pentru uz educațional.
