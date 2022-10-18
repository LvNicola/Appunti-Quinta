


# Argomenti sistemi distribuiti
## Definizione sistema distribuito 
Si tratta di un sistema informatico costituito da un insieme di processi informatici interconnessi fra di loro, le cui comunicazioni avvengono tramite uno scambio di messaggi(dati)
## Struttura di un nodo di un sistema distribuito
Un nodo è un processo in esecuzione su un Host, con la possibilità di scambiare messaggi con gli altri nodi del sistema.
## Modalità di connessione tra i nodi di un sistema distribuito
La connessione fra nodi di un sistema distribuito avviene tramite un broker, un nodo speciale che mette in comunicazione 2 nodi. 
## Tipologie di sistemi distribuiti 
Principalmente di 2 tipi:
- di Calcolo: sono tutti quei sistemi che effettuano delle elaborazioni distribuendo algoritmi sui nodi del sistema distribuito in modo tale che i nodi possano collaborare per la sua esecuzione.
- di Dati: chiamati anche sistemi distribuiti informatici, consentono di operare su grandi quantità di dati e di gestire in modo ottimale grandi quantità di utenti.
## Definizione e ruolo del middleware
Il middleware è un nodo del sistema distribuito che ha funzionalità particolari. Il suo ruolo é quello di essere un elemento che consente la comunicazione tra due nodi diversi del sistema oppure tra il sistema ed applicazioni esterne.
## Service Discovery, Message Broker e API gateway
Il **Service Discovery** è un processo che rileva quali servizi un nodo offre e lo comunica a tutti gli altri nodi.
Il **Message Broker** è un oggetto in un sistema distribuito che mette in comunicazione 2 nodi.
L'**API gateway** è il componente attraverso cui dall’esterno si può comunicare col sistema. Questo componente smista il traffico in entrata tra i nodi interni che si preoccuperanno di rispondere alle richieste provenienti dai client.
## Connessione Client-Server
La richiesta di connessione di un client con un server avviene tramite il protocollo TCP, in cui il client manda una Request al server in formato HTTP per creare la connessione, ed attende dal server una Response.
La modalità di connessione Client-Server può essere di 2 tipi:
- **Unicast**: il server comunica con un solo client per volta, accettando una sola richiesta di connessione per volta;
- **Multicast**: al server possono essere connessi e comunicare più client contemporaneamente.

## HTTP
è un protocollo a livello applicativo usato come principale sistema per la trasmissione d'informazioni sul web in un'architettura Client-Server.
## Heartbeat Server
é un server che consente ad un processo di capire se un altro processo é attivo oltre a recuperare eventualmente altre informazioni relative al carico corrente del processo remoto.
I client ad un certo intervallo di secondi devono inviare un pacchetto al server; se non vengono mandati più pacchetti per un certo numero di intervalli consecutivi, l'HeartBeat avvisa il Service Discovery, che cancella i dati dell'indirizzo e dei servizi che il nodo(client) offriva. 
Nel caso il client tornasse attivo, i suoi dati dell'indirizzo e dei servizi vengono nuovamente registrati nel Service Discovery, e l'HeartBeat server torna a tenere traccia del client.
## Protocollo di comunicazione Pub/Sub 
è una modalità di scambio di messaggi che consente a dei mittenti, chiamati Sender, di inviare dei messaggi carattegorizzati in un topic in un sistema senza sapere chi sarà il destinatario di questi messaggi. Sarà infatti un componente specifico del sistema, chiamato broker, ad occuparsi di recapitare una copia del messaggio pubblicato a tutti quei processi locali o remoti che hanno espresso interesse verso quel tipo di messaggio effettuando una Subscribe per il topic del messaggio inviato.
In questo protocollo vi sono 3 tipi di comandi:
- Subscribe(Topic)
- Unsubscribe(Topic)
- Publish(Topic, Payload): il payload è semplicemente messaggio che viene inviato e può essere di vario tipo (Binario, Testuale, etc..)
## MQTT 
 è un protocollo di messaggistica standard OASIS per l'Internet of Things (IoT). È progettato come un trasporto di messaggistica di pubblicazione/sottoscrizione estremamente leggero, ideale per la connessione di dispositivi remoti con un footprint di codice ridotto e una larghezza di banda di rete minima. MQTT oggi è utilizzato in un'ampia varietà di settori, come automobilistico, manifatturiero, telecomunicazioni, petrolio e gas, ecc.
## Evoluzione storica dai mainframe fino ai sistemi distribuiti
Fino agli anni 60' i sistemi informatici erano per lo più centralizzati. Dato il costo elevato di allora dei calcolatori, risultava vantaggioso concentrare tutta la potenza dei calcolatori in un unico grande calcolatore, piuttosto che in piccoli calcolatori con potenze di calcolo bassissime. 
In questi ambienti il computer centrale, detto mainframe, consentiva il collegamento tramite la rete da un apparecchio denominato terminale che non aveva alcuna potenza di calcolo, ma il solo scopo di inviare e ricevere i codici. 
Nella metà degli anni 60' vi fu la comparsa dei primi minicomputer, una sorta di sistema intermedio fra mainframe e terminali che si diffusero molto, soprattutto nelle università, alla fine degli anni 60', consentendo la programmazione dei primi sistemi operativi scritti in linguaggi di alto livello (nacque il linguaggio C) o delle prime infrastrutture di rete.
La nascita delle prime reti iniziarono a rendere l'informatica uno strumento distribuito, iniziando a creare i primi servizi a cui delle macchine poco potenti potevano connettersi in modo autonomo, rompendo il vincolo della vicinanza fisica ai terminali per poter usufruire di un servizio e portando alla creazione dei sistemi distribuiti.
## Vantaggi e Svantaggi di un sistema distribuito
Vantaggi:
- Scomposizione e divisione dei problemi 
- possibilità di dividere la programmazione tra più persone
- scalabilità (se ti servono più prestazioni aggiungi o togli nodi) 
- può essere su più macchine diverse (se cade una parte non cade tutto il sistema) 
- svolge operazioni in parallelo.
Svantaggi:
- Ideazione, gestione, programmazione complessa, comunicaazione tra nodi complessa.

 
