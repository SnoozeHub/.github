### Table of contents

- [Analisi dei requisiti](#analisi-dei-requisiti)
  - [Obiettivo](#obiettivo)
  - [Requisiti](#requisiti)
    - [Requisiti funzionali](#requisiti-funzionali)
    - [Requisiti non funzionali](#requisiti-non-funzionali)

# Analisi dei requisiti

## Obiettivo

Il progetto ha come obiettivo la realizzazione di una piattaforma che consenta agli utenti di barattare posti letto usando un token, chiamato REST, offrendo 2 tipi di servizi:

1. Mettere a disposizione uno o più posti letto in cambio di 1 REST a notte
2. Usufruire di tali posti letto pagando 1 REST a notte per posto letto

## Requisiti

### Requisiti funzionali

- RF1: Registrazione e Autenticazione

  Alla registrazione di un utente verranno richiesti i seguenti dati: nome, cognome, email, ed un account telegram. Opzionalmente si potrà inserire delle foto.
  ?Ogni nuovo utente riceverà 5 RESTs.

- RF2: Prenotare un posto letto:

  Una volta autenticato l'utente potrà scambiare un REST per ottenere il posto letto; successivamente gli verrà mostrato un codice che dovrà esibire all'host per autenticarsi di persona.

- RF3: Recensire i posti letto:

  Al termine di ogni interazione, chi viene ospitato potrà recensire il posto letto con un voto da 1 a 5.

- RF4: Cercare i posti letto:

  Il sistema consentirà di cercare posti letto inserendo un luogo e una data: verranno elencati i posti letto in ordine di vicinanza a quel luogo e disponibili in tali date.

- RF5: Aggiungere un posto letto al proprio account:

  Gli utenti, una volta autenticati, per inserire un posto letto dovranno fornire: l'indirizzo dell'abitazione, delle foto e il tempo di preavviso per la prenotazione.
  Inoltre dovranno specificare la presenza dei seguenti servizi:

  - connessione internet
  - bagno
  - riscaldamento
  - condizionatore
  - corrente elettrica
  - acqua corrente
  - presenza biancheria da letto
  - presenza cuscini
  - Sarà possibile rimuovere il posto letto

- RF6: Offrire un posto letto:

  Sarà possibile scegliere tra i posti letto caricati sul proprio account e specificarne la disponibilità tramite un annuncio.
  Fatto ciò, gli altri utenti potranno prenotare il posto letto.
  Sarà possibile cancellare i propri annunci

- RF7: Gestione dell'account
  Tutti gli utenti potranno cancellare il proprio account.

### Requisiti non funzionali

- RNF1 Privacy

  - Il sito sarà GDPR compliant.
  - Saranno richiesti agli utenti solamente i dati strettamente necessari al servizio di cui vogliono usufruire, in ottemperanza delle vigenti disposizioni di legge in materia di tutela della privacy e trattamento dei dati, garantendo comunque un livello accettabile di affidabilità.

- RNF2 Sicurezza

  - Il sito garantirà la massima sicurezza per gli utenti, avvalendosi del protocollo grpc per la trasmissione dei dati attraverso la rete, e di JWT per autenticare le sessioni. Per la generazione dei JWT verrà utilizzata la signature fornita da Metamask.

- RNF4 Affidabilità

  - Il token REST sarà decentralizzato su blockchain EVM-compatible, garantendo così agli untenti una maggiore affidabilità in quanto ogni transazione di REST sarà pubblicamente verificabile.
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
  - Il sito deve essere mobile-first, deve aderire allo standard w3c, compatibile con i browsers più utilizzati, quali:
    - Firefox 91 e successivi
    - Chromium 81 e successivi
    - Safari 16 e successivi
    - Edge 88 e successivi
