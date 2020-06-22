---
description: Comandi ed opzioni di eggs
---

# I comandi

### Comandi ed opzioni 

Eggs necessita dei diritti di root, quindi - tranne per eggs info - DEVE essere chiamato preceduto da`sudo`

* adjust
* calamares
* help
* howto
* info
* install
* kill
* prerequisites
* produce
* skel
* sterilize
* update

Non vi fate spaventare da questi pochi comandi, quelli che utilizzerete sono essenzialmente due: produce per creare la iso e kill per cancellarla.

Ogni comando può avere alcuni flag,di questi, il più importante, è il flag -f o --fast del comando produce che consentirà ad eggs di utilizzare come algoritmo di compressione lz4 invece del default xz permettendovi così di risparmiare non poco tempo durante le fasi di sviluppo della vostra remix. 

Altro flag importante e presente nella quasi totalità dei casi è il flag -v o --verbose che vi mostrerà a video il susseguirsi delle vari comandi.

Andiamo ad illustrare i comandi in rigoroso ordine alfabetico, per comodità dello scrivente. Tenete a mente che i comandi che utilizzerete normalmente sono kill e produce.

### eggs adjust

Adatta il video alle capacità del monitor o alla grandezza della finestra in caso di macchina virtuale. Lo trovo molto comodo per ridimensionare le macchine virtuali con interfacce grafiche diverse da cinnamon gnome3 e kde per la quale non è necessario. In pratica eggs richiama xrandr per adattare lo schermo alla risoluzione corrente.

### eggs calamares

Installa e configura l'installatore grafico universale calamares. Può essere utilizzato anche in caso di una iso realizzata senza calamares e che, in sede di installazione si voglia installare con esso.

### help

Come dice il comando stesso genera la lista dei comandi disponibili. A sua volta ogni comando con il flag -h o --help emette usa sua descrizione.

### eggs howto

Mostra a video dei brevissimi suggerimenti. Al momento boot da grub rescue e come configurare eggs.

#### eggs howto:grub

Come avviare da grub rescue.

#### eggs howto:configure

Come configurare eggs.

### eggs info

Mostra a video la configurazione di eggs e del sistema. E' l'unico comando che può essere usato senza sudo.

### eggs install

Lancia l'installaler cli di eggs. 

In alternativa con l'opzione -g o --gui lancia invece calamares.

Attenzione, l'installatore cli è più veloce di calamares, però è MOLTO rudimentale e non raccomandato per i non esperti. Cancellerà compleamente il disco rigido di destinazione! Utilizzatelo solo su macchine virtuali o computer puliti o da pulire.

### eggs kill

Cancella le immagini realizzate e la directory di lavoro di eggs \(il nido\). Esegue rm /home/eggs -rf per cancellare tutte le iso create. Presenta anche un utile flag -u che, prima di procedere alla rimozione tenta smonta i filesystem eventualmente presenti in essa.

### eggs prerequisites

Installa i pacchetti deb necessari al funzionamento di eggs. In particolare, vengono installati:

`'isolinux', 'live-boot', 'live-boot-initramfs-tools', 'live-config-systemd', 'squashfs-tools', 'xorriso', 'xterm', 'whois'`

e, nel caso si sia scelto di installare calamares

`calamares', 'qml-module-qtquick2', 'qml-module-qtquick-controls'`

Oltre a questo vengono creati i file di configurazione.

### eggs produce

E' questo il comando che più utilizzerete, di fatto sostanzialmente l'unico insieme a kill che serve invece a sbarazzarsi delle immagini iso create.

Usato senza parametri produce la iso con compressione di tipo xz. Controlla pure se sono o non sono installati i prerequisiti e creati i file di configurazione e, di fatto, produce la iso.

Presenta alcuni flag utilizzabili:

`-b, --basename=basename basename egg`

 `-c, --compress max compression` 

`-f, --fast compression fast` 

`-h, --info show CLI help` 

`-v, --verbose verbose`

Di gran lunga la modalità d'uso che preferisco, personalmente è

`eggs produce -f -v`

che mi consente si avere una veloce rimasterizzazione ed osservare a video i vari comandi lanciati.

### eggs skel

Con questo comando si ricrea la directory /etc/skel della nostra remix. E' utile per dare una veste coerente e personalizzata all'utente live ed ai futuri utenti che creeremo una volta che il nostro sistema sarà installato. Essenzialmente copia le configurazioni dell'utente primario o di quello passato con il flag -u nella cartella /etc/skel che verrà quindi utilizzata per generare lo scheletro della home degli utenti creati.

Considerando che esistono diversi desktop manager, gnome2, gnome3, cinnamon, mate, kde, lxqt, lxde, etc e che viene fatta una operazione di pulizia dei possibili dati sensibili, è un comando sempre in evoluzione. Attualmente è abbastanza affidabile per cinnamon e, per le prove che ho fatto anche con gli altri Desktop Manager.

### eggs sterilize

E' il comando inverso di prerequisites, sostanzialmente rimuove i pacchetti sopra elencati rendendo il nostro sistema non più in grado di riprodursi.

### eggs update

Aggiorna il pacchetto eggs alla versione corrente. Attenzione, eggs update funziona solo con la versione pacchettizata npm, per la versione rilasciata come pacchetto deb avremmo bisogno di un repository al momento non disponibile.

