`Definitie: `
_**Diagramele de cazuri de utilizare**_ UML descriu cea ce face un sistem, nu modul in care functioneaza. La inceputul crearii unui proiect diagramele de cazuri de utilizare pot ajuta la intelegerea actiunilor ce le poate indeplini un _actor_ cum ar fi un utilizator pe o platforma de shopping. 

_Acest tip de diagrama ne ofera: _
- o descriere generala a modului in care va fi utilizat sistemul/produsul/serviciul. 
- furnizeaza un overview la toate functionalitatile pe care trebuie sa le ofere sistemul/produsul/serviciul. 
- arata cum sistemul/produsul/serviciul interactioneaza cu un sau mai multi actori
- asigura ca sistemul/produsul/serviciul va indeplini cea ce noi ne dorim 

---
_**Structura diagramei cazurilor de utilizare:**_
![[Diagrama cazurilor de utilizare.canvas]]

--- 
Intre actori poate exista relatia de generalizare. _Asta este atunci cand un actor mosteneste un alt acotor cea cei da posibilitatea de a comunica cu aceleasi cazuri de utilizare ale sistemului ca si parintele sau_. 

Asta se noteaza cu o sageata cu varful gol. 

![[Pasted image 20250311224158.png]]

---
In cazurile de utilizare pot exista mai multe tipuri de relatii: 

1. _**Incluziune**_ - un caz de utilizare include comportamentul altui caz de utilizare ![[Pasted image 20250311224350.png]]

2. _**Extindere**_ - arata ca un caz de utilizare este inserat in alt caz de utilizare, dar numai in anumite conditii. ![[Pasted image 20250311224442.png]]

3. _**Generalizare**_ - un caz de utilizare mosteneste comportamentul altui caz si il dezvolta ![[Pasted image 20250311224523.png]]

4. _**Asociere**_ - reprezinta o conexiune semantica intre cazurile de utilizare si actori. ![[Pasted image 20250311224608.png]]

_Un exemeplu a cazurilor de utilizare pentru o retea de socializare:_ 
1. Prezentarea tipurilor de utilizatori ![[Pasted image 20250311224645.png]]

2. Actiunea de creare a unui cont nou![[Pasted image 20250311224854.png]]

3. Actiunea de editare a profilului![[Pasted image 20250311224913.png]]

---

