`Definitie`
O _**clasa**_ defineste aspectele comune [obiectelor](Obiecte.md) create din acea clasa, de obicei aceste aspecte sunt starea (_atributele sau variabilele_) si comportamentul (_metodele sau functiile_) ce sunt asociate pentru fiecare _obiect_ sau _obiecte_ imparte din acea clasa. 

---
_**Atributele**_ - sunt variabile ce descriu starea obiectului cum ar fi numele, varsta sau pretul. 
_**Metode**_ - sunt functiile ce definesc comportamentul clasei cea ce ne ofera functionalitati cum ar calculul, manipularea sau afisarea atributelor. 

![[Pasted image 20250311211035.png]]

--- 
Clasele au _**modificatori de acces**_. 
_Modificarea de acces_ sunt elementele de baza a unei clase ei au ca scop controlarea vizibilitatii si accesul la atributele si metodele din din clase. In C++ exista trei tipuri de modificatori de acces.

_**Private**_ - Atributele si metodele marcate cu acest modificator pot fi accesate doar din interiorul clasei in care sunt definite. Acestea nu sunt accesibile din exteriorul clasei, ceea ce protejeaza datele de modificari necontrolate
_**Public**_ - Membrii declarati public sunt accesibili din orice parte a programului. Acesta este cel mai des folosit in situatii cand avem metode sau atribute ce au ca scop principal comunicarea cu utilizatorul cum ar fi citirea datelor de intrare. 
_**Protected**_ - Membrii protejati sunt accesibili doar in cadrul clasei si al claselor derivate (prin [mostenire](Mostenire.md)). Acest modificator este util in cazul cand avem _mostenire_ intre clase si este necesar sa avem niste atribute intre ele dar ascunse in afara acestora. 

_Modificatorii de acces_ asigura implementarea [incapsularii](Incapsularea.md) cea ce ne garanteaza ca datele interne ale unui obiect nu pot fi modificate sau accesate direct fara controlul clasei. 

![[Pasted image 20250311211733.png]]

---

