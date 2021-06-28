# LoggerLib 1.0
The project is a "Tracing Library" developed in a Borland C++ enviroment.
Il progetto consiste in una libreria di tracciamento, sviluppata in ambiente Borland.

# ENGLISH
The project involves the building of a library containing the tracking tools to be integrated into larger projects.
This library is obtained from sources written in C++, developed in a Borland environment.

The objective is to get the designer/programmer from the burden of implementation of an infrastructure for the management of
tracings (inside a larger project) that is always useful in the first developping phase: debug/test, as well as during
next year to monitor its operation.
The library implements a multi-level tracing mechanism that can be adapted to various modes of use: can be used
directly, in a simple single-threaded, or even multi-threading more complex.

It includes a mechanism to rotate the logs, integrated in the library that limits the size of the files to a preset and
configurable threshold. To User the management of synchronization between the various calls to methods of tracking and to
subsequent entries in the files, as well as the various stages of management of files is transparent.

The basis of the technology used in the library is a client-server process: the client-side interfaces directly with
the host application, through the exposure of the public methods. This part is responsible for performing the configuration phase of the
management of tracings and subsequently limited to the sending of the message tracking to the next processes.
The serving side of the library is responsible for the receipt and management of message tracking on the basis of what is
be the set configuration. This client-server mechanism, which flows in a sequential message handling between producer and
consumer is the basic concept, used in the library. The multiplicity of this concept, applied to the amount of files and/or contexts
rappresnta the solution offered to the developer.

Among the advantages of this management there are processing times smaller, to load the main application: the sending time of a
message is decidedly less than that required for all the processing of a message tracking, until its writing
in the file. Furthermore, by moving the management of writing files elsewhere and reducing it to a sequential processing
of messages, is easily exceeds the barrier of synchronization of access to files.

The main modes of operation of this library are two: one allows the use of tracking methods, implementing directly
parameters in the code and configuration using in this way the features offered.

The other method, more complex, makes use of a configuration file and adds to basic functionality listed above, a management
centrally managed by a manager class that provides "methods of Factory" for instancing of markers, and their
centralized management.

The project structure is quite simple: a base class contains the methods for the tracking capabilities of files,
and two classes of service, suitable to be integrated into the final draft, make available the two modes of operation: the simple,
suitable for a single application or in any case to direct access, and another more articulated and managed, aimed for use in applications
multithreading.

The project includes a package with the library and all the necessary header files for integration into the project and that of an
application testing that shows the operation in the different modes.

---------------------------------------------------------------------------------------------------------------------

# ITALIANO

Il progetto consiste nella realizzazione di una libreria contenente degli strumenti di tracciamento, da integrarsi in progetti più ampi.
Questa libreria è ottenuta da sorgenti scritti in C++, sviluppati in un ambiente Borland.

L'obiettivo prefissato è scaricare il progettista/programmatore dall'onere della realizzazione di un'infrastruttura per la gestione dei
tracciamenti (internamente ad un progetto più ampio) sempre utili sia nella prima fase realizzativa: debug/test, come anche nella fase
successiva di esercizio, per monitorarne il funzionamento.
La libreria implementa un meccanismo di tracciamento multilivello, che può adattarsi a più modalità di impiego: può essere utilizzata
direttamente, in un semplice programma mono-thread, o anche in applicazioni multi-threading più complesse.

E' incluso un meccanismo di rotazione dei file, integrato nella libreria che limita la dimensione dei files ad una soglia prefissata e
configurabile. Trasparente all'utilizzatore la gestione della sincronizzazione tra le varie chiamate ai metodi di tracciamento ed alle
successive scritture nei files, come anche alle varie fasi di gestione dei files.

Alla base della tecnologia impiegata nella libreria vi è una struttura client-server: il lato client, si interfaccia direttamente con
l'applicazione ospite, mediante l'esposizione di metodi pubblici. Questa parte si occupa di eseguire la fase di configurazione della
gestione dei tracciamenti e successivamente di limitarsi al solo invio del messaggio di tracciamento verso la fase elaborativa successiva.
La parte servente della libreria è incaricata della ricezione e gestione del messaggio di tracciamento in funzione di quella che risulta
essere la configurazione impostata. Questo meccanismo client-server, che confluisce in una gestione dei messaggi sequenziale tra produttore e
consumatore, è il concetto base, usato nella libreria. La molteplicità di questo concetto, applicata per la quantità di file e/o contesti
rappresnta la soluzione offerta allo sviluppatore.

Tra i vantaggi di questa gestione vi sono tempi di elaborazione minori, a carico dell'applicazione principale: il tempo di invio di un
messaggio è decisamente minore di quello necessario per tutta l'elaborazione di un messaggio di tracciamento, fino alla sua scrittura
nel file. Inoltre, spostando la gestione della scrittura dei file altrove e riducendola ad un processamento sequenziale di messaggi, si
supera agilmente l'ostacolo della sincronizzazione all'accesso ai files.

Le principali modalità di funzionamento di questa libreria sono due: una permette l'uso di metodi di tracciamento, implementando direttamente
nel codice i parametri di configurazione ed avvalorandosi in questo modo delle funzionalità offerte.

L'altro metodo, più articolato, fa uso di un file di configurazione ed aggiunge alle funzionalità di base appena elencate, una gestione
centralizzata, amministrata tramite una classe manager, che offre "metodi di Factory" per l'instanzazione di tracciatori, e per la loro
gestione centralizzata.

La struttura del progetto è abbastanza semplice: una classe di base contiene i metodi principali per le funzionalità di tracciamento su files,
mentre due classi di servizio, adatte per essere integrate nei progetti finali, rendono disponibili le due modalità d'uso: quella semplice,
adatta per una singola applicazione o comunque ad accesso diretto, ed un'altra più articolata e gestita, finalizzata all'uso in applicazioni
multithreading.

Il progetto include un pacchetto con la libreria e tutti i files di intestazione necessari all'integrazione nel progetto e quello di un'
applicazione di testing che ne mostra il funzionamento nelle diverse modalità.
