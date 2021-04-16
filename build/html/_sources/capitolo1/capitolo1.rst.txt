Sistemi di Riferimento di Coordinate
====================================

La posizione geografica è l'elemento che distingue i dati spaziali da tutti gli altri tipi di informazioni, quindi i metodi per specificare le posizioni sulla superficie terrestre sono essenziali per il GIS.
Per comprendere i dati GIS e i dati spaziali dobbiamo tenere a mente come vengono stabiliti i sistemi di riferimento delle coordinate (CRS) per la Terra e come vengono misurate le coordinate sulla superficie terrestre.

Le coordinate sono serie di numeri che definiscono inequivocabilmente le posizioni, ciascuno di questi valori è "unico" per un dato punto solo per un insieme specificato di misurazioni e ipotesi di calcolo.
Un sistema di coordinate utilizzato a scuola è il sistema di coordinate cartesiane bidimensionale dove è presente una coppia di assi perpendicolari e il punto di incontro degli assi si chiama origine, mentre gli assi orizzontale e verticale sono chiamati X e Y.
Le coordinate di un punto (x, y) sono espresse come la sua distanza euclidea dagli assi X e Y.
Visto che la Terra è uno spazio tridimensionale e curvo abbiamo bisogno di un sistema di coordinate geografiche.

Un sistema di coordinate geografiche è un sistema di riferimento tridimensionale ed è utilizzato per individuare punti sulla superficie terrestre e si basa sulla rotazione della Terra attorno al suo centro di massa e sulla forza di gravità.
Il piano che attraversa il centro di massa, perpendicolare all’asse di rotazione, definisce l’equatore.
Ogni punto nel sistema di coordinate geografiche ha due valori di coordinate: latitudine e longitudine. 
La latitudine e la longitudine misurano gli angoli e la loro unità di misura e il grado decimale e sono simboleggiate con le lettere phi(φ) e lamba(λ).

La latitudine di un punto è definita come l’angolo formato dall’intersezione di una linea perpendicolare alla superficie di riferimento della Terra nel punto e il piano dell’equatore.
I punti a nord dell'Equatore hanno valori di latitudine positivi, mentre i punti a sud hanno valori negativi. I valori di latitudine vanno da -90 a +90 gradi.
Le linee di latitudine sono anche chiamate "parallele".

Il valore di longitudine è definito dall’angolo tra la piano che attraversa i poli e un piano di riferimento. 
Le linee di longitudine sono chiamate “meridiani” e il piano di riferimento è identificato dal primo meridiano che è tradizionalmente riconosciuto con il meridiano che passa per Greenwich (Regno Unito). 
I valori di longitudine vanno da -180 a +180 gradi.

La migliore descrizione della forma della Terra è fornita dal geoide che risulta da modelli fisici complessi e descrive la superficie di uguale gravità formata dagli oceani e la sua estensione sotto i continenti. 
Negli ultimi secoli si è cercato di trovare un ellissoide che si avvicini alla forma della Terra. Di conseguenza, molti ellissoidi diversi sono stati definiti in base al loro applicazione su scala locale o globale.
L'ellissoide noto come WGS84 (World Geodetic System del 1984) è attualmente il dato geodetico globale più ampiamente accettato ed è quello utilizzato, ad esempio, dal Global Positioning System (GPS). 

.. figure:: /immagini/1/1.png
   :alt: Sistemi di Riferimento
   :align: center


Proiezioni
----------

La rappresentazione di informazioni geografiche e mappe su superfici piane (monitor o carta) richiede la trasformazione delle posizioni dalla superficie curva della Terra a posizioni bidimensionali su un piano cartesiano piatto. Ciò può essere ottenuto utilizzando metodi matematici noti come proiezioni.

La migliore proiezione per una mappa dipende dalla scala della mappa e dagli scopi per cui verrà utilizzata. Considerando gli scopi della mappa, le proiezioni devono essere accuratamente selezionate al fine di preservare o distorcere le proprietà geometriche sulla base dell’utilizzo. 
Le proiezioni cartografiche possono quindi essere classificate in base a queste proprietà:

* Le proiezioni conformi preservano la forma locale mantenendo la stessa scala in qualsiasi direzione per qualsiasi posizione della mappa. Meridiani e paralleli si intersecano ad angolo retto. Ciò si ottiene mantenendo tutti gli angoli. Lo svantaggio di ciò è che l'area della superficie può essere notevolmente distorta. Un esempio popolare di proiezione di mappe conformi è la proiezione di Mercatore.
* Le proiezioni di area uguale preservano l'area degli elementi visualizzati; quindi tutte le aree mappate hanno la stessa relazione proporzionale alle aree che rappresentano sulla Terra. Ciò si ottiene distorcendo le altre proprietà spaziali di forma, angolo e scala. Nelle proiezioni di area uguale, i meridiani e i paralleli potrebbero non intersecarsi ad angolo retto. Un esempio popolare di proiezione cartografica di area uguale è la proiezione di Mollweide.

Sono disponibili anche altri tipi di proiezioni come le proiezioni equidistanti che preservano le distanze tra i punti e le proiezioni a distanza reale che rappresentano correttamente le direzioni angolari rispetto al centro della mappa.

.. figure:: /immagini/1/2.png
   :alt: Proiezioni
   :align: center


EPSG
----

Molti CRS e proiezioni sono stati sviluppati nella storia della cartografia. La potenza dei GIS è che consentono di convertire qualsiasi set di dati spaziali tra diversi CRS e proiezioni in modo automatico. A tal fine è di primaria importanza la disponibilità di cataloghi digitali contenenti parametri codificati (come unità, datum e formule di proiezione) dei diversi CRS. Il catalogo più popolare è l' EPSG Geodetic Parameter Dataset, un database di informazioni CRS gestito dalla International Association of Oil and Gas Producers. 

.. figure:: /immagini/1/3.png
   :alt: EPSG
   :align: center

