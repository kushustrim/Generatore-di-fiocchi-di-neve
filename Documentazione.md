# *Fiocco di neve*
---

1. [Introduzione](#introduzione)

  - [Informazioni sul progetto](#informazioni-sul-progetto)

  - [Abstract](#abstract)

  - [Scopo](#scopo)

1. [Analisi](#analisi)

  - [Analisi del dominio](#analisi-del-dominio)

  - [Analisi e specifica dei requisiti](#analisi-e-specifica-dei-requisiti)

  - [Use case](#use-case)

  - [Pianificazione](#pianificazione)

  - [Analisi dei mezzi](#analisi-dei-mezzi)

1. [Progettazione](#progettazione)

  - [Design dell’architettura del sistema](#design-dell’architettura-del-sistema)

  - [Design delle interfacce](#design-delle-interfacce)

  - [Design procedurale](#design-procedurale)

1. [Implementazione](#implementazione)

1. [Test](#test)

  - [Protocollo di test](#protocollo-di-test)

  - [Risultati test](#risultati-test)

  - [Mancanze/limitazioni conosciute](#mancanze/limitazioni-conosciute)

1. [Consuntivo](#consuntivo)

1. [Conclusioni](#conclusioni)

  - [Sviluppi futuri](#sviluppi-futuri)

  - [Considerazioni personali](#considerazioni-personali)

1. [Sitografia](#sitografia)

1. [Allegati](#allegati)

---

## Introduzione

### Informazioni sul progetto

Il progetto si chiama fiocco di neve.

 - Alunno: Kushtrim Rushi

 - Docenti: Luca Muggiasca, Geo Petrini.

 - Scuola: SAMT (arti e mestieri Trevano)

 - Sezione: informatica

 - Materia: Modulo 306

 - Inizio: 06.09.2019 - Fine: 20.12.2019

### Abstract

Il progetto ci è stato imposto nel modulo 306, il programma con un triangolo modificato dall'utente stampa un fiocco di neve.

Il progetto serve a noi per imparare a fare un progetto.

### Scopo

Lo scopo del progetto è didattico.

Quello che viene richiesto è di creare un programma in Java che datto un triangolo modificato dall'utente disegna un fiocco di neve. In più bisogna fare anche un sito web per il download e la descrizione del programma.

---

## Analisi

### Analisi del dominio

 - Esistono prodotti simili ma non specifici come il nostro.

 - L'utente a cui miriamo è quello che ha tempo da perdere con dei giochini inutili.

 - L'utente non deve avere conoscenze base per l'utilizzo del programma, l'unica cosa che deve saper fare è "usare il mouse".


### Analisi e specifica dei requisiti

Il progetto dovrà essere scritto in Java e dovrà avere un interfaccia grafica.

Inizialmente l'utente dovra interagire con un sito web in cui sarà possibile scaricare il .jar, ovvero il programma. Nello stesso sito ci sarà un descrizione del programma.

Il programma avrà un triangolo dove si possono aggiungere, togliere, spostare e resetare i punti di taglio.

Tramite un bottone "Genera" verrà generato un fiocco di neve in base hai punti di taglio.

I punti e il fiocco di neve possono essere salvati con dei bottoni, "salva punti" e "salva fiocco".

Le immagini possono essere salvate in formato raster (PNG) o in formato  vettoriale (SVG), in caso del raster ci sono 2 dimensioni fisse in cui si può salvare le immagini, cioè 500 X 500 px e 1000 X 1000 px.

#### **Lista Requisiti**

|**ID**|**Nome**                                               |**Priorità**|**Vers**|**Note**|
|------|-------------------------------------------------------|------------|--------|--------|
|Req-1 | L'applicativo deve essere scritto in Java             |1           |1.0     |...     |
|Req-2 | Creazione di un piccolo sito web con descrizione      |2           |1.0     |...     |
|Req-3 | Download dell'applicativo tramite sito                |2           |1.0     |...     |
|Req-4 | Guida per gli utenti sul sito, con screenshot e JRE   |2           |1.0     |...     |
|Req-5 | Intarfaccia grafica                                   |1           |1.0     |...     |
|Req-6 | Punti di “taglio” inseriti con il click del mouse     |1           |1.0     |...     |
|Req-7 | Avere 2 funzioni: aggiunta di punti, reset totale     |1           |1.0     |...     |
|Req-8 | Rimozione, spostamento di punti                       |2           |1.0     |Bonus   |
|Req-9 | Deve essere il tasto "Genera" per il fiocco           |1           |1.0     |...     |
|Req-10| Anteprima al click del tasto "Genera"                 |1           |1.0     |...     |
|Req-11| La generazione avviene in tempo reale                 |2           |1.0     |Bonus   |
|Req-12| L’applicativo permettere di salvare il fiocco di neve |1           |1.0     |...     |
|Req-13| Può essere salvato come immagine raster o vettoriale  |2           |1.0     |PNG, SVG|
|Req-14| Raseter dimensioni fisse, 500x500 o 1000x1000         |2           |1.0     |...     |
|Req-15| L'applicativo permettere di salvare i punti di taglio |1           |1.0     |...     |

**Spiegazione elementi tabella dei requisiti:**

**ID**: identificativo univoco del requisito

**Nome**: breve descrizione del requisito

**Priorità**: indica l’importanza di un requisito nell’insieme del
progetto, definita assieme al committente. Ad esempio poter disporre di
report con colonne di colori diversi ha priorità minore rispetto al
fatto di avere un database con gli elementi al suo interno. Solitamente
si definiscono al massimo di 2-3 livelli di priorità.

**Versione**: indica la versione del requisito. Ogni modifica del
requisito avrà una versione aggiornata.

Sulla documentazione apparirà solamente l’ultima versione, mentre le
vecchie dovranno essere inserite nei diari.

**Note**: eventuali osservazioni importanti o riferimenti ad altri
requisiti.


### Use case

Il caso d'uso principale del programma è in un momento di noia, quindi quando si è annoiato inizi a giocare con i fiocchi di neve.

### Pianificazione

![Gantt preventivo](./Foto/Gantt-iniziale.png)

Questo è il gantt fatto in precedenza, prima dell'inizio del progetto, infatti questo è fatto a grandi linee.

### Analisi dei mezzi

Il programma è fatto in java (linguaggio di programmazione), la versione usata è la "12.0.1", come compilatore è stato usato netBeans versione "11.0", il programma neccesità dell'ultima versione disponibile della JRE.

Il sito web è completamente fatto in html e css anche esso non neccesità di specifici software.

---

## Progettazione

### Design dell’architettura del sistema

Diagramma delle classi:

![Immagine del diagramma delle classi](./Foto/UML.png)

### Design delle interfacce

![Immagine dell'interfaccia iniziale](./Foto/interfaccia.png)

Intefaccia iniziale dove si sceglie se caricare punti già esistenti oppure creare un nuovo triangolo.

![Immagine triangolo](./Foto/triangolo.png)

Interfaccia del triangolo, questo triangolo non è stato modificato (è "pulito"). All'interno di questa interfaccia è possibile modificare il triangolo, salvare i punti, ecc...

![Immagine del fiocco di neve finale](./)

Il fiocco di neve non è stato implementato per mancanza di tempo.

### Design procedurale

Diagramma di flusso:

![Immagine del diagramma di flusso](./Foto/flowdiagram.png)

---

## Implementazione

_Controller_:

 - In questa classe si gestiscono i JPanel e i bottoni che fanno cambiare pagina.

_Interfaccia iniziale_:

 - Questo è uno dei JPanel, qua si gestisce la creazione di un nuovo triangolo o la creazione di un triangolo salvato in precedenza (salvati i punti).

_Triangolo_:

 - Questo è un'altro JPanel, qua si gestiscono i poligoni e i bottoni che sono relativi ad essi (ad esempio: il bottone RESET e il bottone SALVA).

_Fiocco di neve_:

 - Questo è l'ultimo JPanel, questa classe non funziona, dovrebbe generare il fiocco di neve con l'ausilio del triangolo.

_KButtun (Kush button)_:

 - Sono i bottoni creati da me, servono per fare specifiche azioni, funzioni (es: RESET, GENERA, SALVA, NUOVO, CARICA).

_Poligono_:

 - Gestisce la creazione, spostamento e cancellazione di punti, la classe disegna anche il singolo poligono.

_Punto_:

 - La sua funzionalità principale è salvare le coordinate dei punti in percentuale così che rende più facile il ridimensionamento di essi.

_Salvare i punti_:

![Salvare i punti: classe triangolo](./Foto/salva_triangolo.png)

Questa parte di codice, che è all'interno della classe triangolo, permette di salvare i punti. Questo è permesso con l'ausilio della classe poligono.

![Salvare i punti: classe poligono](./Foto/salva_poligono.png)

La classe poligono comunica con i singoli punti per poter salvare i punti più facilmente.

![Salvare i punti: calsse punto](./Foto/salva_punto.png)

In questo metodo si scrive all'interno di una stringa la coordinata del punto. Il formato usato è: x,y.

_Caricare i punti_:

![Caricare i punti: classe triangolo](./Foto/carica_triangolo.png)

In questa parte di codice si prende il file e si dividono le X e le Y di ogni punto. Questi poi verrano mandati al poligono.

![Caricare i punti: classe poligono](./Foto/carica_poligono.png)

In questo metodo si aggiungono i punti al poligono.

---

## Test

### Protocollo di test

|Test Case             | TC-01                                                                             |
|----------------------|-----------------------------------------------------------------------------------|
| **Nome**             | Aggiunto punto                                                                    |
| **Riferimento**      | Req-6                                                                             |
| **Descrizione**      | Provo a cliccare e guardo se escono i punti                                       |
| **Procedura**        | All'interno della pagina del triangolo clicco con il tasto sinistro del mouse in vari punti |
| **Risultati attesi** | Dovrebbero uscire dei punti uno collegato all'altro, il primo punto dovrà avere un colore diverso |

|Test Case             | TC-02                                                                             |
|----------------------|-----------------------------------------------------------------------------------|
| **Nome**             | Togliere i punti                                                                  |
| **Riferimento**      | Req-8                                                                             |
| **Descrizione**      | Provo a cliccare con il tasto destro del mouse sopra il punto e vedo se questo si toglie |
| **Procedura**        | Dopo aver creato dei punti vado sopra con il mouse e clicco il tasto destro del mouse sopra ad un punto |
| **Risultati attesi** | Il punto dovrebbe togliersi con anessi collegamenti ai punti conessi              |

|Test Case             | TC-03                                                                             |
|----------------------|-----------------------------------------------------------------------------------|
| **Nome**             | Spostamento dei punti                                                             |
| **Riferimento**      | Req-8                                                                             |
| **Descrizione**      | Provo a trascinare un punto e guardo se il punto si sposta                        |
| **Procedura**        | Dopo aver creato un punto vedo sopra con il mouse e trascino il punto con il tasto sinistro del mouse |
| **Risultati attesi** | Il punto che si è trascinato dovrebbe spostarsi nella stessa direzione del mouse  |

|Test Case             | TC-04                                                                             |
|----------------------|-----------------------------------------------------------------------------------|
| **Nome**             | Chiuso poligono                                                                   |
| **Riferimento**      |                                                                                   |
| **Descrizione**      | Provo a cliccare il primo punto creato e guardo se il traingolo viene tagliato    |
| **Procedura**        | All'interno della pagina del triangolo clicco con il tasto sinistro del mouse il primo punto creato (colore rosso), si può fare solo dopo aver fatto 3 punti |
| **Risultati attesi** | La parte del poligono dovrebbe cancelarsi                                         |

|Test Case             | TC-05                                                                             |
|----------------------|-----------------------------------------------------------------------------------|
| **Nome**             | Reset punti                                                                       |
| **Riferimento**      | Req-7                                                                             |
| **Descrizione**      | Clicco il bottone "RESET" e guardo se tutti i punti creati in precedenza vengano cancellati, e i poligoni |
| **Procedura**        | All'interno della pagina del triangolo c'è il bottone "RESET", lo clicco          |
| **Risultati attesi** | Ogni punto e poligono creato dovrebbe cancelarsi                                  |

|Test Case             | TC-06                                                                             |
|----------------------|-----------------------------------------------------------------------------------|
| **Nome**             | Ridimensionamento                                                                 |
| **Riferimento**      |                                                                                   |
| **Descrizione**      | Aumento la grandezza della pagina e guardo che i punti si spostano in base alla grandezza della pagina |
| **Procedura**        | Dopo aver creato dei punti e poligoni aumento la grandezza della finestra         |
| **Risultati attesi** | I punti si spostano in base alla grandezza della finestra                         |

|Test Case             | TC-07                                                                             |
|----------------------|-----------------------------------------------------------------------------------|
| **Nome**             | Salva punti                                                                       |
| **Riferimento**      | Req-15                                                                            |
| **Descrizione**      | Clicco il bottone "SALVA" e guardo che si sia creato un file con il formato delle coordinate |
| **Procedura**        | All'interno della pagina del triangolo c'è il bottone "SALVA", lo clicco          |
| **Risultati attesi** | Dovrebbe uscire un pop-up con scritto "Punti salvati" e si dovrebbe creare un file con le coordinate dei punti|

|Test Case             | TC-08                                                                             |
|----------------------|-----------------------------------------------------------------------------------|
| **Nome**             | Carica punti                                                                      |
| **Riferimento**      | Req-15                                                                            |
| **Descrizione**      | Clicco il bottone "CARICA" e guardo che si creino tutti i poligoni salvati in precedenza |
| **Procedura**        | All'interfaccia inizile c'è il bottone "CARICA", lo clicco                        |
| **Risultati attesi** | Dovrebbe uscire un triangolo con i punti di taglio che si sono salvati            |

|Test Case             | TC-09                                                                             |
|----------------------|-----------------------------------------------------------------------------------|
| **Nome**             | Genera fiocco                                                                     |
| **Riferimento**      | Req-9/ Req-10/ Req-11/ Req-12/ Req-13/ Req-14                                     |
| **Descrizione**      | Clicco il bottone "GENERA" e dovrebbe crearsi un fiocco di neve in base al trinagolo modificato |
| **Procedura**        | All'interno della pagina del triangolo c'è il bottone "GENERA", lo clicco         |
| **Risultati attesi** | Dovrebbe crearsi un fiocco di neve                                                |

|Test Case             | TC-10                                                                             |
|----------------------|-----------------------------------------------------------------------------------|
| **Nome**             | Sito web                                                                          |
| **Riferimento**      | Req-2                                                                             |
| **Descrizione**      | Sito web con descrizione del funzionamento del progetto                           |
| **Procedura**        | Creato sito  web                                                                  |
| **Risultati attesi** | Un sito web con descrizioni principali del funzionamento del progetto             |

|Test Case             | TC-11                                                                             |
|----------------------|-----------------------------------------------------------------------------------|
| **Nome**             | Download jar                                                                      |
| **Riferimento**      | Req-3                                                                             |
| **Descrizione**      | Il jar è l'eseguibile e tramite un bottone nel sito web si può scaricare          |
| **Procedura**        | Clicco il bottone "DOWNLOAD" nel sito                                             |
| **Risultati attesi** | IL browser cerca di aprire l'eseguibile ma non ci riesce quindi lo scarica        |

### Risultati test

| Test Case | Esito Test  |
|-----------|-------------|
| TC-01     | Funzionante |
| TC-02     | Funzionante |
| TC-03     | Funzionante |
| TC-04     | Funzionante |
| TC-05     | Funzionante |
| TC-06     | Funzionante |
| TC-07     | Funzionante |
| TC-08     | Funzionante |
| TC-09     | Fallito     |
| TC-10     | Funzionante |
| TC-11     | Funzionante |

### Mancanze/limitazioni conosciute

Purtroppo in mancanza di tempo non sono riuscito ad implementare tutta la parte del fiocco di neve, ovviamente è stato iniziato.

Quello che non ho implementato è la generazione del fiocco di neve, il salvataggio delle immagini, il ridimensionamento del fiocco e la generazione in tempo reale sempre del fiocco.

---

## Consuntivo

![Gantt consuntivo](./Foto/Gantt-finale.png)

Questo è il gantt fatto alla fine del progetto, ovvero come è andato realmente il progetto.

---

## Conclusioni

Il mio progetto non ha nessun impatto nel mondo, non credo che cambierà la vita a qualcuno. Non è neanche un successo mondiale.

Ma personalmente è un grande successo, saper fare tutto questo da solo mi fa sentire realizzato. Nessuno userà mai questo programma, ma non lo definirei un progetto inutile perché per me è stato utile, è stato utile per capire cosa riesco e cosa non riesco a fare, anche per capire come si gestisce il tempo in un progetto.

### Sviluppi futuri

Penso che in futuro completerò il fiocco di neve, ma non credo di fare qualcosa in più.

### Considerazioni personali

Con questo progetto ho imparato relativamente poco, più che altro ho messo in pratica ciò che sapevo. Devo dire però che è stato divertente fare il progetto.

---

### Sitografia

 - https://stackoverflow.com/questions/31209541/convert-from-java-awt-geom-area-to-java-awt-polygon, 22-11-2019

Guardato per trasformare le aree in poligoni.

 - http://samtinfo.ch/i17ruskus/, 20-12-2019

Sito web del progetto.

---

## Allegati

- Documentazione

- Diari

- Programma (netBeans, jar)
