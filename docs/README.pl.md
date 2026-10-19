# Vexland_Manhunt


[English](../README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**Kompletna rozgrywka Minecraft: Uciekinierzy kontra Łowcy, współtworzona przez [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) i [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt łączy konfigurację meczu, role drużyn, początek pościgu, śledzenie, postęp, nagrody, wyniki i administrację w jednej wtyczce dla serwera Paper. Uciekinierzy próbują pokonać Ender Dragona, a Łowcy próbują wyeliminować ostatniego Uciekiniera. Wtyczka obsługuje wielu Uciekinierów i utrzymuje pościg mimo śmierci, odrodzeń, zmian wymiaru i ponownych połączeń. Centrum sterowania `/mhgui` pozwala administratorom zarządzać meczem przez menu, z przetłumaczonymi komunikatami i poradnikami dla graczy.

## Pobieranie i zgodność

| Wydana wersja | Pobieranie | Instalacja |
|---|---|---|
| **2.0.0 — pakiet zintegrowany** | [VexLandManhunt-2.0.0.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0.jar) | **Jeden JAR**, ze zintegrowanym GrimAC 2.3.73 |
| **1.13.1 — gałąź z obserwatorami** | [Wydanie i oba pliki JAR](https://github.com/FarlandGame/Vexland_Manhunt/releases/tag/v1.13.1) | Manhunt i osobny GrimAC 2.3.73 |
| 1.9.11 / 1.6.4 — starsze | [Wszystkie wydania](https://github.com/FarlandGame/Vexland_Manhunt/releases) | Archiwalne samodzielne kompilacje |

**Paper 1.21.11 / Java 21.** Są to wtyczki serwerowe, a nie mody klienta. Nazwa dostarczonego pliku i publiczne wydanie to **2.0.0**, ale niezmieniony deskryptor zgłasza **`1.9.11-grim.1`** i wskazuje 1.9.11 jako podstawę rozgrywki. Ten zintegrowany pakiet **nie** zawiera osobnej roli Spectator, `/mspectator <player>`, `/mhspectate`, menu podzielonych na kategorie ani innych dodatków z 1.13.1. Jeśli potrzebujesz tych funkcji, korzystaj z osobno wymienionej gałęzi 1.13.1.

Oryginalne kompilacje na prywatny serwer, ze specjalnymi podwyższonymi uprawnieniami administracyjnymi twórców, zachowano w dostarczonej postaci. Poradnik opisuje publiczne elementy sterowania.

## Rozgrywka Manhunt

- **Drużyny Uciekinierów i Łowców:** przypisz graczy online do jednej ze stron. Mecz wymaga co najmniej jednego Uciekiniera oraz Łowcy lub gracza online bez przypisanej roli. Pozostali przy życiu Uciekinierzy grają dalej, gdy zginie członek drużyny; poległy Uciekinier zostaje Łowcą, chyba że ta śmierć kończy mecz.
- **Filmowy początek meczu:** ekwipunki i tryby gry są przygotowywane, drużyny przedstawiane, a ruletka losuje czas przewagi Uciekinierów. Podczas odliczania Łowcy są zamrożeni, z komunikatami tytułowymi i dźwiękami. Przewaga jest losowa; administratorzy mogą wcześniej wypuścić Łowców.
- **Kompas śledzący z wyborem celu:** Łowcy otrzymują specjalny kompas. Kliknij go prawym przyciskiem, aby wybrać Uciekiniera z menu celów i zmieniać cel podczas pościgu. Między wymiarami śledzenie prowadzi odpowiednią trasą przez portal, aż możliwe będzie śledzenie bezpośrednie. Łowcy ponownie otrzymują kompas po odrodzeniu.
- **Wskaźniki postępu:** paski bossów i informacje o meczu śledzą wyposażenie oraz postęp Uciekinierów przez zasoby Netheru, różdżki blaze, perły, Oczy Endera, twierdzę i End. Nowsza kompilacja dodaje dokładniejsze etapy oraz wizualizacje uwzględniające zdrowie smoka.
- **Nagrody za zabójstwa Uciekinierów:** gdy Uciekinier zabije Łowcę podczas aktywnego meczu, używana jest ważona pula 50 nagród uwzględniająca postęp. Obejmuje animowane losowania, podwójne/potrójne nagrody, ogłoszenia serii zabójstw i celebracje rzadkich przedmiotów.
- **Zwycięstwo i wyniki:** śmierć ostatniego Uciekiniera daje zwycięstwo Łowcom; pokonanie Ender Dragona daje zwycięstwo Uciekinierom. Uwzględniono tytuły końcowe, celebracje, informacje o zabójstwach/śmierciach i usuwanie tymczasowych przedmiotów. Nowsza kompilacja pokazuje także MVP, obrażenia i dystans.
- **Komunikacja drużynowa i narzędzia:** prywatne wiadomości do drużyny przez `/teammsg`, jednorazowy kosz z 54 miejscami przez `/trash` i osobiste widzenie w ciemności przez `/nv`.
- **Administracja przez menu:** role, start/reset, wcześniejsze wypuszczenie Łowców, przyjazny ogień, blokada serwera, teleportowanie wszystkich, leczenie/karmienie, język, ochrona, status i poradniki są dostępne w centrum sterowania. Zamrażanie i pełny reset pomagają przygotować kolejny mecz.
- **Przetłumaczone poradniki:** książki dla Uciekinierów, Łowców i administratorów wyjaśniają cele, użycie kompasu, śmierć, konfigurację i komendy. Wersja 1.9.11 udostępnia graczom poradnik dopasowany do roli przez `/mhhelp`.
- **Integracja z Paper Anti-Xray:** menu konfiguruje ochronę Paper na poziomie świata; zmiany wymagają restartu serwera, aby wejść w życie.

## Co zmieniło się w dostarczonym pakiecie 2.0.0?

- **Jeden zintegrowany JAR:** Manhunt, zmodyfikowany GrimAC 2.3.73 i dołączony PacketEvents współdzielą jedną instancję wtyczki Bukkit. Ten pakiet nie wymaga osobnej instalacji GrimAC ani PacketEvents. Deskryptor udostępnia `GrimAC`; archiwum ma spłaszczoną strukturę i nie zawiera zagnieżdżonego, niezmienionego pliku JAR Grim.
- **Stan modułów:** polecenie administratora `/vexintegration` pokazuje Grim ACTIVE/INACTIVE, właściciela Bukkit, stan VexAC, stan PacketEvents i liczbę śledzonych graczy. Natywne polecenia `/grim` i `/grimac` rejestruje zintegrowany moduł.
- **Kontrolowany rozruch:** moduł ładujący wymaga interfejsu konfiguracji Paper oraz dokładnie Minecraft 1.21.11. Odrzuca ładowanie przy obecności graczy online oraz osobną instancję GrimAC. Jeśli rozruch integracji się nie powiedzie, wtyczka zostaje wyłączona, a dziennik informuje o nieaktywnej ochronie Grim; sam serwer może nadal działać. Sprawdź stan przed rozpoczęciem meczu.
- **Migracja istniejących danych:** podczas pierwszego zintegrowanego ładowania migracja tworzy kopie zapasowe obu starych drzew danych wtyczek i kopiuje stare dane GrimAC tylko wtedy, gdy zintegrowany katalog docelowy jeszcze nie istnieje. Jeśli istnieją oba, pierwszeństwo mają dane integracji; nie są one scalane ani nadpisywane. Oryginalne dane pozostają zachowane.
- **Właściciel korekt ruchu:** `plugins/VexLandManhunt/integration.properties` domyślnie zawiera `movement-correction-owner=legacy`. Obsługiwaną alternatywą jest `grim`; inne wartości przerywają rozruch. Wybranie grim blokuje ścieżki korekty cofania/teleportacji VexAC, zachowując jego kontrole, alerty i materiał dowodowy. Nie wyłącza wszystkich kar starszego silnika.
- **Podstawa rozgrywki:** płaskie menu `/mhgui`, przełączanie ról Runner/Hunter, sterowanie VexAC, Smart Hunter Kit V3, pauza/wznowienie, odzyskiwanie oraz 683 przetłumaczone klucze pochodzą z 1.9.11. Jest to wydanie łączące pakowanie i integrację, a nie zestaw funkcji 1.13.1 z obserwatorami.

## Rozgrywka zachowana z podstawy 1.9.11

Poniższe systemy dodano do podstawy 1.9.11 i zachowano w tym zintegrowanym pakiecie. Są to odziedziczone funkcje rozgrywki, a nie nowe funkcje obserwatorów w 2.0.0.

| Dodatek lub zmiana | Działanie w 1.9.11 |
| --- | --- |
| **Smart Hunter Kit V3** | Adaptacyjne zestawy po odrodzeniu uwzględniają wyposażenie Uciekinierów, drużyny i kontekst meczu. System stara się utrzymać zestawy Łowców poniżej średniego wyposażenia Uciekinierów i można go włączać/wyłączać przez `/mhkit` lub GUI. |
| **Automatyczny spawn w Overworldzie** | Przenosi spawn świata w pobliże odpowiedniego Uciekiniera w Overworldzie w wybranym odstępie: wyłączone, 5, 10, 15, 20 lub 30 minut. System wybiera bezpieczne miejsce na powierzchni i pomija nieodpowiednie przypadki. |
| **Pauza i wznowienie** | `/mhpause` zatrzymuje rozgrywkę, liczniki meczu, śledzenie i przenoszenie spawnu; `/mhresume` wznawia. Czas pauzy jest wyłączany z aktywnego czasu meczu. |
| **Odzyskiwanie po restarcie/awarii** | Warstwa odzyskiwania przywraca stan meczu, role, cele kompasów, postęp, liczniki nagród/śmierci i stan ponownego połączenia dzięki głównym/zapasowym migawkom oraz zapisom okresowym i przy wyłączaniu. |
| **Ustawienia ponownego połączenia Uciekinierów** | Konfigurowalne okno zastępuje poprzednie stałe 60 minut. Początkowa wartość domyślna: 15 minut, z 10 sekundami ochrony po powrocie. Przestój serwera nie jest wliczany; wygaśnięcie może zamienić Uciekiniera w Łowcę lub zakończyć mecz. |
| **Rozszerzona administracja** | Zmieniaj role podczas trwającego meczu, zachowując ostatniego Uciekiniera; działania na wybranym graczu, teleportowanie/zamrażanie drużyn, ponowna synchronizacja stanu wykonania i skróty usprawniają zarządzanie. |
| **Reset ustawień z potwierdzeniem** | Dwa kliknięcia w ciągu ośmiu sekund ustawiają Smart Kit ON, automatyczny spawn co 15 minut i ponowne połączenie 15 minut. To różni się od świeżej instalacji, gdzie automatyczny spawn jest domyślnie OFF. |
| **VexAC 3.0** | Kontrole ruchu, walki, AutoClick, prędkości/odrzutu i budowania; sterowanie grupami/całością, dziennik dowodów, alerty administratorów i wyjątki dla środowiska/lagów. |
| **Ultra Deep Debug v4** | `/mhdebug` zapewnia diagnostykę maszyny stanów, GUI, syntetycznych zestawów/obciążenia, znaczników językowych, pełnego cyklu odzyskiwania i integralności. |
| **Rozszerzone wskaźniki** | Więcej szczegółów postępu, zdrowie smoka, wyniki MVP/obrażeń/dystansu i ping w TAB. |
| **Zmiany komend** | Dodaje `/mhkit`, `/mhspawn`, `/mhpause`, `/mhresume` i `/mhdebug`; usuwa `/mhnone`; dostosowuje `/mhhelp` do graczy/administratorów i dodaje aliasy `/trash`. |
| **Więcej przetłumaczonych komunikatów** | Zasoby tłumaczeń rosną z 446 kluczy komunikatów na język do 683. |

Dołączone kontrole VexAC obejmują Fly, Speed, Timer, Phase, Step, NoSlow, GroundSpoof, Reach, KillAura, AimAssist, uderzenia przez ściany, BadPackets, wzorce czasowe AutoClick, zmodyfikowany odrzut, Scaffold, Tower, FastPlace, Nuker i zasięg bloków. Interfejs używa etykiety „tylko monitorowanie”, ale skompilowany kod zawiera również ścieżki wyrzucania graczy; potwierdź faktyczne działanie moderacji na serwerze testowym, zanim zaufasz tej etykiecie. Wcześniejsza kompilacja zawiera zamiast tego starsze kontrolki Anti AutoClick i Anti Fly.

## Pełna konfiguracja i obsługa przez `/mhgui`

### 1. Instalacja zintegrowanej kompilacji

1. Całkowicie zatrzymaj serwer **Paper 1.21.11 / Java 21** i utwórz kopie zapasowe światów oraz danych wtyczek.
2. Umieść w `plugins/` wyłącznie `VexLandManhunt-2.0.0.jar` z tego wydania. Przenieś starsze pliki JAR Manhunt i samodzielnego GrimAC poza aktywny katalog wtyczek. Zachowaj ich foldery danych; nie usuwaj ich. Gracze nie instalują tego pliku JAR po stronie klienta.
3. Uruchom serwer normalnie, zamiast używać `/reload`. Zintegrowany moduł ładujący zarządza cyklem życia Grim i PacketEvents.
4. Jako OP lub z uprawnieniem `vexland.admin` wykonaj `/vexintegration`. Sprawdź `Grim=ACTIVE` i `PacketEvents=true`, zanim przejdziesz do `/mhgui`. Nieaktywna ochrona oznacza problem z rozruchem, a nie udaną instalację integracji.

Konfiguracja Grim znajduje się w `plugins/VexLandManhunt/grim/` (`config.yml`, `messages.yml`, `punishments.yml`, `discord.yml`), z opcjonalną historią `violations.sqlite`. Kopie zapasowe pierwszej migracji trafiają do `plugins/VexLandManhunt-integration-backups/`; `plugins/VexLandManhunt/integration-migration-v1.txt` oznacza jej zakończenie. Jeśli istnieją zarówno stare, jak i zintegrowane dane Grim, katalog docelowy integracji zostaje zachowany i zapisywane jest ostrzeżenie. Migracja odrzuca dowiązania symboliczne.

Sprawdź właściciela korekt ruchu w `plugins/VexLandManhunt/integration.properties`; zachowaj pozostałe ustawienia. Wartość domyślna nowej instalacji:

```properties
movement-correction-owner=legacy
```

Pełny poradnik publicznych menu poniżej odpowiada podstawie rozgrywki 1.9.11 tego pakietu. Gałąź z obserwatorami ma własny zarchiwizowany poradnik.

### 2. Otwórz centrum sterowania

Dołącz do serwera jako administrator z **OP** lub uprawnieniem **`vexland.admin`** i wpisz:

```text
/mhgui
```

Poniższe instrukcje opisują publiczny interfejs wersji **2.0.0**, używając angielskich nazw przycisków. Etykiety odpowiadają wybranemu językowi serwera. Do pełnej obsługi GUI używaj zaufanego konta **OP**: uprawnienie w deskryptorze pozwala otworzyć komendę, ale niektóre dostarczone procedury GUI stosują bardziej rygorystyczne kontrole OP. Główny ekwipunek ma pięć rzędów po dziewięć miejsc. Najedź kursorem na przycisk, aby odczytać opis i aktualne ustawienie. Większość przycisków używa zwykłego kliknięcia; specjalne działania myszy i potwierdzenia opisano poniżej. Mniejsze menu 1.6.4 omówiono na końcu.

#### Przygotuj pierwszy mecz

1. Otwórz **Player Roles**. Klikaj głowę każdego uczestnika, aż wyświetli się właściwa rola. W 2.0.0 rola przełącza się między **Runner** i **Hunter**; uczestnik bez roli staje się Uciekinierem po pierwszym kliknięciu. Kliknięcia lewym/prawym/z Shift nie są osobnymi skrótami wyboru roli. W razie potrzeby używaj **Previous Page**, **Next Page** i **Back to Control Center**.
2. Przypisz co najmniej jednego Uciekiniera i co najmniej jednego Łowcę. Procedura startowa może zmienić pozostałych graczy online bez roli w Łowców, więc jawne przypisanie wszystkich uczestników wyjaśnia skład drużyn.
3. Kliknij **Friendly Fire**, aby wybrać, czy członkowie drużyny mogą zadawać sobie obrażenia. Po kliknięciu sprawdź wskaźnik ON/OFF.
4. Kliknij **Language**, aby wybrać język całego serwera. Ustawienie wpływa na komunikaty, interfejsy, powiadomienia i poradniki wszystkich, nie tylko twojego gracza.
5. Sprawdź **Smart Hunter Kit**, **Auto World Spawn** i **Anti-Cheat**. Jeśli potrzebujesz wyjaśnienia w grze, przeczytaj poradnik administratora z przycisku książki.
6. Upewnij się, że **Server Freeze** jest wyłączone, i kliknij **Start Match**. Start przygotowuje graczy i ich ekwipunki, uruchamia wprowadzenie i losową ruletkę przewagi przed wypuszczeniem Łowców, a potem rozpoczyna polowanie. Przed startem przechowaj wszystko, co chcesz zachować, poza ekwipunkami uczestników.

#### Główne przyciski centrum sterowania

Pozycje liczą rzędy od góry do dołu, a kolumny od lewej do prawej. Opisują ostateczny, ozdobiony układ 2.0.0.

| Pozycja | Angielski przycisk | Działanie |
|---|---|---|
| Rząd 2, kolumna 2 | Player Roles | Otwiera stronicowane menu głów graczy Uciekinierów/Łowców. |
| Rząd 2, kolumna 3 | Target Player | Przełącza między innymi graczami online dla działań administratora na wybranym celu. Sprawdź aktualną nazwę. |
| Rząd 2, kolumna 4 | Friendly Fire | Włącza/wyłącza obrażenia między członkami drużyny. |
| Rząd 2, kolumna 5 | Match Info | Wysyła krótki raport stanu meczu, drużyn, przyjaznego ognia i wybranego celu. |
| Rząd 2, kolumna 6 | Start Match | Uruchamia normalny start meczu i losową sekwencję przewagi. |
| Rząd 2, kolumna 7 | Full Heal | Przywraca zdrowie wszystkich graczy online. |
| Rząd 2, kolumna 8 | Reset Match | Wykonuje pełny reset meczu. Różni się od Reset Settings. |
| Rząd 3, kolumna 2 | Full Hunger | Przywraca jedzenie i nasycenie wszystkich graczy online. |
| Rząd 3, kolumna 3 | Release Hunters | Wypuszcza oczekujących Łowców przed końcem przewagi. |
| Rząd 3, kolumna 4 | Clear Effects | Usuwa efekty mikstur ze wszystkich graczy online. |
| Rząd 3, kolumna 5 | Server Freeze | Włącza/wyłącza globalne zamrożenie serwera; zwykli gracze bez OP zostają zamrożeni. |
| Rząd 3, kolumna 6 | Clear Target Inventory | Czyści ekwipunek, zbroję i drugą rękę wybranego gracza po potwierdzeniu. |
| Rząd 3, kolumna 7 | Teleport Everyone | Przenosi wszystkich graczy online do twojej aktualnej pozycji. |
| Rząd 3, kolumna 8 | Kill Target | Zabija wybranego gracza po potwierdzeniu; normalne zasady śmierci mogą wpłynąć na mecz. |
| Rząd 4, kolumna 2 | Anti-Cheat | Otwiera kontrolki VexAC Security. |
| Rząd 4, kolumna 3 | Freeze Target | Włącza/wyłącza indywidualne zamrożenie wybranego gracza. |
| Rząd 4, kolumna 4 | Emergency Restore | Przywraca zdrowie, jedzenie i nasycenie wszystkich online. |
| Rząd 4, kolumna 5 | Freeze Team | Lewy przycisk przełącza Uciekinierów; prawy Łowców; Shift-klik usuwa zamrożenia indywidualne/drużynowe. |
| Rząd 4, kolumna 6 | Set Day | Ustawia dzień w twoim aktualnym świecie. |
| Rząd 4, kolumna 7 | Clear Weather | Zatrzymuje deszcz i burzę w aktualnym świecie. |
| Rząd 4, kolumna 8 | Language | Otwiera globalny wybór języka. |
| Rząd 5, kolumna 2 | Smart Hunter Kit | Włącza/wyłącza adaptacyjne zestawy Łowców po odrodzeniu; pokazuje ON/OFF. |
| Rząd 5, kolumna 3 | Clear Dropped Items | Usuwa upuszczone przedmioty w aktualnym świecie. |
| Rząd 5, kolumna 4 | Pause Match / Resume Match | Zatrzymuje lub wznawia aktywną rozgrywkę i liczniki meczu. |
| Rząd 5, kolumna 5 | Emergency Sync | Ponownie synchronizuje role, kompasy i powiązany stan wykonania. |
| Rząd 5, kolumna 6 | Reset Settings | Przywraca zrównoważone ustawienia po potwierdzeniu dwoma kliknięciami. |
| Rząd 5, kolumna 7 | Close | Zamyka centrum sterowania. |
| Rząd 5, kolumna 8 | Auto World Spawn | Otwiera wybór odstępu automatycznego spawnu w Overworldzie. |
| Rząd 5, kolumna 9 | Manhunt Administrator Guide | Daje przetłumaczoną książkę poradnika administratora. |

Dekoracyjne szkło oraz elementy tytułu/statusu nie są przyciskami rozgrywki.

#### Role i wybrane cele

**Player Roles** zmienia faktyczną drużynę Manhunt uczestnika. Kliknij głowę i odczytaj zaktualizowaną rolę. Podczas STARTING/RUNNING interfejs pozwala zmieniać Uciekinierów/Łowców, ale odmawia zamiany ostatniego Uciekiniera w Łowcę. Zachowuje to stronę Uciekinierów w trwającym meczu. Zmieniaj role świadomie, ponieważ stan drużyn i kompasy są po zmianie synchronizowane.

**Target Player** działa osobno: wybiera kogoś do działań takich jak Freeze Target, Clear Target Inventory lub Kill Target bez zmiany drużyny. Przełączaj, aż pokaże się nazwa właściwego gracza online. Jeśli zapisany cel stanie się niedostępny, kod może wybrać pierwszego innego gracza online; dlatego zawsze sprawdzaj nazwę bezpośrednio przed działaniem na wybranym celu. Jeśli nikt inny nie jest online, informuje o braku dostępnego celu.

**Clear Target Inventory** i **Kill Target** wymagają dwukrotnego kliknięcia tego samego działania dla tego samego celu w ciągu **pięciu sekund**. Pierwsze kliknięcie przygotowuje potwierdzenie i wskazuje cel; drugie wykonuje działanie. Zmiana celu lub zbyt długie oczekiwanie wymaga nowego potwierdzenia. Czyszczenie ekwipunku usuwa jego zawartość; zabicie Uciekiniera może zakończyć lub zmienić mecz według normalnych zasad śmierci.

**Freeze Team** ma jedyne w tym menu skróty myszy przypisane do drużyn: zwykłe lewe kliknięcie wybiera Uciekinierów, zwykłe prawe Łowców, a Shift-klik usuwa wszystkie indywidualne/drużynowe zamrożenia zarządzane tym narzędziem. Globalny przełącznik Server Freeze jest osobny i trzeba go osobno wyłączyć, jeśli gracze pozostają zamrożeni.

#### Smart Hunter Kit

Kliknij **Smart Hunter Kit**, aby włączyć lub wyłączyć adaptacyjne zestawy Łowców po odrodzeniu. Przycisk pokazuje bieżący stan. Po włączeniu odradzający się Łowca może otrzymać zestaw dopasowany do wyposażenia Uciekinierów i kontekstu meczu; dołączony poradnik opisuje go jako słabszy od średniej Uciekinierów. Po wyłączeniu Łowcy nie dostają automatycznego zestawu po śmierci. Nie wyłącza to kompasu śledzącego.

Do bezpośredniego ustawienia zamiast przełączania użyj `/mhkit on`, `/mhkit off` lub `/mhkit status`. Sprawdzona wartość awaryjna dla nowej konfiguracji to ON.

#### Auto World Spawn

Kliknij **Auto World Spawn**, a następnie wybierz **OFF**, **5 minutes**, **10 minutes**, **15 minutes**, **20 minutes** lub **30 minutes**. Wybór zapisuje opcję i wraca do `/mhgui`; **Back** wraca bez wybierania nowego odstępu.

Po włączeniu system okresowo szuka bezpiecznej powierzchni Overworldu w pobliżu aktywnego Uciekiniera w tym wymiarze i przenosi tam spawn świata. Pomija przeniesienie, jeśli nie ma Uciekiniera w Overworldzie lub nie znajduje bezpiecznego miejsca. Wartość awaryjna nowej konfiguracji to OFF. Te same ustawienia przez komendy to `/mhspawn off`, `/mhspawn 15` lub `/mhspawn status`, z dowolnym obsługiwanym odstępem zamiast 15.

#### Pauza, ponowne połączenie i odzyskiwanie

**Pause Match** jest dostępne, gdy mecz jest RUNNING. Zatrzymuje systemy rozgrywki, ruch/interakcje, liczniki meczu, śledzenie i przenoszenie spawnu. **Resume Match** wznawia te systemy i kompensuje czas pauzy. Server Freeze zamraża tylko graczy i nie zastępuje pauzy, gdy trzeba zatrzymać zegar meczu.

Okno ponownego połączenia Uciekinierów jest konfigurowalne, z początkową wartością awaryjną **15 minut**. Powrót na czas przywraca stan Uciekiniera i zapewnia dziesięć sekund ochrony. Przestój serwera nie zużywa zapisanego czasu powrotu. Wygasłe miejsca Uciekinierów zmieniają się w Łowców; przekroczenie czasu ostatniego Uciekiniera może dać zwycięstwo Łowcom.

**Dostarczone GUI 2.0.0 nie ma osobnego wyboru czasu ponownego połączenia**. Aby go zmienić, zatrzymaj serwer, edytuj `plugins/VexLandManhunt/config.yml`, zachowaj pozostałe ustawienia i ustaw:

```yaml
features:
  custom-reconnect-minutes: 15
```

Po edycji uruchom ponownie. Wartości poniżej jednej minuty są podnoszone do jednej. **Reset Settings** przywraca 15 minut. Skompilowana wersja zapisuje również stan meczu/ponownego połączenia i zapasowe migawki do odzyskiwania po restartach/awariach; pozwól wtyczce zarządzać tymi plikami zamiast edytować je podczas gry.

#### Reset Settings i Reset Match

**Reset Settings** wymaga dwukrotnego kliknięcia przycisku w ciągu **ośmiu sekund**. Pierwsze przygotowuje potwierdzenie; drugie przywraca **Smart Kit ON**, **Auto Spawn co 15 minut**, **Ponowne połączenie 15 minut** oraz **losową przewagę początkową**. Różni się to od świeżej instalacji, gdzie Auto World Spawn używa OFF. Zmienia konfigurację; nie zastępuje pełnego resetu meczu.

**Reset Match** wykonuje istniejący reset meczu, usuwając tymczasowy stan/przedmioty i przenosząc graczy do spawnu Overworldu na kolejną rundę. Główny przycisk nie używa potwierdzenia dwoma kliknięciami z Reset Settings. **Start Match** może przygotowywać/czyścić ekwipunki uczestników. Przed kliknięciem sprawdź, którego resetu/startu chcesz użyć.

#### Sterowanie językiem i anti-cheatem

**Language** otwiera globalny wybór. Kliknij żądany język. Obie dostarczone kompilacje zawierają angielski, perski, arabski, hiszpański, francuski, niemiecki, rosyjski, chiński uproszczony, hindi i portugalski. Wybrany język jest wspólny dla serwera i zapisywany. Japońska dokumentacja README nie dodaje japońskiego do wyboru języka w grze.

**Anti-Cheat** otwiera **VexAC Security**. Kliknij **VexAC Master**, aby włączyć/wyłączyć wewnętrzny silnik, lub **Movement**, **Combat**, **AutoClick**, **Velocity / AntiKB** albo **World / Scaffold**, aby przełączyć grupę. **Anti X-Ray** przełącza skonfigurowane Anti-Xray Paper; zrestartuj serwer, aby zastosować zmianę. Kafelki statusu, dziennika dowodów i modelu wykrywania opisują bieżące systemy. **Back to Control Center** wraca do menu głównego.

Interfejs kompilacji opisuje moderację wyłącznie przez monitorowanie, ale inspekcja statyczna zachowuje ścieżkę wyrzucania po przekroczeniu progu. Traktuj tekst menu o braku wyrzucania jako rozbieżność implementacji/dokumentacji i potwierdź zachowanie moderacji na kontrolowanym serwerze, zanim na nim polegasz.

#### Zintegrowany GrimAC i starszy VexAC

Istniejący interfejs **VexAC Security** steruje starszym silnikiem VexAC; jego przyciski Master/group nie stanowią nowego panelu sterowania Grim. Zintegrowany GrimAC działa obok niego. Używaj `/vexintegration` do sprawdzania stanu modułów oraz natywnych `/grim` lub `/grimac`, aby korzystać z poleceń Grim i narzędzi chronionych uprawnieniami. Ustawienia Grim i reguły kar znajdują się w `plugins/VexLandManhunt/grim/`.

Menu monitora/grup GrimBridge z 1.13.1 i `grim-settings.yml` nie opisują tego pakietu. Nie zakładaj, że wyłączenie VexAC wyłącza również zintegrowany GrimAC ani że etykieta monitora oznacza zasadę bez wyrzucania graczy. Paper Anti-Xray pozostaje niezależnym ustawieniem wymagającym ponownego uruchomienia.

#### Poradnik w grze i rozwiązywanie problemów

Kliknij **Manhunt Administrator Guide** lub użyj `/mhhelp`, aby otrzymać przetłumaczony poradnik. Gracze mogą w 2.0.0 używać `/mhhelp` do poradnika dla swojej roli. Łowcy klikają kompas prawym przyciskiem, aby wybrać Uciekiniera; ten interfejs śledzenia jest osobny od administracyjnego wyboru Target Player.

Jeśli rola lub kompas wygląda na niezsynchronizowany, **Emergency Sync** odświeża powiązany stan wykonania. **Match Info** pomaga sprawdzić drużyny i stan. Jeśli start się nie udaje, sprawdź gotowość meczu, wyłączenie zamrożenia serwera i obecność drużyny Uciekinierów/Łowców. Po zmianie JAR-a wykonaj pełny restart zamiast `/reload`. `/mhdebug` jest administracyjną komendą diagnostyczną w 2.0.0; jej obecność nie oznacza, że te wydania przeszły testy na działającym serwerze.

#### Korzystanie ze starszego centrum sterowania 1.6.4

1.6.4 zachowuje **Player Roles**, **Friendly Fire**, **Start Match**, **Reset Match**, **Release Hunters Now**, **Server Lock**, **Teleport Everyone To Me**, **Heal & Feed Everyone**, **Match Status**, wybór języka, **Anti Cheat** i poradnik administratora. Role przechodzą przez **None → Runner → Hunter**, a zmiany są zablokowane, gdy mecz się rozpoczyna/trwa.

Menu anti-cheat zawiera starsze **Anti AutoClick** (reguła 30 CPS z ostrzeganiem/wyrzucaniem), **Anti Fly** i **Anti X-Ray** Paper. Okno powrotu Uciekinierów wynosi stale **60 minut**. Nowszy przełącznik Smart Hunter Kit V3, wybór Auto World Spawn, pauza/wznowienie, potwierdzenie Reset Settings i rozszerzone narzędzia celów/świata opisane powyżej należą do 2.0.0 i nie należy ich oczekiwać w starszym menu.

Ten poradnik opracowano z metadanych dostarczonych JAR-ów, dołączonych tekstów językowych/pomocy i statycznej deasemblacji. Podczas inspekcji interfejs nie był uruchamiany na działającym serwerze Minecraft.

### 3. Rozegraj pościg

Uciekinierzy uciekają w czasie losowej przewagi początkowej i dążą do pokonania Ender Dragona. Łowcy czekają na wypuszczenie, a potem klikają kompas prawym przyciskiem, aby wybrać Uciekiniera. Cele można zmieniać w trakcie gry, także gdy pościg przekracza wymiary. Użyj `/teammsg <message>`, aby rozmawiać tylko z drużyną, i `/mhhelp` dla przetłumaczonego poradnika roli w 2.0.0.

Jeśli Uciekinier zginie, pozostali grają dalej, a poległy gracz zostaje Łowcą. Łowca może się odrodzić i kontynuować śledzenie. Śmierć ostatniego Uciekiniera lub wygaśnięcie jego czasu powrotu może zakończyć mecz zwycięstwem Łowców; pokonanie Ender Dragona kończy go zwycięstwem Uciekinierów.

### 4. Wstrzymaj, zakończ i przygotuj kolejny mecz

W 2.0.0 wstrzymaj przez `/mhpause` i kontynuuj przez `/mhresume`. Użyj `/mhrelease`, jeśli Łowcy mają zostać wypuszczeni przed końcem odliczania przewagi. Do nowego meczu użyj pełnego resetu z centrum sterowania lub `/mhreset`; usuwa on tymczasowy stan i przedmioty oraz przenosi graczy do spawnu Overworldu. Zmiana ustawień Paper Anti-Xray wymaga restartu.

## Ustawienia domyślne zintegrowanego pakietu 2.0.0

Sprawdzone wartości awaryjne świeżej konfiguracji to:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` oznacza wyłączenie automatycznego przenoszenia spawnu. Potwierdzony reset ustawień w GUI ustawia zamiast tego odstęp 15 minut. Używaj GUI albo `/mhkit` i `/mhspawn` do odpowiednich ustawień.

## Publiczna lista poleceń — zintegrowane 2.0.0

Polecenia administratora wymagają OP lub `vexland.admin` (domyślnie OP). Czat drużynowy, kosz i noktowizja to narzędzia dla graczy; `/mhhelp` udostępnia poradnik dostosowany do roli. Tabela wymienia 17 poleceń Manhunt/integracji; natywne polecenia Grim mają własne uprawnienia. `/mhnone` nie jest tutaj zarejestrowane.

| Komenda | Cel |
| --- | --- |
| `/vexintegration` | Pokaż stan zintegrowanych Grim, VexAC, PacketEvents oraz wspólnego właściciela Bukkit |
| `/mhgui` | Otwiera centrum sterowania |
| `/mhstart` | Uruchamia pełną sekwencję startu |
| `/mhreset` | Całkowicie resetuje bieżący mecz |
| `/mhrelease` | Wcześniej wypuszcza Łowców |
| `/mrunner <player>` | Przypisuje Uciekiniera |
| `/mhunter <player>` | Przypisuje Łowcę |
| `/teammsg <message>` | Wysyła prywatną wiadomość do drużyny |
| `/trash` | Otwiera jednorazowy kosz z 54 miejscami |
| `/nv` | Przełącza osobiste widzenie w ciemności |
| `/mhlang` | Otwiera globalny wybór języka |
| `/mhhelp` | Daje przetłumaczoną książkę poradnika |
| `/mhkit <on\|off\|toggle\|status>` | Konfiguruje inteligentne zestawy Łowców |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Konfiguruje automatyczne przenoszenie spawnu |
| `/mhpause` | Wstrzymuje trwający mecz |
| `/mhresume` | Wznawia wstrzymany mecz |
| `/mhdebug` | Uruchamia wewnętrzną diagnostykę |

## Języki gry i dokumentacji

Pakiet zachowuje **10 języków gry**: angielski, perski, arabski, hiszpański, francuski, niemiecki, rosyjski, chiński uproszczony, hindi i portugalski. Każde dołączone tłumaczenie zawiera **683 klucze**, zgodnie z 1.9.11. `/mhlang` ustawia jeden język dla całego serwera, zapisywany w `language.txt`.

Dokumentacja projektu jest dostępna w **18 językach**, bez arabskiej wersji dokumentacji. Te tłumaczenia nie dodają japońskiego ani innych dodatkowych języków gry do niezmienionego pliku binarnego.

## Historia wersji, źródła i autorzy

[CHANGELOG.md](../CHANGELOG.md) opisuje każde dostarczone wydanie. Pełny [poradnik obserwatorów 1.13.1](archive/1.13.1/README.pl.md) i [starszy poradnik 1.9.11 / 1.6.4](archive/1.9.11/README.pl.md) pozostają dostępne. Każda dostarczona wersja zachowuje własny plik do pobrania i sumę kontrolną.

**Współtwórcami Manhunt są Bardiya / Farland_game i Ali / Alivexor. GrimAC jest osobnym projektem GrimAC / DefineOutside i współtwórców.** Ten zintegrowany artefakt modyfikuje trzy klasy Grim; nie jest niezmienionym oficjalnym plikiem binarnym Grim ze starszego wydania z dwoma plikami. Dołączony [pakiet źródłowy](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0-source.zip) zachowuje dostarczone źródła, skrypty budowania, wejściowe pliki zależności i informacje licencyjne; pominięto dowody z testów/uruchomień, a kod źródłowy pozostawiono bez zmian. Wydanie zawiera również tekst GPLv3, sumy kontrolne i [informacje o składnikach zewnętrznych](../THIRD_PARTY_NOTICES.md). Podczas tej publikacji nie wykonano testów na uruchomionym serwerze ani testu odtwarzalności kompilacji.

## Żartobliwe wyzwanie dla Dreama

Trochę minecraftowego przekomarzania od Bardiyi 😄

> "Ech... Ali i ja zrobiliśmy wtyczkę Manhunt sto razy lepszą od tej Dreama, ale Dream się boi i nie chce zagrać na naszej!"

## Twórcy i zakres projektu

**Współtworzony przez [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) i [Ali · Alivexor](https://github.com/Alivexor).** Oba konta są również zapisane jako autorzy w oryginalnych deskryptorach wtyczki.

To repozytorium prezentuje oryginalne skompilowane wydania, dokumentację i informacje o wersjach jako wspólny projekt portfolio. Opisy funkcji opierają się na statycznej inspekcji dostarczonych JAR-ów. Zgodność na działającym serwerze, wydajność odzyskiwania, balans i dokładność anti-cheatu nie były testowane w tym procesie publikacji.

[Portfolio Bardiyi na GitHubie](https://github.com/FarlandGame) · [GitHub Alego](https://github.com/Alivexor) · [Wszystkie wydania](https://github.com/FarlandGame/Vexland_Manhunt/releases)
