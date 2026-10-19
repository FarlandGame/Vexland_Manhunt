# Vexland_Manhunt — 1.9.11 / 1.6.4

> Archiwalny przewodnik wersji · [2.0.0 →](../../README.pl.md)

[English](README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**Kompletna rozgrywka Minecraft: Uciekinierzy kontra Łowcy, współtworzona przez [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) i [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt łączy konfigurację meczu, role drużyn, początek pościgu, śledzenie, postęp, nagrody, wyniki i administrację w jednej wtyczce dla serwera Paper. Uciekinierzy próbują pokonać Ender Dragona, a Łowcy próbują wyeliminować ostatniego Uciekiniera. Wtyczka obsługuje wielu Uciekinierów i utrzymuje pościg mimo śmierci, odrodzeń, zmian wymiaru i ponownych połączeń. Centrum sterowania `/mhgui` pozwala administratorom zarządzać meczem przez menu, z przetłumaczonymi komunikatami i poradnikami dla graczy.

## Pobieranie i zgodność

| Wersja wtyczki | Pobieranie | Środowisko docelowe |
| --- | --- | --- |
| **1.9.11** — bieżąca dostarczona kompilacja | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Paper **1.21.11**, Java **21** |
| **1.6.4** — wcześniejsza kompilacja | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Paper **1.21.11**, Java **21** |

**1.6.4 i 1.9.11 to numery wersji wtyczki.** Obie dostarczone kompilacje deklarują API Minecraft `1.21.11` i pliki klas Java 21. Są to wtyczki serwerowe dla Minecraft Java Edition. [Wymagania Java dla poszczególnych wersji Paper](https://docs.papermc.io/paper/getting-started/) również wskazują Java 21 dla Paper 1.21.11. Dostarczone deskryptory nie deklarują dodatkowych zależności od innych wtyczek.

Są to **oryginalne kompilacje dla osobistego serwera, z podwyższonym dostępem administracyjnym przypisanym do twórców**, zachowane dokładnie w dostarczonej postaci. Poniższy poradnik opisuje publiczne sterowanie Manhunt.

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

## Co nowego w 1.9.11?

Te zmiany zidentyfikowano przez porównanie dwóch dostarczonych kompilacji, w tym metadanych, zasobów komunikatów i skompilowanych klas.

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

### 1. Zainstaluj jedną kompilację na serwerze

Zatrzymaj serwer **Paper 1.21.11 / Java 21**. Umieść jeden z pobranych JAR-ów w katalogu `plugins/`. Miej zainstalowaną tylko jedną kompilację VexLandManhunt naraz. Po zastąpieniu kompilacji wykonaj pełny restart serwera. Wewnętrzna nazwa wtyczki pozostaje `VexLandManhunt`; publiczna nazwa projektu to `Vexland_Manhunt`.

### 2. Otwórz centrum sterowania

Dołącz do serwera jako administrator z **OP** lub uprawnieniem **`vexland.admin`** i wpisz:

```text
/mhgui
```

Poniższe instrukcje opisują publiczny interfejs wersji **1.9.11**, używając angielskich nazw przycisków. Etykiety odpowiadają wybranemu językowi serwera. Do pełnej obsługi GUI używaj zaufanego konta **OP**: uprawnienie w deskryptorze pozwala otworzyć komendę, ale niektóre dostarczone procedury GUI stosują bardziej rygorystyczne kontrole OP. Główny ekwipunek ma pięć rzędów po dziewięć miejsc. Najedź kursorem na przycisk, aby odczytać opis i aktualne ustawienie. Większość przycisków używa zwykłego kliknięcia; specjalne działania myszy i potwierdzenia opisano poniżej. Mniejsze menu 1.6.4 omówiono na końcu.

#### Przygotuj pierwszy mecz

1. Otwórz **Player Roles**. Klikaj głowę każdego uczestnika, aż wyświetli się właściwa rola. W 1.9.11 rola przełącza się między **Runner** i **Hunter**; uczestnik bez roli staje się Uciekinierem po pierwszym kliknięciu. Kliknięcia lewym/prawym/z Shift nie są osobnymi skrótami wyboru roli. W razie potrzeby używaj **Previous Page**, **Next Page** i **Back to Control Center**.
2. Przypisz co najmniej jednego Uciekiniera i co najmniej jednego Łowcę. Procedura startowa może zmienić pozostałych graczy online bez roli w Łowców, więc jawne przypisanie wszystkich uczestników wyjaśnia skład drużyn.
3. Kliknij **Friendly Fire**, aby wybrać, czy członkowie drużyny mogą zadawać sobie obrażenia. Po kliknięciu sprawdź wskaźnik ON/OFF.
4. Kliknij **Language**, aby wybrać język całego serwera. Ustawienie wpływa na komunikaty, interfejsy, powiadomienia i poradniki wszystkich, nie tylko twojego gracza.
5. Sprawdź **Smart Hunter Kit**, **Auto World Spawn** i **Anti-Cheat**. Jeśli potrzebujesz wyjaśnienia w grze, przeczytaj poradnik administratora z przycisku książki.
6. Upewnij się, że **Server Freeze** jest wyłączone, i kliknij **Start Match**. Start przygotowuje graczy i ich ekwipunki, uruchamia wprowadzenie i losową ruletkę przewagi przed wypuszczeniem Łowców, a potem rozpoczyna polowanie. Przed startem przechowaj wszystko, co chcesz zachować, poza ekwipunkami uczestników.

#### Główne przyciski centrum sterowania

Pozycje liczą rzędy od góry do dołu, a kolumny od lewej do prawej. Opisują ostateczny, ozdobiony układ 1.9.11.

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

**Dostarczone GUI 1.9.11 nie ma osobnego wyboru czasu ponownego połączenia**. Aby go zmienić, zatrzymaj serwer, edytuj `plugins/VexLandManhunt/config.yml`, zachowaj pozostałe ustawienia i ustaw:

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

#### Poradnik w grze i rozwiązywanie problemów

Kliknij **Manhunt Administrator Guide** lub użyj `/mhhelp`, aby otrzymać przetłumaczony poradnik. Gracze mogą w 1.9.11 używać `/mhhelp` do poradnika dla swojej roli. Łowcy klikają kompas prawym przyciskiem, aby wybrać Uciekiniera; ten interfejs śledzenia jest osobny od administracyjnego wyboru Target Player.

Jeśli rola lub kompas wygląda na niezsynchronizowany, **Emergency Sync** odświeża powiązany stan wykonania. **Match Info** pomaga sprawdzić drużyny i stan. Jeśli start się nie udaje, sprawdź gotowość meczu, wyłączenie zamrożenia serwera i obecność drużyny Uciekinierów/Łowców. Po zmianie JAR-a wykonaj pełny restart zamiast `/reload`. `/mhdebug` jest administracyjną komendą diagnostyczną w 1.9.11; jej obecność nie oznacza, że te wydania przeszły testy na działającym serwerze.

#### Korzystanie ze starszego centrum sterowania 1.6.4

1.6.4 zachowuje **Player Roles**, **Friendly Fire**, **Start Match**, **Reset Match**, **Release Hunters Now**, **Server Lock**, **Teleport Everyone To Me**, **Heal & Feed Everyone**, **Match Status**, wybór języka, **Anti Cheat** i poradnik administratora. Role przechodzą przez **None → Runner → Hunter**, a zmiany są zablokowane, gdy mecz się rozpoczyna/trwa.

Menu anti-cheat zawiera starsze **Anti AutoClick** (reguła 30 CPS z ostrzeganiem/wyrzucaniem), **Anti Fly** i **Anti X-Ray** Paper. Okno powrotu Uciekinierów wynosi stale **60 minut**. Nowszy przełącznik Smart Hunter Kit V3, wybór Auto World Spawn, pauza/wznowienie, potwierdzenie Reset Settings i rozszerzone narzędzia celów/świata opisane powyżej należą do 1.9.11 i nie należy ich oczekiwać w starszym menu.

Ten poradnik opracowano z metadanych dostarczonych JAR-ów, dołączonych tekstów językowych/pomocy i statycznej deasemblacji. Podczas inspekcji interfejs nie był uruchamiany na działającym serwerze Minecraft.

### 3. Rozegraj pościg

Uciekinierzy uciekają w czasie losowej przewagi początkowej i dążą do pokonania Ender Dragona. Łowcy czekają na wypuszczenie, a potem klikają kompas prawym przyciskiem, aby wybrać Uciekiniera. Cele można zmieniać w trakcie gry, także gdy pościg przekracza wymiary. Użyj `/teammsg <message>`, aby rozmawiać tylko z drużyną, i `/mhhelp` dla przetłumaczonego poradnika roli w 1.9.11.

Jeśli Uciekinier zginie, pozostali grają dalej, a poległy gracz zostaje Łowcą. Łowca może się odrodzić i kontynuować śledzenie. Śmierć ostatniego Uciekiniera lub wygaśnięcie jego czasu powrotu może zakończyć mecz zwycięstwem Łowców; pokonanie Ender Dragona kończy go zwycięstwem Uciekinierów.

### 4. Wstrzymaj, zakończ i przygotuj kolejny mecz

W 1.9.11 wstrzymaj przez `/mhpause` i kontynuuj przez `/mhresume`. Użyj `/mhrelease`, jeśli Łowcy mają zostać wypuszczeni przed końcem odliczania przewagi. Do nowego meczu użyj pełnego resetu z centrum sterowania lub `/mhreset`; usuwa on tymczasowy stan i przedmioty oraz przenosi graczy do spawnu Overworldu. Zmiana ustawień Paper Anti-Xray wymaga restartu.

## Domyślne ustawienia w 1.9.11

Sprawdzone wartości awaryjne świeżej konfiguracji to:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` oznacza wyłączenie automatycznego przenoszenia spawnu. Potwierdzony reset ustawień w GUI ustawia zamiast tego odstęp 15 minut. Używaj GUI albo `/mhkit` i `/mhspawn` do odpowiednich ustawień.

## Publiczne komendy

Wymienione komendy administracyjne używają `vexland.admin`, domyślnie przypisanego OP. Czat drużynowy, kosz i widzenie w ciemności nie mają uprawnienia w deskryptorze; `/mhhelp` w 1.9.11 staje się poradnikiem gracza/administratora.

| Komenda | Cel | Dostępność |
| --- | --- | --- |
| `/mhgui` | Otwiera centrum sterowania | Obie kompilacje |
| `/mhstart` | Uruchamia pełną sekwencję startu | Obie kompilacje |
| `/mhreset` | Całkowicie resetuje bieżący mecz | Obie kompilacje |
| `/mhrelease` | Wcześniej wypuszcza Łowców | Obie kompilacje |
| `/mrunner <player>` | Przypisuje Uciekiniera | Obie kompilacje |
| `/mhunter <player>` | Przypisuje Łowcę | Obie kompilacje |
| `/mhnone <player>` | Usuwa rolę | Tylko 1.6.4 |
| `/teammsg <message>` | Wysyła prywatną wiadomość do drużyny | Obie kompilacje |
| `/trash` | Otwiera jednorazowy kosz z 54 miejscami | Obie; aliasy 1.9.11: `/mhtrash`, `/vextrash` |
| `/nv` | Przełącza osobiste widzenie w ciemności | Obie kompilacje |
| `/mhlang` | Otwiera globalny wybór języka | Obie kompilacje; administrator |
| `/mhhelp` | Daje przetłumaczoną książkę poradnika | 1.6.4 tylko administrator; 1.9.11 poradnik gracza/administratora |
| `/mhkit <on\|off\|toggle\|status>` | Konfiguruje inteligentne zestawy Łowców | 1.9.11 |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Konfiguruje automatyczne przenoszenie spawnu | 1.9.11 |
| `/mhpause` | Wstrzymuje trwający mecz | 1.9.11 |
| `/mhresume` | Wznawia wstrzymany mecz | 1.9.11 |
| `/mhdebug` | Uruchamia wewnętrzną diagnostykę | 1.9.11 |

## Języki w grze i języki dokumentacji

Obie dostarczone kompilacje mają **10 języków w grze**: angielski, perski, arabski, hiszpański, francuski, niemiecki, rosyjski, chiński uproszczony, hindi i portugalski. Administrator wybiera **globalny język serwera** przez `/mhlang`; komunikaty, menu, powiadomienia i poradniki używają tego wyboru, zapisanego w `language.txt`.

Dokumentacja GitHub jest publikowana w **18 językach, bez arabskiej edycji dokumentacji**. Japoński, turecki i inne dodatkowe tłumaczenia README pomagają czytelnikom zrozumieć projekt; nie dodają nowych języków do gry w tych oryginalnych JAR-ach.

## Historia wersji i kolejna kompilacja

[CHANGELOG.md](../../../CHANGELOG.md) opisuje różnice między przesłanymi wersjami. Dodatkowa kompilacja z dedykowaną funkcją obserwatora **oczekuje na dostarczenie do przyszłego wydania**. Istniejące odniesienia do standardowego Spectator nie potwierdzają tej nowej funkcji w dwóch dostarczonych plikach. Każda kolejna dostarczona kompilacja otrzyma osobne pobieranie, sumę kontrolną i opis zmian po porównaniu z poprzednią wersją.

## Żartobliwe wyzwanie dla Dreama

Trochę minecraftowego przekomarzania od Bardiyi 😄

> "Ech... Ali i ja zrobiliśmy wtyczkę Manhunt sto razy lepszą od tej Dreama, ale Dream się boi i nie chce zagrać na naszej!"

## Twórcy i zakres projektu

**Współtworzony przez [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) i [Ali · Alivexor](https://github.com/Alivexor).** Oba konta są również zapisane jako autorzy w oryginalnych deskryptorach wtyczki.

To repozytorium prezentuje oryginalne skompilowane wydania, dokumentację i informacje o wersjach jako wspólny projekt portfolio. Opisy funkcji opierają się na statycznej inspekcji dostarczonych JAR-ów. Zgodność na działającym serwerze, wydajność odzyskiwania, balans i dokładność anti-cheatu nie były testowane w tym procesie publikacji.

[Portfolio Bardiyi na GitHubie](https://github.com/FarlandGame) · [GitHub Alego](https://github.com/Alivexor) · [Wszystkie wydania](https://github.com/FarlandGame/Vexland_Manhunt/releases)
