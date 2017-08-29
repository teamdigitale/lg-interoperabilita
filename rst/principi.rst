Principi
========

API come un prodotto
--------------------

La visione che si intende perseguire con il Modello di interoperabilità non si
limita a cercare di ottenere una efficace cooperazione applicativa tra i
sistemi delle diverse Amministrazioni ma tenta di trasformare la Pubblica
Amministrazionie in una *piattaforma* [#gaap]_ che fornisce la sua funzioni
amministrativa in forma di servizi che possono essere consumati online.

La conseguenza di questa visione è che ogni Amministrazione dovrebbre
considerare di avere, tra i propri compiti istituzionali, quello di fornire i
propri servizi alle altre amministrazioni.  Tali servizi vanno quindi trattati
come *prodotti*, costruiti per soddisfare i bisogni dei *clienti*.

Per questo motivo le Amministrazioni dovrebbero:

* Creare API che sono facili da capire, facili da scoprire, facili da usare; che 
  siano irresistibili per gli sviluppatori delle altre Amministrazioni;

* Applicare il miglioramento continuo delle loro API, usando i riscontri e i
  suggerimenti che provengono dagli utilizzatori, e allo stesso tempo mantere
  una coerenza sul lungo termine.

* Garantire livelli di servizio e supporto tecnico per gli Utilizzatori

Considerare le API come prodotti è ciò che marca la differenza tra i
tradizionali metodi enterprise e di system integration e le societa innovative
che hanno creato un business sulla piattaforma di API.

Design delle API
----------------

Come raccomandazione generale le API dovrebbero essere centrate sulle entità e i
dati che dovrebbero essere esposti come risorse identificate univocamente
attraverso URI e manipolabili attraverso i metodi standard del cosiddetto schema
CRUD (Crea, Leggi, Modifica, Distruggi), usando messaggi e rappresentazioni
auto-descrittivi.
Si dovrebbe evitare di creare API centrate sul caso d'uso specifico, rimanere
generici e lasciare invece la logica di composizione e utilizzo
all'utilizzatore.

La filosofia qui indicata è tipica dei principi RESTful[#restful]_ che
adotteremo come standard principale nel design delle API, preferendo
rappresentazioni JSON.  
Gli schemi basati su SOAP e XML saranno considerati deprecati.

Un importante principio per il design delle API è la cosiddetta legge di Postel,
anche nota come Principio di Robustezza [#rfc1122]_ :

  Sii liberale in quello che accetti, sii conservativo in quello che fornisci


Principio API-First
-------------------

Al fine di disegnare una API che sia davvero irresistibile per i suoi
utilizzatori occorre far partire il design proprio dalla API, e non dagli
aspetti tecnici implementativi che la sottendono.

Invece di creare una rappresentazione di come un sistema sofware funziona,
costruendo una interfaccia che lo rappresenta, l'API dovrebbe essere creata in
funzione unicamente dei bisogni degli Utilizzatori.

Occorre quindi procedere in questo modo:

1. si definisce l'API usando un linguaggio di specificazione, senza considerare
   il codice che la implementerà;

2. si cerca di ottenere riscontri e suggerimenti dai potenziali utilizzatori o
   da altri Fornitori che hanno disegnato API ben fatte.

3. si procede all'implementazione
   
Si vuole in questo modo cercare di spostare il focus su

* Il dominio che si intende rappresentare e le funzionalità richieste;

* Generalizzazione di entità e risorse, evitando casi d'uso specifici;

* Separazione tra il servizio fornito e il modo in cui è implementato, in modo
  che l'implementazione possa essere cambiata completamente senza alcun impatto
  sull'API e gli Utilizzatori

La definizione formale dell'API facilita l'interazione tra Fornitore e
Utilizzatore eliminando equivoci e incomprensioni e permette la generazione
automatica di documentazione, controlli automatici, interfacce utente.

Grazie alla raccolta di suggerimenti da potenziali Utilizzatori si ha una
relativa sicurezza che una volta completata l'implementazione risponderà ai
loro bisogni e sarà utilizzata.  

D'altra parte è normale che le funzionalità e bisogni evolvano nel tempo e
quindi è possibile che ad un certo punto sia necessario iterare il processo, nel
qual caso si riparte da capo per generare la successiva versione dell'API.


Definizione usando OpenAPI
--------------------------

Per la descrizione delle API utilizziamo lo standard OpenAPI 3.0 (anche noto
come Swagger).  La definizione dell'API viene costruita usando il linguaggio
YAML per maggiore leggibilità.

La specificazione di una API via OpenAPI genera un file che dovrebbe essere
soggetto a controllo di revisione attraverso uno strumento di gestione del
codice sorgente, in modo che sia sempre chiaro a quale versione si sta facendo
riferimento, e deve essere pubblicato dal Fornitore in modo che tutti possano
leggerlo in ogni momento.

Documentare le API
------------------

È buona pratica per il Fornitore mettere a disposizione un Manuale Utente per
l'API per facilitare il lavoro dello sviluppatore che implementerà il lato
client dell'Utilizzatore.  Un Manuale Utente ben fatto descrive questi aspetti:

* Scopo dell'API e principale casi d'uso
* Esempi concreti di utilizzo
* Casi particolari, situazioni di errore, suggerimenti di mitigazione
* Contesto architetturale e dipendenze, complesi diagrammi di sequenza

Il Manuale Utente deve essere pubblicato onine in un sito specifico che il
Fornitore mette a disposizione degli sviluppatori, oppure utilizzando strumenti
di pubblicazione online.  AgID può fornire strumenti e supporto per la
pubblicazione.

Un link al manuale deve essere inserito dentro la definizione OpenAPI, usando la
proprietà externalDocs.


.. [#gaap] Government as a Platform

.. [#restful] Letture consigliate sull'approccio RESTful:
  "Irresistable APIs: Designing web APIs that developers will love"
  "REST in Practice: Hypermedia and Systems Architecture"
  "Build APIs You Won’t Hate"
  "Web APIs: From Start to Finish"
  Lessons-learned blog: Thoughts on RESTful API Design
  Fielding Dissertation: Architectural Styles and the Design of Network-Based Software Architectures

.. [#rfc1122] RFC1122
