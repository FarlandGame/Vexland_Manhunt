# Vexland_Manhunt — 1.9.11 / 1.6.4

> Handleiding voor gearchiveerde versies · [2.0.0 →](../../README.nl.md)

[English](README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**Een complete Minecraft-ervaring met Runners tegen Hunters, samen gemaakt door [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) en [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt brengt wedstrijdinstellingen, teamrollen, de eerste achtervolging, tracking, voortgang, beloningen, resultaten en beheer samen in één Paper-serverplugin. Runners proberen de Ender Dragon te verslaan, terwijl Hunters de laatste Runner proberen uit te schakelen. De plugin ondersteunt meerdere Runners en houdt de achtervolging gaande bij overlijden, respawnen, dimensiewisselingen en opnieuw verbinden. Het controlecentrum `/mhgui` laat beheerders een wedstrijd via menu’s beheren, met vertaalde berichten en gidsboeken voor spelers.

## Downloads en compatibiliteit

| Pluginversie | Download | Doelomgeving |
| --- | --- | --- |
| **1.9.11** — huidige aangeleverde build | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Paper **1.21.11**, Java **21** |
| **1.6.4** — eerdere build | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Paper **1.21.11**, Java **21** |

**1.6.4 en 1.9.11 zijn versienummers van de plugin.** Beide aangeleverde builds vermelden Minecraft-API `1.21.11` en Java 21-classbestanden. Dit zijn serverplugins voor Minecraft Java Edition. [Papers Java-vereisten per versie](https://docs.papermc.io/paper/getting-started/) noemen ook Java 21 voor Paper 1.21.11. De aangeleverde descriptors vermelden geen extra pluginafhankelijkheid.

Dit zijn **originele builds voor een persoonlijke server met verhoogde beheerrechten specifiek voor de makers**, precies bewaard zoals aangeleverd. De onderstaande gids behandelt de openbare Manhunt-bediening.

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

## Wat is nieuw in 1.9.11?

Deze wijzigingen zijn vastgesteld door de twee aangeleverde builds te vergelijken, inclusief metadata, berichtbronnen en gecompileerde classes.

| Toevoeging of wijziging | Gedrag in 1.9.11 |
| --- | --- |
| **Smart Hunter Kit V3** | Adaptieve respawnkits houden rekening met Runner-uitrusting, teams en wedstrijdcontext. Het systeem probeert Hunter-kits onder de gemiddelde Runner-uitrusting te houden en is aan/uit te zetten met `/mhkit` of de GUI. |
| **Automatische Overworld-spawn** | Verplaatst de wereldspawn nabij een geschikte Overworld-Runner met een gekozen interval: uit, 5, 10, 15, 20 of 30 minuten. Het systeem kiest een veilige plek aan de oppervlakte en slaat ongeschikte gevallen over. |
| **Pauzeren en hervatten** | `/mhpause` bevriest gameplay, wedstrijdtimers, tracking en spawnverplaatsing; `/mhresume` gaat verder. Gepauzeerde tijd wordt van de actieve wedstrijdtijd uitgesloten. |
| **Herstel na herstart/crash** | Een herstellaag herstelt wedstrijdstatus, rollen, kompasdoelen, voortgang, belonings-/doodtimers en verbindingsstatus met primaire/back-upsnapshots, periodieke opslag en opslag bij afsluiten. |
| **Runner-verbindingsinstellingen** | Een instelbare terugkeertijd vervangt het eerdere vaste venster van 60 minuten. Nieuwe standaard: 15 minuten, met 10 seconden bescherming na terugkeer. Serverdowntime telt niet mee; verstrijken kan de Runner in een Hunter veranderen of de wedstrijd beëindigen. |
| **Uitgebreid beheer** | Verander rollen tijdens een lopende wedstrijd met behoud van de laatste Runner; acties voor een gekozen speler, teams teleporteren/bevriezen, runtime opnieuw synchroniseren en snelkoppelingen verbeteren het beheer. |
| **Instellingenreset met bevestiging** | Twee klikken binnen acht seconden stellen Smart Kit ON, automatische spawn elke 15 minuten en terugkeertijd 15 minuten in. Dit verschilt van een nieuwe installatie met automatische spawn standaard OFF. |
| **VexAC 3.0** | Controles voor beweging, gevechten, AutoClick, snelheid/knockback en bouwen; groeps-/hoofdschakelaars, bewijsregistratie, beheerdersmeldingen en uitzonderingen voor omgeving/lag. |
| **Ultra Deep Debug v4** | `/mhdebug` biedt diagnostiek voor toestandsmachine, GUI, synthetische kits/stress, taalplaceholders, een volledige herstelcyclus en integriteit. |
| **Uitgebreide weergaven** | Meer voortgangsdetails, drakengezondheid, MVP-/schade-/afstandsresultaten en pinginformatie in TAB. |
| **Commandowijzigingen** | Voegt `/mhkit`, `/mhspawn`, `/mhpause`, `/mhresume` en `/mhdebug` toe; verwijdert `/mhnone`; past `/mhhelp` aan spelers/beheerders aan en voegt `/trash`-aliassen toe. |
| **Meer vertaalde berichten** | De vertaalbronnen groeien van 446 berichtsleutels per taal naar 683. |

De meegeleverde VexAC-controles dekken Fly, Speed, Timer, Phase, Step, NoSlow, GroundSpoof, Reach, KillAura, AimAssist, slaan door muren, BadPackets, AutoClick-tijdpatronen, gewijzigde knockback, Scaffold, Tower, FastPlace, Nuker en blokbereik. De interface gebruikt een label voor alleen monitoring, terwijl gecompileerde code ook kickpaden bevat; controleer het daadwerkelijke moderatiegedrag op een testserver voordat je op dat label vertrouwt. De eerdere build bevat in plaats daarvan de oude Anti AutoClick- en Anti Fly-bediening.

## Volledige voorbereiding en gebruik met `/mhgui`

### 1. Installeer één build op de server

Stop je **Paper 1.21.11 / Java 21**-server. Plaats een van de gedownloade JARs in de map `plugins/`. Houd slechts één VexLandManhunt-build tegelijk geïnstalleerd. Start de server volledig opnieuw nadat je een build hebt vervangen. De interne pluginnaam blijft `VexLandManhunt`; de openbare projectnaam is `Vexland_Manhunt`.

### 2. Open het controlecentrum

Meld je op de server aan als beheerder met **OP** of de permissie **`vexland.admin`** en voer in:

```text
/mhgui
```

De instructies hieronder beschrijven de openbare interface in pluginversie **1.9.11**, met Engelse knopnamen. Labels volgen de gekozen servertaal. Gebruik voor volledige GUI-bediening een vertrouwd **OP**-account: de descriptorpermissie staat het openen van het commando toe, terwijl sommige meegeleverde GUI-handlers strengere OP-controles uitvoeren. De hoofdinventaris heeft vijf rijen van negen vakken. Houd de muis boven een knop voor de beschrijving en huidige instelling. De meeste knoppen gebruiken een normale klik; bijzondere muisacties en bevestigingen worden hieronder uitgelegd. Het kleinere 1.6.4-menu komt aan het einde aan bod.

#### Bereid je eerste wedstrijd voor

1. Open **Player Roles**. Klik op het spelershoofd van elke deelnemer tot de juiste rol verschijnt. In 1.9.11 wisselt de rol tussen **Runner** en **Hunter**; een deelnemer zonder rol wordt bij de eerste klik Runner. Links-/rechts-/shift-klikken zijn geen afzonderlijke snelkoppelingen voor rolkeuze. Gebruik zo nodig **Previous Page**, **Next Page** en **Back to Control Center**.
2. Wijs minstens één Runner en minstens één Hunter toe. De startroutine kan overige online spelers zonder rol in Hunters veranderen; iedereen expliciet indelen maakt de teams duidelijk.
3. Klik op **Friendly Fire** om te bepalen of teamgenoten elkaar schade mogen toebrengen. Controleer na klikken de ON/OFF-indicator.
4. Klik op **Language** om de serverbrede taal te kiezen. Dit beïnvloedt berichten, interfaces, meldingen en gidsboeken voor iedereen, niet alleen voor jezelf.
5. Controleer **Smart Hunter Kit**, **Auto World Spawn** en **Anti-Cheat**. Lees via de boekknop de beheerdersgids als je uitleg in het spel nodig hebt.
6. Zorg dat **Server Freeze** uitstaat en klik op **Start Match**. De start bereidt spelers en inventarissen voor, toont de introductie en willekeurige roulette voor de voorsprong voordat Hunters vrijkomen, en begint de jacht. Bewaar vooraf alles wat je wilt behouden buiten de inventarissen van deelnemers.

#### Hoofdknoppen van het controlecentrum

De posities tellen rijen van boven naar beneden en kolommen van links naar rechts. Ze beschrijven de uiteindelijke versierde 1.9.11-indeling.

| Positie | Engelse knop | Functie |
|---|---|---|
| Rij 2, kolom 2 | Player Roles | Opent het paginamenu met Runner-/Hunter-spelershoofden. |
| Rij 2, kolom 3 | Target Player | Wisselt tussen andere online spelers voor beheerdersacties op het gekozen doel. Controleer de huidige naam. |
| Rij 2, kolom 4 | Friendly Fire | Schakelt schade tussen teamgenoten aan/uit. |
| Rij 2, kolom 5 | Match Info | Stuurt een kort rapport over wedstrijdstatus, teams, friendly fire en gekozen doel. |
| Rij 2, kolom 6 | Start Match | Voert de normale wedstrijdstart en willekeurige voorsprong uit. |
| Rij 2, kolom 7 | Full Heal | Herstelt de gezondheid van alle online spelers. |
| Rij 2, kolom 8 | Reset Match | Voert de volledige wedstrijdreset uit. Dit verschilt van Reset Settings. |
| Rij 3, kolom 2 | Full Hunger | Herstelt voedsel en verzadiging van alle online spelers. |
| Rij 3, kolom 3 | Release Hunters | Laat wachtende Hunters vrij voordat de voorsprong afloopt. |
| Rij 3, kolom 4 | Clear Effects | Verwijdert drankjeseffecten van alle online spelers. |
| Rij 3, kolom 5 | Server Freeze | Schakelt globale serverbevriezing aan/uit; gewone spelers zonder OP worden bevroren. |
| Rij 3, kolom 6 | Clear Target Inventory | Leegt inventaris, pantser en tweede hand van de gekozen speler na bevestiging. |
| Rij 3, kolom 7 | Teleport Everyone | Brengt alle online spelers naar je huidige positie. |
| Rij 3, kolom 8 | Kill Target | Doodt de gekozen speler na bevestiging; normale doodregels kunnen de wedstrijd beïnvloeden. |
| Rij 4, kolom 2 | Anti-Cheat | Opent de VexAC Security-bediening. |
| Rij 4, kolom 3 | Freeze Target | Schakelt individuele bevriezing van de gekozen speler aan/uit. |
| Rij 4, kolom 4 | Emergency Restore | Herstelt gezondheid, voedsel en verzadiging van iedereen online. |
| Rij 4, kolom 5 | Freeze Team | Linksklik schakelt Runners; rechtsklik Hunters; shift-klik verwijdert individuele/teambevriezingen. |
| Rij 4, kolom 6 | Set Day | Stelt dagtijd in voor je huidige wereld. |
| Rij 4, kolom 7 | Clear Weather | Stopt regen en onweer in je huidige wereld. |
| Rij 4, kolom 8 | Language | Opent de globale taalkeuze. |
| Rij 5, kolom 2 | Smart Hunter Kit | Schakelt adaptieve Hunter-respawnkits aan/uit; toont ON/OFF. |
| Rij 5, kolom 3 | Clear Dropped Items | Verwijdert gevallen item-entiteiten in je huidige wereld. |
| Rij 5, kolom 4 | Pause Match / Resume Match | Stopt of hervat actieve gameplay en wedstrijdtimers. |
| Rij 5, kolom 5 | Emergency Sync | Synchroniseert rollen, kompassen en gerelateerde runtime opnieuw. |
| Rij 5, kolom 6 | Reset Settings | Herstelt evenwichtige instellingen na bevestiging met twee klikken. |
| Rij 5, kolom 7 | Close | Sluit het controlecentrum. |
| Rij 5, kolom 8 | Auto World Spawn | Opent de intervalkeuze voor automatische Overworld-spawn. |
| Rij 5, kolom 9 | Manhunt Administrator Guide | Geeft het vertaalde beheerdersgidsboek. |

Decoratief glas en titel-/statusitems zijn geen spelknoppen.

#### Rollen en gekozen doelen

**Player Roles** verandert het daadwerkelijke Manhunt-team van een deelnemer. Klik op het hoofd en lees de bijgewerkte rol. Tijdens STARTING/RUNNING staat de interface Runner-/Hunter-wijzigingen toe, maar weigert de laatste Runner in Hunter te veranderen. Zo blijft de Runner-kant in de lopende wedstrijd behouden. Verander rollen bewust, want teamruntime en kompassen worden na een wijziging gesynchroniseerd.

**Target Player** staat hier los van: het selecteert iemand voor acties als Freeze Target, Clear Target Inventory of Kill Target zonder diens team te veranderen. Wissel tot de bedoelde online speler wordt getoond. Als een opgeslagen doel niet meer beschikbaar is, kan de code terugvallen op de eerste andere online speler; controleer daarom de naam vlak vóór een actie op het gekozen doel. Als niemand anders online is, meldt het dat er geen doel beschikbaar is.

**Clear Target Inventory** en **Kill Target** vereisen twee klikken op dezelfde actie voor hetzelfde doel binnen **vijf seconden**. De eerste klik zet de bevestiging klaar en toont het doel; de tweede voert de actie uit. Van doel wisselen of te lang wachten vereist een nieuwe bevestiging. Een inventaris legen verwijdert de inhoud; een Runner doden kan de wedstrijd beëindigen of veranderen volgens de normale doodregels.

**Freeze Team** heeft de enige teamspecifieke muissnelkoppelingen in dit menu: gewoon linksklikken kiest het Runner-team, gewoon rechtsklikken het Hunter-team, en shift-klikken verwijdert alle individuele/teambevriezingen die dit hulpmiddel beheert. De globale Server Freeze-schakelaar is apart en moet apart worden uitgezet als spelers bevroren blijven.

#### Smart Hunter Kit

Klik op **Smart Hunter Kit** om adaptieve Hunter-respawnkits aan/uit te zetten. De knop toont de huidige status. Met de functie aan kan een respawnende Hunter een kit krijgen die is aangepast aan Runner-uitrusting en wedstrijdcontext; de meegeleverde spelersgids beschrijft de kit als zwakker dan het Runner-gemiddelde. Met de functie uit krijgen Hunters na overlijden geen automatische kit. Dit schakelt het trackingkompas niet uit.

Gebruik voor een directe instelling in plaats van omschakelen `/mhkit on`, `/mhkit off` of `/mhkit status`. De geïnspecteerde terugvalwaarde voor een nieuwe configuratie is ON.

#### Auto World Spawn

Klik op **Auto World Spawn** en kies **OFF**, **5 minutes**, **10 minutes**, **15 minutes**, **20 minutes** of **30 minutes**. Een keuze wordt opgeslagen en brengt je terug naar `/mhgui`; **Back** gaat terug zonder een nieuw interval te kiezen.

Indien ingeschakeld zoekt het systeem periodiek een veilige Overworld-oppervlakte nabij een actieve Runner daar en verplaatst de wereldspawn. Het slaat verplaatsing over als er geen Runner in de Overworld is of geen veilige plek gevonden wordt. De terugvalwaarde voor een nieuwe configuratie is OFF. Gebruik voor dezelfde bediening via commando `/mhspawn off`, `/mhspawn 15` of `/mhspawn status`, met een ondersteund interval in plaats van 15.

#### Pauze, opnieuw verbinden en herstel

**Pause Match** is beschikbaar als de wedstrijd RUNNING is. Het bevriest gameplay-systemen, beweging/interacties, wedstrijdtimers, tracking en spawnverplaatsing. **Resume Match** hervat die systemen en compenseert gepauzeerde tijd. Server Freeze bevriest alleen spelers en dient niet als vervanging wanneer ook de wedstrijdklok moet pauzeren.

Het Runner-terugkeervenster is instelbaar, met een nieuwe terugvalwaarde van **15 minuten**. Tijdig terugkeren herstelt Runner-status en geeft tien seconden bescherming. Serverdowntime verbruikt de opgeslagen terugkeertijd niet. Verlopen Runner-plaatsen worden Hunters; de timeout van de laatste Runner kan Hunters de winst geven.

**De aangeleverde 1.9.11-GUI bevat geen afzonderlijke keuze voor de terugkeerduur**. Stop om dit aan te passen de server, bewerk `plugins/VexLandManhunt/config.yml`, behoud de overige instellingen en stel in:

```yaml
features:
  custom-reconnect-minutes: 15
```

Herstart na bewerken. Waarden onder één minuut worden begrensd op één. **Reset Settings** zet dit terug op 15 minuten. De gecompileerde build bewaart ook wedstrijd-/verbindingsstatus en back-upsnapshots voor herstel na herstart/crash; laat de plugin die bestanden beheren in plaats van ze tijdens het spelen te bewerken.

#### Reset Settings en Reset Match

**Reset Settings** vereist twee klikken op de knop binnen **acht seconden**. De eerste zet de bevestiging klaar; de tweede herstelt **Smart Kit ON**, **Auto Spawn elke 15 minuten**, **Terugkeertijd 15 minuten** en een **willekeurige voorsprong**. Dit verschilt van een nieuwe installatie, waar Auto World Spawn terugvalt op OFF. Het verandert de configuratie; het vervangt de volledige wedstrijdreset niet.

**Reset Match** voert de bestaande wedstrijdreset uit, wist tijdelijke wedstrijdstatus/items en brengt spelers naar de Overworld-spawn voor een volgende ronde. De hoofdknop gebruikt niet de bevestiging met twee klikken van Reset Settings. **Start Match** kan deelnemersinventarissen voorbereiden/legen. Controleer welke reset-/startbediening je wilt gebruiken voordat je klikt.

#### Taal- en anti-cheatbediening

**Language** opent de globale keuze. Klik op de gewenste taal. Beide aangeleverde builds bevatten Engels, Perzisch, Arabisch, Spaans, Frans, Duits, Russisch, Vereenvoudigd Chinees, Hindi en Portugees. De geselecteerde taal geldt voor de server en wordt opgeslagen. Japanse README-documentatie voegt geen Japans toe aan de taalkeuze in de plugin.

**Anti-Cheat** opent **VexAC Security**. Klik op **VexAC Master** om de interne engine aan/uit te zetten, of op **Movement**, **Combat**, **AutoClick**, **Velocity / AntiKB** of **World / Scaffold** om die groep te schakelen. **Anti X-Ray** schakelt Papers ingestelde Anti-Xray; herstart de server om dit toe te passen. Status-, bewijslog- en detectiemodeltegels leggen de huidige systemen uit. **Back to Control Center** gaat terug naar het hoofdmenu.

De interface beschrijft moderatie via alleen monitoring, maar statische inspectie toont nog een kickpad op basis van drempelwaarden. Behandel de menutekst over geen kicks als een verschil tussen implementatie/documentatie en controleer moderatie op een gecontroleerde server voordat je erop vertrouwt.

#### Gids in het spel en probleemoplossing

Klik op **Manhunt Administrator Guide** of gebruik `/mhhelp` voor een vertaald gidsboek. Spelers kunnen in 1.9.11 `/mhhelp` gebruiken voor hun rolgebonden gids. Hunters klikken met rechts op hun kompas om een Runner te kiezen; die trackinginterface staat los van de beheerderskeuze Target Player.

Als een rol of kompas niet gesynchroniseerd lijkt, vernieuwt **Emergency Sync** de gerelateerde runtime. **Match Info** helpt teams en status te controleren. Mislukt een start, controleer dan of de wedstrijd klaarstaat, serverbevriezing uitstaat en er een Runner-/Hunter-team is. Gebruik na vervangen van de JAR een volledige serverherstart in plaats van `/reload`. `/mhdebug` is een beheerderscommando voor diagnostiek in 1.9.11; de aanwezigheid betekent niet dat deze versies tests op een actieve server hebben doorstaan.

#### Het oudere 1.6.4-controlecentrum gebruiken

1.6.4 behoudt **Player Roles**, **Friendly Fire**, **Start Match**, **Reset Match**, **Release Hunters Now**, **Server Lock**, **Teleport Everyone To Me**, **Heal & Feed Everyone**, **Match Status**, taalkeuze, **Anti Cheat** en een beheerdersgids. Rollen doorlopen **None → Runner → Hunter**, en rolwijzigingen zijn geblokkeerd terwijl een wedstrijd start/loopt.

Het anti-cheatmenu bevat de oude **Anti AutoClick** (30-CPS-regel met waarschuwing/kick), **Anti Fly** en Papers **Anti X-Ray**. Het Runner-terugkeervenster is vast **60 minuten**. De nieuwere Smart Hunter Kit V3-schakelaar, Auto World Spawn-keuze, pauze/hervatten, Reset Settings-bevestiging en uitgebreide doel-/wereldhulpmiddelen hierboven horen bij 1.9.11 en zijn niet te verwachten in het oudere menu.

Deze gids is afgeleid van metadata van de aangeleverde JARs, meegeleverde taal-/hulpteksten en statische disassemblage. De interface is tijdens deze inspectie niet uitgevoerd op een actieve Minecraft-server.

### 3. Speel de achtervolging

Runners ontsnappen tijdens de willekeurige voorsprong en werken toe naar het verslaan van de Ender Dragon. Hunters wachten op vrijlating en klikken dan met rechts op hun trackingkompas om een Runner te kiezen. Doelen kunnen tijdens het spelen veranderen, ook als de achtervolging dimensies doorkruist. Gebruik `/teammsg <message>` om alleen met je team te praten en `/mhhelp` voor de vertaalde rolgids in 1.9.11.

Als een Runner sterft, spelen de overige Runners door en wordt de overleden speler Hunter. Een Hunter kan respawnen en verder volgen. De dood van de laatste Runner of het verlopen van een Runner-terugkeertijd kan de wedstrijd voor Hunters beëindigen; het verslaan van de Ender Dragon beëindigt haar voor Runners.

### 4. Pauzeer, beëindig en bereid een volgende wedstrijd voor

Pauzeer in 1.9.11 met `/mhpause` en ga verder met `/mhresume`. Gebruik `/mhrelease` als Hunters vóór het einde van de voorsprongaftelling vrij moeten komen. Gebruik voor een nieuwe wedstrijd de volledige reset in het controlecentrum of `/mhreset`; de reset wist tijdelijke wedstrijdstatus en items en brengt spelers naar de Overworld-spawn. Wijzigingen in Paper Anti-Xray vereisen een herstart.

## Standaardinstellingen in 1.9.11

De geïnspecteerde terugvalwaarden voor een nieuwe configuratie zijn:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` betekent dat automatische spawnverplaatsing uitstaat. De bevestigde instellingenreset in de GUI stelt het spawninterval in op 15 minuten. Gebruik de GUI of `/mhkit` en `/mhspawn` voor de bijbehorende instellingen.

## Overzicht openbare commando’s

De genoemde beheerderscommando’s gebruiken `vexland.admin`, standaard voor OP. Teamchat, afval en nachtzicht hebben geen descriptorpermissie; `/mhhelp` wordt in 1.9.11 een spelers-/beheerdersgids.

| Commando | Doel | Beschikbaarheid |
| --- | --- | --- |
| `/mhgui` | Controlecentrum openen | Beide builds |
| `/mhstart` | Volledige startprocedure uitvoeren | Beide builds |
| `/mhreset` | Huidige wedstrijd volledig resetten | Beide builds |
| `/mhrelease` | Hunters eerder vrijlaten | Beide builds |
| `/mrunner <player>` | Runner toewijzen | Beide builds |
| `/mhunter <player>` | Hunter toewijzen | Beide builds |
| `/mhnone <player>` | Rol verwijderen | Alleen 1.6.4 |
| `/teammsg <message>` | Privébericht naar teamgenoten sturen | Beide builds |
| `/trash` | Wegwerpinventaris met 54 vakken openen | Beide; 1.9.11-aliassen: `/mhtrash`, `/vextrash` |
| `/nv` | Persoonlijk nachtzicht schakelen | Beide builds |
| `/mhlang` | Globale taalkeuze openen | Beide builds; beheerder |
| `/mhhelp` | Vertaald gidsboek ontvangen | 1.6.4 alleen beheerder; 1.9.11 spelers-/beheerdersgids |
| `/mhkit <on\|off\|toggle\|status>` | Smart Hunter-kits instellen | 1.9.11 |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Automatische spawnverplaatsing instellen | 1.9.11 |
| `/mhpause` | Lopende wedstrijd pauzeren | 1.9.11 |
| `/mhresume` | Gepauzeerde wedstrijd hervatten | 1.9.11 |
| `/mhdebug` | Interne diagnostiek uitvoeren | 1.9.11 |

## Talen in het spel en documentatietalen

Beide aangeleverde builds hebben **10 talen in het spel**: Engels, Perzisch, Arabisch, Spaans, Frans, Duits, Russisch, Vereenvoudigd Chinees, Hindi en Portugees. Een beheerder kiest de **globale servertaal** met `/mhlang`; berichten, menu’s, meldingen en gidsboeken gebruiken die keuze, opgeslagen in `language.txt`.

De GitHub-documentatie wordt gepubliceerd in **18 talen, zonder Arabische documentatie-editie**. Japans, Turks en andere aanvullende README-vertalingen helpen lezers het project te begrijpen; ze voegen geen talen in het spel toe aan deze originele JARs.

## Versiegeschiedenis en volgende build

[CHANGELOG.md](../../../CHANGELOG.md) legt verschillen tussen geüploade versies vast. De extra build met een specifieke spectatorfunctie **wacht op ontvangst voor een toekomstige release**. Bestaande verwijzingen naar vanilla Spectator bewijzen die nieuwe functie niet in de twee aangeleverde downloads. Iedere volgende aangeleverde build krijgt een eigen download, checksum en wijzigingsnotities na vergelijking met de vorige versie.

## Een speelse uitdaging aan Dream

Een beetje Minecraft-geplaag van Bardiya 😄

> "Zucht... Ali en ik hebben een Manhunt-plugin gemaakt die honderd keer beter is dan die van Dream, maar Dream is bang en wil de onze niet spelen!"

## Makers en projectomvang

**Samen gemaakt door [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) en [Ali · Alivexor](https://github.com/Alivexor).** Beide accounts staan ook als auteurs in de oorspronkelijke plugindescriptors.

Deze repository presenteert de originele gecompileerde releases, hun documentatie en versienotities als gezamenlijk portfolioproject. Functiebeschrijvingen zijn gebaseerd op statische inspectie van de aangeleverde JARs. Compatibiliteit op actieve servers, herstelprestaties, balans en anti-cheatnauwkeurigheid zijn niet getest tijdens deze publicatiewerkwijze.

[Bardiya’s GitHub-portfolio](https://github.com/FarlandGame) · [Ali’s GitHub](https://github.com/Alivexor) · [Alle releases](https://github.com/FarlandGame/Vexland_Manhunt/releases)
