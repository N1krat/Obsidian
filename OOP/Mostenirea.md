`Definitie:`
In OOP _mostenirea_ este un mecanism de bazare a unui [obiect](Obiecte.md) sau [clase](Clase.md) pe alt obiect sau clasa. De asemenea derivarea unei clase noi (_subclasa_) de la una existenta (_clasa de baza sau super clasa_) si formarea unei iererhii intre clase. 

---
_Constructorii_ si _destructorii_ sunt functii membre ce <span style="color:rgb(255, 0, 0)">nu se mostenesc</span>. 

La instantierea unui obiect din clasa derivata se apeleaza mai _intai constructorii_ claselor de baza in ordinea in care acestia apar in lista de declarare a clasei derivate. 

La distrugerea obiectelor se apeleaza mai _intai destructorul_ clasei derivat, apoi destructorii claselor de baza. 

--- 
O clasa mostenita se numeste _subclasa_ a parintelui sau _super clasei_. 

_**Exista mai multe tipuri de mostenire:**_
1. <span style="color:rgb(255, 255, 0)">Single inheritance</span> (mostenire singura): este atunci cand numai o singura subclasa mosteneste proprietatile unei superclase. O clasa primeste proprietatile altei clase.
![[Pasted image 20250311233309.jpg]]

2. <span style="color:rgb(255, 255, 0)">Multiple inheritance</span> (Mostenire multipla): este atunci cand o clasa mosteneste proprietatile de la mai multe superclase de la care va mosteni proprietatile. 
![[Pasted image 20250311233612.jpg]]

3. <span style="color:rgb(255, 255, 0)">Multilevel inheritance</span> (Mostenire de multe niveluri): este atunci cand avem o subclasa mosteneste proprietatile de la alta subclasa care mosteneste proprietatile de la clasa parinte. 
``` cpp
// implementarea in C++
class A { ... }; // clasa de baza
class B : public A { ... }; // B este derivat de la A
class C : public B { ... }; // C este derivat de la B
```
Acest proces poate fi marit pana orice numar de nivele. 

![[Pasted image 20250311234240.jpg]]

--- 
`Subclasele si superclasele:`
_Subclasele_ sunt preiau una sau mai multe entitati de la una sau mai multe clase numite _superclase sau clase de baza_. 

``` cpp
class SubClass: visibility SuperClass { 
	// membrii subclasei
};
```
- Colonoana ( _:_ ) indica ca subclasa mosteneste superclasa. Vizibilitatea este optionala dar ea poate fi _private_ sau _public_. Valoarea default este _private_. Vizibilitatea specifica ce proprietati a clasei de baza subclasa va mosteni cele private sau publice. 

--- 
