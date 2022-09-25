### Table of contents

- [Analisi dei requisiti](#analisi-dei-requisiti)
  - [Obiettivo](#obiettivo)
  - [Requisiti](#requisiti)
    - [Requisiti funzionali](#requisiti-funzionali)
    - [Requisiti non funzionali](#requisiti-non-funzionali)
- [Architettura](#architettura)
  - [Architettura front-end](#architettura-front-end)
  - [Architettura back-end](#architettura-back-end)

# Analisi dei requisiti
## Obiettivo
Il progetto ha come obiettivo la realizzazione di una piattaforma che consente agli utenti di usufruire di 2 servizi:
1. Mettere a disposizione posti letto a pagamento, chi lo fa viene chiamato host.
2. Usufruire di tali posti letto a pagamento, chi lo fa viene chiamato guest.

## Requisiti
### Requisiti funzionali
- Saranno richiesti agli utenti solamente i dati strettamente necessari al servizio di cui vogliono usufruire con un minimo di affidabilità.
- Un guest non dovrà in qualche modo registrarsi, infatti al momento della prenotazione di un posto letto gli verrà richiesto di dare un nominativo e di pagare una fee (#TODO(Di quanto?)) in Ether usando Metamask, al termine del pagamento gli verrà dato un token (codice) il quale dovrà esibire di persona al suo host per autenticarsi
- Un host dovrà necessariamente registrarsi (autenticandosi con un account Ethereum usando Metamask) fornendo i seguenti dati: un nominativo, un contatto telegram (che dovrà essere autenticato) e #TODO(minimo ad un massimo di giorni per poter ricevere una prenotazione?). Poi quando vuole inserire un annuncio dovrà fornire ulteriori informazioni, cioè l'indirizzo dell'abitazione, una descrizione, un prezzo (in qualsiasi moneta), e una serie di funzionalità del posto letto #TODO( come internet?, un bagno?, dovrò lasciare la stanza come l'ho trovata?, riscaldamento? Condizionatore? e una descri)
- Dovrà essere creato un account speciale per un admin, sempre autenticato con un account Ethereum, il quale potrà rimuovere annunci di posti letto.
- Un utente che ha usufruito di un posto letto può lasciare un voto da 1 a 5 stelle alla persona che ha messo a lo ha messo a disposizione, autenticandosi con Metamask. (#TODO(Se togliessimo questa fueature potremmo anche non salvare le prenotazioni e renderebbe tutto più snello))
- Per il pagamento del posto letto dovranno pensarci chi lo mette a disposizione e chi lo usufruisce mettendosi d'accordo. Avvenuta la prenotazione la piattaforma non sarà responsabile di nulla qualsiasi cosa avvenga.
- La ricerca dei posti letto avverrà inserendo un luogo, dal quale verranno elencati i posti letto in ordine di vicinanza a quel luogo.
- Sarà possibile cancellare il proprio profilo da host.
- Sarà possibile cancellare i propri annunci.
### Requisiti non funzionali
- La piattaforma dovrà essere una #TODO(PWA? Vue.js?).
- Il backend sarà scritto in Java.
- Le API per comunicare col il server saranno implementate con gRPC.


# Architettura
## Architettura front-end
#TODO
## Architettura back-end
#TODO