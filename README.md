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
 
