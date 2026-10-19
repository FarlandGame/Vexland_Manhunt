# Vexland_Manhunt — 1.13.1

> Handleiding voor de gearchiveerde versie · [2.0.0 →](../../README.nl.md)

[English](README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**Een complete Minecraft-ervaring met Runners tegen Hunters, samen gemaakt door [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) en [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt brengt wedstrijdinstellingen, teamrollen, de eerste achtervolging, tracking, voortgang, beloningen, resultaten en beheer samen in één Paper-serverplugin. Runners proberen de Ender Dragon te verslaan, terwijl Hunters de laatste Runner proberen uit te schakelen. De plugin ondersteunt meerdere Runners en houdt de achtervolging gaande bij overlijden, respawnen, dimensiewisselingen en opnieuw verbinden. Het controlecentrum `/mhgui` laat beheerders een wedstrijd via menu’s beheren, met vertaalde berichten en gidsboeken voor spelers.

## Downloads en compatibiliteit

| Bestand / versie | Download | Doel |
|---|---|---|
| **1.13.1 — huidig** | [VexLandManhunt-1.13.1.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/VexLandManhunt-1.13.1.jar) | Manhunt-plugin van Bardiya en Ali |
| **GrimAC 2.3.73 — vereist** | [grimac-bukkit-2.3.73.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/grimac-bukkit-2.3.73.jar) | Afzonderlijke anti-cheatafhankelijkheid van derden |
| 1.9.11 — gearchiveerd | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Vorige Manhunt-build |
| 1.6.4 — gearchiveerd | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Eerdere Manhunt-build |

**Doelplatform: Paper 1.21.11, Java 21.** De nummers 1.6.4, 1.9.11 en 1.13.1 zijn pluginversies, geen ondersteunde Minecraft-versies. In 1.13.1 is GrimAC een verplichte afhankelijkheid en vereist de bridge de API van 2.3.73. Download **beide huidige JAR-bestanden**. Dit zijn serverplugins; spelers installeren ze niet in een modsmap van hun client.

Dit zijn de oorspronkelijke builds voor persoonlijke servers, met verhoogde beheerderstoegang voor de makers, exact bewaard zoals ze zijn aangeleverd. Deze handleiding beschrijft de openbare bediening van Manhunt.

## De Manhunt-ervaring

- **Runner- en Hunter-teams:** wijs online spelers aan een van beide kanten toe. Een wedstrijd heeft minstens één Runner en een Hunter of een online speler zonder rol nodig. Overlevende Runners gaan door als een teamgenoot sterft; een overleden Runner wordt Hunter, tenzij die dood de wedstrijd beëindigt.
- **Filmische wedstrijdstart:** inventarissen en spelmodi worden voorbereid, teams worden voorgesteld en een roulette bepaalt de voorsprong voor Runners. Hunters zijn tijdens die aftelling bevroren, met titels en geluiden. De voorsprong is willekeurig; beheerders kunnen Hunters eerder vrijlaten.
- **Trackingkompas met doelkeuze:** Hunters krijgen een speciaal kompas. Klik er met rechts op om een Runner in het doelmenu te kiezen en tijdens de achtervolging van doel te wisselen. Tussen dimensies volgt tracking de relevante portaalroute tot rechtstreeks volgen mogelijk is. Hunters krijgen hun kompas opnieuw na respawnen.
- **Voortgangsweergaven:** bossbars en wedstrijdinformatie volgen Runner-uitrusting en voortgang via Nether-grondstoffen, blaze rods, parels, Eyes of Ender, de stronghold en de End. De nieuwere build voegt fijnere fasen en voortgangsbeelden op basis van de drakengezondheid toe.
- **Beloningen voor kills door Runners:** als een Runner tijdens een actieve wedstrijd een Hunter doodt, wordt een gewogen beloningspool van 50 mogelijkheden gebruikt die rekening houdt met voortgang. Geanimeerde trekkingen, dubbele/drievoudige beloningen, aankondigingen van killreeksen en vieringen van zeldzame items zijn inbegrepen.
- **Overwinning en resultaten:** de dood van de laatste Runner geeft Hunters de winst; de Ender Dragon verslaan geeft Runners de winst. Eindtitels, vieringen, kill-/doodinformatie en opruimen van tijdelijke items zijn inbegrepen. De nieuwere build rapporteert ook MVP, schade en afstand.
- **Teamcommunicatie en hulpmiddelen:** privéberichten aan teamgenoten met `/teammsg`, een wegwerpinventaris met 54 vakken via `/trash` en persoonlijk nachtzicht met `/nv`.
- **Beheer via menu’s:** rollen, starten/resetten, Hunters eerder vrijlaten, friendly fire, serververgrendeling, iedereen teleporteren, genezen/voeden, taal, beschermingsinstellingen, status en gidsboeken zijn beschikbaar in het controlecentrum. Bevriezen en een volledige reset helpen de volgende wedstrijd voor te bereiden.
- **Vertaalde gidsen:** boeken voor Runners, Hunters en beheerders leggen doelen, kompasgebruik, overlijden, voorbereiding en commando’s uit. Versie 1.9.11 geeft spelers via `/mhhelp` een gids voor hun rol.
- **Paper Anti-Xray-integratie:** menuopties configureren Papers bescherming per wereld; wijzigingen vereisen een serverherstart om van kracht te worden.

## Wat is er nieuw in 1.13.1?

Vergeleken met de aangeleverde build 1.9.11:

- **Onzichtbare toeschouwers:** een afzonderlijke rol, toewijzing door een beheerder, beschermd vliegen, verborgen spelers, opgeslagen/herstelde status en een menu met pagina's om naar deelnemers te teleporteren.
- **Vernieuwd bedieningscentrum:** menu's met categorieën, expliciete keuze uit vier rollen, doelwitselectie op naam, selectie van de herverbindingstijd, de voorinstellingen Classic/Fast/Hardcore/Custom en afzonderlijke bevestigingsschermen met een termijn van 30 seconden.
- **GrimAC-integratie:** het verplichte GrimAC 2.3.73 vervangt het actieve VexAC-opstartpad. De GUI biedt de hoofdschakelaar, vijf controlegroepen, meldingen en bediening voor monitoren/handhaving. Paper Anti-Xray blijft onafhankelijk.
- **Nieuwe Smart Hunter Kit-planner:** past uitrusting en voorraden aan op de uitrusting/betoveringen van Runners, de dichtstbijzijnde Runner, teamaantallen, afstand, dimensie en terrein. Hij behoudt bestaande sterkere uitrusting, vermijdt dubbele gereedschappen en beperkt het aanvullen van verbruiksartikelen met een geschiedenis van 30 seconden. Dit garandeert geen vast verschil in uitrusting of gemeten spelbalans.
- **Gevalideerd herstel:** snapshots met SHA-256-verzegeling, controles van schema/status en terugval op een geldige back-up; ongeldige snapshots of snapshots in een nieuwer formaat blijven bewaard zonder ze te overschrijven. De toeschouwersstatus wordt afzonderlijk bewaard.
- **Uitgebreide berichten:** het aantal vertaalde sleutels groeit van 683 naar 762 per meegeleverde vertaling, nog steeds in dezelfde tien speltalen. Er zijn twee nieuwe openbare commando's geregistreerd: `/mspectator <player>` en `/mhspectate`.
- **Terugval bij reset:** als er geen veilig oppervlak bij de spawn in de Overworld wordt gevonden, kan de reset die teleportatie overslaan in plaats van af te dwingen.

## Volledige installatie en gebruik met `/mhgui`

Stop de server en bewaar een back-up van de werelden en plugingegevens. Plaats beide huidige JAR-bestanden in `plugins/` en houd daar slechts één Manhunt-JAR en één GrimAC-JAR. Behoud bestaande instellingen/gegevens in `plugins/VexLandManhunt/` bij het upgraden. Start de Paper 1.21.11 / Java 21-server volledig op; voer een volledige herstart uit wanneer je builds vervangt. GrimAC moet succesvol laden. De interne pluginnaam blijft `VexLandManhunt`.

Deze handleiding beschrijft pluginversie **1.13.1** met Engelse labels. De labels volgen de taal voor de hele server. Posities tellen rijen van boven naar beneden en kolommen van links naar rechts. Gebruik een normale linkermuisklik, tenzij een speciale handeling wordt vermeld. Deze handleiding is gebaseerd op statische inspectie; er is geen Minecraft-server uitgevoerd.

### Een wedstrijd instellen

1. Gebruik `/mhgui` met `vexland.admin` (standaard: OP).
2. Open **Player Roles**, klik op een spelertegel met naam en kies vervolgens **Runner**, **Hunter**, **Spectator** of **No Team**. Hiermee open je een keuzemenu voor een specifieke rol; klikken op de speler doorloopt de rollen niet.
3. Wijs minstens één Runner en één Hunter toe. Online spelers zonder toegewezen rol kunnen Hunter worden wanneer een wedstrijd begint; toeschouwers vullen de vereiste plek van geen van beide teams.
4. Controleer **Match Settings**, **GrimAC Security** en **Global Language**. Schakel Server Freeze uit voordat je begint.
5. Open **Match Controls → Start Match**. De inventarissen van deelnemers worden voorbereid/leeggemaakt, de introductie wordt afgespeeld en de roulette kiest hoe lang de Hunters bij de start moeten wachten.

### Home: `/mhgui` (vijf rijen)

| Positie | Knop | Actie |
|---|---|---|
| R2 C2 | Match Controls | Starten, pauzeren/hervatten, vrijlaten en resetten. |
| R2 C4 | Player Roles | Open de rollenlijst van online spelers. |
| R2 C6 | Match Settings | Eigen vuur, kits, spawn, herverbinding en voorinstellingen. |
| R2 C8 | Player Management | Kies een doelwit en gebruik speler-/wereldhulpmiddelen. |
| R4 C2 | GrimAC Security | Open de beveiligingsinstellingen. |
| R4 C4 | Global Language | Kies de taal die voor iedereen wordt gebruikt. |
| R4 C6 | Administrator Guide | Voeg het gelokaliseerde beheerdersboek toe aan je inventaris. |
| R5 C5 | Close | Sluit het menu. |

Het baken op R1 C5 geeft de wedstrijdstatus en aantallen Runners/Hunters weer.

### Match Controls (vijf rijen)

| Positie | Knop | Actie |
|---|---|---|
| R2 C2 | Start Match | Start de volledige reeks. |
| R2 C4 | Pause Match / Resume Match | Pauzeer of hervat het spel en de wedstrijdtimers; beschikbaar voor een wedstrijd met status RUNNING. |
| R2 C6 | Release Hunters | Beëindig de huidige wachttijd voor Hunters voortijdig. |
| R2 C8 | Reset Match | Open de bevestiging en reset vervolgens de wedstrijd volledig. |
| R4 C2 | Server Freeze | Schakel het globaal bevriezen van spelers zonder OP in of uit. |
| R4 C4 | Teleport Everyone | Open de bevestiging en haal vervolgens alle online spelers naar je toe. |
| R4 C6 | Match Info | Verstuur het wedstrijd- en teamrapport. |

**Back** staat op R5 C1; **Close** staat op R5 C9. Server Freeze staat los van Pause Match: gebruik Pause wanneer de klok en de spelsystemen tegelijk moeten stoppen.

### Player Roles

De spelerslijst met zes rijen toont maximaal 45 roltegels met naam, gesorteerd op spelersnaam, in de eerste vijf rijen. Runner gebruikt lichtgroen beton, Hunter rood beton, Spectator een Enderoog en No Team grijs beton. De onderste rij bevat **Previous Page** op C1, pagina-/online-informatie op C3, **Back to Control Center** op C5 en **Next Page** op C9.

Klik op een speler om **Choose Player Role** te openen (drie rijen):

| Positie | Specifieke rol |
|---|---|
| R2 C2 | Runner |
| R2 C4 | Hunter |
| R2 C6 | Spectator |
| R2 C8 | No Team |

De naam/huidige rol van de speler verschijnt op R1 C5; **Back** staat op R3 C1 en **Close** op R3 C9. Rollen kunnen tijdens een wedstrijd veranderen. Als je tijdens RUNNING de laatste toegewezen Runner een andere rol dan Runner geeft, verschijnt de bevestiging **Last Runner: the match will end**. Het toepassen hiervan kan de Hunters de overwinning geven. Directe rolcommando's worden onmiddellijk toegepast, dus gebruik ze weloverwogen. No Team kan hier worden toegewezen; de normale synchronisatie bij starten/deelnemen kan een speler zonder toegewezen rol tijdens een actieve wedstrijd veranderen in een Hunter.

### Toeschouwers

Een beheerder wijst de rol toe met `/mspectator <player>` of kiest **Spectator** in Player Roles. Het commando controleert beheerderstoegang, hoewel de descriptor geen machtigingsregel heeft. Spelers schrijven zichzelf niet in door `/mhspectate` uit te voeren.

Een toeschouwer krijgt een **Spectator teleport**-kompas in het eerste vak van de snelbalk. Houd het in de hoofdhand en klik met de rechtermuisknop, of gebruik `/mhspectate`, om het teleportatiemenu met zes rijen te openen. Het menu werkt alleen zolang de speler de rol Spectator heeft. De eerste vijf rijen bevatten maximaal 45 levende, online Runners/Hunters, gesorteerd op naam; klik op een roltegel met naam om naar de huidige locatie van die speler te teleporteren, ook in een andere wereld. De onderste rij bevat **Previous Page** op C1, **Close** op C5 en **Next Page** op C9. Als er geen geschikte deelnemer is, staat op R3 C5 **No players available**. Als je dit menu sluit, blijf je toeschouwer.

Toeschouwers vliegen, zijn verborgen voor andere spelers, hebben geen botsingen en zijn beschermd tegen schade. De implementatie gebruikt de avonturenmodus met vliegen; ze geeft geen camera van de standaard toeschouwersmodus of beweging door blokken. Aanvallen, blokken breken/plaatsen, normale interacties met blokken/entiteiten, voorwerpen oppakken/weggooien, wisselen met de tweede hand, klikken/slepen in de inventaris, aanpassen van harnashouders en ervaring oppakken/verkrijgen worden geblokkeerd. Mobs kunnen hen niet als doelwit kiezen en veranderingen in honger worden geannuleerd. `/teammsg <message>` bereikt andere spelers met de rol Spectator. Geef geen locaties van deelnemers of andere hulp van buitenaf door aan wedstrijdspelers.

Om te stoppen wijst een beheerder **Runner**, **Hunter** of **No Team** toe, of gebruikt `/mrunner <player>` of `/mhunter <player>`. Er is geen specifiek commando of specifieke knop waarmee je zelf kunt stoppen. Bij het verlaten worden de opgeslagen inventaris/cursor, locatie, spelmodus, vliegstatus, botsingen en immuniteitsstatus hersteld; daarna wordt het wedstrijdgedrag van de nieuwe rol toegepast. De toeschouwersstatus wordt opgeslagen om opnieuw verbinding te kunnen maken. Een volledige wedstrijdreset herstelt de toeschouwersstatus, wist rollen en verplaatst online spelers naar een veilige spawn in de Overworld wanneer die beschikbaar is. De normale opruiming na afloop van een wedstrijd laat toeschouwers buiten de afhandeling van voorwerpen/vliegen voor deelnemers.

### Match Settings (vijf rijen)

| Positie | Knop | Actie |
|---|---|---|
| R2 C2 | Friendly Fire | Schakel schade aan teamgenoten in of uit. |
| R2 C4 | Smart Hunter Kit | Schakel adaptieve kits voor Hunters bij respawnen in of uit. |
| R2 C6 | Auto World Spawn | Open de intervalkeuze. |
| R2 C8 | Reconnect Grace | Open de keuze van de herverbindingstijd voor Runners. |
| R4 C2 | Match Preset | Kies Classic, Fast, Hardcore of Custom. |
| R4 C4 | Reset Settings | Bevestig gebalanceerde instellingen: Kit ON, Spawn 15m, Reconnect 15m. |
| R4 C6 | Random Head Start | Informatietegel; de roulette blijft de vertraging bepalen. |

**Back** staat op R5 C1; **Close** op R5 C9.

Het keuzemenu **Reconnect Grace** met drie rijen biedt **1, 5, 10, 15, 20, 30 minuten** op R2 C2–C7, in die volgorde. Een klik slaat de waarde op en houdt het keuzemenu open. Back staat op R3 C1; Close op R3 C9.

Het keuzemenu **Match Preset** met drie rijen zet **Classic**, **Fast**, **Hardcore**, **Custom** op R2 C2, C4, C6, C8. Classic: Kit ON, Spawn 15m, Reconnect 15m. Fast: ON, 5m, 10m. Hardcore: OFF, OFF, 5m. Custom behoudt de huidige handmatige instellingen. Voorinstellingen behouden de willekeurige voorsprong bij de start. Na de keuze blijft dit menu open; Back staat op R3 C1, Close op R3 C9.

**Auto World Spawn** biedt OFF, 5m, 10m op R2 C2, C3, C4 en 15m, 20m, 30m op R2 C6, C7, C8. Back staat op R3 C5. Kies een interval of gebruik `/mhspawn <off|5|10|15|20|30|status>`. Dit verplaatst de spawn in de Overworld naar de buurt van een geschikte Runner in de Overworld; als niemand geschikt is, kan dit worden overgeslagen. `/mhkit <on|off|toggle|status>` bedient kits rechtstreeks.

### Player Management (zes rijen)

| Positie | Knop | Van toepassing op |
|---|---|---|
| R1 C5 | Target Player | Open een spelerskiezer met namen. |
| R2 C2 | Full Heal | Alle online spelers. |
| R2 C4 | Full Hunger | Alle online spelers. |
| R2 C6 | Clear Effects | Alle online spelers. |
| R2 C8 | Freeze Target | Geselecteerde speler. |
| R4 C2 | Clear Target Inventory | Geselecteerde speler; bevestiging vereist. |
| R4 C4 | Kill Target | Geselecteerde speler; bevestiging vereist en de normale wedstrijduitkomsten zijn van toepassing. |
| R4 C6 | Set Day | Je huidige wereld. |
| R4 C8 | Clear Weather | Je huidige wereld. |
| R5 C2 | Clear Dropped Items | Je huidige wereld; bevestiging vereist. |
| R5 C4 | Emergency Sync | Vernieuw de rol-/runtimesystemen voor online spelers. |
| R5 C6 | Freeze Team | Links: Runners; rechts: Hunters; shift-klik: hef deze team-/individuele bevriezingen op. |

Back staat op R6 C1; Close op R6 C9. Doelwitselectie verandert geen rollen. De kiezer biedt 28 andere online spelers per pagina, in rij 2–5, kolom 2–8; klik op een naam om die te selecteren en terug te keren. Previous/Back/Next staan op R6 C1/C5/C9. Controleer het weergegeven doelwit opnieuw voordat je een actie toepast.

### Bevestigingsschermen

Reset Match, Teleport Everyone, Reset Settings, Clear Target Inventory, Kill Target, Clear Dropped Items en de wijziging van de laatste Runner via de GUI gebruiken een afzonderlijk scherm **Confirm Action** met drie rijen. Lees de actie/het doelwit op R1 C5 en klik vervolgens op de groene knop **Confirm** op R2 C3 of de rode knop **Cancel** op R2 C7. De bevestiging verloopt na **30 seconden**. Gewijzigde/offline doelwitten of gewijzigde rollen vereisen een nieuwe selectie. Dit vervangt de instructies uit de oude handleiding over herhaald klikken binnen vijf/acht seconden voor deze nieuwe menupaden.

### GrimAC Security en taal

Het Grim-menu met zes rijen heeft de status op R1 C5; schakelaars op R2 C2 **GrimAC Master**, C4 **Movement**, C6 **Combat**, C8 **Packets**; R4 C2 **Velocity / AntiKB**, C4 **World / Scaffold**, C6 **Anti X-Ray**, C8 **Admin Alerts**; en R5 C5 **Monitor mode**. Back staat op R6 C1 en Close op R6 C9. Monitor mode regelt meldingen/bewijs tegenover handhaving. Paper Anti-Xray is onafhankelijk en vereist een herstart na wijzigingen. Dit zijn GrimAC-instellingen; de oudere beschrijving van het VexAC/AutoClick-menu beschrijft deze versie niet.

Global Language geldt voor iedereen en vernieuwt menu's/voorwerpen. Klik op de taalnaam; Back staat op R3 C5. `/mhlang` opent hetzelfde keuzemenu en `/mhhelp` levert de gelokaliseerde handleiding voor spelers/beheerders.

### Huidige standaardwaarden, herverbinding en moderatie

De terugvalwaarden voor een nieuwe configuratie in `plugins/VexLandManhunt/config.yml` zijn:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` betekent dat automatische spawnverplaatsing uit staat. Reset Settings en Classic kiezen in plaats daarvan 15 minuten. Tijdens het herverbindingsvenster van een Runner blijft diens plek behouden; een tijdige terugkeer biedt tien seconden bescherming. Opgeslagen serveruitvaltijd wordt niet meegerekend. Na het verstrijken van de termijn kan de Runner een Hunter worden of kan de wedstrijd eindigen met winst voor de Hunters. Pause/Resume bevriest spelsystemen en past de tijdmeting van de actieve wedstrijd aan. Herstelbestanden worden door de plugin beheerd.

De instellingen van de Grim-bridge worden bewaard in `plugins/VexLandManhunt/grim-settings.yml`. De oorspronkelijke standaardwaarden zijn Master ON, alle vijf groepen ON, Admin Alerts ON en **Monitor mode OFF: handhaving is ingeschakeld**. Monitor mode zet bewijs/meldingen in een wachtrij en annuleert signaleringen die aan de voorwaarden voldoen. In de handhavingsmodus kan de bridge een Grim-kickcommando omzetten in een gelokaliseerde verbreking van de verbinding die opnieuw verbinden toestaat; er wordt geen beleid voor permanente bans ingesteld. De daadwerkelijke drempels hangen ook af van de configuratie van Grim. Bewijs wordt in een wachtrij geplaatst voor `plugins/VexLandManhunt/anticheat/grim-evidence.log`; begrensde wachtrijen kunnen bij belasting vermeldingen laten vallen. De bridge geeft uitzonderingen aan toeschouwers, gepauzeerd/bevroren spel en bepaalde voertuigsituaties, met een respijtperiode van drie seconden na verbinden, teleporteren en respawnen. Er worden geen benchmarks voor de nauwkeurigheid of prestaties van de anti-cheat geclaimd.

## Overzicht van openbare commando's — 1.13.1

Beheerderstoegang betekent OP of `vexland.admin` (standaard OP). De handler van `/mspectator <player>` controleert dit ondanks het ontbreken van een machtigingsregel in de descriptor. Directe rolcommando's worden onmiddellijk toegepast; het wijzigen van de laatste Runner tijdens RUNNING kan de wedstrijd beëindigen. De GUI biedt hiervoor een bevestiging.

| Commando | Doel | Toegang |
|---|---|---|
| `/mhgui` | Open het bedieningscentrum met categorieën | Beheerder |
| `/mhstart` | Start de volledige wedstrijdreeks | Beheerder |
| `/mhreset` | Reset de wedstrijd volledig | Beheerder |
| `/mhrelease` | Laat wachtende Hunters vrij | Beheerder |
| `/mrunner <player>` | Wijs Runner toe | Beheerder |
| `/mhunter <player>` | Wijs Hunter toe | Beheerder |
| `/mspectator <player>` | Wijs Spectator toe | Beheerder; nieuw |
| `/mhspectate` | Open het menu voor teleportatie naar deelnemers | Huidige Spectator; nieuw |
| `/teammsg <message>` | Stuur naar je eigen rol/team | Speler |
| `/trash` | Wegwerpinventaris met 54 vakken; aliassen `/mhtrash`, `/vextrash` | Speler |
| `/nv` | Schakel persoonlijk nachtzicht in of uit | Speler |
| `/mhlang` | Open de globale taalkeuze | Beheerder |
| `/mhkit <on\|off\|toggle\|status>` | Configureer adaptieve Hunter-kits | Beheerder |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Configureer spawnverplaatsing | Beheerder |
| `/mhhelp` | Ontvang een gelokaliseerde rol-/beheerdershandleiding | Speler / beheerder |
| `/mhpause` | Pauzeer de lopende wedstrijd | Beheerder |
| `/mhresume` | Hervat een gepauzeerde wedstrijd | Beheerder |
| `/mhdebug` | Interne diagnostiek | Beheerder |

`/mhnone` is niet geregistreerd in deze versie; gebruik de rol No Team in de GUI. Hunters klikken met de rechtermuisknop op hun volgkompas om een Runner te kiezen; dit staat los van teleportatie door toeschouwers en de doelwitkiezer van de beheerder. Runners winnen door de Ender Dragon te verslaan; Hunters winnen wanneer er geen Runner meer over is. Een gesneuvelde Runner wordt Hunter als er nog andere Runners over zijn.

## Talen, geschiedenis en erkenning van derden

De oorspronkelijke plugin biedt **10 speltalen**: Engels, Perzisch, Arabisch, Spaans, Frans, Duits, Russisch, Vereenvoudigd Chinees, Hindi en Portugees. `/mhlang` kiest één taal voor de hele server, opgeslagen in `language.txt`. De GitHub-handleiding heeft **18 talen**, zonder een Arabische documentatie-editie. Japans en andere extra README-talen voegen geen vertalingen in het spel toe aan de ongewijzigde JAR-bestanden.

De [versiegeschiedenis](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/CHANGELOG.md) beschrijft elke aangeleverde build. De volledige oudere handleiding voor 1.9.11 / 1.6.4 blijft bewaard in het [versiearchief](../1.9.11/README.nl.md). De speciale build voor toeschouwers is nu aangeleverd en gepubliceerd als 1.13.1; de functies ervan mogen niet aan de oudere downloads worden toegeschreven.

**GrimAC is een onafhankelijk project van de GrimAC-bijdragers, verspreid onder GPL-3.0.** Bardiya en Ali hebben Vexland_Manhunt en de integratie ervan gemaakt; zij worden niet als auteurs van GrimAC genoemd. De aangeleverde Grim-JAR komt overeen met het officiële Bukkit-artifact van Modrinth 2.3.73 wat betreft SHA-512 en SHA-1. De ingebedde broncodecommit komt overeen met [upstream v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73). De release bevat ongewijzigde binaire bestanden, controlesommen, de upstream-broncodesnapshot, de licentie en [kennisgevingen over derden](../../../THIRD_PARTY_NOTICES.md). Deze componentkennisgevingen kennen geen licentie toe aan het afzonderlijke Manhunt-project.

## Een speelse uitdaging aan Dream

Een beetje Minecraft-geplaag van Bardiya 😄

> "Zucht... Ali en ik hebben een Manhunt-plugin gemaakt die honderd keer beter is dan die van Dream, maar Dream is bang en wil de onze niet spelen!"

## Makers en projectomvang

**Samen gemaakt door [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) en [Ali · Alivexor](https://github.com/Alivexor).** Beide accounts staan ook als auteurs in de oorspronkelijke plugindescriptors.

Deze repository presenteert de originele gecompileerde releases, hun documentatie en versienotities als gezamenlijk portfolioproject. Functiebeschrijvingen zijn gebaseerd op statische inspectie van de aangeleverde JARs. Compatibiliteit op actieve servers, herstelprestaties, balans en anti-cheatnauwkeurigheid zijn niet getest tijdens deze publicatiewerkwijze.

[Bardiya’s GitHub-portfolio](https://github.com/FarlandGame) · [Ali’s GitHub](https://github.com/Alivexor) · [Alle releases](https://github.com/FarlandGame/Vexland_Manhunt/releases)
