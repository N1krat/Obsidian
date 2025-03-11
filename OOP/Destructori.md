`Definitie:`
In [OOP](OOP.md) un _**destructor**_ este o metoda ce este apelata automat atunci cand un [obiect](Obiecte.md) este eliberat din memorie. Acestea sunt utilizati pentru a optimiza resursele consumate de program ce sunt folosite pentru obiecte, precum memoria dinamica sau fisierele deschise. 

_**Destructorii nu primesc valori si nu returneaza nimic in raspuns.**_ 

[Constructorii](Constructor.md) si _destructorii_ sunt fundamentali in ciclul de viata a unui obiect si sunt folosite pentru optimizarea errorilor legate de alocarea sau eliberarea resurselor. 

```cpp
class Clasa { 
	public: 
		// constructor
		Clasa() { 
			// am creat un constructor in care initializam codul
		}

		// destructor 
		~Clasa() { 
			// am creat un destructor cu ajutorul caruia noi curatim memoria
		}
}
```
---

