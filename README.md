# Bevezető

GitHub repo a forrásokkal és slide-okkal:
https://github.com/Training360/ ??

## Tematika megjegyzések

### Deprecation Stories

A legmodernebb eszközökkel kezdjük el.
REST már nem túl szeretett.
Sok minden, mint pl. az Open Feign már "deprecated".
Általánosságban nagyon gyorsan elhasználódik a dolgok nagy része...
Domain-Driven Desing kék könyv nem annyira jó ellenben van egy másik könyv a -Distilled postfixű jobb.  
Microservices with Spring Boot and Spring Cloud ISBN 1801072973

### Bemutatkozások

Kolléga:
Moduláris monolit: modulit, lehet, hogy nem is jó rögtön microservice-eket csinálni.
SOA-ból lettek microservice-ek.   
Mondjuk el az előítéleteinket!

# Üzleti tervezés

Agilis fejlesztés -> monitoring -> DevOps (IaC)  
Funkcionális és nem funkcionális követelmények különválasztása

Hogyan képzelem el az alkalmazást?
Egy "Hello World" alkalmazásnál nincsen értelme még microservice-eket alkalmazni. Egy bonyolult alkalmazás kell ehhez a demozáshoz.  
Skills, szerepkör, tanfolyam: entitások... -> Logikai adatmodell, UML: osztálydiagram (statikus nézet), UseCases, ezekből Epics, Stories (UML Distilled book, easy)

## Use Case Diagram

Lényeg: az ügyfél is megértse az ábrát :)

- A rendszer határai
    - Actors (alkalmazott, főnök, HRManager), other systems
- UseCases
   - Beléptetés (alkalmazott)
   - Kurzus (indítás, kiválasztás, jelentkezés, jóváhagyás, teljesítés)
   - Kiléptetés (alkalmazott)

## Event Storming

- Developed by Alberto Brandolini
- Workshop
- Látható lesz, hogy nincsen egy egységes modell -> a domain számára kell egy reprezentáció mindössze.
- Bounded Context: az adott üzleti szakértő mentális modellje. Ne akarjam, mint fejlesztő megváltoztatni az ő nézőpontját. Ezért különböző bounded context-ek lesznek.

## DDD (Domain Driven Design)

1. Strategic design: 
   1. Problem Space (Domains) <-> Solution Space
      1. Sub-Domains: Core (amihez a cég a legjobban ért, a bevételi forrás), Supporting (ezzekkel a Core miatt kötelezően kell foglalkozni), Generic (erre vannak kész megoldások -> 3rd party megoldások)
      2. Bounded Contexts in Solution Space (e.g. HR, kurzus, alkalmazott) és ezek között mapping létrehozása szükséges! Ilyen stratégia van 8 db.