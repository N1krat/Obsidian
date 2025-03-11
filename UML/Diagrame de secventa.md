`Definitie:`
Este diagrama cu ajutorul careia noi reprezentam interactiunile intre diversi operatori si obiecte si evenimentele pe care le genereaza aranjate dupa timp. Acest tip de diagrame sunt populare in procesele de business si de asemenea la reprezentarea multitaskingului. 

---
Acest tip de diagrama prezinta colaborarea intre mai multe obiecte, mai precis, secventele de mesaje trimise intre acestea pe masura scurgerii timpului. Acestea afiseaza setul de actiuni case se executa _sincron_ sau _asincron_ pentru executarea functionalului unui sistem. 

_**Obiectele**_ - sunt entitatile unei clase
![[Pasted image 20250311231320.png]]

_**Relatiile intre obiecte:**_
- _sincrone_ - ele opresc executarea a procesului atata timp cat se asteapta o confirmare sau un raspuns de la receptor. ![[Pasted image 20250311231547.png]]

- _asincrone_ - sunt mesaje ce nu opresc executarea procesului si nu asteapta un mesaj de raspuns. ![[Pasted image 20250311231647.png]]

- _return_ - sunt mesajele de raspuns a unui apel de operatie (unui mesaj sincron). ![[Pasted image 20250311231739.png]]

---
_**Exemplu de diagrama de secventa:**_
Interacțiunea obiectelor la crearea orarului. Acest drept îl are doar directorul. Întîi de toate el va deschide orarul, iar pentru aceasta, frontend-ul va face cerere la server, pentru a descarca orarul. Mai apoi, în mod asincron se întroduce graficul, constructorul, designerul și perioadă de vacacță. După ce utilizatorul apasă pe salvează, datele se transmit la server, unde se validează. Dacă validare a fost cu succes, datele se inserează în baza de date. În caz contrar, se returnează mesaj de eroare către utilizator
![[Pasted image 20250311231807.png]]

--- 

