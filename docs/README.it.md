# Vexland_Manhunt

[English](../README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**Un’esperienza Minecraft completa con Corridori contro Cacciatori, creata insieme da [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) e [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt riunisce preparazione della partita, ruoli delle squadre, inseguimento iniziale, tracciamento, progressione, ricompense, risultati e amministrazione in un unico plugin per server Paper. I Corridori cercano di sconfiggere l’Ender Dragon, mentre i Cacciatori cercano di eliminare l’ultimo Corridore. Il plugin supporta più Corridori e mantiene l’inseguimento attraverso morti, rinascite, cambi di dimensione e riconnessioni. Il centro di controllo `/mhgui` permette agli amministratori di gestire la partita tramite menu, con messaggi e libri guida tradotti per i giocatori.

## Download e compatibilità

| File / versione | Download | Scopo |
|---|---|---|
| **1.13.1 — attuale** | [VexLandManhunt-1.13.1.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/VexLandManhunt-1.13.1.jar) | Plugin Manhunt di Bardiya e Ali |
| **GrimAC 2.3.73 — obbligatorio** | [grimac-bukkit-2.3.73.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/grimac-bukkit-2.3.73.jar) | Dipendenza anti-cheat separata di terze parti |
| 1.9.11 — archiviata | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Build precedente di Manhunt |
| 1.6.4 — archiviata | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Build più vecchia di Manhunt |

**Piattaforma prevista: Paper 1.21.11, Java 21.** I numeri 1.6.4, 1.9.11 e 1.13.1 indicano le versioni del plugin, non le versioni di Minecraft supportate. In 1.13.1, GrimAC è una dipendenza obbligatoria e il bridge richiede l'API 2.3.73. Scarica **entrambi i JAR attuali**. Sono plugin per server; i giocatori non devono installarli nella cartella delle mod del client.

Queste sono le build originali per server personali, con accesso amministrativo elevato riservato ai creatori, conservate esattamente come sono state fornite. Questo manuale descrive i controlli pubblici di Manhunt.

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

## Quali sono le novità di 1.13.1?

Rispetto alla build 1.9.11 fornita:

- **Spettatori fantasma:** un ruolo separato, assegnazione da parte dell'amministratore, volo protetto, giocatori nascosti, stato salvato/ripristinato e un menu a pagine per teletrasportarsi ai partecipanti.
- **Centro di controllo riprogettato:** menu suddivisi per categoria, selezione esplicita tra quattro ruoli, selettore del bersaglio per nome, selettore della durata di riconnessione, preimpostazioni Classic/Fast/Hardcore/Custom e schermate di conferma dedicate da 30 secondi.
- **Integrazione GrimAC:** GrimAC 2.3.73, obbligatorio, sostituisce il percorso di avvio attivo di VexAC. La GUI espone il controllo principale, cinque gruppi di controlli, avvisi e controlli di monitoraggio/applicazione delle sanzioni. Paper Anti-Xray rimane indipendente.
- **Nuovo pianificatore Smart Hunter Kit:** adatta equipaggiamento e scorte all'equipaggiamento/incantesimi dei Runner, al Runner più vicino, al numero di membri delle squadre, alla distanza, alla dimensione e al terreno. Conserva l'equipaggiamento esistente più potente, evita strumenti duplicati e limita i rifornimenti dei consumabili mediante una cronologia di 30 secondi. Questo non garantisce una differenza fissa di equipaggiamento né un bilanciamento misurato.
- **Ripristino convalidato:** snapshot sigillati con SHA-256, controlli dello schema/stato e ripiego su un backup valido; gli snapshot non validi o in un formato più recente vengono conservati senza sovrascriverli. Lo stato degli spettatori ha una persistenza propria.
- **Messaggi ampliati:** le chiavi tradotte passano da 683 a 762 per ciascuna traduzione inclusa, sempre nelle stesse dieci lingue di gioco. Sono registrati due nuovi comandi pubblici: `/mspectator <player>` e `/mhspectate`.
- **Ripiego durante il reset:** se non viene trovata una superficie sicura vicino allo spawn dell'Overworld, il reset può saltare quel teletrasporto invece di forzarlo.

## Configurazione e utilizzo completi con `/mhgui`

Arresta il server e conserva un backup dei mondi e dei dati dei plugin. Inserisci entrambi i JAR attuali in `plugins/`, lasciando in quella cartella un solo JAR di Manhunt e un solo JAR di GrimAC. Durante l'aggiornamento conserva le impostazioni/i dati esistenti in `plugins/VexLandManhunt/`. Avvia completamente il server Paper 1.21.11 / Java 21; quando sostituisci le build, esegui un riavvio completo. GrimAC deve caricarsi correttamente. Il nome interno del plugin rimane `VexLandManhunt`.

Questa guida descrive la versione **1.13.1** del plugin con etichette in inglese. Le etichette seguono la lingua impostata per tutto il server. Le posizioni contano le righe dall'alto verso il basso e le colonne da sinistra a destra. Usa un normale clic sinistro, salvo quando è indicata un'azione speciale. Questa guida deriva da un'ispezione statica; non è stato eseguito alcun server Minecraft.

### Preparare una partita

1. Usa `/mhgui` con `vexland.admin` (predefinito: OP).
2. Apri **Player Roles**, fai clic sul riquadro con il nome di un giocatore, quindi scegli **Runner**, **Hunter**, **Spectator** o **No Team**. Si apre un selettore del ruolo esatto; fare clic sul giocatore non cambia il suo ruolo a rotazione.
3. Assegna almeno un Runner e un Hunter. I giocatori online senza assegnazione possono diventare Hunter all'avvio della partita; gli spettatori non occupano il posto richiesto da nessuna delle due squadre.
4. Controlla **Match Settings**, **GrimAC Security** e **Global Language**. Disattiva Server Freeze prima di iniziare.
5. Apri **Match Controls → Start Match**. Gli inventari dei partecipanti vengono preparati/svuotati, viene riprodotta l'introduzione e la roulette sceglie il ritardo iniziale degli Hunter.

### Home: `/mhgui` (cinque righe)

| Posizione | Pulsante | Azione |
|---|---|---|
| R2 C2 | Match Controls | Avvio, pausa/ripresa, rilascio e reset. |
| R2 C4 | Player Roles | Apre l'elenco dei ruoli dei giocatori online. |
| R2 C6 | Match Settings | Fuoco amico, kit, spawn, riconnessione e preimpostazioni. |
| R2 C8 | Player Management | Scegli un bersaglio e usa gli strumenti per giocatori/mondo. |
| R4 C2 | GrimAC Security | Apre le impostazioni di protezione. |
| R4 C4 | Global Language | Scegli la lingua usata per tutti. |
| R4 C6 | Administrator Guide | Aggiunge all'inventario il libro dell'amministratore localizzato. |
| R5 C5 | Close | Chiude il menu. |

Il faro in R1 C5 indica lo stato della partita e il numero di Runner/Hunter.

### Match Controls (cinque righe)

| Posizione | Pulsante | Azione |
|---|---|---|
| R2 C2 | Start Match | Avvia la sequenza completa. |
| R2 C4 | Pause Match / Resume Match | Mette in pausa o riprende il gioco e i timer della partita; disponibile per una partita RUNNING. |
| R2 C6 | Release Hunters | Termina in anticipo l'attuale periodo di attesa degli Hunter. |
| R2 C8 | Reset Match | Apre la conferma, quindi reimposta completamente la partita. |
| R4 C2 | Server Freeze | Attiva/disattiva il blocco globale dei giocatori non OP. |
| R4 C4 | Teleport Everyone | Apre la conferma, quindi porta da te tutti i giocatori online. |
| R4 C6 | Match Info | Invia il rapporto sulla partita e sulle squadre. |

**Back** è in R5 C1; **Close** è in R5 C9. Server Freeze è separato da Pause Match: usa Pause quando l'orologio e i sistemi di gioco devono fermarsi insieme.

### Player Roles

L'elenco dei giocatori, su sei righe, mostra fino a 45 riquadri di ruolo con nome, ordinati per nome del giocatore, nelle prime cinque righe. Runner usa cemento verde lime, Hunter cemento rosso, Spectator un occhio di Ender e No Team cemento grigio. La riga inferiore contiene **Previous Page** in C1, le informazioni sulla pagina/sui giocatori online in C3, **Back to Control Center** in C5 e **Next Page** in C9.

Fai clic su un giocatore per aprire **Choose Player Role** (tre righe):

| Posizione | Ruolo esatto |
|---|---|
| R2 C2 | Runner |
| R2 C4 | Hunter |
| R2 C6 | Spectator |
| R2 C8 | No Team |

Il nome/ruolo attuale del giocatore appare in R1 C5; **Back** è in R3 C1 e **Close** in R3 C9. I ruoli possono cambiare durante una partita. Cambiare il ruolo dell'ultimo Runner assegnato da Runner a un altro ruolo durante RUNNING apre la conferma **Last Runner: the match will end**. Applicare la modifica può assegnare la vittoria agli Hunter. I comandi diretti dei ruoli si applicano immediatamente, quindi usali con attenzione. Qui è possibile assegnare No Team; la normale sincronizzazione all'avvio/all'accesso può trasformare un giocatore non assegnato in un Hunter durante una partita attiva.

### Spettatori

Un amministratore assegna il ruolo con `/mspectator <player>` oppure sceglie **Spectator** in Player Roles. Il comando verifica l'accesso amministratore anche se il suo descrittore non contiene una riga di autorizzazione. I giocatori non si iscrivono autonomamente eseguendo `/mhspectate`.

Uno spettatore riceve una bussola **Spectator teleport** nel primo slot della barra rapida. Tienila nella mano principale e fai clic destro, oppure usa `/mhspectate`, per aprire il menu di teletrasporto su sei righe. Il menu funziona solo mentre il giocatore ha il ruolo Spectator. Le prime cinque righe contengono fino a 45 Runner/Hunter vivi e online, ordinati per nome; fai clic su un riquadro di ruolo con nome per teletrasportarti alla posizione attuale di quel giocatore, anche in un altro mondo. La riga inferiore contiene **Previous Page** in C1, **Close** in C5 e **Next Page** in C9. Se non ci sono partecipanti adatti, R3 C5 mostra **No players available**. Chiudendo questo menu rimani uno spettatore.

Gli spettatori volano, sono nascosti agli altri giocatori, non hanno collisioni e sono protetti dai danni. L'implementazione usa la modalità Avventura con il volo; non concede la telecamera della modalità Spettatore vanilla né il movimento attraverso i blocchi. Blocca gli attacchi, la rottura/il piazzamento di blocchi, le normali interazioni con blocchi/entità, la raccolta/il lancio di oggetti, lo scambio con la mano secondaria, i clic/trascinamenti nell'inventario, la manipolazione dei supporti per armature e la raccolta/l'acquisizione di esperienza. I mob non possono prenderli di mira e le variazioni della fame vengono annullate. `/teammsg <message>` raggiunge gli altri giocatori con il ruolo Spectator. Non comunicare ai concorrenti le posizioni dei partecipanti o altri aiuti esterni.

Per uscire, un amministratore assegna **Runner**, **Hunter** o **No Team**, oppure usa `/mrunner <player>` o `/mhunter <player>`. Non esiste un comando/pulsante dedicato per uscire autonomamente. L'uscita ripristina l'inventario/il cursore salvati, la posizione, la modalità di gioco, il volo, le collisioni e lo stato di immunità, quindi applica il comportamento del nuovo ruolo nella partita. Lo stato dello spettatore viene salvato per il rientro. Un reset completo della partita ripristina lo stato degli spettatori, cancella i ruoli e sposta i giocatori online a uno spawn sicuro dell'Overworld quando disponibile. La normale pulizia di fine partita esclude gli spettatori dalla gestione degli oggetti/del volo dei partecipanti.

### Match Settings (cinque righe)

| Posizione | Pulsante | Azione |
|---|---|---|
| R2 C2 | Friendly Fire | Attiva/disattiva i danni ai compagni di squadra. |
| R2 C4 | Smart Hunter Kit | Attiva/disattiva i kit adattivi degli Hunter alla rinascita. |
| R2 C6 | Auto World Spawn | Apre la selezione dell'intervallo. |
| R2 C8 | Reconnect Grace | Apre la selezione della durata di riconnessione dei Runner. |
| R4 C2 | Match Preset | Scegli Classic, Fast, Hardcore o Custom. |
| R4 C4 | Reset Settings | Conferma le impostazioni bilanciate: Kit ON, Spawn 15m, Reconnect 15m. |
| R4 C6 | Random Head Start | Riquadro informativo; la roulette continua a scegliere il ritardo. |

**Back** è in R5 C1; **Close** in R5 C9.

Il selettore **Reconnect Grace** su tre righe offre **1, 5, 10, 15, 20, 30 minuti** in R2 C2–C7, in quest'ordine. Un clic salva il valore e lascia aperto il selettore. Back è in R3 C1; Close in R3 C9.

Il selettore **Match Preset** su tre righe dispone **Classic**, **Fast**, **Hardcore**, **Custom** in R2 C2, C4, C6, C8. Classic: Kit ON, Spawn 15m, Reconnect 15m. Fast: ON, 5m, 10m. Hardcore: OFF, OFF, 5m. Custom conserva le attuali impostazioni manuali. Le preimpostazioni mantengono il ritardo iniziale casuale. La selezione lascia aperto questo menu; Back è in R3 C1, Close in R3 C9.

**Auto World Spawn** offre OFF, 5m, 10m in R2 C2, C3, C4 e 15m, 20m, 30m in R2 C6, C7, C8. Back è in R3 C5. Seleziona un intervallo oppure usa `/mhspawn <off|5|10|15|20|30|status>`. Sposta lo spawn dell'Overworld vicino a un Runner adatto nell'Overworld; può saltare l'operazione se nessuno è adatto. `/mhkit <on|off|toggle|status>` controlla direttamente i kit.

### Player Management (sei righe)

| Posizione | Pulsante | Si applica a |
|---|---|---|
| R1 C5 | Target Player | Apre un selettore di giocatori per nome. |
| R2 C2 | Full Heal | Tutti i giocatori online. |
| R2 C4 | Full Hunger | Tutti i giocatori online. |
| R2 C6 | Clear Effects | Tutti i giocatori online. |
| R2 C8 | Freeze Target | Giocatore selezionato. |
| R4 C2 | Clear Target Inventory | Giocatore selezionato; conferma obbligatoria. |
| R4 C4 | Kill Target | Giocatore selezionato; conferma obbligatoria e si applicano le normali conseguenze della partita. |
| R4 C6 | Set Day | Il tuo mondo attuale. |
| R4 C8 | Clear Weather | Il tuo mondo attuale. |
| R5 C2 | Clear Dropped Items | Il tuo mondo attuale; conferma obbligatoria. |
| R5 C4 | Emergency Sync | Aggiorna i sistemi dei ruoli/di esecuzione per i giocatori online. |
| R5 C6 | Freeze Team | Clic sinistro: Runner; clic destro: Hunter; Maiusc-clic: rimuove questi blocchi di squadra/individuali. |

Back è in R6 C1; Close in R6 C9. La selezione del bersaglio non cambia i ruoli. Il selettore offre 28 altri giocatori online per pagina, nelle righe 2–5, colonne 2–8; fai clic su un nome per selezionarlo e tornare indietro. Previous/Back/Next sono in R6 C1/C5/C9. Ricontrolla il bersaglio visualizzato prima di applicare un'azione.

### Schermate di conferma

Reset Match, Teleport Everyone, Reset Settings, Clear Target Inventory, Kill Target, Clear Dropped Items e la modifica dell'ultimo Runner tramite GUI usano una schermata separata **Confirm Action** su tre righe. Leggi l'azione/il bersaglio in R1 C5, quindi fai clic sul pulsante verde **Confirm** in R2 C3 o sul pulsante rosso **Cancel** in R2 C7. La conferma scade dopo **30 secondi**. Bersagli cambiati/offline o ruoli modificati richiedono una nuova selezione. Questo sostituisce le istruzioni della vecchia guida sui clic ripetuti entro cinque/otto secondi per questi nuovi percorsi nei menu.

### GrimAC Security e lingua

Il menu Grim su sei righe ha lo stato in R1 C5; i controlli di attivazione/disattivazione in R2 C2 **GrimAC Master**, C4 **Movement**, C6 **Combat**, C8 **Packets**; R4 C2 **Velocity / AntiKB**, C4 **World / Scaffold**, C6 **Anti X-Ray**, C8 **Admin Alerts**; e R5 C5 **Monitor mode**. Back è in R6 C1 e Close in R6 C9. Monitor mode controlla l'uso di avvisi/prove rispetto all'applicazione delle sanzioni. Paper Anti-Xray è indipendente e richiede un riavvio dopo le modifiche. Questi sono i controlli di GrimAC; la vecchia descrizione del menu VexAC/AutoClick non descrive questa versione.

Global Language si applica a tutti e aggiorna menu/oggetti. Fai clic sulla lingua indicata per nome; Back è in R3 C5. `/mhlang` apre lo stesso selettore e `/mhhelp` fornisce la guida localizzata per giocatori/amministratori.

### Valori predefiniti attuali, riconnessione e moderazione

I valori di ripiego per una nuova configurazione in `plugins/VexLandManhunt/config.yml` sono:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` significa che lo spostamento automatico dello spawn è disattivato. Reset Settings e Classic scelgono invece 15 minuti. Durante la finestra di riconnessione di un Runner, il suo posto viene mantenuto; un ritorno tempestivo fornisce dieci secondi di protezione. Il tempo di inattività del server salvato viene escluso. La scadenza può trasformare il Runner in un Hunter oppure terminare la partita con la vittoria degli Hunter. Pause/Resume blocca i sistemi di gioco e regola il conteggio del tempo della partita attiva. I file di ripristino sono gestiti dal plugin.

Le impostazioni del bridge Grim vengono conservate in `plugins/VexLandManhunt/grim-settings.yml`. I valori predefiniti iniziali sono Master ON, tutti e cinque i gruppi ON, Admin Alerts ON e **Monitor mode OFF: l'applicazione delle sanzioni è abilitata**. Monitor mode accoda prove/avvisi e annulla le segnalazioni che soddisfano i criteri. Nella modalità di applicazione delle sanzioni, il bridge può trasformare un comando di espulsione di Grim in una disconnessione localizzata che consente la riconnessione; non stabilisce una politica di ban permanenti. Le soglie effettive dipendono anche dalla configurazione di Grim. Le prove vengono accodate in `plugins/VexLandManhunt/anticheat/grim-evidence.log`; le code di dimensione limitata possono scartare voci sotto carico. Il bridge esenta gli spettatori, il gioco in pausa/bloccato e determinati contesti con veicoli, con tre secondi di tolleranza dopo l'accesso, il teletrasporto e la rinascita. Non viene dichiarato alcun benchmark di precisione o prestazioni dell'anti-cheat.

## Riferimento dei comandi pubblici — 1.13.1

L'accesso amministratore significa OP o `vexland.admin` (predefinito OP). Il gestore di `/mspectator <player>` lo verifica nonostante l'assenza di una riga di autorizzazione nel descrittore. I comandi diretti dei ruoli si applicano immediatamente; cambiare l'ultimo Runner durante RUNNING può terminare la partita. La GUI fornisce una conferma per questa situazione.

| Comando | Scopo | Accesso |
|---|---|---|
| `/mhgui` | Apre il centro di controllo suddiviso per categorie | Amministratore |
| `/mhstart` | Avvia la sequenza completa della partita | Amministratore |
| `/mhreset` | Reimposta completamente la partita | Amministratore |
| `/mhrelease` | Rilascia gli Hunter in attesa | Amministratore |
| `/mrunner <player>` | Assegna Runner | Amministratore |
| `/mhunter <player>` | Assegna Hunter | Amministratore |
| `/mspectator <player>` | Assegna Spectator | Amministratore; nuovo |
| `/mhspectate` | Apre il menu di teletrasporto ai partecipanti | Spectator attuale; nuovo |
| `/teammsg <message>` | Invia al proprio ruolo/alla propria squadra | Giocatore |
| `/trash` | Inventario temporaneo di 54 slot per eliminare oggetti; alias `/mhtrash`, `/vextrash` | Giocatore |
| `/nv` | Attiva/disattiva la visione notturna personale | Giocatore |
| `/mhlang` | Apre il selettore della lingua globale | Amministratore |
| `/mhkit <on\|off\|toggle\|status>` | Configura i kit adattivi degli Hunter | Amministratore |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Configura lo spostamento dello spawn | Amministratore |
| `/mhhelp` | Riceve la guida localizzata per ruolo/amministratore | Giocatore / amministratore |
| `/mhpause` | Mette in pausa la partita in corso | Amministratore |
| `/mhresume` | Riprende la partita in pausa | Amministratore |
| `/mhdebug` | Diagnostica interna | Amministratore |

`/mhnone` non è registrato in questa versione; usa il ruolo No Team nella GUI. Gli Hunter fanno clic destro sulla propria bussola di tracciamento per scegliere un Runner; questa funzione è separata dal teletrasporto degli spettatori e dal selettore del bersaglio dell'amministratore. I Runner vincono sconfiggendo l'Ender Dragon; gli Hunter vincono quando non rimane alcun Runner. Un Runner caduto diventa un Hunter se rimangono altri Runner.

## Lingue, cronologia e riconoscimenti di terze parti

Il plugin originale offre **10 lingue di gioco**: inglese, persiano, arabo, spagnolo, francese, tedesco, russo, cinese semplificato, hindi e portoghese. `/mhlang` seleziona una lingua per tutto il server, conservata in `language.txt`. Il manuale GitHub ha **18 lingue**, escludendo un'edizione della documentazione in arabo. Il giapponese e le altre lingue aggiuntive dei README non aggiungono traduzioni di gioco ai JAR invariati.

La [cronologia delle versioni](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/CHANGELOG.md) documenta ogni build fornita. Il manuale precedente completo di 1.9.11 / 1.6.4 è conservato nell'[archivio delle versioni](archive/1.9.11/README.it.md). La build dedicata agli spettatori è stata ora fornita e pubblicata come 1.13.1; le sue funzionalità non devono essere attribuite ai download precedenti.

**GrimAC è un progetto indipendente dei contributori di GrimAC, distribuito con licenza GPL-3.0.** Bardiya e Ali hanno creato Vexland_Manhunt e la sua integrazione; non sono accreditati come autori di GrimAC. Il JAR di Grim fornito corrisponde all'artefatto ufficiale Bukkit 2.3.73 su Modrinth per SHA-512 e SHA-1. Il commit sorgente incorporato corrisponde a [upstream v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73). La versione include binari invariati, checksum, lo snapshot del sorgente upstream, la licenza e le [note sulle componenti di terze parti](../THIRD_PARTY_NOTICES.md). Queste note sulle componenti non assegnano una licenza al progetto Manhunt separato.

## Una sfida scherzosa a Dream

Una piccola provocazione Minecraft da Bardiya 😄

> "Uff... Ali e io abbiamo fatto un plugin Manhunt cento volte migliore di quello di Dream, ma Dream ha paura e non vuole giocare con il nostro!"

## Creatori e ambito del progetto

**Creato insieme da [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) e [Ali · Alivexor](https://github.com/Alivexor).** Entrambi gli account sono registrati come autori anche nei descrittori originali del plugin.

Questo repository presenta le versioni compilate originali, la documentazione e le note di versione come progetto di portfolio condiviso. Le descrizioni delle funzionalità si basano sull’ispezione statica dei JAR forniti. Compatibilità su server attivi, prestazioni del recupero, bilanciamento e precisione dell’anti-cheat non sono stati testati in questo processo di pubblicazione.

[Portfolio GitHub di Bardiya](https://github.com/FarlandGame) · [GitHub di Ali](https://github.com/Alivexor) · [Tutte le versioni](https://github.com/FarlandGame/Vexland_Manhunt/releases)
