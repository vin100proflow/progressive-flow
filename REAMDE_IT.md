# Progressive Flow Whitepaper

## Introduzione

### Che cos’è Progressive Flow?
Progressive Flow è un paradigma applicato a Git, parallelo a Git Flow, che nasce per risolvere uno dei principali problemi di quest’ultimo: il collo di bottiglia causato dalla gestione delle release.

Chi ha utilizzato Git Flow su progetti dinamici e in team collaborativi si sarà probabilmente trovato a dover gestire molteplici feature parallele, generate dalle richieste dei clienti. Inizialmente, il processo funziona senza intoppi: le attività procedono, le feature vengono sviluppate e chiuse, e la prima modifica completata avvia l'apertura di una release. Tuttavia, proprio qui emergono le criticità.

Le feature chiuse vengono man mano aggiunte alla release in attesa di approvazione del cliente. Se una singola feature richiede più tempo del previsto per essere approvata o, peggio, necessita di rielaborazioni complesse, tutte le modifiche successive rimangono bloccate nella release. Questa situazione genera un accumulo, ritarda i test e impedisce il rilascio delle modifiche che sarebbero già pronte.

### La soluzione di Progressive Flow
Progressive Flow è stato progettato per superare queste limitazioni. Grazie all'introduzione del ramo intermedio `candidate`, elimina il collo di bottiglia e garantisce un flusso continuo, allineandosi pienamente ai principi di CI/CD. Questo approccio permette di isolare le modifiche approvate da quelle ancora in lavorazione, assicurando rilasci rapidi, test accurati e una migliore gestione delle attività in corso.

## Panoramica del Paradigma

Progressive Flow si propone come un’alternativa migliorata a Git Flow, progettata per risolverne le limitazioni strutturali. Il suo approccio si concentra sulla gestione indipendente delle feature, mantenendole pronte per essere rilasciate in qualsiasi momento, senza creare colli di bottiglia nel processo di sviluppo e rilascio.

### I vantaggi di Progressive Flow

- **Flessibilità:** Progressive Flow consente rilasci più frequenti e indipendenti, avvicinandosi ai principi fondamentali di Continuous Integration e Continuous Delivery (CI/CD).
- **Familiarità:** Costruito con una forte ispirazione a Git Flow, Progressive Flow mantiene un flusso di lavoro simile.
- **Riduzione dei conflitti:** Grazie all’introduzione del ramo intermedio `candidate`, consente merge parziali tra i branch `candidate` e `release`.
- **Collaborazione migliorata:** I team di sviluppo possono lavorare in parallelo senza blocchi o ritardi.
- **Supporto alla scalabilità:** Adatto per progetti complessi o dinamici.
- **Tracciabilità e controllo:** Rami intermedi e flussi di lavoro strutturati migliorano il monitoraggio delle modifiche.

## Differenze con gli altri paradigmi

### Progressive Flow vs. Git Flow
- **Flessibilità delle Release:** Il ramo `candidate` permette un'integrazione selettiva delle feature.
- **Complessità:** Progressive Flow migliora la modularità delle feature.

### Progressive Flow vs. GitHub Flow
- **Supporto per Ambienti Multipli:** Progressive Flow include test e approvazioni.
- **Scalabilità:** Adatto a workflow complessi.

### Progressive Flow vs. Trunk-Based Development
- **Focus su Stabilità:** Progressive Flow offre maggiore controllo con il ramo `candidate`.
- **Rischio di Rilasci Prematuri:** Riduce il rischio di integrare modifiche non testate.

## Dettagli tecnici

### Le Candidate
Le `candidate` sono rami che nascono da `develop` e rappresentano funzionalità candidate al rilascio.

#### Come funzionano le Candidate?
1. **Creazione:** Ogni nuova `candidate` nasce da `develop`.
2. **Sviluppo:** Tutti gli sviluppi vengono effettuati all'interno della `candidate`.
3. **Test su Staging:** Le modifiche vengono integrate nel ramo `release`.
4. **Approvazione:** Dopo i test, la `candidate` è pronta per il rilascio.
5. **Chiusura e Merge:** Le modifiche vengono mergeate su `develop` e `master`.

#### Differenze principali
- **Feature:** Utilizzate per lo sviluppo, integrate in `develop`.
- **Candidate:** Rimangono aperte fino all'approvazione finale.
- **Release:** Stato aggregato delle `candidate` pronte per la produzione.

## Diagramma di Progressive Flow
(TODO: Aggiungere diagramma)

## Conclusione
Progressive Flow rappresenta un passo avanti nella gestione dei flussi di sviluppo software. Con l’introduzione dei rami `candidate`, offre una maggiore flessibilità, supporta un rilascio più rapido e riduce i colli di bottiglia.

Per maggiori informazioni, contattatemi all’indirizzo **vincent.legnani.biz@gmail.com**.

Un cordiale saluto,  
**Vincent Legnani**
