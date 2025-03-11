`Definitie`
_Ierarhia clasei_ sau _copacul de mostenire_ este clasificarea tipurilor de [obiecte](Obiecte.md), si notarea obiectelor ca instantieri a [claselor](Clase.md). 

Conceptul de iererhie a clasei in computer science este foarte similar cu cel al [taxonomiei](https://en.wikipedia.org/wiki/Taxonomy_(biology)) clasificarii speciilor. 

Ierarhia unei clase poate fi adanca atat cat este necesar. Variabilele si metodele sunt mostenite prin mai multe nivele si pot fi redefinite in corespondenta cu necesitatea in subclase. In general cu cat mai adanc o clasa apare cu atat comportamentul ei este mai specializat. Cand un mesaj este trimis catre un obiect el trece prin copacul de mostenire incepand cu clasa ce primeste obiectul pana cand este gasita o definitie. Acest proces este numit _upcasting_.