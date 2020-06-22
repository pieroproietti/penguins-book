---
description: >-
  Scarica i pacchetti di installazione di eggs o utilizza direttamente il codice
  sorgente
---

# Installazione

### Pacchetto Debian

L'installazione da pacchetto Debian è senz'altro la più semplice. Basta scaricare l'ultima versione di eggs dal sito di [sourceforge](https://sourceforge.net/projects/penguins-eggs/files/DEBS/) ed installarla con il comando:

`sudo dpkg -i eggs-7.5.81-1.deb`

La versione .deb  comprende al suo interno nodejs per cui non è necessario disporre di questo pacchetto. 

### Pacchetto npm \(nodejs\)

Essendo eggs un software sviluppato con nodejs, la versione originale e quella preferibile,  e sempre la più aggiornata. Inoltre, una volta installata, questa versione è sempre aggiornabile semplicemente con il comando `sudo eggs update`.

Per poter installare questa versione è necessario quindi installare prima il pacchetto nodejs. La descrizione di quale nodejs utilizzare e le modalità di installazione di nodejs sono riportare nel file README,md compreso nella [repository di eggs](https://github.com/pieroproietti/penguins-eggs).

L'installazione di eggs da pacchetto npm è semplice e sicura, solo questi comandi:

`sudo npm config set unsafe-perm true`

`sudo npm install penguins-eggs -g`

Per aggiornare il pacchetto - una volta installato - alle successive versioni, basterà il comando

`sudo eggs update`

### Utilizzo di eggs da codice sorgente

Utilizzare eggs a partire dai sorgenti può essere estremamente utile sia per debug che collaborare allo sviluppo. Una volta scaricato il sorgente con il comando

`git clone` [`https://github.com/pieroproietti/penguins-eggs`](https://github.com/pieroproietti/penguins-eggs)\`\`

entrare. quindi, nella directory penguins-eggs e dare il comando

`npm install`

A questo punto, dalla directory penguins-eggs stessa, si potrà utilizzare il sorgente direttamente. Ad esempio

sudo ./eggs produce -f -v

Per gli sviluppatori od i curiosi, sarà possibile vedere, segnalare o correggere il codice. 



