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
Il progetto ha come obiettivo la realizzazione di una piattaforma che consenta agli utenti di barattare posti letto usando un token decentralizzato su blockchain Ethereum chiamato REST, offrendo 2 tipi di servizi:
1. Mettere a disposizione posti letto in cambio di 1 REST, chi lo fa viene chiamato host.
2. Usufruire di tali posti letto pagando 1 REST, chi lo fa viene chiamato guest.

Inoltre il token è indipendente dalla piattaforma, l'unica convenzione per usare il token è implementare esclusivamente i 2 servizi sopra elencati.

## Requisiti
### Requisiti funzionali
- Saranno richiesti agli utenti solamente i dati strettamente necessari al servizio di cui vogliono usufruire con un minimo di affidabilità.
- Un utente solamente al momento di ogni prenotazione dovrà autenticarsi con Metamask, fornire un nominativo, e poi scambire un REST per ottenere il posto letto, successivamente gli verrà mostrato un codice che dovrà esibire al suo host per autenticarsi di persona. Una volta autenticati, gli hosts potranno inoltre pubblicare richieste di posti letto, specificando luogo e data dell'abitazione. 
- Un host dovrà necessariamente registrarsi (autenticandosi con un account Ethereum usando Metamask) fornendo i seguenti dati: un nominativo, un contatto telegram (che dovrà essere autenticato) ed un minimo e massimo di giorni per poter ricevere una prenotazione. Poi quando vuole inserire un annuncio dovrà fornire ulteriori informazioni, cioè l'indirizzo dell'abitazione, una descrizione, ed una serie di funzionalità del posto letto, come la presenza di internet, di un bagno, se sarà necessario lasciare la stanza come l'ho trovata, etc.
- La ricerca dei posti letto avverrà inserendo un luogo e una data, dal quale verranno elencati i posti letto in ordine di vicinanza a quel luogo e disponibili in tali date.
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