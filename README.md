# Poređenje performansi Dijkstrinog algoritma implementiranog s binarnom i Fibonacci gomilom

Ovaj repozitorij sadrži implementaciju i eksperimentalnu analizu Dijkstrinog algoritma korištenjem dvije različite strukture podataka za prioritetni red: *binarne gomile* i *Fibonaccijeve gomile*. Cilj projekta je empirijski ispitati kako se teorijske prednosti Fibonacci heapa odražavaju na praktične performanse algoritma na grafovima različite veličine i gustine.

Projekat je realizovan u okviru predmeta *Napredni algoritmi i strukture podataka (NASP)*.

---

## Opis projekta

Dijkstra algoritam je jedan od najčešće korištenih algoritama za pronalaženje najkraćih puteva u grafovima sa nenegativnim težinama. Njegova vremenska složenost u velikoj mjeri zavisi od strukture podataka koja se koristi za implementaciju prioritetnog reda.

U ovom projektu implementirane su dvije verzije algoritma:
- Dijkstra algoritam sa *binarnom gomilom*, korištenjem Pythonove standardne biblioteke heapq
- Dijkstra algoritam sa *Fibonaccijevom gomilom*, implementiranom od nule sa podrškom za operaciju decrease-key

Cilj je poređenje vremena izvršavanja ovih implementacija u različitim uslovima.

---

## Implementacija

Cjelokupna implementacija projekta nalazi se u jednom *Jupyter/Google Colab notebooku* (.ipynb), koji sadrži:
- implementaciju Dijkstrinog algoritma sa binarnom gomilom,
- implementaciju Fibonaccijeve gomile i Dijkstrinog algoritma zasnovanog na njoj,
- funkcije za generisanje nasumičnih, povezanih, ponderisanih grafova,
- kod za izvođenje benchmark testova,
- generisanje tabela i grafičkih prikaza rezultata.

Korištene biblioteke i alati:
- *Python 3*
- *NetworkX* (generisanje i rad s grafovima)
- *heapq* (binarna gomila)
- *pandas* (obrada rezultata)
- *matplotlib* (vizualizacija)
- *tqdm* (praćenje toka izvršavanja)
- *Google Colab / Jupyter Notebook*

---

## Metodologija testiranja

Testiranje je izvršeno nad nasumično generisanim, povezanim, ponderisanim grafovima različitih veličina i gustine:
- *Rijetki grafovi*, gdje je broj grana približno proporcionalan broju čvorova,
- *Gusti grafovi*, gdje broj grana znatno premašuje broj čvorova.

Za svaku konfiguraciju grafa:
- izvršene su obje implementacije algoritma,
- mjereno je ukupno vrijeme izvršavanja,
- testovi su ponovljeni više puta,
- provjerena je korektnost rezultata poređenjem dobijenih udaljenosti.

---

## Rezultati

Rezultati testiranja pokazuju da se teorijska prednost Fibonaccijeve gomile ne mora nužno preslikati u praktične performanse. Iako Fibonacci heap ima povoljniju asimptotsku složenost, binarna gomila se u praksi pokazala kao vrlo konkurentno, a često i brže rješenje za posmatrane veličine grafova.

Rezultati su prikazani kroz:
- tabelarni prikaz izmjerenih vremena,
- grafove poređenja vremena izvršavanja za rijetke i guste grafove.

---

## Pokretanje

Notebook je namijenjen za pokretanje u *Google Colab-u* ili lokalno kroz *Jupyter Notebook*.  
Sve ćelije su organizovane tako da se kod može izvršavati sekvencijalno bez dodatne konfiguracije.

---

## Autori

- *Berina Zejnilović*  
  Elektrotehnički fakultet, Univerzitet u Sarajevu  

- *Naida Bošnjović*  
  Elektrotehnički fakultet, Univerzitet u Sarajevu  

---

## Napomena

Ovaj repozitorij predstavlja studentski projekat i služi u edukativne i istraživačke svrhe.
