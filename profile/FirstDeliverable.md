### Table of contents

- [Analisi dei requisiti](#analisi-dei-requisiti)
  - [Obiettivo](#obiettivo)
  - [Requisiti](#requisiti)
    - [Requisiti funzionali](#requisiti-funzionali)
    - [Requisiti non funzionali](#requisiti-non-funzionali)

# Analisi dei requisiti

## Obiettivo

Il progetto ha come obiettivo la realizzazione di una piattaforma che consenta agli utenti di barattare posti letto usando un token, chiamato REST, offrendo 2 tipi di servizi:

1. Mettere a disposizione posti letto in cambio di 1 REST, chi lo fa viene chiamato host.
2. Usufruire di tali posti letto pagando 1 REST, chi lo fa viene chiamato guest.

## Requisiti

### Requisiti funzionali

- RF1: Registrazione e Autenticazione

  - Alla registrazione verranno richiesti i seguenti dati: nome, cognome, data e luogo di nascita, indirizzo ed email, ed un account telegram. Opzionalmente si potrà inserire delle foto ed una breve bio. L'autenticazione avverrà attraverso Metamask.
  - Ogni nuovo utente riceverà 5 RESTs.
  - Tutti gli utenti potranno cancellare il proprio account.

- RF2: Prenotare un posto letto:

  - Solamente al momento di ogni prenotazione il sistema richierà ai guests di registrarsi o autenticarsi.
    Una volta autenticato il guest potrà scambiare un REST per ottenere il posto letto; successivamente gli verrà mostrato un codice che dovrà esibire al suo host per autenticarsi di persona.
  - (#TODO maybe) I guests potranno inoltre pubblicare richieste di posti letto, specificando luogo e data.
  - Il sistema consentirà ai guests di cercare posti letto inserendo un luogo e una data: verranno elencati i posti letto in ordine di vicinanza a quel luogo e disponibili in tali date.

- RF3: Offrire un posto letto:

  - Una volta autenticato l'host sarà in grado di inserire un annuncio: dovrà fornire l'indirizzo dell'abitazione, una descrizione, ed una serie di funzionalità del posto letto, come la presenza di internet, di un bagno, se sarà necessario lasciare la stanza come l'ho trovata, etc.
  - Gli host potranno cancellare i propri annunci

### Requisiti non funzionali

- RNF1 Privacy

  - Il sito sarà GDPR compliant.
  - Saranno richiesti agli utenti solamente i dati strettamente necessari al servizio di cui vogliono usufruire, in ottemperanza delle vigenti disposizioni di legge in materia di tutela della privacy e trattamento dei dati, garantendo comunque un livello accettabile di affidabilità.

- RNF2 Sicurezza

  - Il sito garantirà la massima sicurezza per gli utenti, avvalendosi del protocollo HTTPS per la trasmissione dei dati attraverso la rete, e di JWT per autenticare le sessioni. Per la generazione dei JWT verrà utilizzata la signature fornita da Metamask.

- RNF3 Scalabilità

  - Il sito deve riuscire a gestire almeno 1000 utenti attivi contemporaneamente, e fino a 100000 utenti registrati.

- RNF4 Affidabilità

  - Il token REST sarà decentralizzato su blockchain Ethereum, garantendo così agli untenti una maggiore affidabilità in quanto ogni transazione di REST sarà pubblicamente verificabile.
    Inoltre il token sarà indipendente dalla piattaforma: l'unica convenzione per usarlo è implementare esclusivamente i 2 servizi elencati negli obiettivi.
    Ciò garantirà agli utenti di poter utilizzare i REST anche al di fuori della piattaforma.

- RNF5 Memorizzazione

  - Il sito utilizzerà mongoDb per memorizzare i dati degli utenti, i loro annunci contenti foto ed informazioni.

- RNF6 Logging & Monitoring

  - Il sito consentirà di registrarsi ed autenticarsi con Metamask. Ciò consentirà agli utenti di possedere e scambiare REST.

- RNF7 Lingua di sistema

  - Il sito sarà disponibile in lingua italiana ed inglese.

- RNF8 Prestazioni

  - Il sito utilizzerà sistemi di caching per migliorare le prestazioni in situazioni di scarsa connessione.

- RNF9 Compatibilità
  - Il sito deve essere compatibile con i browsers più utilizzati, quali:
    - Firefox 91 e successivi
    - Chromium 81 e successivi
    - Safari 16 e successivi
    - Edge 88 e successivi
