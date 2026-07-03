☠ Bounty
Un plugin avanzato ed efficiente per server Minecraft (Spigot/Paper 1.21+) progettato per rendere il PvP e il PvE molto più competitivi e dinamici attraverso un sistema di taglie automatico basato sulle serie di uccisioni (KillStreak).

🚀 Funzionalità Principali
Taglie Dinamiche Automatiche: Incremento casuale e automatico del valore sulla testa di un giocatore quando raggiunge una determinata serie di uccisioni (KillStreak).

Supporto PvP e PvE (Mob): Configurabile per far salire la taglia uccidendo altri giocatori, entità/mostri (ottimo per i test in solitaria o modalità PvE), o entrambi.

Integrazione Economica Nativa: Collegamento completo con l'economia del server tramite Vault (compatibile con EssentialsX, TheNewEconomy, ecc.).

Riscossione Automatica: Quando un ricercato viene ucciso da un altro giocatore, la taglia viene accreditata all'istante nel conto dell'assassino. Se muore per cause naturali, la taglia va perduta.

Interfaccia GUI Intelligente (/taglie): Un menu grafico intuitivo che mostra le teste personalizzate di tutti i giocatori ricercati nel server con il rispettivo valore.

Integrazione PlaceholderAPI (PAPI): Include il placeholder %bounty_val% per mostrare la taglia attuale direttamente nella TAB, nelle Scoreboard o nei plugin di Chat, senza decimali fastidiosi (cifre tonde con simbolo €).

Database Leggero: Salvataggio automatico e persistente dei dati e delle taglie attive all'interno del file data.yml.

🛠 Comandi e Permessi
/taglie

Descrizione: Apre l'interfaccia grafica (GUI) contenente la lista di tutti i ricercati del server e il valore della loro taglia.

Permesso: Disponibile per tutti i giocatori di default.

⚙ Configurazione (config.yml)
Il file di configurazione permette di personalizzare interamente l'esperienza e attivare i test in solitaria con i mob:

# Configurazione Generale del Plugin Bounty

settings:
   Abilita/Disabilita l'incremento della taglia quando si uccidono altri giocatori
  enable-player-kills: true
   Ogni quante kill sui player scatta l'aumento della taglia?
  player-killstreak-every: 5

   Abilita/Disabilita l'incremento della taglia quando si uccidono i MOB
  enable-mob-kills: false
   Ogni quante kill sui mob scatta l'aumento della taglia? (es. 1 per testare da solo)
  mob-killstreak-every: 1

   Impostazioni sull'aumento economico della taglia (Valori in Euro)
  bounty-increase:
    min: 3000.0
    max: 5000.0
📊 Integrazione PlaceholderAPI (TAB & Scoreboard)
Il plugin si registra nativamente su PlaceholderAPI. Puoi usare il seguente segnaposto:

%bounty_val%

Cosa mostra: Restituisce la taglia formattata in questo modo:  ☠ 5000€ (mostra il valore arrotondato all'intero più vicino per una resa grafica pulita). Se il giocatore non ha una taglia sulla testa, non restituisce nulla (vuoto).

📌 Requisiti di Sistema
Per funzionare correttamente, il plugin necessita dei seguenti componenti all'interno della cartella plugins:

Vault (Fondamentale per il bridge economico)

Un plugin di Economia (Es. EssentialsX, necessario per memorizzare i bilanci)

PlaceholderAPI (Opzionale, ma caldamente consigliato per la compatibilità con la TAB)
