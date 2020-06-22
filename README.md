---
description: Un sistema riproduttivo per pinguini!
---

# Introduzione

Penguin's eggs nasce con l'idea della "riproduzione" e "selezione delle popolazioni" applicata ai sistemi operativi. 

Erano i tempi di remastersys e systemBack, due dei più diffusi programmi per rimasterizzare un sistema operativo - ad un certo punto - sia remastersys, che aveva sempre sofferto di problemi di manutenzione da parte del suo autore, che systemback furono in qualche modo dismessi. \(_Vedi **nota**_\) 

Per la verità per un po' non vi fu problema alcuno, ma quando cominciarono i "primi dolori" per non poter più rimasterizzare le ultime versioni delle mie distro preferite, essenzialmente Debian e derivate, quella che era una idea, cominciò a prendere forma.

Volevo uno strumento nuovo, scritto con un linguaggio moderno e comune a più distribuzioni, provvisto di un proprio sistema di pacchettizzazione. La scelta cadde su nodejs, con javascript, successivamente sono passato a typescript come linguaggio di sviluppo.

Immaginai un processo di produzione dell'uovo, denominato produce, l'operazione di cova - ovvero l'installazione - originalmente denominata hatch. Gli altri comandi vennero da sè con kill preferito ad abort per togliere di mezzo le iso prodotte, update per gli aggiornamenti, prerequisites per installare i pacchetti .deb necessari al processo, calamares per l'installazione e la configurazione dell'installer grafico.

Prima o poi, trattandosi di un uovo, troverò anche il modo di implementare un server PXE che lo distribuisca attraverso la rete locale, al momento oltre all'intenzione c'è il nome e non poteva essere che cuckoo \(cuculo\), dal comportamento del cuculo che fa covare le proprie uova da altri.



_**Nota**: la situazione  di systemBack  in effetti non è più quella degli inizi di eggs,. Ho conosciuto recentemente il buon Franco Conidi  \(Edmond \) che  ne cura tutt'ora gli aggiornamenti._

