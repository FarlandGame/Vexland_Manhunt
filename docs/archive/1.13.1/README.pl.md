# Vexland_Manhunt — 1.13.1

> Archiwalny przewodnik wersji · [2.0.0 →](../../README.pl.md)

[English](README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**Kompletna rozgrywka Minecraft: Uciekinierzy kontra Łowcy, współtworzona przez [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) i [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt łączy konfigurację meczu, role drużyn, początek pościgu, śledzenie, postęp, nagrody, wyniki i administrację w jednej wtyczce dla serwera Paper. Uciekinierzy próbują pokonać Ender Dragona, a Łowcy próbują wyeliminować ostatniego Uciekiniera. Wtyczka obsługuje wielu Uciekinierów i utrzymuje pościg mimo śmierci, odrodzeń, zmian wymiaru i ponownych połączeń. Centrum sterowania `/mhgui` pozwala administratorom zarządzać meczem przez menu, z przetłumaczonymi komunikatami i poradnikami dla graczy.

## Pobieranie i zgodność

| Plik / wersja | Pobierz | Przeznaczenie |
|---|---|---|
| **1.13.1 — aktualna** | [VexLandManhunt-1.13.1.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/VexLandManhunt-1.13.1.jar) | Plugin Manhunt autorstwa Bardiyi i Alego |
| **GrimAC 2.3.73 — wymagany** | [grimac-bukkit-2.3.73.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/grimac-bukkit-2.3.73.jar) | Osobna zależność antycheatowa innego projektu |
| 1.9.11 — archiwalna | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Poprzednia kompilacja Manhunt |
| 1.6.4 — archiwalna | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Wcześniejsza kompilacja Manhunt |

**Platforma docelowa: Paper 1.21.11, Java 21.** Liczby 1.6.4, 1.9.11 i 1.13.1 oznaczają wydania pluginu, a nie obsługiwane wersje Minecrafta. W 1.13.1 GrimAC jest obowiązkową zależnością, a integracja wymaga API 2.3.73. Pobierz **oba aktualne pliki JAR**. Są to pluginy serwerowe; gracze nie instalują ich w folderze modów klienta.

Są to oryginalne kompilacje z prywatnego serwera, z podwyższonym dostępem administracyjnym dla konkretnych twórców, zachowane dokładnie w dostarczonej postaci. Ten podręcznik opisuje publiczne funkcje sterowania Manhunt.

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

## Co nowego w 1.13.1?

W porównaniu z dostarczoną kompilacją 1.9.11:

- **Niewidoczni obserwatorzy:** osobna rola nadawana przez administratora, chroniony lot, ukrywanie graczy, zapisywanie i przywracanie stanu oraz stronicowane menu teleportacji do uczestników.
- **Przeprojektowane centrum sterowania:** menu podzielone na kategorie, jawny wybór jednej z czterech ról, wybór celu według nazwy, wybór czasu na ponowne połączenie, ustawienia Classic/Fast/Hardcore/Custom oraz osobne ekrany potwierdzenia z limitem 30 sekund.
- **Integracja GrimAC:** wymagany GrimAC 2.3.73 zastępuje aktywną ścieżkę uruchamiania VexAC. Interfejs udostępnia przełącznik główny, pięć grup kontroli, alerty oraz sterowanie monitorowaniem i egzekwowaniem. Paper Anti-Xray pozostaje niezależny.
- **Nowy planista Smart Hunter Kit:** dostosowuje wyposażenie i zapasy do ekwipunku oraz zaklęć Runnerów, najbliższego Runnera, liczebności drużyn, odległości, wymiaru i terenu. Zachowuje lepszy posiadany sprzęt, unika powielania narzędzi i ogranicza uzupełnianie przedmiotów zużywalnych, korzystając z historii ostatnich 30 sekund. Nie gwarantuje to stałej różnicy wyposażenia ani zmierzonego balansu.
- **Weryfikowane odzyskiwanie:** migawki zabezpieczone SHA-256, kontrola schematu i stanu oraz przejście na poprawną kopię zapasową; migawki nieprawidłowe lub zapisane w nowszym formacie są zachowywane bez nadpisywania. Stan obserwatora jest zapisywany osobno.
- **Rozszerzone komunikaty:** liczba przetłumaczonych kluczy rośnie z 683 do 762 w każdym dołączonym tłumaczeniu, nadal w tych samych dziesięciu językach gry. Zarejestrowano dwie nowe publiczne komendy: `/mspectator <player>` i `/mhspectate`.
- **Awaryjne zachowanie resetu:** jeśli nie uda się znaleźć bezpiecznej powierzchni w pobliżu punktu odrodzenia Overworld, reset może pominąć tę teleportację zamiast ją wymuszać.

## Pełna konfiguracja i obsługa przez `/mhgui`

Zatrzymaj serwer i wykonaj kopię zapasową światów oraz danych pluginów. Umieść oba aktualne pliki JAR w `plugins/`, pozostawiając tam tylko jeden JAR Manhunt i jeden JAR GrimAC. Przy aktualizacji zachowaj dotychczasowe ustawienia i dane `plugins/VexLandManhunt/`. Uruchom w pełni serwer Paper 1.21.11 / Java 21; przy wymianie kompilacji wykonuj pełny restart. GrimAC musi załadować się poprawnie. Wewnętrzna nazwa pluginu pozostaje `VexLandManhunt`.

Przewodnik opisuje wydanie pluginu **1.13.1** z angielskimi etykietami. Etykiety odpowiadają językowi ustawionemu dla całego serwera. W pozycjach wiersze liczy się od góry, a kolumny od lewej. Używaj zwykłego kliknięcia lewym przyciskiem, chyba że wskazano inną czynność. Przewodnik powstał na podstawie analizy statycznej; nie uruchamiano serwera Minecraft.

### Konfiguracja meczu

1. Użyj `/mhgui` z uprawnieniem `vexland.admin` (domyślnie: OP).
2. Otwórz **Player Roles**, kliknij kafelek z nazwą gracza, a następnie wybierz **Runner**, **Hunter**, **Spectator** lub **No Team**. Otwiera to wybór konkretnej roli; kliknięcie gracza nie przełącza kolejno jego ról.
3. Przydziel co najmniej jednego Runnera i jednego Huntera. Nieprzypisani gracze online mogą zostać Hunterami przy rozpoczęciu meczu; obserwatorzy nie zajmują wymaganego miejsca w żadnej drużynie.
4. Sprawdź **Match Settings**, **GrimAC Security** i **Global Language**. Przed rozpoczęciem wyłącz Server Freeze.
5. Otwórz **Match Controls → Start Match**. Ekwipunki uczestników zostaną przygotowane/wyczyszczone, zostanie odtworzone wprowadzenie, a ruletka wybierze czas oczekiwania Hunterów.

### Ekran główny: `/mhgui` (pięć wierszy)

| Pozycja | Przycisk | Działanie |
|---|---|---|
| R2 C2 | Match Controls | Rozpoczęcie, wstrzymanie/wznowienie, wypuszczenie i reset. |
| R2 C4 | Player Roles | Otwiera listę ról graczy online. |
| R2 C6 | Match Settings | Ogień bratobójczy, zestawy, punkt odrodzenia, ponowne łączenie i ustawienia wstępne. |
| R2 C8 | Player Management | Wybór celu oraz narzędzia dla graczy i świata. |
| R4 C2 | GrimAC Security | Otwiera ustawienia ochrony. |
| R4 C4 | Global Language | Wybór języka używanego przez wszystkich. |
| R4 C6 | Administrator Guide | Dodaje do ekwipunku przetłumaczony podręcznik administratora. |
| R5 C5 | Close | Zamyka menu. |

Latarnia w R1 C5 pokazuje stan meczu oraz liczbę Runnerów/Hunterów.

### Match Controls (pięć wierszy)

| Pozycja | Przycisk | Działanie |
|---|---|---|
| R2 C2 | Start Match | Rozpoczyna pełną sekwencję. |
| R2 C4 | Pause Match / Resume Match | Wstrzymuje lub wznawia rozgrywkę i zegary meczu; dostępne dla meczu RUNNING. |
| R2 C6 | Release Hunters | Kończy wcześniej bieżący okres oczekiwania Hunterów. |
| R2 C8 | Reset Match | Otwiera potwierdzenie, po czym całkowicie resetuje mecz. |
| R4 C2 | Server Freeze | Przełącza globalne zamrożenie graczy bez OP. |
| R4 C4 | Teleport Everyone | Otwiera potwierdzenie, po czym przenosi do ciebie wszystkich graczy online. |
| R4 C6 | Match Info | Wysyła raport meczu i drużyn. |

**Back** znajduje się w R5 C1, a **Close** w R5 C9. Server Freeze jest niezależne od Pause Match: używaj Pause, gdy zegar i systemy rozgrywki mają zatrzymać się razem.

### Player Roles

Sześciowierszowa lista pokazuje do 45 kafelków ról z nazwami graczy, uporządkowanych według nazw, w pierwszych pięciu wierszach. Runner używa jasnozielonego betonu, Hunter czerwonego betonu, Spectator Oka Endera, a No Team szarego betonu. Dolny wiersz zawiera **Previous Page** w C1, informacje o stronie/graczach online w C3, **Back to Control Center** w C5 i **Next Page** w C9.

Kliknij gracza, aby otworzyć **Choose Player Role** (trzy wiersze):

| Pozycja | Konkretna rola |
|---|---|
| R2 C2 | Runner |
| R2 C4 | Hunter |
| R2 C6 | Spectator |
| R2 C8 | No Team |

Nazwa gracza i bieżąca rola są widoczne w R1 C5; **Back** znajduje się w R3 C1, a **Close** w R3 C9. Role można zmieniać podczas meczu. Zmiana roli ostatniego przypisanego Runnera na inną podczas RUNNING otwiera potwierdzenie **Last Runner: the match will end**. Zatwierdzenie może dać zwycięstwo Hunterom. Bezpośrednie komendy ról działają natychmiast, więc używaj ich świadomie. Tutaj można nadać No Team; zwykła synchronizacja przy starcie/dołączeniu może podczas aktywnego meczu zmienić nieprzypisanego gracza w Huntera.

### Obserwatorzy

Administrator nadaje rolę przez `/mspectator <player>` lub wybiera **Spectator** w Player Roles. Komenda sprawdza dostęp administratora, mimo że jej deskryptor nie zawiera wiersza uprawnienia. Gracze nie zapisują się sami przez uruchomienie `/mhspectate`.

Obserwator otrzymuje kompas **Spectator teleport** w pierwszym slocie paska szybkiego dostępu. Trzymaj go w głównej ręce i kliknij prawym przyciskiem albo użyj `/mhspectate`, aby otworzyć sześciowierszowe menu teleportacji. Menu działa tylko dla gracza z rolą Spectator. Pierwsze pięć wierszy zawiera do 45 żyjących Runnerów/Hunterów online, posortowanych według nazw; kliknij kafelek z nazwą i rolą, aby teleportować się do aktualnej lokalizacji gracza, również w innym świecie. Dolny wiersz zawiera **Previous Page** w C1, **Close** w C5 i **Next Page** w C9. Gdy nie ma odpowiedniego uczestnika, R3 C5 pokazuje **No players available**. Zamknięcie menu nie odbiera roli obserwatora.

Obserwatorzy latają, są ukryci przed innymi graczami, nie powodują kolizji i są chronieni przed obrażeniami. Implementacja używa trybu Adventure z lotem; nie daje standardowej kamery Spectator ani przenikania przez bloki. Blokuje ataki, niszczenie/stawianie bloków, zwykłe interakcje z blokami i bytami, podnoszenie/wyrzucanie przedmiotów, zamianę drugiej ręki, kliknięcia/przeciąganie w ekwipunku, manipulowanie stojakami na zbroję oraz podnoszenie/zdobywanie doświadczenia. Moby nie mogą ich namierzać, a zmiany głodu są anulowane. `/teammsg <message>` dociera do pozostałych graczy z rolą Spectator. Nie przekazuj uczestnikom lokalizacji innych graczy ani innej pomocy z zewnątrz.

Aby zakończyć obserwowanie, administrator nadaje **Runner**, **Hunter** lub **No Team**, albo używa `/mrunner <player>` lub `/mhunter <player>`. Nie ma osobnej komendy/przycisku samodzielnego wyjścia. Wyjście przywraca zapisany ekwipunek i przedmiot kursora, lokalizację, tryb gry, lot, kolizje i odporność, po czym stosuje zachowanie meczowe nowej roli. Stan obserwatora jest zapisywany na potrzeby ponownego dołączenia. Pełny Match Reset przywraca stan obserwatorów, usuwa role i przenosi graczy online do bezpiecznego punktu odrodzenia Overworld, jeśli taki jest dostępny. Zwykłe porządkowanie po końcu meczu pomija obserwatorów przy obsłudze przedmiotów i lotu uczestników.

### Match Settings (pięć wierszy)

| Pozycja | Przycisk | Działanie |
|---|---|---|
| R2 C2 | Friendly Fire | Przełącza zadawanie obrażeń członkom drużyny. |
| R2 C4 | Smart Hunter Kit | Przełącza adaptacyjne zestawy odrodzenia Hunterów. |
| R2 C6 | Auto World Spawn | Otwiera wybór interwału. |
| R2 C8 | Reconnect Grace | Otwiera wybór czasu na ponowne połączenie Runnera. |
| R4 C2 | Match Preset | Wybór Classic, Fast, Hardcore lub Custom. |
| R4 C4 | Reset Settings | Potwierdza zrównoważone ustawienia: Kit ON, Spawn 15m, Reconnect 15m. |
| R4 C6 | Random Head Start | Kafelek informacyjny; ruletka nadal wybiera opóźnienie. |

**Back** znajduje się w R5 C1, a **Close** w R5 C9.

Trzywierszowy wybór **Reconnect Grace** oferuje **1, 5, 10, 15, 20, 30 minut** w R2 C2–C7, w tej kolejności. Kliknięcie zapisuje wartość i pozostawia wybór otwarty. Back znajduje się w R3 C1, a Close w R3 C9.

Trzywierszowy wybór **Match Preset** umieszcza **Classic**, **Fast**, **Hardcore**, **Custom** w R2 C2, C4, C6, C8. Classic: Kit ON, Spawn 15m, Reconnect 15m. Fast: ON, 5m, 10m. Hardcore: OFF, OFF, 5m. Custom zachowuje bieżące ustawienia ręczne. Presety zachowują losowy czas przewagi. Wybór pozostawia menu otwarte; Back znajduje się w R3 C1, a Close w R3 C9.

**Auto World Spawn** oferuje OFF, 5m, 10m w R2 C2, C3, C4 oraz 15m, 20m, 30m w R2 C6, C7, C8. Back znajduje się w R3 C5. Wybierz interwał lub użyj `/mhspawn <off|5|10|15|20|30|status>`. Funkcja przesuwa punkt odrodzenia Overworld w pobliże odpowiedniego Runnera w Overworld; może pominąć czynność, jeśli takiego nie ma. `/mhkit <on|off|toggle|status>` bezpośrednio steruje zestawami.

### Player Management (sześć wierszy)

| Pozycja | Przycisk | Zakres |
|---|---|---|
| R1 C5 | Target Player | Otwiera wybór gracza według nazwy. |
| R2 C2 | Full Heal | Wszyscy gracze online. |
| R2 C4 | Full Hunger | Wszyscy gracze online. |
| R2 C6 | Clear Effects | Wszyscy gracze online. |
| R2 C8 | Freeze Target | Wybrany gracz. |
| R4 C2 | Clear Target Inventory | Wybrany gracz; wymaga potwierdzenia. |
| R4 C4 | Kill Target | Wybrany gracz; wymaga potwierdzenia i podlega normalnym rozstrzygnięciom meczu. |
| R4 C6 | Set Day | Twój bieżący świat. |
| R4 C8 | Clear Weather | Twój bieżący świat. |
| R5 C2 | Clear Dropped Items | Twój bieżący świat; wymaga potwierdzenia. |
| R5 C4 | Emergency Sync | Odświeża systemy ról i działania dla graczy online. |
| R5 C6 | Freeze Team | Lewy przycisk: Runnerzy; prawy: Hunterzy; Shift+kliknięcie: usuwa te zamrożenia drużynowe/indywidualne. |

Back znajduje się w R6 C1, a Close w R6 C9. Wybór celu nie zmienia ról. Lista wyboru pokazuje 28 innych graczy online na stronę, w wierszach 2–5 i kolumnach 2–8; kliknij nazwę, aby wybrać i wrócić. Previous/Back/Next znajdują się w R6 C1/C5/C9. Przed działaniem ponownie sprawdź wyświetlany cel.

### Ekrany potwierdzenia

Reset Match, Teleport Everyone, Reset Settings, Clear Target Inventory, Kill Target, Clear Dropped Items oraz zmiana ostatniego Runnera przez GUI używają osobnego trzywierszowego ekranu **Confirm Action**. Przeczytaj działanie/cel w R1 C5, a następnie kliknij zielone **Confirm** w R2 C3 albo czerwone **Cancel** w R2 C7. Potwierdzenie wygasa po **30 sekundach**. Zmieniony/nieobecny cel lub zmienione role wymagają nowego wyboru. Dla tych nowych ścieżek menu zastępuje to opisane w starym przewodniku powtarzanie kliknięć w odstępach pięciu/ośmiu sekund.

### GrimAC Security i język

Sześciowierszowe menu Grim pokazuje stan w R1 C5; przełączniki to R2 C2 **GrimAC Master**, C4 **Movement**, C6 **Combat**, C8 **Packets**; R4 C2 **Velocity / AntiKB**, C4 **World / Scaffold**, C6 **Anti X-Ray**, C8 **Admin Alerts**; oraz R5 C5 **Monitor mode**. Back znajduje się w R6 C1, a Close w R6 C9. Monitor mode wybiera między alertami/dowodami a egzekwowaniem. Paper Anti-Xray jest niezależny i wymaga restartu po zmianach. Są to funkcje GrimAC; starszy opis menu VexAC/AutoClick nie opisuje tego wydania.

Global Language obowiązuje wszystkich i odświeża menu/przedmioty. Kliknij nazwę języka; Back znajduje się w R3 C5. `/mhlang` otwiera ten sam wybór, a `/mhhelp` dostarcza przetłumaczony przewodnik gracza/administratora.

### Aktualne ustawienia domyślne, ponowne łączenie i moderacja

Wartości zapasowe świeżej konfiguracji w `plugins/VexLandManhunt/config.yml` to:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` oznacza wyłączenie automatycznego przesuwania punktu odrodzenia. Reset Settings i Classic wybierają zamiast tego 15 minut. W czasie okna ponownego połączenia Runnera jego miejsce pozostaje zarezerwowane; powrót na czas zapewnia dziesięć sekund ochrony. Zapisany czas wyłączenia serwera nie jest wliczany. Upływ terminu może zmienić Runnera w Huntera lub zakończyć mecz zwycięstwem Hunterów. Pause/Resume zamraża systemy rozgrywki i koryguje czas aktywnego meczu. Plikami odzyskiwania zarządza plugin.

Ustawienia integracji Grim są zapisywane w `plugins/VexLandManhunt/grim-settings.yml`. Nowa konfiguracja ma Master ON, wszystkie pięć grup ON, Admin Alerts ON i **Monitor mode OFF: egzekwowanie jest włączone**. Monitor mode kolejkuje dowody/alerty i anuluje kwalifikujące się zgłoszenia. W trybie egzekwowania integracja może zamienić komendę wyrzucenia Grim na przetłumaczone rozłączenie umożliwiające ponowne połączenie; nie ustanawia to zasad permanentnych banów. Rzeczywiste progi zależą również od konfiguracji Grim. Dowody są kolejkowane do `plugins/VexLandManhunt/anticheat/grim-evidence.log`; kolejki o ograniczonej pojemności mogą odrzucać wpisy pod obciążeniem. Integracja wyłącza z kontroli obserwatorów, grę wstrzymaną/zamrożoną i niektóre sytuacje w pojazdach, zapewniając trzy sekundy ochrony po dołączeniu, teleportacji i odrodzeniu. Nie deklaruje się wyników pomiarów dokładności ani wydajności antycheata.

## Publiczne komendy — 1.13.1

Dostęp administratora oznacza OP lub `vexland.admin` (domyślnie OP). Obsługa `/mspectator <player>` sprawdza to mimo braku wiersza uprawnienia w deskryptorze. Bezpośrednie komendy ról działają natychmiast; zmiana ostatniego Runnera podczas RUNNING może zakończyć mecz. GUI zapewnia potwierdzenie w tej sytuacji.

| Komenda | Przeznaczenie | Dostęp |
|---|---|---|
| `/mhgui` | Otwiera centrum sterowania z kategoriami | Administrator |
| `/mhstart` | Rozpoczyna pełną sekwencję meczu | Administrator |
| `/mhreset` | Całkowicie resetuje mecz | Administrator |
| `/mhrelease` | Wypuszcza oczekujących Hunterów | Administrator |
| `/mrunner <player>` | Nadaje Runner | Administrator |
| `/mhunter <player>` | Nadaje Hunter | Administrator |
| `/mspectator <player>` | Nadaje Spectator | Administrator; nowa |
| `/mhspectate` | Otwiera menu teleportacji do uczestników | Obecny Spectator; nowa |
| `/teammsg <message>` | Wysyła do własnej roli/drużyny | Gracz |
| `/trash` | Jednorazowy ekwipunek o 54 slotach; aliasy `/mhtrash`, `/vextrash` | Gracz |
| `/nv` | Przełącza osobiste widzenie w ciemności | Gracz |
| `/mhlang` | Otwiera wybór globalnego języka | Administrator |
| `/mhkit <on\|off\|toggle\|status>` | Konfiguruje adaptacyjne zestawy Hunterów | Administrator |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Konfiguruje przesuwanie punktu odrodzenia | Administrator |
| `/mhhelp` | Daje przetłumaczony przewodnik roli/administratora | Gracz / administrator |
| `/mhpause` | Wstrzymuje trwający mecz | Administrator |
| `/mhresume` | Wznawia wstrzymany mecz | Administrator |
| `/mhdebug` | Diagnostyka wewnętrzna | Administrator |

`/mhnone` nie jest zarejestrowane w tym wydaniu; użyj roli No Team w GUI. Hunterzy klikają prawym przyciskiem swój kompas śledzący, aby wybrać Runnera; jest to funkcja odrębna od teleportacji obserwatorów i wyboru celu administratora. Runnerzy wygrywają po pokonaniu Smoka Endu; Hunterzy wygrywają, gdy nie pozostanie żaden Runner. Poległy Runner staje się Hunterem, jeśli pozostają inni Runnerzy.

## Języki, historia i autorzy komponentów zewnętrznych

Oryginalny plugin oferuje **10 języków gry**: angielski, perski, arabski, hiszpański, francuski, niemiecki, rosyjski, chiński uproszczony, hindi i portugalski. `/mhlang` wybiera jeden język dla całego serwera, zapisywany w `language.txt`. Podręcznik GitHub ma **18 języków**, bez arabskiego wydania dokumentacji. Japoński i inne dodatkowe języki README nie dodają tłumaczeń w grze do niezmienionych JAR-ów.

[Historia wersji](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/CHANGELOG.md) opisuje każdą dostarczoną kompilację. Pełny starszy podręcznik 1.9.11 / 1.6.4 zachowano w [archiwum wersji](../1.9.11/README.pl.md). Osobna kompilacja z obserwatorami została dostarczona i opublikowana jako 1.13.1; jej funkcji nie należy przypisywać starszym plikom.

**GrimAC jest niezależnym projektem twórców GrimAC, rozpowszechnianym na licencji GPL-3.0.** Bardiya i Ali stworzyli Vexland_Manhunt oraz jego integrację; nie przypisuje się im autorstwa GrimAC. Dostarczony JAR Grim ma takie same SHA-512 i SHA-1 jak oficjalny artefakt Bukkit 2.3.73 w Modrinth. Zapisany w nim commit źródłowy odpowiada [upstream v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73). Wydanie zawiera niezmienione pliki binarne, sumy kontrolne, migawkę źródeł upstream, licencję i [informacje o komponentach zewnętrznych](../../../THIRD_PARTY_NOTICES.md). Te informacje nie nadają licencji osobnemu projektowi Manhunt.

## Żartobliwe wyzwanie dla Dreama

Trochę minecraftowego przekomarzania od Bardiyi 😄

> "Ech... Ali i ja zrobiliśmy wtyczkę Manhunt sto razy lepszą od tej Dreama, ale Dream się boi i nie chce zagrać na naszej!"

## Twórcy i zakres projektu

**Współtworzony przez [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) i [Ali · Alivexor](https://github.com/Alivexor).** Oba konta są również zapisane jako autorzy w oryginalnych deskryptorach wtyczki.

To repozytorium prezentuje oryginalne skompilowane wydania, dokumentację i informacje o wersjach jako wspólny projekt portfolio. Opisy funkcji opierają się na statycznej inspekcji dostarczonych JAR-ów. Zgodność na działającym serwerze, wydajność odzyskiwania, balans i dokładność anti-cheatu nie były testowane w tym procesie publikacji.

[Portfolio Bardiyi na GitHubie](https://github.com/FarlandGame) · [GitHub Alego](https://github.com/Alivexor) · [Wszystkie wydania](https://github.com/FarlandGame/Vexland_Manhunt/releases)
