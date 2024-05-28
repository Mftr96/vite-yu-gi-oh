CONSEGNA
Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.

 MILESTONE 1
Dopo aver creato il progetto ragionate sui componenti e cercate di ricalcare quanto visto nei live coding di oggi e venerdì.
Come dati utilizzate l'array in allegato. Potete incollarlo nel vostro data, oppure importare il file come visto oggi.
Avrete un componente padre (es. CardsList) che dichiara l'array nel data e vi cicla per passare il singolo dato al figlio (es. SingleCard) tramite le sue props.

 MILESTONE 2
Spostate i dati in questione in uno store.js, all'interno di un array che chiamerete ad esempio carte.
Il componente padre (es. CardsList) richiama store.carte e vi cicla per passare il singolo dato al figlio (es. SingleCard).
Vi chiederete cosa cambia rispetto a prima? Cosa ci guadagno? Nulla! Ma ci tornerà utile per bonus con axios :

BONUS
Recuperate questi dati tramite una chiamata axios da effettuare al mount dell'applicazione.
Per oggi possiamo importare axios tramite CDN, come al solito.
Questa chiamata andrà a scrivere su store.carte che quindi dovrà essere dichiarato come array vuoto nello store.js
L'api da richiamare si trova qui.
:regalo: BONUS #2
L'indirizzo che vi ho fornito stampa solo le prime 10 carte. Se volessi visualizzare le prime 20 carte? Oppure le prime 20 carte a partire dalla 15esima? Guardate bene l'indirizzo e fate qualche prova :occhiolino:
Qui trovate anche la documentazione delle API se volete capire bene quali dati aspettarvi.
:razzo: CONSIGLI
Ragionate bene sul da farsi e seguite con attenzione le milestone. Può aiutarvi un'occhiata al codice del live coding.
Buon lavoro a tutti!
--------------------------------
esecuzione:

milestone 1:creare elementi necessari al progetto
al progetto serve:
-un file store.js da mettere in una cartella data. Il file avrà al suo interno l'array dato in traccia fatto
due componenti vue(CardList e SingleCard) creato

-dopo la creazione degli elementi necessari, andare a ricreare il mockup servendosi dei components.
In questo caso, bisogna avere chiaro lo schema per ricreare il mockup, quindi avere chiaro come strutturare il container mettendo in fila le carte e come ciclare sulla carta capendo come disporre gli elementi della carta.
cosa mi serve:
-div container in CardList fatto
-struttura carta in SingleCard()fatto
-creazione ciclo v-for per stampare le carte fatto
come ciclo?
ciclo sulla carta singola e poi inserisco in pagina(fare domanda a lezione in caso su come ciclare da padre e passare il componente di CardList a SingleCard del ciclo)
-------------------------
bonus 1:
andare a richiamare tramite axios l'API e stampare l'array e ciclare con l''array nuovo
cosa mi serve
-link axios in HTML fatto
-scrivere funzione axios nel mounted di app.vue
------------------------------------------------------------------------------------------ 
CONSEGNA SECONDO ES


CONSEGNA
Continuate a lavorare nella stessa repo di ieri. Oggi gli obiettivi sono:
richiamare le card tramite axios (per chi non avesse fatto il bonus di ieri)    /FATTO
aggiungere una select per filtrare i risultati in base all’archetipo


 MILESTONE 0
Assicuratevi di aver completato la consegna di ieri inclusi i bonus: dovrete avere le cards all'interno di un array dello store. Questo array va popolato grazie ad una chiamata axios fatta al caricamento di App.vue.


 MILESTONE 1
Aggiungete una select in pagina per scegliere l'archetipo.
La select dovrà essere direttamente in App.vue e non in un componente.
Le options della select verranno popolate dinamicamente, grazie a un array contenente tutti gli archetipi.
Dove prendo gli archetipi? Con un'altra chiamata, sempre al caricamento di App.vue ma a questo endpoint. I dati vanno sempre nello store.

 MILESTONE 2
Quando l'utente seleziona un valore dalla lista, dovrete aggiornare la lista di cards che avete in store.
Vuol dire che effettuerete una chiamata alle API (simile a quella iniziale) ma con l'archetipo selezionato.

BONUS
Creare un componente che mostri il numero totale di risultati ottenuti.
-------------------
milesone 1:
creazione del select nell'app principale(app.vue)e creazione tramite ciclo delle option tramite chiamata axios(installare axios con npm).
cosa serve:
-axios installato tramite npm
-creazione tag select in app.vue
-ciclo tag option con dentro l'archetipo delle carte 
