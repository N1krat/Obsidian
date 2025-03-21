`Definitie:`
_**Polimorfismul**_ este atunci cand putem utiliza un simbol pentru a indeplini mai multe sarcini. 

In [OOP](OOP.md) _polimorfismul_ este atunci cand noi putem sa dam o interfata sau functional pentru mai multe [clase](Clase.md) (sau subclase) sau tipuri de date. 

---
_Polimorfismul_ este de asemenea proprietatea unei clase, unui obiect, unei substante pentru a avea mai multe forme. 

--- 
#### Tipuri de polimorfism
Exista cateva tipuri de polimorfism: 
- _**Polimorfism dinamic:**_ Este atunci cand noi avem o clasa de baza ce are o metoda ce este redefinita(cu aceleasi parametri) in subclase. <span style="color:rgb(255, 0, 0)">In C++ acest functional este implementat cu ajutorul functiilor virtuale</span>.

- _**Polimorfism parametric:**_ este atunci cand avem mai multe metode cu acelasi nume dar cu un numar/tip de parametri diferiti cea ce si le diferentieaza. ex: 
``` cpp 
complex a, b, c; 
a = b + c; 
a = b + 2.43; 
```

![[Pasted image 20250321092021.png]]

--- 
`Virtual methods and Overriding` 
Daca o metoda din superclasa este una _virtuala_ atunci toate invocatiile metodei din superclasa vor fi dinamice. 

Multe limbaje de programare orientate pe OOP ne permit unei clase sau unui obiect sa modifice implementarea unui aspect (deobicei a unor actiuni) ce este mostenit. Acest proces se cheama _**overriding**_. 
![[Pasted image 20250311235453.png]]

Overrinding-ul ne permite sa facem reuse la codul care poate sa se repete de mai multe ori la noi in program. 
![[Pasted image 20250311235526.png]]

--- 
#### Avantaje si dezavantaje

| Avantaje                                                                                                                             | Dezavantaje                                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1.Permite utilizarea acelorași metode sau clase pentru a gestiona diferite tipuri de date sau obiecte.                               | 1.În timpul execuției, compilatorul trebuie să determine ce metodă trebuie apelată, ceea ce poate încetini programul în comparație cu metodele statice.<br> |
| 2.Odată ce un sistem a fost construit folosind polimorfism, este mai ușor de extins.                                                 | 2.Polimorfismul se bazează pe moștenire și pe alocarea dinamică a memoriei, astfel se poate consuma mai multe resurse (consum mai mare de memorie).         |
| 3.Orice modificare necesară se face într-un singur loc(în superclasă), reducând riscul de erori și făcând debugging-ul mai eficient. |                                                                                     

---
