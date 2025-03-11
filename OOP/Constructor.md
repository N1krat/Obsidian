`Definitie:`
In [OOP](OOP.md) un _**Constructor**_ este un tip special de functie ce este chemata pentru a _crea un obiect_. _Constructorii_ prepara obiectele noi pentru utilizare, cel mai des acceptand _argumente_ care sunt folosite pentru a seta variabilele din obiecte. 

Un _constructor_ este asemanator cu o metoda de instanta, dar se difera de metoda prin faptul ca _constructorul nu are nici un fel de return_. Constructorii de obicei au acelasi nume ca si clasa care ii declara. 

Majoritatea limbajelor de programare ne permit sa facem _overloading_ la constructori cea ce inseamana ca noi putem avea mai multi constructori per clasa cu parametri ce se difera. 

---
_Exista 3 tipuri de constructori: _

- _**Constructor parametrizat:**_ este constructorul ce primeste minim un argument. Cand un obiect este initializat in acest tip de constructor, valoarea initiala este transmisa ca argument catre functia constructorului. Ex: 
``` cpp 
class Example { 
	private: 
	float x, y; 
	
	public: 
	Example(int a, int b){ // constructor parametrizat  
		x = a; 
		y = b; 
	}; 
	int sum() { 
	 return x + y; 
	}
};
```

 - _**Constructor default:**_ daca un obiect nu necesita transmiterea sau initializarea acestuia cu ajutorul unui constructor care va primi parametri noi putem folosi un _constructor default_. El nu primeste parametri si este a crea obiecte cu valori predefinite. 
``` cpp
class Exemple { 
	public: 
	float x, y; 
	Exemple(){ // constructor default
		x = 10; 
		y = 2; 
	}
}
```

- _**Constructor de copiere:**_ acest tip de constructor are ca scop copierea valorilor atributelor dintr-un alt obiect existent. Constructorii de copiere sunt metodele standarte de a copia obiecte in C++. 
```cpp
class Example { 
	public: int a; 
	Example(int x) { // constructor cu parametri
		a = x; 
	}
	Example(const Example &obj) { // constructor de copiere
		a = obj.x;
	}
}
```

---
