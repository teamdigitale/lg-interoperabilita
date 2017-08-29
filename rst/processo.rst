Elementi di Processo
====================

Parte integrante del Modello di interoperabilità sono i processi che permettono
di gestire in maniera ordinata la collaborazione tra i vari attori partecipanti
all'ecosistema.

Schema di governance
--------------------

Gli attori che partecipano al Modello di interoperabilità sono:

Fornitori:
   Sono Amministrazioni che mettono a disposizione una funzionalità attraverso
   una API, al fine di permettere a altre Amministrazioni l'utilizzo.  
   Sono responsabili della conduzione del servizio che mettono a disposizione.

Utilizzatori:
   Utilizzano l'API messa a disposizione di un Fornitore al fine di costruire un
   servizio per il cittadino.  Sono responsabili di un uso corretto delle API
   che non violi i termini di utilizzo pubblicati dal Fornitore..

AgID:
   Gestisce l'Ecosistema pubblicando il Modello e uno schema di accordi tipo
   validi per Fornitori e Utilizzatori.  Fornisce alcuni componenti centrali
   utili per il funzionamento dell'Ecosistema.  

Garante della Privacy:
   Controlla che le interazioni tra Fornitori e Utilizzatori siano conformi alla
   normativa sulla protezione dei dati personali in particolar modo verificando
   che gli Utilizzatori abbiano chiesto l'accesso solamente alle informazioni di
   cui hai hanno necessità per l'espletamento dei loro compiti istituzionali.

Di norma le Amministrazioni sono contemporaneamente Fornitori e Utilizzatori.

Processi di onboarding
----------------------

Al fine di avere accessso all'Ecosistema, Fornitori e Utilizzatori sottoscrivono
un accordo con AgID in virtù del quale si impegnano a rispettare le regole del
Modello.
Il testo dell'accordo è standardizzato, uguale per tutte le Amministrazioni, ed
è stabilito da AgID.
L'accordo definisce tra le altre cose i seguenti elementi:

TBD: inserire qui gli elementi

L'accordo viene firmato una sola volta e per gli Utilizzatori permette l'accesso
alle API pubblicate da tutti i Fornitori presenti, seguendo un processo formale
gestito completamente online, mentre per i Fornitori permette la pubblicazione
di un numero illimitato di API

Pubblicazione delle API
-----------------------

Per ottenere la pubblicazione di una API il Fornitore accede ad uno strumento
online messo a disposizione da AgID e, in modalità self-service, descrive i
parametri di funzionamento e la locazione logica del servizio.
Tra le altre cose il Fornitore dichiara:

* Il nome e la descrizione dell'API

* I riferimenti dei responsabili della conduzione dell'API (riferimento legale,
  riferimento tecnico, contatti per il supporto, processo di escalation)

* Livelli di servizio quali orari, disponibilità garantita, tempi di intervento
  in caso di guasto.

* Capacità del sistema in termini di numero di richieste per unità di tempo che
  è in grado di gestire per ogni Utilizzatore

* Termini e condizioni per l'utilizzo

* Schema formale dell'API con sintassi di invocazione, parametri di input,
  formati di output.

A valle di controlli formali l'API viene automaticamente pubblicata in un elenco
di API che sono a disposizione degli Utilizzatori.

A posteriori, AgID può eseguire controlli di qualità sulle API pubblicate e
nel caso sia opportuno, stabilire con il Fornitore un eventuale percorso di
adeguamento a degli standard minimi o la rimozione dell'API dall'elenco.

Accesso alle API
----------------

Per ottenere l'accesso l'Utilizzatore consulta l'elenco delle API disponibili
e, scelta l'API che desidera utilizzare, compila un modulo online dichiarando
per quale tipo di utilizzo richiede l'accesso, secondo quali profili di carico. 

Solo il Garante della Privacy può decidere di approvare o negare l'accesso
richiesto secondo le modalità descritte in seguito.

I Fornitori non possono opporsi all'accesso di un Utilizzatore se non per
proteggere il loro sistema da tentativi di violare la sicurezza o da picchi di
richieste che possano avere impatto sulle prestazioni e la stabilità.

Al termine del processo di autorizzazione l'Utilizzatore ottiene dal sistema una
chiave di accesso generata in automatico la quale permette al Fornitore di
riconoscere in maniera univoca tutte le richieste pervenute da un certo
Utilizzatore.

Interazione con Garante Privacy
-------------------------------

Al Garante della Privacy viene fornita una mappa completa e sempre aggiornata di
tutte le API disponibili e di tutti gli accessi richiesti dagli Utilizzatori,
che viene mantenuta in un database sotto il controllo di AgID.

Viene inoltre fornito un elenco di tutte le richieste di utilizzo recentemente
pervenute, che il Garante può approvare con un semplice processo one-click.

Ciclo di vita delle API
-----------------------

Le API pubblicate possono subire modifiche.  Al fine di non compromettere il
funzionamento delle applicazioni costruite dagli Utilizzatori, i Fornitori si
impegnano a mantenere funzionante una API in una certa versione per un periodo
certo (non inferiore a un minimo stabilito da AgID) e dichiarato in anticipo.
Il sistema di controllo fornito da AgID permette agli Utilizzatori di definire
una API come *deprecata* e di comunicare fino a quale data il funzionamento di
questa API sarà garantito nella modalità attuale e/o di comunicare altre
variazioni che saranno applicate.


