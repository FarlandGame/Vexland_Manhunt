# Vexland_Manhunt


[English](../README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**Ein vollständiges Minecraft-Erlebnis mit Runnern gegen Hunter, gemeinsam entwickelt von [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) und [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt vereint Spielvorbereitung, Teamrollen, den Beginn der Verfolgung, Ortung, Fortschritt, Belohnungen, Ergebnisse und Verwaltung in einem Plugin für Paper-Server. Runner versuchen, den Enderdrachen zu besiegen; Hunter versuchen, den letzten Runner auszuschalten. Das Plugin unterstützt mehrere Runner und hält die Jagd bei Todesfällen, Respawns, Dimensionswechseln und erneuten Verbindungen am Laufen. Die Steuerzentrale `/mhgui` ermöglicht Administratoren die Verwaltung über Menüs und bietet Spielern übersetzte Nachrichten und Anleitungsbücher.

## Downloads und Kompatibilität

| Bereitgestellte Version | Download | Installation |
|---|---|---|
| **2.0.0 — kombiniertes Paket** | [VexLandManhunt-2.0.0.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0.jar) | **Eine JAR**, einschließlich integriertem GrimAC 2.3.73 |
| **1.13.1 — Zuschauer-Zweig** | [Version und beide JARs](https://github.com/FarlandGame/Vexland_Manhunt/releases/tag/v1.13.1) | Manhunt plus separates GrimAC 2.3.73 |
| 1.9.11 / 1.6.4 — älter | [Alle Versionen](https://github.com/FarlandGame/Vexland_Manhunt/releases) | Historische eigenständige Builds |

**Paper 1.21.11 / Java 21.** Dies sind Server-Plugins, keine Client-Mods. Der bereitgestellte Dateiname und die öffentliche Version lauten **2.0.0**, der unveränderte Deskriptor meldet jedoch **`1.9.11-grim.1`** und nennt 1.9.11 als Gameplay-Grundlage. Dieses kombinierte Paket enthält **nicht** die dedizierte Spectator-Rolle, `/mspectator <player>`, `/mhspectate`, kategorisierte Menüs oder andere Ergänzungen aus 1.13.1. Verwende weiterhin den separat aufgeführten Zweig 1.13.1, wenn du diese Funktionen benötigst.

Die ursprünglichen Builds für persönliche Server mit erstellerspezifischem erweitertem Administratorzugriff bleiben wie bereitgestellt erhalten. Die Anleitung behandelt die öffentlichen Bedienelemente.

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

## Was hat sich im bereitgestellten Paket 2.0.0 geändert?

- **Eine integrierte JAR:** Manhunt, modifiziertes GrimAC 2.3.73 und das mitgelieferte PacketEvents teilen sich eine Bukkit-Plugin-Instanz. Für dieses Paket ist keine separate Installation von GrimAC oder PacketEvents erforderlich. Der Deskriptor stellt `GrimAC` bereit; das Archiv ist zusammengeführt und enthält keine verschachtelte, unveränderte Grim-JAR.
- **Modulstatus:** Der Administratorbefehl `/vexintegration` meldet Grim ACTIVE/INACTIVE, den Bukkit-Eigentümer, den VexAC-Status, den PacketEvents-Status und die Anzahl erfasster Spieler. Native Befehle `/grim` und `/grimac` werden vom integrierten Modul registriert.
- **Kontrollierter Start:** Der Loader benötigt die Konfigurations-API von Paper und exakt Minecraft 1.21.11. Er verweigert das Laden im laufenden Betrieb bei anwesenden Spielern sowie eine separate GrimAC-Instanz. Wenn der integrierte Start fehlschlägt, wird das Plugin deaktiviert und protokolliert, dass der Grim-Schutz inaktiv ist; der Server selbst kann weiterlaufen. Prüfe den Status, bevor du ein Spiel startest.
- **Migration vorhandener Daten:** Beim ersten integrierten Laden sichert die Migration beide alten Plugin-Datenverzeichnisbäume und kopiert alte GrimAC-Daten nur, wenn das integrierte Ziel noch nicht existiert. Sind beide vorhanden, haben vorhandene integrierte Daten Vorrang; es erfolgt kein Zusammenführen oder Überschreiben. Die Originaldaten bleiben erhalten.
- **Zuständigkeit für Bewegungskorrekturen:** `plugins/VexLandManhunt/integration.properties` verwendet standardmäßig `movement-correction-owner=legacy`. Die unterstützte Alternative ist `grim`; andere Werte brechen den Start ab. Die Auswahl von grim unterdrückt VexAC-Korrekturpfade für Zurücksetzen/Teleportieren, während VexAC-Prüfungen, Warnungen und Belege bestehen bleiben. Sie deaktiviert nicht jede alte Sanktion.
- **Gameplay-Grundlage:** Das flache `/mhgui`, der Wechsel zwischen den Rollen Runner/Hunter, die VexAC-Steuerung, Smart Hunter Kit V3, Pause/Fortsetzen, Wiederherstellung und 683 übersetzte Schlüssel entsprechen 1.9.11. Dies ist eine kombinierte Paketierungs-/Integrationsversion, nicht der Funktionsumfang von 1.13.1 mit Zuschauerunterstützung.

## Von der Grundlage 1.9.11 übernommenes Gameplay

Die folgenden Systeme wurden der Grundlage 1.9.11 hinzugefügt und bleiben in diesem kombinierten Paket erhalten. Es handelt sich um übernommene Gameplay-Funktionen, nicht um neue Zuschauerfunktionen von 2.0.0.

| Ergänzung oder Änderung | Verhalten in 1.9.11 |
| --- | --- |
| **Smart Hunter Kit V3** | Adaptive Respawn-Ausrüstung berücksichtigt Runner-Ausrüstung, Teams und Spielkontext. Das System soll Hunter-Ausrüstung unter dem Durchschnitt der Runner halten und lässt sich mit `/mhkit` oder im Menü umschalten. |
| **Automatischer Oberwelt-Spawn** | Verschiebt den Welt-Spawn in die Nähe eines geeigneten Oberwelt-Runners: aus, alle 5, 10, 15, 20 oder 30 Minuten. Das System wählt eine sichere Oberfläche und überspringt ungeeignete Fälle. |
| **Pause und Fortsetzen** | `/mhpause` stoppt das Spielgeschehen und zugehörige Zeitgeber, Ortung und Spawn-Verschiebung; `/mhresume` setzt fort. Pausenzeit wird aus der aktiven Spielzeit herausgerechnet. |
| **Wiederherstellung nach Neustart/Absturz** | Eine Wiederherstellungsschicht stellt Spielzustand, Rollen, Kompassziele, Fortschritt, Belohnungs-/Todeszeitgeber und Wiederverbindungsstatus mit primären/gesicherten Schnappschüssen sowie regelmäßigen und abschließenden Speicherungen wieder her. |
| **Runner-Wiederverbindung** | Ein einstellbares Zeitfenster ersetzt die bisherigen festen 60 Minuten. Neuer Standard: 15 Minuten mit 10 Sekunden Schutz beim Wiedereintritt. Serverausfallzeit zählt nicht; Ablauf kann den Runner zum Hunter machen oder das Spiel beenden. |
| **Erweiterte Verwaltung** | Rollenänderung im laufenden Spiel unter Erhalt des letzten Runners; Aktionen für ausgewählte Spieler, Teamteleport/Einfrieren, Laufzeit-Synchronisierung und Abkürzungen erleichtern die Verwaltung. |
| **Bestätigtes Zurücksetzen der Einstellungen** | Zwei Klicks innerhalb von acht Sekunden setzen Smart Kit AN, automatischen Spawn alle 15 Minuten und Wiederverbindung auf 15 Minuten. Anders als bei einer neuen Installation ist automatischer Spawn danach nicht AUS. |
| **VexAC 3.0** | Prüfungen für Bewegung, Kampf, AutoClick, Geschwindigkeit/Rückstoß und Bauen; Gruppen-/Gesamtsteuerung, Beweisprotokolle, Administratorwarnungen sowie Ausnahmen für Umgebung und Verzögerungen. |
| **Ultra Deep Debug v4** | `/mhdebug` bietet Diagnosen für Zustandsautomat, GUI, synthetische Ausrüstungs-/Lasttests, Sprachplatzhalter, Wiederherstellungs-Rundlauf und Integrität. |
| **Erweiterte Anzeigen** | Genauere Fortschritte, Drachen-Lebenspunkte, MVP-/Schadens-/Distanzresultate und Ping-Informationen in TAB. |
| **Befehlsänderungen** | Ergänzt `/mhkit`, `/mhspawn`, `/mhpause`, `/mhresume` und `/mhdebug`; entfernt `/mhnone`; macht `/mhhelp` spieler-/administratorabhängig und ergänzt `/trash`-Aliasse. |
| **Mehr übersetzte Nachrichten** | Die Ressourcen wachsen von 446 auf 683 Nachrichtenschlüssel je Sprache. |

VexAC enthält Prüfungen für Fly, Speed, Timer, Phase, Step, NoSlow, GroundSpoof, Reach, KillAura, AimAssist, wall-hit, BadPackets, AutoClick-Zeitmuster, veränderten Rückstoß, Scaffold, Tower, FastPlace, Nuker und Blockreichweite. Die Oberfläche nennt einen reinen Beobachtungsmodus, während der kompilierte Code auch Kick-Pfade enthält; prüfe das tatsächliche Moderationsverhalten auf einem Testserver, bevor du dich auf diese Bezeichnung verlässt. Die frühere Version enthält stattdessen ältere Anti-AutoClick- und Anti-Fly-Schalter.

## Vollständige Einrichtung und Verwendung mit `/mhgui`

### 1. Den kombinierten Build installieren

1. Stoppe den Server mit **Paper 1.21.11 / Java 21** vollständig und sichere Welten und Plugin-Daten.
2. Lege nur `VexLandManhunt-2.0.0.jar` aus dieser Version in `plugins/` ab. Verschiebe ältere Manhunt-JARs und eigenständige GrimAC-JARs aus dem aktiven Plugin-Verzeichnis. Bewahre ihre Datenordner auf; lösche sie nicht. Spieler installieren diese JAR nicht auf dem Client.
3. Starte normal, statt `/reload` zu verwenden. Der integrierte Loader verwaltet den Lebenszyklus von Grim und PacketEvents.
4. Führe als OP oder mit `vexland.admin` den Befehl `/vexintegration` aus. Prüfe `Grim=ACTIVE` und `PacketEvents=true`, bevor du mit `/mhgui` fortfährst. Inaktiver Schutz ist ein Startproblem, keine erfolgreiche integrierte Installation.

Die Grim-Konfiguration befindet sich in `plugins/VexLandManhunt/grim/` (`config.yml`, `messages.yml`, `punishments.yml`, `discord.yml`), mit optionalem Verlauf in `violations.sqlite`. Die Sicherungen der ersten Migration werden in `plugins/VexLandManhunt-integration-backups/` abgelegt; `plugins/VexLandManhunt/integration-migration-v1.txt` kennzeichnet den Abschluss. Wenn sowohl alte als auch integrierte Grim-Daten existieren, bleibt das integrierte Ziel erhalten und eine Warnung wird protokolliert. Die Migration lehnt symbolische Links ab.

Prüfe die Zuständigkeit für Bewegungskorrekturen in `plugins/VexLandManhunt/integration.properties`; behalte die anderen Einstellungen bei. Standardwert bei einer Neuinstallation:

```properties
movement-correction-owner=legacy
```

Die vollständige Anleitung zu den öffentlichen Menüs unten folgt der Gameplay-Grundlage 1.9.11 dieses Pakets. Der Zuschauer-Zweig hat eine eigene archivierte Anleitung.

### 2. Die Steuerzentrale öffnen

Betritt den Server als Administrator mit **OP** oder der Berechtigung **`vexland.admin`** und gib ein:

```text
/mhgui
```

Die folgende Anleitung beschreibt die öffentliche Oberfläche der Plugin-Version **2.0.0** mit ihren englischen Schaltflächennamen. Die Beschriftungen folgen der ausgewählten Serversprache. Verwende für vollständigen GUI-Zugriff ein vertrauenswürdiges **OP**-Konto: Die Deskriptorberechtigung erlaubt das Öffnen des Befehls, einige bereitgestellte GUI-Handler prüfen OP jedoch strenger. Das Hauptinventar hat fünf Reihen mit je neun Plätzen. Fahre über eine Schaltfläche, um Beschreibung und aktuellen Wert zu lesen. Meist genügt ein normaler Klick; besondere Mausaktionen und Bestätigungen werden unten erklärt. Das kleinere 1.6.4-Menü folgt am Ende.

#### Dein erstes Spiel einrichten

1. Öffne **Player Roles**. Klicke auf den Kopf jedes Teilnehmers, bis die angezeigte Rolle stimmt. In 2.0.0 wechselt die Rolle zwischen **Runner** und **Hunter**; ein bisher nicht zugewiesener Teilnehmer wird beim ersten Klick Runner. Links-/Rechts-/Shift-Klick sind keine getrennten Rollenauswahl-Kürzel. Nutze bei Bedarf **Previous Page**, **Next Page** und **Back to Control Center**.
2. Weise mindestens einen Runner und einen Hunter zu. Der Startablauf kann übrige angemeldete Spieler ohne Rolle zu Huntern machen; explizite Zuweisung aller Teilnehmer macht die Teams eindeutig.
3. Klicke **Friendly Fire**, um Schaden unter Teammitgliedern zu erlauben oder zu verhindern. Kontrolliere danach die AN/AUS-Anzeige.
4. Wähle mit **Language** die serverweite Sprache. Das betrifft Nachrichten, Oberflächen, Hinweise und Anleitungsbücher für alle, nicht nur deinen Spieler.
5. Prüfe **Smart Hunter Kit**, **Auto World Spawn** und **Anti-Cheat**. Öffne bei Bedarf über die Buch-Schaltfläche die Administratoranleitung für Erklärungen im Spiel.
6. Stelle sicher, dass **Server Freeze** aus ist, und klicke **Start Match**. Der Start bereitet Spieler und Inventare vor, zeigt die Einführung und das zufällige Roulette für die Wartezeit der Hunter und beginnt die Jagd. Bewahre benötigte Gegenstände vor dem Start außerhalb der Teilnehmerinventare auf.

#### Hauptschaltflächen der Steuerzentrale

Die Positionen zählen Reihen von oben nach unten und Spalten von links nach rechts. Sie beschreiben das fertig dekorierte Layout von 2.0.0.

| Position | Englische Schaltfläche | Funktion |
|---|---|---|
| Reihe 2, Spalte 2 | Player Roles | Öffnet das mehrseitige Runner-/Hunter-Menü mit Spielerköpfen. |
| Reihe 2, Spalte 3 | Target Player | Wechselt zwischen anderen angemeldeten Spielern für Zielaktionen. Prüfe den aktuellen Zielnamen. |
| Reihe 2, Spalte 4 | Friendly Fire | Schaltet Schaden unter Teammitgliedern um. |
| Reihe 2, Spalte 5 | Match Info | Sendet einen Kurzbericht zu Zustand, Teams, Teamschaden und ausgewähltem Ziel. |
| Reihe 2, Spalte 6 | Start Match | Führt den normalen Start und die zufällige Vorsprungssequenz aus. |
| Reihe 2, Spalte 7 | Full Heal | Stellt die Gesundheit aller angemeldeten Spieler wieder her. |
| Reihe 2, Spalte 8 | Reset Match | Setzt das Spiel vollständig zurück. Anders als Reset Settings. |
| Reihe 3, Spalte 2 | Full Hunger | Stellt Nahrung und Sättigung aller angemeldeten Spieler wieder her. |
| Reihe 3, Spalte 3 | Release Hunters | Gibt wartende Hunter vor Ablauf des Vorsprungs frei. |
| Reihe 3, Spalte 4 | Clear Effects | Entfernt Trankeffekte aller angemeldeten Spieler. |
| Reihe 3, Spalte 5 | Server Freeze | Schaltet globales Einfrieren um; gewöhnliche Spieler ohne OP werden eingefroren. |
| Reihe 3, Spalte 6 | Clear Target Inventory | Leert nach Bestätigung Inventar, Rüstung und Nebenhand des ausgewählten Spielers. |
| Reihe 3, Spalte 7 | Teleport Everyone | Bringt alle angemeldeten Spieler zu deiner aktuellen Position. |
| Reihe 3, Spalte 8 | Kill Target | Tötet nach Bestätigung den ausgewählten Spieler; normale Todesregeln können das Spiel beeinflussen. |
| Reihe 4, Spalte 2 | Anti-Cheat | Öffnet die VexAC-Sicherheitssteuerung. |
| Reihe 4, Spalte 3 | Freeze Target | Schaltet das individuelle Einfrieren des ausgewählten Spielers um. |
| Reihe 4, Spalte 4 | Emergency Restore | Stellt Gesundheit, Nahrung und Sättigung aller angemeldeten Spieler wieder her. |
| Reihe 4, Spalte 5 | Freeze Team | Linksklick schaltet Runner um; Rechtsklick Hunter; Shift-Klick löst individuelle/Team-Einfrierungen. |
| Reihe 4, Spalte 6 | Set Day | Stellt deine aktuelle Welt auf Tag. |
| Reihe 4, Spalte 7 | Clear Weather | Beendet Regen und Gewitter in deiner aktuellen Welt. |
| Reihe 4, Spalte 8 | Language | Öffnet die globale Sprachauswahl. |
| Reihe 5, Spalte 2 | Smart Hunter Kit | Schaltet adaptive Hunter-Respawn-Ausrüstung um; zeigt AN/AUS. |
| Reihe 5, Spalte 3 | Clear Dropped Items | Entfernt fallengelassene Gegenstände in deiner aktuellen Welt. |
| Reihe 5, Spalte 4 | Pause Match / Resume Match | Stoppt oder setzt aktives Spielgeschehen und Spielzeitgeber fort. |
| Reihe 5, Spalte 5 | Emergency Sync | Synchronisiert Rollen, Kompasse und zugehörigen Laufzeitzustand erneut. |
| Reihe 5, Spalte 6 | Reset Settings | Stellt nach Bestätigung durch zwei Klicks ausgewogene Einstellungen wieder her. |
| Reihe 5, Spalte 7 | Close | Schließt die Steuerzentrale. |
| Reihe 5, Spalte 8 | Auto World Spawn | Öffnet die Intervallauswahl für automatischen Oberwelt-Spawn. |
| Reihe 5, Spalte 9 | Manhunt Administrator Guide | Gibt das übersetzte Administrator-Anleitungsbuch aus. |

Dekoratives Glas und Titel-/Statusgegenstände sind keine Spielschaltflächen.

#### Rollen und ausgewählte Ziele

**Player Roles** ändert das tatsächliche Manhunt-Team eines Teilnehmers. Klicke auf seinen Kopf und lies die aktualisierte Rolle. Während STARTING/RUNNING erlaubt die Oberfläche Runner-/Hunter-Wechsel, verhindert aber die Umwandlung des letzten Runners zum Hunter. So bleibt die Runner-Seite im laufenden Spiel erhalten. Ändere Rollen bewusst, da Team-Laufzeitzustand und Kompasse danach synchronisiert werden.

**Target Player** ist davon unabhängig: Es wählt jemanden für Freeze Target, Clear Target Inventory oder Kill Target, ohne sein Team zu ändern. Wechsle, bis der gewünschte angemeldete Spieler angezeigt wird. Ist ein gespeichertes Ziel nicht mehr verfügbar, kann der Code auf den ersten anderen angemeldeten Spieler zurückfallen; kontrolliere deshalb den Namen unmittelbar vor jeder Zielaktion. Ist niemand anderes online, meldet das System, dass kein Ziel verfügbar ist.

**Clear Target Inventory** und **Kill Target** benötigen zwei Klicks auf dieselbe Aktion für dasselbe Ziel innerhalb von **fünf Sekunden**. Der erste aktiviert die Bestätigung und nennt das Ziel; der zweite führt die Aktion aus. Zielwechsel oder zu langes Warten verlangen eine neue Bestätigung. Inventarleeren löscht den Inhalt; das Töten eines Runners kann das Spiel nach normalen Todesregeln ändern oder beenden.

**Freeze Team** hat die einzigen teamspezifischen Mauskurzbefehle dieses Menüs: normaler Linksklick wählt Runner, normaler Rechtsklick Hunter, Shift-Klick löst alle durch dieses Werkzeug verwalteten individuellen/Team-Einfrierungen. Globales Server Freeze ist ein eigener Schalter und muss separat ausgeschaltet werden, wenn Spieler weiterhin eingefroren sind.

#### Smart Hunter Kit

Klicke **Smart Hunter Kit**, um adaptive Hunter-Respawn-Ausrüstung ein- oder auszuschalten. Die Schaltfläche zeigt den Zustand. Bei aktivierter Funktion kann ein respawnender Hunter Ausrüstung passend zur Runner-Ausrüstung und zum Spielkontext erhalten; die mitgelieferte Spieleranleitung beschreibt sie als schwächer als den Runner-Durchschnitt. Bei ausgeschalteter Funktion erhalten Hunter nach dem Tod keine automatische Ausrüstung. Der Ortungskompass wird dadurch nicht abgeschaltet.

Für direktes Setzen statt Umschalten nutze `/mhkit on`, `/mhkit off` oder `/mhkit status`. Der untersuchte Standard-Rückfallwert einer neuen Konfiguration ist AN.

#### Auto World Spawn

Klicke **Auto World Spawn** und wähle **OFF**, **5 minutes**, **10 minutes**, **15 minutes**, **20 minutes** oder **30 minutes**. Eine Auswahl speichert das Intervall und führt zu `/mhgui` zurück; **Back** kehrt ohne neue Intervallauswahl zurück.

Bei Aktivierung sucht das System regelmäßig eine sichere Oberwelt-Oberfläche nahe einem aktiven Oberwelt-Runner und verschiebt den Welt-Spawn dorthin. Es überspringt die Verschiebung, wenn kein Runner in der Oberwelt ist oder kein sicherer Ort gefunden wird. Der Rückfallwert einer neuen Konfiguration ist AUS. Entsprechende Befehle sind `/mhspawn off`, `/mhspawn 15` und `/mhspawn status`; ersetze 15 durch ein beliebiges unterstütztes Intervall.

#### Pause, Wiederverbindung und Wiederherstellung

**Pause Match** ist im Zustand RUNNING verfügbar. Es stoppt Spielsysteme, Bewegung/Interaktionen, Spielzeitgeber, Ortung und Spawn-Verschiebung. **Resume Match** setzt sie fort und gleicht die Pausenzeit aus. Server Freeze friert nur Spieler ein und ersetzt keine Pause der Spieluhr.

Das Runner-Wiederverbindungsfenster ist einstellbar und fällt bei neuer Konfiguration auf **15 Minuten** zurück. Rechtzeitiges Zurückkehren stellt den Runner-Zustand wieder her und gibt zehn Sekunden Wiedereintrittsschutz. Serverausfallzeit verbraucht die gespeicherte Wiederverbindungszeit nicht. Abgelaufene Runner-Plätze werden Hunter; der Ablauf für den letzten Runner kann den Huntern den Sieg geben.

Die bereitgestellte 2.0.0-GUI enthält **keine eigene Auswahl für die Wiederverbindungsdauer**. Stoppe zum Anpassen den Server, bearbeite `plugins/VexLandManhunt/config.yml`, erhalte die übrigen Einstellungen und setze:

```yaml
features:
  custom-reconnect-minutes: 15
```

Starte danach neu. Werte unter einer Minute werden auf eine Minute begrenzt. **Reset Settings** setzt diesen Wert auf 15 Minuten zurück. Der kompilierte Build speichert auch Spiel-/Wiederverbindungszustand und Sicherungsschnappschüsse zur Wiederherstellung nach Neustart/Absturz; überlasse diese Dateien dem Plugin, statt sie während des Spiels zu bearbeiten.

#### Reset Settings und Reset Match

**Reset Settings** benötigt zwei Klicks innerhalb von **acht Sekunden**. Der erste aktiviert die Bestätigung; der zweite setzt **Smart Kit AN**, **Auto Spawn alle 15 Minuten**, **Wiederverbindung 15 Minuten** und einen **zufälligen Vorsprung**. Das unterscheidet sich von einer neuen Installation, bei der Auto World Spawn auf AUS zurückfällt. Es ändert die Konfiguration und ersetzt kein vollständiges Spielzurücksetzen.

**Reset Match** führt das vorhandene Spielzurücksetzen aus: temporärer Spielzustand/Gegenstände werden bereinigt und Spieler für die nächste Runde zum Oberwelt-Spawn zurückgebracht. Seine Hauptschaltfläche verwendet nicht die Zwei-Klick-Bestätigung von Reset Settings. **Start Match** kann Teilnehmerinventare vorbereiten/leeren. Prüfe vor dem Klick, welchen Zurücksetz-/Startschalter du verwenden möchtest.

#### Sprach- und Anti-Cheat-Steuerung

**Language** öffnet die globale Auswahl. Klicke die gewünschte Sprache. Beide bereitgestellten Versionen enthalten Englisch, Persisch, Arabisch, Spanisch, Französisch, Deutsch, Russisch, vereinfachtes Chinesisch, Hindi und Portugiesisch. Die Auswahl gilt serverweit und wird gespeichert. Japanische README-Dokumentation ergänzt kein Japanisch in der Sprachauswahl des Plugins.

**Anti-Cheat** öffnet **VexAC Security**. **VexAC Master** aktiviert/deaktiviert die interne Engine; **Movement**, **Combat**, **AutoClick**, **Velocity / AntiKB** und **World / Scaffold** schalten die jeweilige Gruppe um. **Anti X-Ray** schaltet Papers konfigurierte Anti-Xray-Funktion; starte den Server zur Anwendung neu. Status-, Beweisprotokoll- und Erkennungsmodellfelder erklären die aktuellen Systeme. **Back to Control Center** führt zum Hauptmenü zurück.

Die Oberfläche beschreibt reine Beobachtungsmoderation, die statische Untersuchung zeigt aber weiterhin einen schwellenwertbasierten Kick-Pfad. Betrachte den Hinweis auf ausbleibende Kicks als Widerspruch zwischen Implementierung und Dokumentation und prüfe das Moderationsverhalten auf einem kontrollierten Server, bevor du dich darauf verlässt.

#### Integriertes GrimAC und bisheriges VexAC

Die vorhandene GUI **VexAC Security** steuert die bisherige VexAC-Engine; ihre Schaltflächen Master/group sind kein neues Grim-Bedienfeld. Integriertes GrimAC läuft parallel dazu. Verwende `/vexintegration` für den Modulstatus und die nativen Befehle `/grim` oder `/grimac` für Grims eigene Befehle und berechtigungsgesteuerte Werkzeuge. Grims Einstellungen und Sanktionsregeln befinden sich in `plugins/VexLandManhunt/grim/`.

Das GrimBridge-Menü für Überwachung/Gruppen aus 1.13.1 und `grim-settings.yml` beschreiben dieses Paket nicht. Gehe nicht davon aus, dass das Ausschalten von VexAC auch integriertes GrimAC deaktiviert oder eine Überwachungsbezeichnung eine Richtlinie ohne Kicks festlegt. Paper Anti-Xray bleibt eine unabhängige Einstellung, die einen Neustart erfordert.

#### Anleitung im Spiel und Problemlösung

Klicke **Manhunt Administrator Guide** oder verwende `/mhhelp` für ein übersetztes Anleitungsbuch. Spieler erhalten in 2.0.0 über `/mhhelp` ihre rollenabhängige Anleitung. Hunter rechtsklicken ihren Kompass, um einen Runner auszuwählen; diese Ortungsoberfläche ist von der administrativen Target-Player-Auswahl getrennt.

Wenn Rolle oder Kompass nicht synchron wirken, aktualisiert **Emergency Sync** den zugehörigen Laufzeitzustand. **Match Info** hilft beim Prüfen von Teams und Zustand. Scheitert der Start, prüfe Spielbereitschaft, ausgeschaltetes Server Freeze und vorhandene Runner-/Hunter-Teams. Nutze nach JAR-Wechsel einen vollständigen Neustart statt `/reload`. `/mhdebug` ist ein Administrator-Diagnosebefehl in 2.0.0; seine Existenz bedeutet nicht, dass diese Versionen Tests auf einem laufenden Server bestanden haben.

#### Die ältere Steuerzentrale von 1.6.4 verwenden

1.6.4 enthält **Player Roles**, **Friendly Fire**, **Start Match**, **Reset Match**, **Release Hunters Now**, **Server Lock**, **Teleport Everyone To Me**, **Heal & Feed Everyone**, **Match Status**, Sprachauswahl, **Anti Cheat** und eine Administratoranleitung. Die Rollen wechseln **None → Runner → Hunter**; während Start/laufendem Spiel sind Rollenänderungen gesperrt.

Das Anti-Cheat-Menü enthält ältere **Anti AutoClick**-Kontrollen (30-CPS-Regel mit Warn-/Kick-Behandlung), **Anti Fly** und Papers **Anti X-Ray**. Das Runner-Wiederverbindungsfenster beträgt fest **60 Minuten**. Der neuere Smart-Hunter-Kit-V3-Schalter, Auto-World-Spawn-Auswahl, Pause/Fortsetzen, bestätigtes Reset Settings und erweiterte Zielspieler-/Weltwerkzeuge oben gehören zu 2.0.0 und sind im älteren Menü nicht zu erwarten.

Diese Anleitung wurde aus bereitgestellten JAR-Metadaten, mitgelieferten Sprach-/Hilfetexten und statischer Disassemblierung abgeleitet. Die Oberfläche wurde während der Untersuchung nicht auf einem laufenden Minecraft-Server ausgeführt.

### 3. Die Jagd spielen

Runner fliehen während des zufälligen Vorsprungs und arbeiten darauf hin, den Enderdrachen zu besiegen. Hunter warten auf Freigabe und rechtsklicken dann ihren Ortungskompass zur Runner-Auswahl. Ziele lassen sich während des Spiels wechseln, auch bei Dimensionswechseln. Nutze `/teammsg <message>` für reine Teamkommunikation und `/mhhelp` für die übersetzte Rollenanleitung in 2.0.0.

Stirbt ein Runner, spielen die übrigen weiter und der gestorbene Spieler wird Hunter. Ein Hunter kann respawnen und weiter orten. Tod des letzten Runners oder Ablauf seiner Wiederverbindungsfrist kann das Spiel für Hunter beenden; der besiegte Enderdrache beendet es für Runner.

### 4. Pausieren, beenden und die nächste Runde vorbereiten

Pausiere in 2.0.0 mit `/mhpause` und setze mit `/mhresume` fort. Verwende `/mhrelease` für vorzeitige Hunter-Freigabe. Nutze für eine neue Runde das vollständige Zurücksetzen der Steuerzentrale oder `/mhreset`; es bereinigt temporären Spielzustand/Gegenstände und bringt Spieler zum Oberwelt-Spawn zurück. Änderungen an Papers Anti-Xray benötigen einen Neustart.

## Standardeinstellungen im kombinierten Paket 2.0.0

Die untersuchten Rückfallwerte einer neuen Konfiguration sind:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` bedeutet, dass automatische Spawn-Verschiebung aus ist. Die bestätigte GUI-Aktion zum Einstellungszurücksetzen setzt das Intervall stattdessen auf 15 Minuten. Nutze GUI oder `/mhkit` und `/mhspawn` für diese Einstellungen.

## Referenz öffentlicher Befehle — kombiniertes 2.0.0

Administratorbefehle erfordern OP oder `vexland.admin` (standardmäßig OP). Teamchat, Papierkorb und Nachtsicht sind Spielerwerkzeuge; `/mhhelp` liefert die rollenbezogene Anleitung. Die Tabelle führt die 17 Manhunt-/Integrationsbefehle auf; native Grim-Befehle haben eigene Berechtigungen. `/mhnone` ist hier nicht registriert.

| Befehl | Zweck |
| --- | --- |
| `/vexintegration` | Status von integriertem Grim, VexAC, PacketEvents und gemeinsamem Bukkit-Eigentümer melden |
| `/mhgui` | Steuerzentrale öffnen |
| `/mhstart` | Vollständige Startsequenz ausführen |
| `/mhreset` | Aktuelles Spiel vollständig zurücksetzen |
| `/mhrelease` | Hunter vorzeitig freigeben |
| `/mrunner <player>` | Runner zuweisen |
| `/mhunter <player>` | Hunter zuweisen |
| `/teammsg <message>` | Private Teamnachricht senden |
| `/trash` | Wegwerfinventar mit 54 Plätzen öffnen |
| `/nv` | Persönliche Nachtsicht umschalten |
| `/mhlang` | Globale Sprachauswahl öffnen |
| `/mhhelp` | Übersetztes Anleitungsbuch erhalten |
| `/mhkit <on\|off\|toggle\|status>` | Smart-Hunter-Ausrüstung konfigurieren |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Automatische Spawn-Verschiebung konfigurieren |
| `/mhpause` | Laufendes Spiel pausieren |
| `/mhresume` | Pausiertes Spiel fortsetzen |
| `/mhdebug` | Interne Diagnosen ausführen |

## Spielsprachen und Dokumentation

Dieses Paket behält **10 Spielsprachen** bei: Englisch, Persisch, Arabisch, Spanisch, Französisch, Deutsch, Russisch, vereinfachtes Chinesisch, Hindi und Portugiesisch. Jede mitgelieferte Übersetzung hat **683 Schlüssel**, entsprechend 1.9.11. `/mhlang` legt eine serverweite Sprache fest, gespeichert in `language.txt`.

Die Projektdokumentation umfasst **18 Sprachen**, ohne arabische Dokumentationsausgabe. Diese Übersetzungen fügen der unveränderten Binärdatei weder Japanisch noch andere zusätzliche Spielsprachen hinzu.

## Versionsverlauf, Quellcode und Mitwirkende

[CHANGELOG.md](../CHANGELOG.md) dokumentiert jede bereitgestellte Version. Die vollständige [Zuschaueranleitung für 1.13.1](archive/1.13.1/README.de.md) und die [ältere Anleitung für 1.9.11 / 1.6.4](archive/1.9.11/README.de.md) bleiben verfügbar. Jede bereitgestellte Version behält ihren eigenen Download und ihre Prüfsumme.

**Manhunt wurde gemeinsam von Bardiya / Farland_game und Ali / Alivexor entwickelt. GrimAC ist ein separates Projekt von GrimAC / DefineOutside und Mitwirkenden.** Dieses integrierte Artefakt modifiziert drei Grim-Klassen; es ist nicht die unveränderte offizielle Grim-Binärdatei aus der älteren Version mit zwei Dateien. Das zugehörige [Quellcodepaket](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0-source.zip) bewahrt die bereitgestellten Quellen, Build-Skripte, Abhängigkeitseingaben und Hinweise; Test-/Laufzeitnachweise wurden weggelassen und der Quellcode blieb unverändert. Die Version enthält außerdem den GPLv3-Text, Prüfsummen und [Hinweise zu Drittanbietern](../THIRD_PARTY_NOTICES.md). Bei dieser Veröffentlichung wurde weder ein Test auf einem laufenden Server noch ein Test auf reproduzierbare Builds durchgeführt.

## Eine scherzhafte Herausforderung an Dream

Ein bisschen Minecraft-Geplänkel von Bardiya 😄

> „Seufz ... Ali und ich haben ein Manhunt-Plugin gemacht, hundertmal besser als Dreams, aber Dream hat Angst und will unseres nicht spielen!“

## Entwickler und Projektumfang

**Gemeinsam entwickelt von [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) und [Ali · Alivexor](https://github.com/Alivexor).** Beide Namen sind auch als Autoren in den ursprünglichen Plugin-Deskriptoren verzeichnet.

Dieses Repository stellt originale kompilierte Releases, Dokumentation und Versionsnotizen als gemeinsames Portfolio-Projekt vor. Funktionsbeschreibungen beruhen auf statischer Untersuchung der bereitgestellten JARs. Kompatibilität im laufenden Server, Wiederherstellungsleistung, Balance und Anti-Cheat-Genauigkeit wurden im Rahmen dieser Veröffentlichung nicht getestet.

[Bardiyas GitHub-Portfolio](https://github.com/FarlandGame) · [Alis GitHub](https://github.com/Alivexor) · [Alle Releases](https://github.com/FarlandGame/Vexland_Manhunt/releases)
