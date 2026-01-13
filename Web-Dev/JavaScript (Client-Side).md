Cand deabia se dezvolta web-ul toate paginile erau de tip _static_, si nu aveau posibilitatea de a fi modificate in timp real numai dupa un refresh total al paginii. Iar tot lucrul cu datele erau procesate pe server. Aceasta o dus la limitari cum ar fi: slow response time, poor UX and poor server utilizations and optimizations. 

Taman pentru asta o fost creat limbajul de programare _JS_ ce ne permite executarea codului direct in web browser, care avea ca scop: 
- adaugarea interactivitatii in pagina noastra 
- crearea a SPA's sau dynamic web pages
- adaugarea unor reactii la actiunile user-ului

_**JS**_ - este un limbaj de programare de tip scripting ( de la care deja so derivat si [TypeScript](TypeScript.md) ) interpretat si utilizat in majoritate in [web dev](Web%20Development.md) pe partea de client sau de server (depinde deja de cerintele proiectului). 

_**Caracteristicile Principale a JS:**_
- El nu este compilat cea ce ajuta pentru un performance mai rapid  deoarece noi nu pierdem timp pe compilare 
- El este compatibil cu toate browserele moderne cea ce ne da posibilitatea de a crea proiecte ce vor lucra pentru mai multe platforme simultan fara optimizari adaugatoare. 
- Este _case sensitive_
- Ruleaza direct in browserul user-ului
- Este orientat pe evenimente ce pot fi create din motivul unor actiuni specifice pe care user-ul lea facut sau ceva ce o facut pagina in sine.

Rolul a _**JS**_ in Web proiecte moderne este de a controla comportamentul paginilor prin adaugarea unor structuri logice sofisticate. Pana cand HTML sau CSS creaza corpul si look-ul paginii noastre. 

_**JS**_ este responsabil pentru: 
- afisarea mesajelor dinamice 
- validarea si interactiune cu formulare 
- evenimente la actiuni (click, drag, etc)
- modificarea continutului in live fara a face refresh la pagina

---
# JS Client-Side

_**JS Client-Side**_ este: 
- executat in browser 
- este descarcat impreuna cu pagina web
- este interpretat de modulul JS din browser 

![[Acrobat_XjvoDY3pa8.png]]

Codul _**JS**_ poate fi integrat in pagina prin mai multe metode cum ar fi: 
- _JavaScript inline_ - este codul ce este scris direct in atributele componentelor HTML. Asta are mai multe dezavantaje cum ar fi: <span style="color:rgb(255, 0, 0)">codul neorganizat, greu de intretinut in proiecte complexe, este un haos in cod</span>. 
- _JavaScript intern_ - este codul ce este scris in etichetele <script></script> din HTML. El este mai clar si comod daca este necesar sa avem scripturi mici in pagina pentru o logica adaugatoare. 
- _JavaScript extern (recommended)_ - este codul scris in fisier aparte cu formatul _**.js**_. Acest tip are cele mai mari avantaje cum ar fi: cod ce poate fi reutilizat mai ales daca cream functionalitati ce sunt reutilizate in mai multe pagini, separarea dintre _looks of the page_ de _logic of the page_, si de asemenea crearea unei structuri mai clare ce este mai usor de intretinut kinda. 

---
# JS functionalities 

In _**JS**_ noi avem conceptul de _**instructiune**_. 

O _**Instructiune**_ reprezinta o comanda pentru browser care ii spune browserului ce sa faca ! Dar totul depinde de context deoarece o instructiune poate fi diferita de sarcina noastra !.

_Variabilele_ in _JS_ pot fi declarate prin intermadiul: 
- _**let**_ - valoare ce poate fi modificata mai departe in codul nostru. Des pentru variabile simple ce sunt modificate anterior. 
- _**const**_ - valoare constanta ce nu poate fi modificata dupa. Des utilizate pentru variabile ce trebuie sa aiba valori unice. 

Un avantaj foarte mare a _JS_ este interactiunea si lucrul cu [DOM](DOM.md) prin intermediul a diversor elemente HTML cum ar fi: pop-ups, confirmation tabs, data input, etc. 

---
# JS in modern context 

_**JS**_ in contextul modern este unul din cele mai utilizate limbaje de programare din motivul a compatibilitatii sale cu aproape toate platformele moderne in web si de asemenea _Native_ prin intermediul frame-work-urilor speciale pentru a crea proiecte pentru diferite OS cum ar fi _React Native_ unul din cel mai populari reprezentanti. 

_JS_ sta la baza a asa proiecte cum ar fi: 
- Web browser games
- Hybrid mobile projects
- Modern Web apps
- Dynamic Interfaces 

---
Fara _**JS**_ nu ar lucra aproape toate paginile web sau ele ar fi la acelasi nivel primitiv. 