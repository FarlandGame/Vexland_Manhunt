# Vexland_Manhunt

[English](../README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**Ein vollständiges Minecraft-Erlebnis mit Runnern gegen Hunter, gemeinsam entwickelt von [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) und [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt vereint Spielvorbereitung, Teamrollen, den Beginn der Verfolgung, Ortung, Fortschritt, Belohnungen, Ergebnisse und Verwaltung in einem Plugin für Paper-Server. Runner versuchen, den Enderdrachen zu besiegen; Hunter versuchen, den letzten Runner auszuschalten. Das Plugin unterstützt mehrere Runner und hält die Jagd bei Todesfällen, Respawns, Dimensionswechseln und erneuten Verbindungen am Laufen. Die Steuerzentrale `/mhgui` ermöglicht Administratoren die Verwaltung über Menüs und bietet Spielern übersetzte Nachrichten und Anleitungsbücher.

## Downloads und Kompatibilität

| Datei / Version | Download | Zweck |
|---|---|---|
| **1.13.1 — aktuell** | [VexLandManhunt-1.13.1.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/VexLandManhunt-1.13.1.jar) | Manhunt-Plugin von Bardiya und Ali |
| **GrimAC 2.3.73 — erforderlich** | [grimac-bukkit-2.3.73.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/grimac-bukkit-2.3.73.jar) | Separate Anti-Cheat-Abhängigkeit eines Drittanbieters |
| 1.9.11 — archiviert | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Vorheriger Manhunt-Build |
| 1.6.4 — archiviert | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Früherer Manhunt-Build |

**Zielplattform: Paper 1.21.11, Java 21.** Die Nummern 1.6.4, 1.9.11 und 1.13.1 bezeichnen Plugin-Versionen, keine unterstützten Minecraft-Versionen. In 1.13.1 ist GrimAC eine zwingende Abhängigkeit; die Anbindung benötigt die API 2.3.73. Lade **beide aktuellen JARs** herunter. Dies sind Server-Plugins; Spieler installieren sie nicht im Mods-Ordner ihres Clients.

Dies sind ursprüngliche Builds für einen privaten Server mit besonderen erweiterten Administratorrechten für die Ersteller, unverändert wie bereitgestellt. Dieses Handbuch beschreibt die öffentlichen Manhunt-Bedienelemente.

## Das Manhunt-Erlebnis

- **Runner- und Hunter-Teams:** Weise angemeldete Spieler einer Seite zu. Ein Spiel benötigt mindestens einen Runner und einen Hunter oder einen angemeldeten Spieler ohne Rolle. Überlebende Runner spielen nach dem Tod eines Teammitglieds weiter; ein gestorbener Runner wird zum Hunter, sofern dieser Tod das Spiel nicht beendet.
- **Inszenierter Spielbeginn:** Inventare und Spielmodi werden vorbereitet, die Teams vorgestellt und der Vorsprung der Runner per Roulette bestimmt. Während dieses Countdowns sind Hunter eingefroren, begleitet von Titeln und Tönen. Der Vorsprung ist zufällig; Administratoren können Hunter vorzeitig freigeben.
- **Ortungskompass mit Zielauswahl:** Hunter erhalten einen besonderen Kompass. Rechtsklick öffnet die Runner-Zielauswahl; das Ziel lässt sich während der Jagd wechseln. Über Dimensionsgrenzen hinweg folgt die Ortung der passenden Portalroute, bis direkte Ortung möglich wird. Hunter erhalten den Kompass nach dem Respawn erneut.
- **Fortschrittsanzeigen:** Bossleisten und Spielinformationen verfolgen Runner-Ausrüstung und Fortschritt über Nether-Ressourcen, Lohenruten, Perlen, Enderaugen, die Festung und das Ende. Die neuere Version ergänzt genauere Stufen und Fortschrittsanzeigen anhand der Drachen-Lebenspunkte.
- **Belohnungen für Runner-Kills:** Tötet ein Runner während eines aktiven Spiels einen Hunter, wird ein fortschrittsabhängig gewichteter Belohnungspool mit 50 Einträgen verwendet. Animierte Ziehungen, doppelte/dreifache Belohnungen, Ankündigungen von Serien und Feiern seltener Gegenstände gehören dazu.
- **Sieg und Ergebnisse:** Der Tod des letzten Runners bedeutet den Sieg der Hunter; der besiegte Enderdrache den Sieg der Runner. Titel zum Spielende, Feiern, Kill-/Todesinformationen und die Bereinigung temporärer Gegenstände sind enthalten. Die neuere Version zeigt zusätzlich MVP-, Schadens- und Distanzresultate.
- **Teamkommunikation und Hilfsmittel:** Private Teamnachrichten mit `/teammsg`, ein Wegwerfinventar mit 54 Plätzen über `/trash` und persönliche Nachtsicht mit `/nv`.
- **Verwaltung über Menüs:** Rollen, Start/Zurücksetzen, vorzeitige Hunter-Freigabe, Teamschaden, Serversperre, Teleportieren aller Spieler, Heilen/Sättigen, Sprache, Schutzoptionen, Status und Anleitungsbücher stehen in der Steuerzentrale bereit. Einfrieren und vollständiges Zurücksetzen helfen beim Vorbereiten der nächsten Runde.
- **Übersetzte Anleitungen:** Bücher für Runner, Hunter und Administratoren erklären Ziele, Kompass, Todesfälle, Vorbereitung und Befehle. Version 1.9.11 bietet Spielern mit `/mhhelp` eine rollenabhängige Anleitung.
- **Paper-Anti-Xray-Integration:** Menüoptionen konfigurieren Papers Schutz auf Weltebene; Änderungen benötigen einen Serverneustart.

## Was ist neu in 1.13.1?

Im Vergleich zum bereitgestellten Build 1.9.11:

- **Geisterzuschauer:** eine eigene Rolle, Zuweisung durch Administratoren, geschütztes Fliegen, verborgene Spieler, gespeicherter und wiederhergestellter Zustand sowie ein mehrseitiges Teleportmenü für Teilnehmer.
- **Überarbeitete Steuerzentrale:** kategorisierte Menüs, direkte Auswahl zwischen vier Rollen, Zielauswahl nach Spielernamen, Auswahl der Wiederverbindungsfrist, Voreinstellungen Classic/Fast/Hardcore/Custom und eigene Bestätigungsseiten mit 30 Sekunden Gültigkeit.
- **GrimAC-Anbindung:** das erforderliche GrimAC 2.3.73 ersetzt den aktiven VexAC-Startpfad. Hauptschalter, fünf Prüfgruppen, Meldungen und Überwachungs-/Durchsetzungsmodus sind über die Oberfläche erreichbar. Paper Anti-Xray bleibt unabhängig.
- **Neuer Smart Hunter Kit-Planer:** passt Ausrüstung und Vorräte an Ausrüstung/Verzauberungen der Runner, den nächsten Runner, Teamgrößen, Entfernung, Dimension und Gelände an. Bessere vorhandene Ausrüstung bleibt erhalten, doppelte Werkzeuge werden vermieden und Vorräte anhand eines 30-Sekunden-Verlaufs begrenzt aufgefüllt. Dies garantiert weder einen festen Ausrüstungsabstand noch eine gemessene Spielbalance.
- **Validierte Wiederherstellung:** mit SHA-256 versiegelte Momentaufnahmen, Schema-/Zustandsprüfung und Rückgriff auf gültige Sicherungen; ungültige oder neuere Formate werden unverändert aufbewahrt. Der Zuschauerzustand wird separat gespeichert.
- **Erweiterte Meldungen:** die übersetzten Schlüssel wachsen je mitgelieferter Übersetzung von 683 auf 762, weiterhin in denselben zehn Spielsprachen. Zwei neue öffentliche Befehle sind registriert: `/mspectator <player>` und `/mhspectate`.
- **Sicherer Rücksetzungsfall:** findet sich keine sichere Oberfläche nahe dem Overworld-Spawn, kann das Zurücksetzen diesen Teleport überspringen, statt ihn zu erzwingen.

## Vollständige Einrichtung und Nutzung mit `/mhgui`

Stoppe den Server und sichere Welten und Plugin-Daten. Lege beide aktuellen JARs in `plugins/` ab; dort darf nur je eine Manhunt-JAR und eine GrimAC-JAR liegen. Behalte beim Aktualisieren vorhandene Einstellungen/Daten in `plugins/VexLandManhunt/`. Starte den Paper-1.21.11-/Java-21-Server vollständig; starte beim Austausch von Builds vollständig neu. GrimAC muss erfolgreich laden. Der interne Plugin-Name bleibt `VexLandManhunt`.

Diese Anleitung beschreibt Plugin-Version **1.13.1** mit englischen Beschriftungen. Die Beschriftungen folgen der serverweiten Sprache. Zeilen werden von oben nach unten, Spalten von links nach rechts gezählt. Verwende einen normalen Linksklick, sofern keine besondere Aktion genannt wird. Diese Anleitung beruht auf statischer Prüfung; es wurde kein Minecraft-Server ausgeführt.

### Ein Match einrichten

1. Verwende `/mhgui` mit `vexland.admin` (Standard: OP).
2. Öffne **Player Roles**, klicke die Kachel eines benannten Spielers und wähle **Runner**, **Hunter**, **Spectator** oder **No Team**. Dabei öffnet sich die direkte Rollenauswahl; ein Klick auf den Spieler schaltet seine Rolle nicht zyklisch um.
3. Weise mindestens einen Runner und einen Hunter zu. Nicht zugewiesene verbundene Spieler können beim Matchstart zu Huntern werden; Zuschauer erfüllen den erforderlichen Platz keines Teams.
4. Prüfe **Match Settings**, **GrimAC Security** und **Global Language**. Schalte Server Freeze vor dem Start aus.
5. Öffne **Match Controls → Start Match**. Die Inventare der Teilnehmer werden vorbereitet/geleert, die Einführung läuft und das Roulette bestimmt den Vorsprung vor der Freigabe der Hunter.

### Startseite: `/mhgui` (fünf Zeilen)

| Position | Schaltfläche | Aktion |
|---|---|---|
| R2 C2 | Match Controls | Starten, pausieren/fortsetzen, freigeben und zurücksetzen. |
| R2 C4 | Player Roles | Die Rollenliste verbundener Spieler öffnen. |
| R2 C6 | Match Settings | Teambeschuss, Kits, Spawn, Wiederverbindung und Voreinstellungen. |
| R2 C8 | Player Management | Ein Ziel wählen und Spieler-/Weltwerkzeuge verwenden. |
| R4 C2 | GrimAC Security | Schutzeinstellungen öffnen. |
| R4 C4 | Global Language | Die Sprache für alle auswählen. |
| R4 C6 | Administrator Guide | Das übersetzte Administratorhandbuch ins Inventar legen. |
| R5 C5 | Close | Das Menü schließen. |

Das Leuchtfeuer bei R1 C5 zeigt Matchzustand und Runner-/Hunter-Anzahlen.

### Match Controls (fünf Zeilen)

| Position | Schaltfläche | Aktion |
|---|---|---|
| R2 C2 | Start Match | Den vollständigen Startablauf beginnen. |
| R2 C4 | Pause Match / Resume Match | Spiel und Matchzeit pausieren oder fortsetzen; für ein RUNNING-Match verfügbar. |
| R2 C6 | Release Hunters | Die aktuelle Wartezeit der Hunter vorzeitig beenden. |
| R2 C8 | Reset Match | Die Bestätigung öffnen und das Match anschließend vollständig zurücksetzen. |
| R4 C2 | Server Freeze | Die globale Sperre für Spieler ohne OP umschalten. |
| R4 C4 | Teleport Everyone | Die Bestätigung öffnen und anschließend alle verbundenen Spieler zu dir holen. |
| R4 C6 | Match Info | Den Match- und Teambericht senden. |

**Back** befindet sich bei R5 C1, **Close** bei R5 C9. Server Freeze ist von Pause Match getrennt: Verwende Pause, wenn Uhr und Spielsysteme gemeinsam angehalten werden sollen.

### Player Roles

Die sechszeilige Spielerliste zeigt auf den ersten fünf Zeilen bis zu 45 benannte Rollenkacheln, nach Spielernamen sortiert. Runner verwendet hellgrünen Beton, Hunter roten Beton, Spectator ein Enderauge und No Team grauen Beton. In der unteren Zeile liegen **Previous Page** bei C1, Seiten-/Online-Informationen bei C3, **Back to Control Center** bei C5 und **Next Page** bei C9.

Klicke einen Spieler, um **Choose Player Role** zu öffnen (drei Zeilen):

| Position | Direkte Rolle |
|---|---|
| R2 C2 | Runner |
| R2 C4 | Hunter |
| R2 C6 | Spectator |
| R2 C8 | No Team |

Name/aktuelle Rolle erscheinen bei R1 C5; **Back** liegt bei R3 C1 und **Close** bei R3 C9. Rollen können während eines Matches geändert werden. Wird dem letzten zugewiesenen Runner während RUNNING eine andere Rolle gegeben, öffnet sich die Bestätigung **Last Runner: the match will end**. Das Anwenden kann den Huntern den Sieg geben. Direkte Rollenbefehle wirken sofort; verwende sie bewusst. No Team kann hier zugewiesen werden; die gewöhnliche Start-/Beitrittssynchronisierung kann einen nicht zugewiesenen Spieler während eines aktiven Matches zum Hunter machen.

### Zuschauer

Ein Administrator weist `/mspectator <player>` zu oder wählt **Spectator** in Player Roles. Der Befehl prüft Administratorrechte, obwohl sein Deskriptor keine Berechtigungszeile enthält. Spieler melden sich durch `/mhspectate` nicht selbst als Zuschauer an.

Ein Zuschauer erhält im ersten Schnellzugriffsplatz einen Kompass **Spectator teleport**. Halte ihn in der Haupthand und klicke rechts, oder verwende `/mhspectate`, um das sechszeilige Teleportmenü zu öffnen. Das Menü funktioniert nur mit der Rolle Spectator. Die ersten fünf Zeilen enthalten bis zu 45 lebende, verbundene Runner/Hunter, nach Namen sortiert; klicke eine benannte Rollenkachel, um zum aktuellen Standort dieses Spielers zu teleportieren, auch in eine andere Welt. Unten liegen **Previous Page** bei C1, **Close** bei C5 und **Next Page** bei C9. Gibt es keinen geeigneten Teilnehmer, steht bei R3 C5 **No players available**. Das Schließen des Menüs beendet die Zuschauerrolle nicht.

Zuschauer fliegen, sind für andere Spieler verborgen, kollidieren nicht und sind vor Schaden geschützt. Die Implementierung verwendet Adventure-Modus mit Flugfähigkeit; sie gewährt weder die Vanilla-Zuschauerkamera noch Bewegung durch Blöcke. Angriffe, Blockabbau/-platzierung, gewöhnliche Block-/Entitätsinteraktionen, Aufheben/Abwerfen von Gegenständen, Nebenhandtausch, Inventarklicks/-ziehen, Rüstungsständermanipulation und Erfahrungssammlung/-gewinn werden blockiert. Mobs können sie nicht anvisieren und Hungeränderungen werden abgebrochen. `/teammsg <message>` erreicht andere Spieler mit der Rolle Spectator. Gib Teilnehmerstandorte oder andere Hilfen von außerhalb nicht an Wettkämpfer weiter.

Zum Verlassen weist ein Administrator **Runner**, **Hunter** oder **No Team** zu oder verwendet `/mrunner <player>` beziehungsweise `/mhunter <player>`. Es gibt keinen eigenen Befehl/Knopf zum selbstständigen Verlassen. Beim Verlassen werden gespeichertes Inventar/Cursor, Position, Spielmodus, Flugfähigkeit, Kollision und Unverwundbarkeitszustand wiederhergestellt; anschließend gilt das Matchverhalten der neuen Rolle. Der Zuschauerzustand wird für erneutes Beitreten gespeichert. Full Match Reset stellt den Zuschauerzustand wieder her, leert die Rollen und bewegt verbundene Spieler zu einem sicheren Overworld-Spawn, sofern verfügbar. Die normale Bereinigung am Matchende nimmt Zuschauer von der Gegenstands-/Flugbehandlung der Teilnehmer aus.

### Match Settings (fünf Zeilen)

| Position | Schaltfläche | Aktion |
|---|---|---|
| R2 C2 | Friendly Fire | Schaden unter Teammitgliedern umschalten. |
| R2 C4 | Smart Hunter Kit | Angepasste Wiederbelebungs-Kits für Hunter umschalten. |
| R2 C6 | Auto World Spawn | Intervallauswahl öffnen. |
| R2 C8 | Reconnect Grace | Auswahl der Runner-Wiederverbindungsfrist öffnen. |
| R4 C2 | Match Preset | Classic, Fast, Hardcore oder Custom wählen. |
| R4 C4 | Reset Settings | Ausgewogene Einstellungen bestätigen: Kit ON, Spawn 15m, Reconnect 15m. |
| R4 C6 | Random Head Start | Informationskachel; das Roulette bestimmt weiterhin die Verzögerung. |

**Back** liegt bei R5 C1, **Close** bei R5 C9.

Die dreizeilige Auswahl **Reconnect Grace** bietet **1, 5, 10, 15, 20, 30 Minuten** bei R2 C2–C7 in dieser Reihenfolge. Ein Klick speichert den Wert und lässt die Auswahl geöffnet. Back liegt bei R3 C1, Close bei R3 C9.

Die dreizeilige Auswahl **Match Preset** zeigt **Classic**, **Fast**, **Hardcore**, **Custom** bei R2 C2, C4, C6, C8. Classic: Kit ON, Spawn 15m, Reconnect 15m. Fast: ON, 5m, 10m. Hardcore: OFF, OFF, 5m. Custom behält die aktuellen manuellen Einstellungen. Die Voreinstellungen behalten den zufälligen Vorsprung bei. Das Menü bleibt nach der Auswahl offen; Back liegt bei R3 C1, Close bei R3 C9.

**Auto World Spawn** bietet OFF, 5m, 10m bei R2 C2, C3, C4 und 15m, 20m, 30m bei R2 C6, C7, C8. Back liegt bei R3 C5. Wähle ein Intervall oder verwende `/mhspawn <off|5|10|15|20|30|status>`. Der Overworld-Spawn wird in die Nähe eines geeigneten Overworld-Runners verlegt; ohne geeignetes Ziel kann der Vorgang ausfallen. `/mhkit <on|off|toggle|status>` steuert die Kits direkt.

### Player Management (sechs Zeilen)

| Position | Schaltfläche | Gilt für |
|---|---|---|
| R1 C5 | Target Player | Eine Auswahl nach Spielernamen öffnen. |
| R2 C2 | Full Heal | Alle verbundenen Spieler. |
| R2 C4 | Full Hunger | Alle verbundenen Spieler. |
| R2 C6 | Clear Effects | Alle verbundenen Spieler. |
| R2 C8 | Freeze Target | Ausgewählten Spieler. |
| R4 C2 | Clear Target Inventory | Ausgewählten Spieler; Bestätigung erforderlich. |
| R4 C4 | Kill Target | Ausgewählten Spieler; Bestätigung erforderlich, normale Matchergebnisse gelten. |
| R4 C6 | Set Day | Deine aktuelle Welt. |
| R4 C8 | Clear Weather | Deine aktuelle Welt. |
| R5 C2 | Clear Dropped Items | Deine aktuelle Welt; Bestätigung erforderlich. |
| R5 C4 | Emergency Sync | Rollen-/Laufzeitsysteme für verbundene Spieler aktualisieren. |
| R5 C6 | Freeze Team | Links: Runner; rechts: Hunter; Umschalt-Klick: diese Team-/Einzelsperren aufheben. |

Back liegt bei R6 C1, Close bei R6 C9. Die Zielauswahl verändert keine Rollen. Die Auswahl bietet pro Seite 28 andere verbundene Spieler in Zeilen 2–5, Spalten 2–8; ein Klick wählt den Namen und führt zurück. Previous/Back/Next liegen bei R6 C1/C5/C9. Prüfe das angezeigte Ziel vor der Aktion erneut.

### Bestätigungsseiten

Reset Match, Teleport Everyone, Reset Settings, Clear Target Inventory, Kill Target, Clear Dropped Items und die Änderung des letzten Runners über die Oberfläche verwenden eine separate dreizeilige Seite **Confirm Action**. Lies Aktion/Ziel bei R1 C5 und klicke das grüne **Confirm** bei R2 C3 oder das rote **Cancel** bei R2 C7. Die Bestätigung verfällt nach **30 Sekunden**. Bei geänderten/nicht mehr verbundenen Zielen oder geänderten Rollen ist eine neue Auswahl nötig. Dies ersetzt bei diesen neuen Menüwegen die wiederholten Klicks innerhalb von fünf/acht Sekunden aus der alten Anleitung.

### GrimAC Security und Sprache

Das sechszeilige Grim-Menü zeigt den Status bei R1 C5; Schalter bei R2 C2 **GrimAC Master**, C4 **Movement**, C6 **Combat**, C8 **Packets**; R4 C2 **Velocity / AntiKB**, C4 **World / Scaffold**, C6 **Anti X-Ray**, C8 **Admin Alerts** und R5 C5 **Monitor mode**. Back liegt bei R6 C1, Close bei R6 C9. Monitor mode wählt Meldungen/Beweise gegenüber Durchsetzung. Paper Anti-Xray ist unabhängig und benötigt nach Änderungen einen Neustart. Dies sind GrimAC-Bedienelemente; die alte Beschreibung des VexAC-/AutoClick-Menüs gilt für diese Version nicht.

Global Language gilt für alle und aktualisiert Menüs/Gegenstände. Klicke die benannte Sprache; Back liegt bei R3 C5. `/mhlang` öffnet dieselbe Auswahl, `/mhhelp` liefert die übersetzte Spieler-/Administratoranleitung.

### Aktuelle Standardwerte, Wiederverbindung und Moderation

Frische Konfigurations-Standardwerte in `plugins/VexLandManhunt/config.yml` sind:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` bedeutet, dass die automatische Spawn-Verlegung aus ist. Reset Settings und Classic wählen stattdessen 15 Minuten. Während der Wiederverbindungsfrist bleibt der Platz eines Runners erhalten; eine rechtzeitige Rückkehr gewährt zehn Sekunden Schutz. Gespeicherte Serverausfallzeit wird nicht mitgezählt. Nach Ablauf kann der Runner zum Hunter werden oder das Match zugunsten der Hunter enden. Pause/Resume hält Spielsysteme an und passt die aktive Matchzeit an. Wiederherstellungsdateien verwaltet das Plugin.

Die Grim-Anbindung speichert Einstellungen in `plugins/VexLandManhunt/grim-settings.yml`. Neue Standardwerte sind Master ON, alle fünf Gruppen ON, Admin Alerts ON und **Monitor mode OFF: Durchsetzung ist aktiviert**. Monitor mode reiht Beweise/Meldungen ein und bricht passende Flags ab. Im Durchsetzungsmodus kann die Anbindung einen Grim-Kickbefehl in eine übersetzte Trennung mit erlaubter Wiederverbindung umwandeln; sie legt keine dauerhafte Bannrichtlinie fest. Tatsächliche Schwellenwerte hängen auch von Grims Konfiguration ab. Beweise werden für `plugins/VexLandManhunt/anticheat/grim-evidence.log` eingereiht; begrenzte Warteschlangen können unter Last Einträge verwerfen. Die Anbindung nimmt Zuschauer, pausiertes/eingefrorenes Spiel und bestimmte Fahrzeugkontexte aus; nach Beitritt, Teleport und Wiederbelebung gelten drei Sekunden Schonfrist. Es wird keine gemessene Anti-Cheat-Genauigkeit oder Leistung behauptet.

## Öffentliche Befehlsreferenz — 1.13.1

Administratorzugriff bedeutet OP oder `vexland.admin` (Standard OP). Der Handler für `/mspectator <player>` prüft dies trotz fehlender Berechtigungszeile im Deskriptor. Direkte Rollenbefehle wirken sofort; das Ändern des letzten Runners während RUNNING kann das Match beenden. Die Oberfläche bietet für diesen Fall eine Bestätigung.

| Befehl | Zweck | Zugriff |
|---|---|---|
| `/mhgui` | Kategorisierte Steuerzentrale öffnen | Administrator |
| `/mhstart` | Vollständigen Matchablauf starten | Administrator |
| `/mhreset` | Match vollständig zurücksetzen | Administrator |
| `/mhrelease` | Wartende Hunter freigeben | Administrator |
| `/mrunner <player>` | Runner zuweisen | Administrator |
| `/mhunter <player>` | Hunter zuweisen | Administrator |
| `/mspectator <player>` | Spectator zuweisen | Administrator; neu |
| `/mhspectate` | Teilnehmer-Teleportmenü öffnen | Aktueller Spectator; neu |
| `/teammsg <message>` | An eigene Rolle/eigenes Team senden | Spieler |
| `/trash` | Wegwerf-Inventar mit 54 Plätzen; Aliase `/mhtrash`, `/vextrash` | Spieler |
| `/nv` | Persönliche Nachtsicht umschalten | Spieler |
| `/mhlang` | Globale Sprachauswahl öffnen | Administrator |
| `/mhkit <on\|off\|toggle\|status>` | Angepasste Hunter-Kits konfigurieren | Administrator |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Spawn-Verlegung konfigurieren | Administrator |
| `/mhhelp` | Übersetzte Rollen-/Administratoranleitung erhalten | Spieler / Administrator |
| `/mhpause` | Laufendes Match pausieren | Administrator |
| `/mhresume` | Pausiertes Match fortsetzen | Administrator |
| `/mhdebug` | Interne Diagnose | Administrator |

`/mhnone` ist in dieser Version nicht registriert; verwende No Team in der Oberfläche. Hunter wählen per Rechtsklick auf ihren Tracker-Kompass einen Runner; dies ist von Zuschauerteleport und Administrator-Zielauswahl getrennt. Runner siegen durch das Besiegen des Enderdrachen; Hunter siegen, wenn kein Runner übrig ist. Ein gefallener Runner wird zum Hunter, wenn andere Runner verbleiben.

## Sprachen, Verlauf und Drittanbieterangaben

Das ursprüngliche Plugin bietet **10 Spielsprachen**: Englisch, Persisch, Arabisch, Spanisch, Französisch, Deutsch, Russisch, vereinfachtes Chinesisch, Hindi und Portugiesisch. `/mhlang` wählt eine Sprache für den ganzen Server, gespeichert in `language.txt`. Das GitHub-Handbuch bietet **18 Sprachen**, ohne arabische Dokumentationsausgabe. Japanisch und andere zusätzliche README-Sprachen ergänzen keine Spielübersetzungen in den unveränderten JARs.

Der [Versionsverlauf](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/CHANGELOG.md) dokumentiert jeden bereitgestellten Build. Das vollständige frühere Handbuch für 1.9.11 / 1.6.4 bleibt im [Versionsarchiv](archive/1.9.11/README.de.md) erhalten. Der eigene Zuschauer-Build wurde jetzt als 1.13.1 bereitgestellt und veröffentlicht; seine Funktionen dürfen älteren Downloads nicht zugeschrieben werden.

**GrimAC ist ein unabhängiges Projekt der GrimAC-Mitwirkenden, veröffentlicht unter GPL-3.0.** Bardiya und Ali schufen Vexland_Manhunt und dessen Anbindung; sie werden nicht als Autoren von GrimAC genannt. Die bereitgestellte Grim-JAR stimmt in SHA-512 und SHA-1 mit dem offiziellen Modrinth-Bukkit-Artefakt 2.3.73 überein. Ihr eingebetteter Quellcode-Commit entspricht [Upstream v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73). Die Veröffentlichung enthält unveränderte Binärdateien, Prüfsummen, den Upstream-Quellcode-Schnappschuss, Lizenz und [Drittanbieterhinweise](../THIRD_PARTY_NOTICES.md). Diese Komponentenhinweise legen keine Lizenz für das eigenständige Manhunt-Projekt fest.

## Eine scherzhafte Herausforderung an Dream

Ein bisschen Minecraft-Geplänkel von Bardiya 😄

> „Seufz ... Ali und ich haben ein Manhunt-Plugin gemacht, hundertmal besser als Dreams, aber Dream hat Angst und will unseres nicht spielen!“

## Entwickler und Projektumfang

**Gemeinsam entwickelt von [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) und [Ali · Alivexor](https://github.com/Alivexor).** Beide Namen sind auch als Autoren in den ursprünglichen Plugin-Deskriptoren verzeichnet.

Dieses Repository stellt originale kompilierte Releases, Dokumentation und Versionsnotizen als gemeinsames Portfolio-Projekt vor. Funktionsbeschreibungen beruhen auf statischer Untersuchung der bereitgestellten JARs. Kompatibilität im laufenden Server, Wiederherstellungsleistung, Balance und Anti-Cheat-Genauigkeit wurden im Rahmen dieser Veröffentlichung nicht getestet.

[Bardiyas GitHub-Portfolio](https://github.com/FarlandGame) · [Alis GitHub](https://github.com/Alivexor) · [Alle Releases](https://github.com/FarlandGame/Vexland_Manhunt/releases)
