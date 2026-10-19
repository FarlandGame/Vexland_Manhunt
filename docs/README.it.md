# Vexland_Manhunt


[English](../README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**Un’esperienza Minecraft completa con Corridori contro Cacciatori, creata insieme da [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) e [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt riunisce preparazione della partita, ruoli delle squadre, inseguimento iniziale, tracciamento, progressione, ricompense, risultati e amministrazione in un unico plugin per server Paper. I Corridori cercano di sconfiggere l’Ender Dragon, mentre i Cacciatori cercano di eliminare l’ultimo Corridore. Il plugin supporta più Corridori e mantiene l’inseguimento attraverso morti, rinascite, cambi di dimensione e riconnessioni. Il centro di controllo `/mhgui` permette agli amministratori di gestire la partita tramite menu, con messaggi e libri guida tradotti per i giocatori.

## Download e compatibilità

| Versione fornita | Download | Installazione |
|---|---|---|
| **2.0.0 — pacchetto combinato** | [VexLandManhunt-2.0.0.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0.jar) | **Un solo JAR**, con GrimAC 2.3.73 integrato |
| **1.13.1 — ramo spettatore** | [Versione ed entrambi i JAR](https://github.com/FarlandGame/Vexland_Manhunt/releases/tag/v1.13.1) | Manhunt più GrimAC 2.3.73 separato |
| 1.9.11 / 1.6.4 — precedenti | [Tutte le versioni](https://github.com/FarlandGame/Vexland_Manhunt/releases) | Build autonome storiche |

**Paper 1.21.11 / Java 21.** Sono plugin per server, non mod per client. Il nome del file fornito e la versione pubblica sono **2.0.0**, ma il descrittore invariato riporta **`1.9.11-grim.1`** e identifica la base di gioco come 1.9.11. Questo pacchetto combinato **non** contiene il ruolo dedicato Spectator, `/mspectator <player>`, `/mhspectate`, menu suddivisi per categoria o altre aggiunte della 1.13.1. Continua a usare il ramo 1.13.1 elencato separatamente se ti servono queste funzionalità.

Le build originali per server personali con accesso amministrativo elevato specifico dei creatori sono conservate così come fornite. La guida descrive i controlli pubblici.

## L’esperienza Manhunt

- **Squadre di Corridori e Cacciatori:** assegna i giocatori online a uno dei due schieramenti. Una partita richiede almeno un Corridore e un Cacciatore o un giocatore online senza ruolo. I Corridori sopravvissuti continuano se un compagno muore; un Corridore caduto diventa Cacciatore, a meno che quella morte termini la partita.
- **Avvio cinematografico:** inventari e modalità di gioco vengono preparati, le squadre presentate e una roulette sceglie il vantaggio iniziale dei Corridori. I Cacciatori restano immobilizzati durante il conto alla rovescia, con titoli e suoni. Il vantaggio iniziale è casuale; gli amministratori possono liberare i Cacciatori in anticipo.
- **Bussola di tracciamento con scelta del bersaglio:** i Cacciatori ricevono una bussola speciale. Fai clic destro per scegliere un Corridore dal menu dei bersagli e cambiarlo durante l’inseguimento. Tra dimensioni, il tracciamento segue il percorso del portale pertinente finché diventa possibile quello diretto. I Cacciatori ricevono nuovamente la bussola dopo la rinascita.
- **Indicatori di progresso:** barre dei boss e informazioni della partita seguono equipaggiamento e progressione dei Corridori attraverso risorse del Nether, verghe di blaze, perle, Occhi di Ender, roccaforte ed End. La build più recente aggiunge fasi più dettagliate e indicatori sensibili alla salute del drago.
- **Ricompense per le uccisioni dei Corridori:** quando un Corridore uccide un Cacciatore durante una partita attiva, viene usato un insieme ponderato di 50 ricompense che considera la progressione. Sono inclusi sorteggi animati, ricompense doppie/triple, annunci delle serie di uccisioni e celebrazioni degli oggetti rari.
- **Vittoria e risultati:** la morte dell’ultimo Corridore dà la vittoria ai Cacciatori; sconfiggere l’Ender Dragon dà la vittoria ai Corridori. Sono inclusi titoli finali, celebrazioni, informazioni su uccisioni/morti e pulizia degli oggetti temporanei. La build più recente riporta anche MVP, danni e distanza.
- **Comunicazione di squadra e utilità:** messaggi privati ai compagni con `/teammsg`, inventario usa e getta di 54 slot con `/trash` e visione notturna personale con `/nv`.
- **Amministrazione tramite menu:** ruoli, avvio/ripristino, liberazione anticipata dei Cacciatori, fuoco amico, blocco server, teletrasporto di tutti, cura/cibo, lingua, protezioni, stato e guide sono disponibili nel centro di controllo. Immobilizzazione e ripristino completo aiutano a preparare la partita successiva.
- **Guide tradotte:** i libri per Corridori, Cacciatori e amministratori spiegano obiettivi, bussola, morti, preparazione e comandi. La versione 1.9.11 fornisce ai giocatori una guida adatta al ruolo tramite `/mhhelp`.
- **Integrazione Paper Anti-Xray:** i controlli del menu configurano la protezione di Paper a livello di mondo; le modifiche richiedono un riavvio del server per avere effetto.

## Cosa cambia nel pacchetto 2.0.0 fornito?

- **Un solo JAR integrato:** Manhunt, GrimAC 2.3.73 modificato e PacketEvents incluso condividono una sola istanza del plugin Bukkit. Questo pacchetto non richiede installazioni separate di GrimAC o PacketEvents. Il descrittore fornisce `GrimAC`; l'archivio è appiattito e non contiene un JAR Grim invariato annidato.
- **Stato dei moduli:** il comando amministratore `/vexintegration` riporta Grim ACTIVE/INACTIVE, il proprietario Bukkit, lo stato di VexAC, lo stato di PacketEvents e il numero di giocatori monitorati. I comandi nativi `/grim` e `/grimac` sono registrati dal modulo integrato.
- **Avvio controllato:** il caricatore richiede l'API di configurazione di Paper ed esattamente Minecraft 1.21.11. Rifiuta il caricamento a caldo con giocatori online e un'istanza GrimAC separata. Se l'avvio integrato fallisce, il plugin viene disabilitato e registra che la protezione Grim è inattiva; il server stesso può continuare a funzionare. Verifica lo stato prima di iniziare una partita.
- **Migrazione dei dati esistenti:** al primo caricamento integrato, la migrazione esegue il backup di entrambe le vecchie strutture di dati dei plugin e copia i vecchi dati GrimAC solo quando la destinazione integrata non esiste. Se esistono entrambe, prevalgono i dati integrati esistenti; non viene eseguita alcuna unione o sovrascrittura. I dati originali vengono conservati.
- **Responsabilità della correzione del movimento:** `plugins/VexLandManhunt/integration.properties` usa per impostazione predefinita `movement-correction-owner=legacy`. L'alternativa supportata è `grim`; altri valori interrompono l'avvio. Scegliere grim sopprime i percorsi di correzione VexAC con riposizionamento/teletrasporto, mentre rimangono controlli, avvisi e prove di VexAC. Non disabilita tutte le punizioni legacy.
- **Base di gioco:** il menu piatto `/mhgui`, l'alternanza dei ruoli Runner/Hunter, i controlli VexAC, Smart Hunter Kit V3, pausa/ripresa, recupero e 683 chiavi tradotte seguono la 1.9.11. Questa è una versione che combina pacchettizzazione e integrazione, non l'insieme di funzionalità della 1.13.1 con supporto spettatore.

## Meccaniche di gioco mantenute dalla base 1.9.11

I sistemi seguenti sono stati aggiunti alla base 1.9.11 e sono mantenuti da questo pacchetto combinato. Sono funzionalità di gioco ereditate, anziché nuove funzionalità spettatore della 2.0.0.

| Aggiunta o modifica | Comportamento nella 1.9.11 |
| --- | --- |
| **Smart Hunter Kit V3** | I kit adattivi alla rinascita considerano equipaggiamento dei Corridori, squadre e contesto della partita. Il sistema mira a mantenere i kit dei Cacciatori sotto la media dell’equipaggiamento dei Corridori e si attiva/disattiva con `/mhkit` o dalla GUI. |
| **Spawn automatico nell’Overworld** | Sposta lo spawn del mondo vicino a un Corridore idoneo nell’Overworld a intervalli scelti: disattivato, 5, 10, 15, 20 o 30 minuti. Seleziona un punto sicuro in superficie e salta i casi inadatti. |
| **Pausa e ripresa** | `/mhpause` sospende gioco, timer della partita, tracciamento e spostamento dello spawn; `/mhresume` continua. Il tempo in pausa viene escluso dal tempo attivo della partita. |
| **Recupero dopo riavvio/crash** | Un livello di recupero ripristina stato della partita, ruoli, bersagli delle bussole, progresso, timer di ricompense/morti e riconnessioni usando snapshot principali/di riserva, salvataggi periodici e allo spegnimento. |
| **Impostazioni di riconnessione dei Corridori** | Una finestra configurabile sostituisce quella precedente fissa di 60 minuti. Valore iniziale: 15 minuti, con 10 secondi di protezione al rientro. Il tempo con server spento è escluso; la scadenza può trasformare il Corridore in Cacciatore o terminare la partita. |
| **Amministrazione ampliata** | Cambia ruoli durante una partita mantenendo l’ultimo Corridore; azioni sul giocatore selezionato, teletrasporto/immobilizzazione di squadra, risincronizzazione dello stato di esecuzione e scorciatoie migliorano la gestione. |
| **Ripristino delle impostazioni con conferma** | Due clic entro otto secondi applicano Smart Kit ON, spawn automatico ogni 15 minuti e riconnessione di 15 minuti. Diversamente da una nuova installazione, che usa spawn automatico OFF. |
| **VexAC 3.0** | Controlli di movimento, combattimento, AutoClick, velocità/contraccolpo e costruzione; controlli di gruppo/generali, registrazione delle prove, avvisi agli amministratori ed esenzioni per ambiente/lag. |
| **Ultra Deep Debug v4** | `/mhdebug` fornisce diagnostica di macchina a stati, GUI, kit sintetici/stress, segnaposto delle lingue, ciclo di recupero e integrità. |
| **Indicatori ampliati** | Più dettagli di progressione, salute del drago, risultati MVP/danni/distanza e informazioni sul ping nel TAB. |
| **Modifiche ai comandi** | Aggiunge `/mhkit`, `/mhspawn`, `/mhpause`, `/mhresume` e `/mhdebug`; rimuove `/mhnone`; adatta `/mhhelp` a giocatori/amministratori e aggiunge alias di `/trash`. |
| **Più messaggi tradotti** | Le risorse di traduzione passano da 446 chiavi di messaggio per lingua a 683. |

I controlli inclusi in VexAC coprono Fly, Speed, Timer, Phase, Step, NoSlow, GroundSpoof, Reach, KillAura, AimAssist, colpi attraverso muri, BadPackets, schemi temporali AutoClick, contraccolpo alterato, Scaffold, Tower, FastPlace, Nuker e portata sui blocchi. L’interfaccia usa un’etichetta di solo monitoraggio, mentre il codice compilato contiene anche percorsi di espulsione; verifica il comportamento effettivo della moderazione su un server di prova prima di affidarti a quell’etichetta. La build precedente contiene invece i controlli legacy Anti AutoClick e Anti Fly.

## Preparazione e uso completi con `/mhgui`

### 1. Installa la build combinata

1. Arresta completamente il server **Paper 1.21.11 / Java 21** ed esegui il backup dei mondi e dei dati dei plugin.
2. Inserisci solo `VexLandManhunt-2.0.0.jar` di questa versione in `plugins/`. Sposta i vecchi JAR di Manhunt e GrimAC autonomo fuori dalla directory dei plugin attivi. Conserva le loro cartelle dati; non eliminarle. I giocatori non installano questo JAR sul client.
3. Avvia normalmente anziché usare `/reload`. Il caricatore integrato gestisce il ciclo di vita di Grim e PacketEvents.
4. Come OP o con `vexland.admin`, esegui `/vexintegration`. Controlla `Grim=ACTIVE` e `PacketEvents=true` prima di procedere a `/mhgui`. Una protezione inattiva è un problema di avvio, non un'installazione integrata riuscita.

La configurazione di Grim si trova in `plugins/VexLandManhunt/grim/` (`config.yml`, `messages.yml`, `punishments.yml`, `discord.yml`), con cronologia facoltativa in `violations.sqlite`. I backup della prima migrazione vanno in `plugins/VexLandManhunt-integration-backups/`; `plugins/VexLandManhunt/integration-migration-v1.txt` ne contrassegna il completamento. Se esistono sia i vecchi dati Grim sia quelli integrati, la destinazione integrata viene preservata e viene registrato un avviso. La migrazione rifiuta i collegamenti simbolici.

Esamina la responsabilità del movimento in `plugins/VexLandManhunt/integration.properties`; conserva le altre impostazioni. Valore predefinito per una nuova installazione:

```properties
movement-correction-owner=legacy
```

La guida completa ai menu pubblici qui sotto segue la base di gioco 1.9.11 di questo pacchetto. Il ramo spettatore ha una propria guida archiviata.

### 2. Apri il centro di controllo

Entra nel server come amministratore con **OP** o il permesso **`vexland.admin`** e digita:

```text
/mhgui
```

Le istruzioni seguenti descrivono l’interfaccia pubblica della versione **2.0.0**, usando i nomi inglesi dei pulsanti. Le etichette seguono la lingua selezionata per il server. Per usare tutta la GUI, utilizza un account **OP** fidato: il permesso del descrittore consente di aprire il comando, ma alcuni gestori della GUI fornita applicano controlli OP più restrittivi. L’inventario principale ha cinque righe di nove slot. Passa il cursore su un pulsante per leggerne descrizione e impostazione attuale. La maggior parte usa un clic normale; azioni speciali del mouse e conferme sono spiegate sotto. Il menu più piccolo della 1.6.4 è descritto alla fine.

#### Prepara la prima partita

1. Apri **Player Roles**. Fai clic sulla testa di ogni partecipante finché il ruolo visualizzato è corretto. Nella 2.0.0 il ruolo alterna **Runner** e **Hunter**; un partecipante senza ruolo diventa Corridore al primo clic. Clic sinistro/destro/con Maiusc non sono scorciatoie separate per scegliere il ruolo. Usa **Previous Page**, **Next Page** e **Back to Control Center** quando necessario.
2. Assegna almeno un Corridore e almeno un Cacciatore. La procedura di avvio può trasformare in Cacciatori i giocatori online rimasti senza ruolo, quindi assegnare esplicitamente tutti chiarisce le squadre.
3. Fai clic su **Friendly Fire** per scegliere se i compagni possono danneggiarsi. Controlla l’indicatore ON/OFF dopo il clic.
4. Fai clic su **Language** per scegliere la lingua dell’intero server. Influisce su messaggi, interfacce, avvisi e guide di tutti, non solo del tuo giocatore.
5. Controlla **Smart Hunter Kit**, **Auto World Spawn** e **Anti-Cheat**. Se serve una spiegazione nel gioco, leggi la guida dell’amministratore tramite il pulsante del libro.
6. Assicurati che **Server Freeze** sia disattivato, poi fai clic su **Start Match**. L’avvio prepara giocatori e inventari, esegue introduzione e roulette casuale del vantaggio iniziale prima della liberazione dei Cacciatori, quindi avvia la caccia. Prima di iniziare, conserva fuori dagli inventari dei partecipanti ciò che vuoi mantenere.

#### Pulsanti principali del centro di controllo

Le posizioni contano le righe dall’alto al basso e le colonne da sinistra a destra. Descrivono il layout finale decorato della 2.0.0.

| Posizione | Pulsante inglese | Funzione |
|---|---|---|
| Riga 2, colonna 2 | Player Roles | Apre il menu paginato delle teste dei giocatori Corridori/Cacciatori. |
| Riga 2, colonna 3 | Target Player | Scorre gli altri giocatori online per azioni amministrative sul bersaglio selezionato. Controlla il nome attuale. |
| Riga 2, colonna 4 | Friendly Fire | Attiva/disattiva il danno fra compagni. |
| Riga 2, colonna 5 | Match Info | Invia un rapporto rapido su stato, squadre, fuoco amico e bersaglio selezionato. |
| Riga 2, colonna 6 | Start Match | Esegue l’avvio normale della partita e il vantaggio iniziale casuale. |
| Riga 2, colonna 7 | Full Heal | Ripristina la salute di tutti i giocatori online. |
| Riga 2, colonna 8 | Reset Match | Esegue il ripristino completo della partita. È diverso da Reset Settings. |
| Riga 3, colonna 2 | Full Hunger | Ripristina cibo e saturazione di tutti i giocatori online. |
| Riga 3, colonna 3 | Release Hunters | Libera i Cacciatori in attesa prima della fine del vantaggio iniziale. |
| Riga 3, colonna 4 | Clear Effects | Rimuove gli effetti di pozione da tutti i giocatori online. |
| Riga 3, colonna 5 | Server Freeze | Attiva/disattiva l’immobilizzazione globale; i giocatori normali senza OP restano immobili. |
| Riga 3, colonna 6 | Clear Target Inventory | Svuota inventario, armatura e mano secondaria del giocatore selezionato dopo conferma. |
| Riga 3, colonna 7 | Teleport Everyone | Porta tutti i giocatori online nella tua posizione attuale. |
| Riga 3, colonna 8 | Kill Target | Uccide il giocatore selezionato dopo conferma; le regole normali di morte possono influire sulla partita. |
| Riga 4, colonna 2 | Anti-Cheat | Apre i controlli VexAC Security. |
| Riga 4, colonna 3 | Freeze Target | Attiva/disattiva l’immobilizzazione individuale del giocatore selezionato. |
| Riga 4, colonna 4 | Emergency Restore | Ripristina salute, cibo e saturazione per tutti i giocatori online. |
| Riga 4, colonna 5 | Freeze Team | Clic sinistro alterna i Corridori; destro i Cacciatori; Maiusc-clic rimuove immobilizzazioni individuali/di squadra. |
| Riga 4, colonna 6 | Set Day | Imposta il giorno nel mondo attuale. |
| Riga 4, colonna 7 | Clear Weather | Ferma pioggia e temporali nel mondo attuale. |
| Riga 4, colonna 8 | Language | Apre il selettore globale della lingua. |
| Riga 5, colonna 2 | Smart Hunter Kit | Attiva/disattiva kit adattivi alla rinascita dei Cacciatori; mostra ON/OFF. |
| Riga 5, colonna 3 | Clear Dropped Items | Rimuove le entità degli oggetti a terra nel mondo attuale. |
| Riga 5, colonna 4 | Pause Match / Resume Match | Sospende o riprende gioco e timer della partita. |
| Riga 5, colonna 5 | Emergency Sync | Risincronizza ruoli, bussole e relativo stato di esecuzione. |
| Riga 5, colonna 6 | Reset Settings | Ripristina le impostazioni bilanciate dopo conferma con due clic. |
| Riga 5, colonna 7 | Close | Chiude il centro di controllo. |
| Riga 5, colonna 8 | Auto World Spawn | Apre il selettore d’intervallo dello spawn automatico nell’Overworld. |
| Riga 5, colonna 9 | Manhunt Administrator Guide | Fornisce il libro guida tradotto per gli amministratori. |

I vetri decorativi e gli oggetti titolo/stato non sono pulsanti di gioco.

#### Ruoli e bersagli selezionati

**Player Roles** modifica la squadra Manhunt effettiva del partecipante. Fai clic sulla testa e leggi il ruolo aggiornato. Durante STARTING/RUNNING, l’interfaccia permette cambi Corridore/Cacciatore ma rifiuta di trasformare l’ultimo Corridore in Cacciatore. Questo preserva la squadra dei Corridori nella partita in corso. Cambia i ruoli consapevolmente, perché lo stato delle squadre e le bussole vengono sincronizzati dopo la modifica.

**Target Player** è separato: seleziona qualcuno per azioni come Freeze Target, Clear Target Inventory o Kill Target senza cambiarne la squadra. Scorri finché compare il nome del giocatore online desiderato. Se un bersaglio salvato diventa indisponibile, il codice può scegliere il primo altro giocatore online; verifica quindi sempre il nome immediatamente prima di agire sul bersaglio. Se non c’è nessun altro online, segnala che non è disponibile alcun bersaglio.

**Clear Target Inventory** e **Kill Target** richiedono due clic sulla stessa azione per lo stesso bersaglio entro **cinque secondi**. Il primo prepara la conferma e identifica il bersaglio; il secondo esegue l’azione. Cambiare bersaglio o attendere troppo richiede una nuova conferma. Svuotare un inventario ne elimina il contenuto; uccidere un Corridore può terminare o cambiare la partita secondo le regole normali di morte.

**Freeze Team** ha le uniche scorciatoie del mouse specifiche per squadra in questo menu: clic sinistro normale seleziona i Corridori, clic destro normale seleziona i Cacciatori e Maiusc-clic rimuove tutte le immobilizzazioni individuali/di squadra gestite da questo strumento. L’interruttore globale Server Freeze è separato e va disattivato separatamente se i giocatori restano immobili.

#### Smart Hunter Kit

Fai clic su **Smart Hunter Kit** per attivare/disattivare i kit adattivi alla rinascita dei Cacciatori. Il pulsante mostra lo stato attuale. Quando è attivo, un Cacciatore che rinasce può ricevere un kit adattato all’equipaggiamento dei Corridori e al contesto; la guida fornita lo descrive come più debole della media dei Corridori. Quando è disattivato, i Cacciatori non ricevono kit automatici dopo la morte. Questo non disattiva la bussola di tracciamento.

Per impostare direttamente invece di alternare, usa `/mhkit on`, `/mhkit off` o `/mhkit status`. Il valore di fallback verificato per una configurazione nuova è ON.

#### Auto World Spawn

Fai clic su **Auto World Spawn**, poi scegli **OFF**, **5 minutes**, **10 minutes**, **15 minutes**, **20 minutes** o **30 minutes**. Selezionare un’opzione la salva e torna a `/mhgui`; **Back** torna senza selezionare un nuovo intervallo.

Quando è attivo, il sistema cerca periodicamente una superficie sicura nell’Overworld vicino a un Corridore attivo lì e vi sposta lo spawn del mondo. Salta lo spostamento se nessun Corridore è nell’Overworld o non trova un punto sicuro. Il fallback per una configurazione nuova è OFF. Per gli stessi controlli via comando, usa `/mhspawn off`, `/mhspawn 15` o `/mhspawn status`, sostituendo 15 con qualsiasi intervallo supportato.

#### Pausa, riconnessione e recupero

**Pause Match** è disponibile mentre la partita è RUNNING. Sospende sistemi di gioco, movimento/interazioni, timer, tracciamento e spostamento dello spawn. **Resume Match** li riprende e compensa il tempo in pausa. Server Freeze immobilizza soltanto i giocatori e non va usato come sostituto quando serve fermare l’orologio della partita.

La finestra di riconnessione dei Corridori è configurabile, con fallback iniziale di **15 minuti**. Un rientro tempestivo ripristina lo stato del Corridore e fornisce dieci secondi di protezione. Il tempo con server inattivo non consuma la finestra salvata. Gli slot dei Corridori scaduti diventano Cacciatori; la scadenza dell’ultimo Corridore può dare la vittoria ai Cacciatori.

**La GUI 2.0.0 fornita non ha un selettore separato per la durata della riconnessione**. Per personalizzarla, arresta il server, modifica `plugins/VexLandManhunt/config.yml`, conserva le altre impostazioni e imposta:

```yaml
features:
  custom-reconnect-minutes: 15
```

Riavvia dopo la modifica. I valori sotto un minuto vengono portati a uno. **Reset Settings** ripristina questo valore a 15 minuti. La build compilata salva anche stato di partita/riconnessione e snapshot di riserva per recuperare dopo riavvii/crash; lascia gestire quei file al plugin invece di modificarli durante il gioco.

#### Reset Settings e Reset Match

**Reset Settings** richiede due clic sul pulsante entro **otto secondi**. Il primo prepara la conferma; il secondo ripristina **Smart Kit ON**, **Auto Spawn ogni 15 minuti**, **Riconnessione 15 minuti** e un **vantaggio iniziale casuale**. È diverso da una nuova installazione, dove Auto World Spawn usa fallback OFF. Modifica la configurazione; non sostituisce il ripristino completo della partita.

**Reset Match** esegue il ripristino esistente della partita, eliminando stato/oggetti temporanei e riportando i giocatori allo spawn dell’Overworld per un altro round. Il pulsante principale non usa la conferma a due clic di Reset Settings. **Start Match** può preparare/svuotare gli inventari dei partecipanti. Verifica quale controllo di ripristino/avvio intendi usare prima di fare clic.

#### Controlli di lingua e anti-cheat

**Language** apre il selettore globale. Fai clic sulla lingua desiderata. Entrambe le build fornite contengono inglese, persiano, arabo, spagnolo, francese, tedesco, russo, cinese semplificato, hindi e portoghese. La lingua scelta è condivisa dal server e salvata. La documentazione README giapponese non aggiunge il giapponese al selettore del gioco.

**Anti-Cheat** apre **VexAC Security**. Fai clic su **VexAC Master** per attivare/disattivare il motore interno, oppure su **Movement**, **Combat**, **AutoClick**, **Velocity / AntiKB** o **World / Scaffold** per alternare il gruppo. **Anti X-Ray** attiva/disattiva l’Anti-Xray configurato di Paper; riavvia il server per applicare la modifica. Le caselle di stato, registro delle prove e modello di rilevamento spiegano i sistemi attuali. **Back to Control Center** torna al menu principale.

L’interfaccia della build descrive una moderazione di solo monitoraggio, ma l’ispezione statica conserva un percorso di espulsione basato su soglie. Considera l’indicazione senza espulsioni del menu una discrepanza fra implementazione/documentazione e verifica la moderazione su un server controllato prima di farvi affidamento.

#### GrimAC integrato e VexAC legacy

La GUI esistente **VexAC Security** controlla il motore VexAC legacy; i suoi pulsanti Master/di gruppo non sono un nuovo pannello di controllo Grim. GrimAC integrato funziona al suo fianco. Usa `/vexintegration` per lo stato dei moduli e i comandi nativi `/grim` o `/grimac` per i comandi di Grim e gli strumenti controllati dai permessi. Le impostazioni e le regole di punizione di Grim si trovano in `plugins/VexLandManhunt/grim/`.

Il menu monitor/gruppi di GrimBridge della 1.13.1 e `grim-settings.yml` non descrivono questo pacchetto. Non presumere che disattivare VexAC disabiliti anche GrimAC integrato, o che un'etichetta di monitoraggio stabilisca una politica senza espulsioni. Paper Anti-Xray rimane un'impostazione indipendente che richiede un riavvio.

#### Guida nel gioco e risoluzione dei problemi

Fai clic su **Manhunt Administrator Guide** o usa `/mhhelp` per un libro guida tradotto. Nella 2.0.0 i giocatori possono usare `/mhhelp` per la guida adatta al ruolo. I Cacciatori fanno clic destro sulla bussola per scegliere un Corridore; questa interfaccia è separata dal selettore Target Player dell’amministratore.

Se un ruolo o una bussola sembra fuori sincronia, **Emergency Sync** aggiorna il relativo stato di esecuzione. **Match Info** aiuta a controllare squadre e stato attuale. Se l’avvio richiesto fallisce, verifica che la partita sia pronta, che Server Freeze sia disattivato e che esista una squadra Corridori/Cacciatori. Dopo aver cambiato JAR, esegui un riavvio completo invece di `/reload`. `/mhdebug` è un comando diagnostico per amministratori incluso nella 2.0.0; la sua presenza non significa che queste versioni abbiano superato test su un server attivo.

#### Uso del vecchio centro di controllo 1.6.4

La 1.6.4 mantiene **Player Roles**, **Friendly Fire**, **Start Match**, **Reset Match**, **Release Hunters Now**, **Server Lock**, **Teleport Everyone To Me**, **Heal & Feed Everyone**, **Match Status**, selezione della lingua, **Anti Cheat** e una guida amministrativa. I ruoli seguono **None → Runner → Hunter**, e i cambi sono bloccati mentre la partita si avvia/è in corso.

Il menu anti-cheat contiene i controlli legacy **Anti AutoClick** (regola di 30 CPS con avviso/espulsione), **Anti Fly** e **Anti X-Ray** di Paper. La finestra di riconnessione dei Corridori è fissa a **60 minuti**. L’interruttore più recente Smart Hunter Kit V3, il selettore Auto World Spawn, pausa/ripresa, conferma Reset Settings e strumenti ampliati su bersagli/mondi descritti sopra appartengono alla 2.0.0 e non sono da aspettarsi nel menu precedente.

Questa guida deriva da metadati dei JAR forniti, testi di lingua/aiuto inclusi e disassemblaggio statico. Durante l’ispezione, l’interfaccia non è stata eseguita su un server Minecraft attivo.

### 3. Gioca l’inseguimento

I Corridori fuggono durante il vantaggio iniziale casuale e progrediscono verso la sconfitta dell’Ender Dragon. I Cacciatori aspettano la liberazione, poi fanno clic destro sulla bussola per selezionare un Corridore. I bersagli possono cambiare durante il gioco, anche quando l’inseguimento attraversa dimensioni. Usa `/teammsg <message>` per parlare solo alla squadra e `/mhhelp` per la guida tradotta del ruolo nella 2.0.0.

Se un Corridore muore, gli altri continuano e il giocatore caduto diventa Cacciatore. Un Cacciatore può rinascere e continuare a tracciare. La morte dell’ultimo Corridore o la scadenza della riconnessione di un Corridore può terminare la partita a favore dei Cacciatori; la sconfitta dell’Ender Dragon la termina per i Corridori.

### 4. Metti in pausa, termina e prepara un’altra partita

Nella 2.0.0, metti in pausa con `/mhpause` e continua con `/mhresume`. Usa `/mhrelease` per liberare i Cacciatori prima della fine del conto alla rovescia iniziale. Per una nuova partita, usa il ripristino completo del centro di controllo o `/mhreset`; elimina stato e oggetti temporanei e riporta i giocatori allo spawn dell’Overworld. Modificare Paper Anti-Xray richiede un riavvio.

## Impostazioni predefinite nel pacchetto combinato 2.0.0

I valori di fallback verificati per una configurazione nuova sono:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` significa che lo spostamento automatico dello spawn è disattivato. Il ripristino delle impostazioni confermato dalla GUI imposta invece l’intervallo a 15 minuti. Usa la GUI oppure `/mhkit` e `/mhspawn` per le rispettive impostazioni.

## Riferimento dei comandi pubblici — combinato 2.0.0

I comandi amministratore richiedono OP o `vexland.admin` (OP per impostazione predefinita). Chat di squadra, cestino e visione notturna sono utilità per i giocatori; `/mhhelp` fornisce la guida in base al ruolo. La tabella elenca i 17 comandi Manhunt/integrazione; i comandi nativi di Grim hanno permessi propri. `/mhnone` non è registrato qui.

| Comando | Scopo |
| --- | --- |
| `/vexintegration` | Mostra lo stato di Grim integrato, VexAC, PacketEvents e del proprietario Bukkit condiviso |
| `/mhgui` | Aprire il centro di controllo |
| `/mhstart` | Eseguire l’intera sequenza di avvio |
| `/mhreset` | Ripristinare completamente la partita attuale |
| `/mhrelease` | Liberare i Cacciatori in anticipo |
| `/mrunner <player>` | Assegnare un Corridore |
| `/mhunter <player>` | Assegnare un Cacciatore |
| `/teammsg <message>` | Inviare un messaggio privato ai compagni |
| `/trash` | Aprire l’inventario usa e getta di 54 slot |
| `/nv` | Attivare/disattivare la visione notturna personale |
| `/mhlang` | Aprire il selettore globale della lingua |
| `/mhhelp` | Ricevere un libro guida tradotto |
| `/mhkit <on\|off\|toggle\|status>` | Configurare gli Smart Hunter Kit |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Configurare lo spostamento automatico dello spawn |
| `/mhpause` | Mettere in pausa la partita in corso |
| `/mhresume` | Riprendere la partita in pausa |
| `/mhdebug` | Eseguire la diagnostica interna |

## Lingue di gioco e documentazione

Questo pacchetto mantiene **10 lingue di gioco**: inglese, persiano, arabo, spagnolo, francese, tedesco, russo, cinese semplificato, hindi e portoghese. Ogni traduzione inclusa ha **683 chiavi**, come nella 1.9.11. `/mhlang` imposta un'unica lingua per tutto il server, salvata in `language.txt`.

La documentazione del progetto ha **18 lingue**, escludendo un'edizione araba della documentazione. Queste traduzioni non aggiungono il giapponese o altre lingue di gioco al binario invariato.

## Cronologia delle versioni, sorgenti e riconoscimenti

[CHANGELOG.md](../CHANGELOG.md) documenta ogni versione fornita. La [guida completa spettatore della 1.13.1](archive/1.13.1/README.it.md) e la [guida precedente della 1.9.11 / 1.6.4](archive/1.9.11/README.it.md) restano disponibili. Ogni versione fornita conserva il proprio download e checksum.

**Manhunt è creato congiuntamente da Bardiya / Farland_game e Ali / Alivexor. GrimAC è un progetto separato di GrimAC / DefineOutside e collaboratori.** Questo artefatto integrato modifica tre classi Grim; non è il binario ufficiale Grim invariato della precedente versione a due file. Il [pacchetto sorgente](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0-source.zip) di accompagnamento conserva i sorgenti forniti, gli script di build, gli input delle dipendenze e gli avvisi, omettendo le prove di test/esecuzione e lasciando invariato il codice sorgente. La versione include anche il testo GPLv3, i checksum e gli [avvisi di terze parti](../THIRD_PARTY_NOTICES.md). Durante questa pubblicazione non è stato eseguito alcun test su server attivo o di build riproducibile.

## Una sfida scherzosa a Dream

Una piccola provocazione Minecraft da Bardiya 😄

> "Uff... Ali e io abbiamo fatto un plugin Manhunt cento volte migliore di quello di Dream, ma Dream ha paura e non vuole giocare con il nostro!"

## Creatori e ambito del progetto

**Creato insieme da [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) e [Ali · Alivexor](https://github.com/Alivexor).** Entrambi gli account sono registrati come autori anche nei descrittori originali del plugin.

Questo repository presenta le versioni compilate originali, la documentazione e le note di versione come progetto di portfolio condiviso. Le descrizioni delle funzionalità si basano sull’ispezione statica dei JAR forniti. Compatibilità su server attivi, prestazioni del recupero, bilanciamento e precisione dell’anti-cheat non sono stati testati in questo processo di pubblicazione.

[Portfolio GitHub di Bardiya](https://github.com/FarlandGame) · [GitHub di Ali](https://github.com/Alivexor) · [Tutte le versioni](https://github.com/FarlandGame/Vexland_Manhunt/releases)
