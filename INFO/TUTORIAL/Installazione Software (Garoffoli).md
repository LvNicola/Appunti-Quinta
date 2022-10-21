#	Installazione in Laboratorio
#### Autore: Giacomo Garoffoli
 
 ### XAMPP
 
 Normalmente, XAMPP è installato sui computer dei laboratorio, quindi nessuna installazione è necessaria.
 Per accedere al pannello di configurazione di XAMPP, bisogna navigare alla cartella ( *C:\xampp* ) e bisogna aprire il programma *xampp-control.exe*
In questo pannello di controllo è possibile avviare o fermare i server, configurarli e vedere i log.
> Per controllare il funzionamento di XAMPP, avvia il server Apache e vai su un browser di tua scelta andando sull'indirizzo 127.0.0.1 o localhost. Se appare la scritta "Welcome to XAMPP/It works!" tutto funziona correttamente.

### JETBRAINS DATAGRIP

Il primo software da installare è Datagrip, che si può scaricare a [questo link](https://www.jetbrains.com/datagrip/download/).
Dopo essersi scaricato, avvia il file di installazione (es. datagrip-202x.x.x.exe)
> Se stai eseguendo l'installer sui computer della scuola, premi NO quando vengono richieste le credenziali dell'amministratore di sistema.

Nella schermata "Installation Options", le seguenti opzioni deve essere spuntate:

 - Create Desktop Shortcut: Datagrip
 - Create Associations: .SQL

Alla schermata iniziale di DataGrips, bisogna configurare il proxy premendo "Proxy Settings" in basso a sinistra.
>Se la schermata iniziale non appare, segui la guida presente nella sezione *JetBrains PhpStorm*

 - Premi *Manual proxy configuration* e inserisci:
   
   `HTTP Hostname: 10.250.0.1` `HTTP Port number: 8080`
 - Premi _Proxy  Authentication_ e inserisci le credenziali della scuola:
   
   `Username: CODICE ISA` `Password: PASSWORD ISA`
 - Premi _Remember_ e poi _Apply_ e esci dalle impostazioni.

Dopo aver configurato il proxy, è possibile accedere premendo "**Log In To JetBrains Account**. 
Se non hai un account Educational, si può richiedere l'account a [questo link](https://www.jetbrains.com/community/education/#students). (Ricordati che devi usare l'email della scuola!)

### JETBRAINS PHPSTORM
Il prossimo software da installare è PhpStorm, che si può scaricare a [questo link](https://www.jetbrains.com/phpstorm/download/).
Dopo essersi scaricato, avvia il file di installazione (es. phpstorm-202x.x.x.exe).
> Se stai eseguendo l'installer sui computer della scuola, premi NO quando vengono richieste le credenziali dell'amministratore di sistema.

Nella schermata "Installation Options", le seguenti opzioni deve essere spuntate:

 - Create Desktop Shortcut: PhpStorm
 - Create Associations: Tutte le opzioni spuntate.

Se hai attivato DataGrip precedentemente, PhpStorm non dovrebbe lamentarsi del login, però le impostazioni del proxy non sono configurate.

> Se PhpStorm dice che nessuna licenza è stata trovata, segui la guida del proxy di DataGrips indicata precedentemente e dopo aver premuto "Refresh Licenses" dovrebbe attivarsi tranquillamente.

Per configurare il proxy se la licenza è attivata:

 - Apri PhpStorm e premi su _Customize_.
 - Premi _All Settings_ e premi la frecciettina a lato di _System Settings_.
 - Seleziona _HTTP Proxy_.
 - Premi *Manual proxy configuration* e inserisci:
   
   `HTTP Hostname: 10.250.0.1` `HTTP Port number: 8080`
 - Premi _Proxy  Authentication_ e inserisci le credenziali della scuola:
   
   `Username: CODICE ISA` `Password: PASSWORD ISA`
 - Premi _Remember_ e poi _Apply_ e esci dalle impostazioni.


