# Vexland_Manhunt — 1.13.1

> Guide de la version archivée · [2.0.0 →](../../README.fr.md)

[English](README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**Une expérience Minecraft complète opposant les Runner aux Hunter, créée conjointement par [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) et [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt réunit la préparation des parties, les rôles des équipes, le début de la poursuite, le suivi, la progression, les récompenses, les résultats et l'administration dans un seul plugin pour serveur Paper. Les Runner tentent de vaincre l'Ender Dragon, tandis que les Hunter cherchent à éliminer le dernier Runner. Le plugin prend en charge plusieurs Runner et maintient la poursuite malgré les morts, réapparitions, changements de dimension et reconnexions. Son centre de contrôle `/mhgui` permet aux administrateurs de gérer une partie par des menus, avec des messages et des guides traduits pour les joueurs.

## Téléchargements et compatibilité

| Fichier / version | Téléchargement | Utilité |
|---|---|---|
| **1.13.1 — actuelle** | [VexLandManhunt-1.13.1.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/VexLandManhunt-1.13.1.jar) | Plugin Manhunt de Bardiya et Ali |
| **GrimAC 2.3.73 — obligatoire** | [grimac-bukkit-2.3.73.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/grimac-bukkit-2.3.73.jar) | Dépendance anti-triche tierce et distincte |
| 1.9.11 — archivée | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Version précédente de Manhunt |
| 1.6.4 — archivée | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Ancienne version de Manhunt |

**Cible : Paper 1.21.11, Java 21.** Les numéros 1.6.4, 1.9.11 et 1.13.1 désignent des versions du plugin, pas des versions de Minecraft compatibles. Dans 1.13.1, GrimAC est une dépendance obligatoire et la passerelle nécessite l’API 2.3.73. Téléchargez **les deux JAR actuels**. Ce sont des plugins serveur ; les joueurs ne les installent pas dans le dossier de mods de leur client.

Ces versions originales destinées à un serveur personnel comportent des accès administratifs élevés propres aux créateurs et sont conservées exactement telles qu’elles ont été fournies. Ce manuel couvre les commandes publiques de Manhunt.

## L'expérience Manhunt

- **Équipes Runner et Hunter :** affectez les joueurs connectés à l'un des camps. Une partie nécessite au moins un Runner et un Hunter ou un joueur connecté sans rôle. Les Runner survivants continuent si un coéquipier meurt ; un Runner mort devient Hunter, sauf si cette mort termine la partie.
- **Début de partie cinématique :** les inventaires et modes de jeu sont préparés, les équipes présentées, puis une roulette détermine l'avance des Runner. Les Hunter sont immobilisés pendant ce compte à rebours, avec des titres et des sons. L'avance est aléatoire ; les administrateurs peuvent libérer les Hunter avant la fin.
- **Boussole de suivi avec choix de cible :** les Hunter reçoivent une boussole spéciale. Faites un clic droit pour choisir un Runner dans le menu des cibles et changez de cible pendant la poursuite. Entre dimensions, le suivi emprunte l'itinéraire du portail pertinent jusqu'à ce qu'un suivi direct soit possible. Les Hunter récupèrent leur boussole après réapparition.
- **Affichage de progression :** les barres de boss et informations de partie suivent l'équipement des Runner et leur progression à travers les ressources du Nether, les bâtons de Blaze, les perles, les yeux de l'Ender, le fort et l'End. La version plus récente ajoute des étapes plus détaillées et des visuels tenant compte de la santé du dragon.
- **Récompenses pour les éliminations des Runner :** lorsqu'un Runner tue un Hunter pendant une partie active, un ensemble pondéré de 50 récompenses tenant compte de la progression est utilisé. Il comprend des tirages animés, des récompenses doubles ou triples, des annonces de séries et des célébrations d'objets rares.
- **Victoire et résultats :** la mort du dernier Runner donne la victoire aux Hunter ; vaincre l'Ender Dragon donne la victoire aux Runner. Des titres de fin, des célébrations, les informations d'éliminations et de morts et le nettoyage des objets temporaires sont inclus. La version récente affiche aussi le MVP, les dégâts et les distances.
- **Communication d'équipe et utilitaires :** messages privés aux coéquipiers avec `/teammsg`, inventaire jetable de 54 emplacements avec `/trash` et vision nocturne personnelle avec `/nv`.
- **Administration par menus :** rôles, démarrage/réinitialisation, libération anticipée des Hunter, tirs alliés, verrouillage du serveur, téléportation générale, soins/nourriture, langue, protections, état et guides sont accessibles dans le centre de contrôle. L'immobilisation et la réinitialisation complète aident à préparer la partie suivante.
- **Guides traduits :** des livres pour Runner, Hunter et administrateurs expliquent les objectifs, la boussole, les morts, la préparation et les commandes. La version 1.9.11 donne aux joueurs un guide adapté à leur rôle avec `/mhhelp`.
- **Intégration Anti-Xray de Paper :** les menus configurent la protection de Paper au niveau du monde ; un redémarrage est nécessaire pour appliquer les changements.

## Quoi de neuf dans 1.13.1 ?

Par rapport à la version 1.9.11 fournie :

- **Spectateurs fantômes :** rôle distinct, attribution par l’administrateur, vol protégé, joueurs masqués, état sauvegardé/restauré et menu paginé de téléportation vers les participants.
- **Centre de contrôle repensé :** menus par catégories, choix explicite entre quatre rôles, sélection d’une cible nommée, durée de reconnexion, préréglages Classic/Fast/Hardcore/Custom et écrans de confirmation dédiés valables 30 secondes.
- **Intégration de GrimAC :** GrimAC 2.3.73, désormais obligatoire, remplace le chemin de démarrage actif de VexAC. L’interface expose le commutateur général, cinq groupes de vérifications, les alertes et les modes surveillance/application. Paper Anti-Xray reste indépendant.
- **Nouveau planificateur Smart Hunter Kit :** adapte équipement et ressources à l’équipement/enchantements des Runner, au Runner le plus proche, aux effectifs, à la distance, à la dimension et au terrain. Il préserve le meilleur équipement existant, évite les outils en double et limite le réapprovisionnement avec un historique de 30 secondes. Cela ne garantit ni un écart d’équipement fixe ni un équilibrage mesuré.
- **Restauration validée :** instantanés scellés par SHA-256, vérifications du schéma/de l’état et recours à une sauvegarde valide ; les instantanés invalides ou de format plus récent sont conservés sans écrasement. L’état des spectateurs est enregistré séparément.
- **Messages enrichis :** les clés traduites passent de 683 à 762 par traduction incluse, toujours dans les mêmes dix langues de jeu. Deux nouvelles commandes publiques sont enregistrées : `/mspectator <player>` et `/mhspectate`.
- **Solution de repli lors de la réinitialisation :** en l’absence de surface sûre près du point d’apparition de l’Overworld, la réinitialisation peut ignorer cette téléportation au lieu de la forcer.

## Configuration et utilisation complètes avec `/mhgui`

Arrêtez le serveur et sauvegardez les mondes et les données des plugins. Placez les deux JAR actuels dans `plugins/`, en n’y gardant qu’un JAR Manhunt et un JAR GrimAC. Conservez les réglages/données existants de `plugins/VexLandManhunt/` lors d’une mise à niveau. Démarrez complètement le serveur Paper 1.21.11 / Java 21 ; effectuez un redémarrage complet après remplacement des versions. GrimAC doit se charger correctement. Le nom interne du plugin reste `VexLandManhunt`.

Ce guide décrit la version **1.13.1** du plugin avec ses libellés anglais. Les libellés suivent la langue commune du serveur. Les lignes se comptent de haut en bas et les colonnes de gauche à droite. Utilisez un clic gauche ordinaire, sauf indication contraire. Ce guide provient d’une inspection statique ; aucun serveur Minecraft n’a été exécuté.

### Préparer une partie

1. Utilisez `/mhgui` avec `vexland.admin` (par défaut : OP).
2. Ouvrez **Player Roles**, cliquez sur la case portant le nom d’un joueur, puis choisissez **Runner**, **Hunter**, **Spectator** ou **No Team**. Un sélecteur de rôle précis s’ouvre ; cliquer sur le joueur ne fait pas défiler son rôle.
3. Attribuez au moins un Runner et un Hunter. Les joueurs connectés sans attribution peuvent devenir Hunter au démarrage ; les spectateurs ne remplissent la place requise d’aucune équipe.
4. Vérifiez **Match Settings**, **GrimAC Security** et **Global Language**. Désactivez Server Freeze avant de commencer.
5. Ouvrez **Match Controls → Start Match**. Les inventaires des participants sont préparés/vidés, l’introduction se joue et la roulette choisit le délai avant la libération des Hunter.

### Accueil : `/mhgui` (cinq lignes)

| Position | Bouton | Action |
|---|---|---|
| R2 C2 | Match Controls | Démarrer, suspendre/reprendre, libérer et réinitialiser. |
| R2 C4 | Player Roles | Ouvrir la liste des rôles des joueurs connectés. |
| R2 C6 | Match Settings | Dégâts alliés, kits, apparition, reconnexion et préréglages. |
| R2 C8 | Player Management | Choisir une cible et utiliser les outils joueurs/monde. |
| R4 C2 | GrimAC Security | Ouvrir les réglages de protection. |
| R4 C4 | Global Language | Choisir la langue utilisée pour tout le monde. |
| R4 C6 | Administrator Guide | Ajouter le livre d’administration traduit à votre inventaire. |
| R5 C5 | Close | Fermer le menu. |

La balise en R1 C5 affiche l’état de la partie et les effectifs Runner/Hunter.

### Match Controls (cinq lignes)

| Position | Bouton | Action |
|---|---|---|
| R2 C2 | Start Match | Lancer toute la séquence. |
| R2 C4 | Pause Match / Resume Match | Suspendre ou reprendre le jeu et les chronomètres ; disponible pour une partie RUNNING. |
| R2 C6 | Release Hunters | Terminer plus tôt l’attente actuelle des Hunter. |
| R2 C8 | Reset Match | Ouvrir la confirmation, puis réinitialiser complètement la partie. |
| R4 C2 | Server Freeze | Activer/désactiver le gel global des joueurs non OP. |
| R4 C4 | Teleport Everyone | Ouvrir la confirmation, puis amener tous les joueurs connectés à vous. |
| R4 C6 | Match Info | Envoyer le rapport de partie et d’équipes. |

**Back** est en R5 C1 ; **Close**, en R5 C9. Server Freeze est distinct de Pause Match : utilisez Pause pour arrêter ensemble le chronomètre et les systèmes de jeu.

### Player Roles

La liste de joueurs à six lignes affiche jusqu’à 45 cases de rôle nommées, triées par nom, dans ses cinq premières lignes. Runner utilise du béton vert clair, Hunter du béton rouge, Spectator un œil de l’Ender et No Team du béton gris. La ligne du bas contient **Previous Page** en C1, les informations de page/connexion en C3, **Back to Control Center** en C5 et **Next Page** en C9.

Cliquez sur un joueur pour ouvrir **Choose Player Role** (trois lignes) :

| Position | Rôle précis |
|---|---|
| R2 C2 | Runner |
| R2 C4 | Hunter |
| R2 C6 | Spectator |
| R2 C8 | No Team |

Le nom/rôle actuel du joueur apparaît en R1 C5 ; **Back** est en R3 C1 et **Close**, en R3 C9. Les rôles peuvent changer pendant une partie. Retirer le rôle Runner au dernier Runner attribué pendant RUNNING ouvre la confirmation **Last Runner: the match will end**. La valider peut donner la victoire aux Hunter. Les commandes directes de rôle s’appliquent immédiatement : utilisez-les avec discernement. No Team peut être attribué ici ; la synchronisation ordinaire au démarrage/à la connexion peut transformer un joueur sans rôle en Hunter pendant une partie active.

### Spectateurs

Un administrateur attribue `/mspectator <player>` ou choisit **Spectator** dans Player Roles. La commande vérifie les droits administratifs même si son descripteur n’a pas de ligne de permission. Les joueurs ne s’inscrivent pas eux-mêmes en lançant `/mhspectate`.

Un spectateur reçoit une boussole **Spectator teleport** dans le premier emplacement de sa barre rapide. Tenez-la dans la main principale et faites un clic droit, ou utilisez `/mhspectate`, pour ouvrir le menu de téléportation à six lignes. Ce menu fonctionne uniquement si le joueur a le rôle Spectator. Ses cinq premières lignes contiennent jusqu’à 45 Runner/Hunter vivants et connectés, triés par nom ; cliquez sur une case de rôle nommée pour rejoindre la position actuelle du joueur, y compris dans un autre monde. En bas, **Previous Page** est en C1, **Close** en C5 et **Next Page** en C9. Sans participant approprié, R3 C5 indique **No players available**. Fermer ce menu ne quitte pas le rôle de spectateur.

Les spectateurs volent, sont cachés aux autres joueurs, n’entrent pas en collision et sont protégés des dégâts. L’implémentation utilise le mode Aventure avec vol ; elle n’accorde ni caméra Spectateur vanilla ni déplacement à travers les blocs. Elle bloque attaques, destruction/placement de blocs, interactions ordinaires avec blocs/entités, ramassage/lâcher d’objets, échange de main secondaire, clics/glissements d’inventaire, manipulation de porte-armures et ramassage/gain d’expérience. Les créatures ne peuvent pas les cibler et les variations de faim sont annulées. `/teammsg <message>` atteint les autres joueurs ayant le rôle Spectator. Ne transmettez pas aux concurrents les positions des participants ni d’autres aides extérieures.

Pour quitter ce rôle, un administrateur attribue **Runner**, **Hunter** ou **No Team**, ou utilise `/mrunner <player>` ou `/mhunter <player>`. Il n’existe ni commande ni bouton dédié permettant de sortir soi-même. La sortie restaure inventaire/curseur, position, mode de jeu, vol, collisions et immunité sauvegardés, puis applique le comportement de partie du nouveau rôle. L’état du spectateur est enregistré pour la reconnexion. Full Match Reset restaure cet état, efface les rôles et déplace les joueurs connectés vers un point d’apparition sûr de l’Overworld lorsqu’il est disponible. Le nettoyage normal de fin de partie laisse les spectateurs hors du traitement des objets/du vol des participants.

### Match Settings (cinq lignes)

| Position | Bouton | Action |
|---|---|---|
| R2 C2 | Friendly Fire | Activer/désactiver les dégâts entre équipiers. |
| R2 C4 | Smart Hunter Kit | Activer/désactiver les kits adaptatifs de réapparition Hunter. |
| R2 C6 | Auto World Spawn | Ouvrir le choix d’intervalle. |
| R2 C8 | Reconnect Grace | Ouvrir le choix de durée de reconnexion des Runner. |
| R4 C2 | Match Preset | Choisir Classic, Fast, Hardcore ou Custom. |
| R4 C4 | Reset Settings | Confirmer les réglages équilibrés : Kit ON, Spawn 15m, Reconnect 15m. |
| R4 C6 | Random Head Start | Case d’information ; la roulette choisit toujours le délai. |

**Back** est en R5 C1 ; **Close**, en R5 C9.

Le sélecteur **Reconnect Grace** à trois lignes propose **1, 5, 10, 15, 20, 30 minutes** en R2 C2–C7, dans cet ordre. Un clic enregistre la valeur et garde le sélecteur ouvert. Back est en R3 C1 ; Close, en R3 C9.

Le sélecteur **Match Preset** à trois lignes place **Classic**, **Fast**, **Hardcore**, **Custom** en R2 C2, C4, C6, C8. Classic : Kit ON, Spawn 15m, Reconnect 15m. Fast : ON, 5m, 10m. Hardcore : OFF, OFF, 5m. Custom conserve les réglages manuels actuels. Les préréglages maintiennent le délai aléatoire. Le menu reste ouvert après sélection ; Back est en R3 C1, Close en R3 C9.

**Auto World Spawn** propose OFF, 5m, 10m en R2 C2, C3, C4 et 15m, 20m, 30m en R2 C6, C7, C8. Back est en R3 C5. Choisissez un intervalle ou utilisez `/mhspawn <off|5|10|15|20|30|status>`. Cela déplace le point d’apparition de l’Overworld près d’un Runner approprié de l’Overworld ; l’action peut être ignorée en l’absence de cible appropriée. `/mhkit <on|off|toggle|status>` contrôle directement les kits.

### Player Management (six lignes)

| Position | Bouton | S’applique à |
|---|---|---|
| R1 C5 | Target Player | Ouvrir un sélecteur de joueurs nommés. |
| R2 C2 | Full Heal | Tous les joueurs connectés. |
| R2 C4 | Full Hunger | Tous les joueurs connectés. |
| R2 C6 | Clear Effects | Tous les joueurs connectés. |
| R2 C8 | Freeze Target | Joueur sélectionné. |
| R4 C2 | Clear Target Inventory | Joueur sélectionné ; confirmation nécessaire. |
| R4 C4 | Kill Target | Joueur sélectionné ; confirmation nécessaire et conséquences normales de partie applicables. |
| R4 C6 | Set Day | Votre monde actuel. |
| R4 C8 | Clear Weather | Votre monde actuel. |
| R5 C2 | Clear Dropped Items | Votre monde actuel ; confirmation nécessaire. |
| R5 C4 | Emergency Sync | Actualiser les systèmes de rôles/d’exécution des joueurs connectés. |
| R5 C6 | Freeze Team | Gauche : Runner ; droite : Hunter ; Maj-clic : retirer ces gels d’équipes/individuels. |

Back est en R6 C1 ; Close, en R6 C9. Le choix de cible ne modifie pas les rôles. Son sélecteur offre 28 autres joueurs connectés par page, lignes 2–5 et colonnes 2–8 ; cliquez sur un nom pour le sélectionner et revenir. Previous/Back/Next sont en R6 C1/C5/C9. Revérifiez la cible affichée avant d’appliquer une action.

### Écrans de confirmation

Reset Match, Teleport Everyone, Reset Settings, Clear Target Inventory, Kill Target, Clear Dropped Items et le changement du dernier Runner par l’interface utilisent un écran séparé **Confirm Action** à trois lignes. Lisez l’action/la cible en R1 C5, puis cliquez sur **Confirm** vert en R2 C3 ou **Cancel** rouge en R2 C7. La confirmation expire après **30 secondes**. Une cible modifiée/déconnectée ou un rôle modifié impose une nouvelle sélection. Pour ces nouveaux parcours, cela remplace les clics répétés sous cinq/huit secondes de l’ancien guide.

### GrimAC Security et langue

Le menu Grim à six lignes affiche l’état en R1 C5 ; les commutateurs en R2 C2 **GrimAC Master**, C4 **Movement**, C6 **Combat**, C8 **Packets** ; R4 C2 **Velocity / AntiKB**, C4 **World / Scaffold**, C6 **Anti X-Ray**, C8 **Admin Alerts** ; et R5 C5 **Monitor mode**. Back est en R6 C1 et Close en R6 C9. Monitor mode choisit alertes/preuves ou application des mesures. Paper Anti-Xray est indépendant et exige un redémarrage après modification. Ce sont des contrôles GrimAC ; la description de l’ancien menu VexAC/AutoClick ne correspond pas à cette version.

Global Language s’applique à tous et actualise menus/objets. Cliquez sur la langue nommée ; Back est en R3 C5. `/mhlang` ouvre le même sélecteur et `/mhhelp` fournit le guide joueur/administrateur traduit.

### Valeurs actuelles, reconnexion et modération

Les valeurs de repli d’une configuration neuve dans `plugins/VexLandManhunt/config.yml` sont :

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` signifie que le déplacement automatique du point d’apparition est désactivé. Reset Settings et Classic choisissent plutôt 15 minutes. Pendant la fenêtre de reconnexion d’un Runner, sa place est conservée ; un retour à temps offre dix secondes de protection. La durée d’arrêt enregistrée du serveur est exclue. L’expiration peut transformer le Runner en Hunter ou terminer la partie au profit des Hunter. Pause/Resume gèle les systèmes de jeu et ajuste le temps de partie actif. Le plugin gère les fichiers de restauration.

Les réglages de la passerelle Grim sont enregistrés dans `plugins/VexLandManhunt/grim-settings.yml`. Les valeurs initiales sont Master ON, les cinq groupes ON, Admin Alerts ON et **Monitor mode OFF : l’application des mesures est activée**. Monitor mode met en file preuves/alertes et annule les flags concernés. En mode d’application, la passerelle peut convertir une commande d’expulsion Grim en déconnexion traduite autorisant le retour ; elle ne définit pas de bannissement permanent. Les seuils réels dépendent également de la configuration de Grim. Les preuves sont mises en file vers `plugins/VexLandManhunt/anticheat/grim-evidence.log` ; les files limitées peuvent perdre des entrées sous charge. La passerelle exempte les spectateurs, le jeu suspendu/gelé et certains contextes de véhicules, avec trois secondes de grâce après connexion, téléportation et réapparition. Aucune mesure de précision anti-triche ou de performances n’est revendiquée.

## Référence des commandes publiques — 1.13.1

L’accès administrateur signifie OP ou `vexland.admin` (OP par défaut). Le gestionnaire de `/mspectator <player>` le vérifie malgré l’absence de ligne de permission dans le descripteur. Les commandes directes de rôle s’appliquent immédiatement ; changer le dernier Runner pendant RUNNING peut terminer la partie. L’interface offre une confirmation dans cette situation.

| Commande | Utilité | Accès |
|---|---|---|
| `/mhgui` | Ouvrir le centre de contrôle par catégories | Administrateur |
| `/mhstart` | Lancer toute la séquence de partie | Administrateur |
| `/mhreset` | Réinitialiser complètement la partie | Administrateur |
| `/mhrelease` | Libérer les Hunter en attente | Administrateur |
| `/mrunner <player>` | Attribuer Runner | Administrateur |
| `/mhunter <player>` | Attribuer Hunter | Administrateur |
| `/mspectator <player>` | Attribuer Spectator | Administrateur ; nouveau |
| `/mhspectate` | Ouvrir le menu de téléportation des participants | Spectator actuel ; nouveau |
| `/teammsg <message>` | Envoyer à son propre rôle/équipe | Joueur |
| `/trash` | Inventaire jetable de 54 emplacements ; alias `/mhtrash`, `/vextrash` | Joueur |
| `/nv` | Activer/désactiver sa vision nocturne | Joueur |
| `/mhlang` | Ouvrir le sélecteur de langue globale | Administrateur |
| `/mhkit <on\|off\|toggle\|status>` | Configurer les kits adaptatifs Hunter | Administrateur |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Configurer le déplacement du point d’apparition | Administrateur |
| `/mhhelp` | Recevoir le guide traduit de rôle/d’administration | Joueur / administrateur |
| `/mhpause` | Suspendre la partie en cours | Administrateur |
| `/mhresume` | Reprendre la partie suspendue | Administrateur |
| `/mhdebug` | Diagnostics internes | Administrateur |

`/mhnone` n’est pas enregistré dans cette version ; utilisez No Team dans l’interface. Les Hunter font un clic droit avec leur boussole de suivi pour choisir un Runner ; ce mécanisme est distinct de la téléportation des spectateurs et du sélecteur de cible administratif. Les Runner gagnent en battant l’Ender Dragon ; les Hunter gagnent lorsqu’aucun Runner ne reste. Un Runner tombé devient Hunter si d’autres Runner restent.

## Langues, historique et crédits tiers

Le plugin original propose **10 langues de jeu** : anglais, persan, arabe, espagnol, français, allemand, russe, chinois simplifié, hindi et portugais. `/mhlang` choisit une langue pour tout le serveur, enregistrée dans `language.txt`. Le manuel GitHub existe en **18 langues**, sans édition arabe de la documentation. Le japonais et les autres langues supplémentaires du README n’ajoutent pas de traductions en jeu aux JAR inchangés.

L’[historique des versions](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/CHANGELOG.md) décrit chaque version fournie. L’intégralité de l’ancien manuel 1.9.11 / 1.6.4 demeure dans les [archives versionnées](../1.9.11/README.fr.md). La version dédiée aux spectateurs a maintenant été fournie et publiée sous 1.13.1 ; ses fonctions ne doivent pas être attribuées aux anciens téléchargements.

**GrimAC est un projet indépendant des contributeurs GrimAC, distribué sous GPL-3.0.** Bardiya et Ali ont créé Vexland_Manhunt et son intégration ; ils ne sont pas présentés comme auteurs de GrimAC. Le JAR Grim fourni correspond aux SHA-512 et SHA-1 de l’artefact Bukkit officiel Modrinth 2.3.73. Son commit source intégré correspond à [la version amont v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73). La publication comprend les binaires inchangés, sommes de contrôle, instantané du code source amont, licence et [mentions tierces](../../../THIRD_PARTY_NOTICES.md). Ces mentions de composants n’attribuent pas de licence au projet Manhunt distinct.

## Un défi humoristique à Dream

Une petite taquinerie Minecraft de Bardiya 😄

> « Pfff… Ali et moi avons créé un plugin Manhunt cent fois meilleur que celui de Dream, mais Dream a peur et ne veut pas jouer avec le nôtre ! »

## Créateurs et périmètre du projet

**Créé conjointement par [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) et [Ali · Alivexor](https://github.com/Alivexor).** Les deux pseudonymes sont également enregistrés comme auteurs dans les descripteurs originaux du plugin.

Ce dépôt présente les versions compilées originales, leur documentation et leurs notes de version comme un projet de portfolio commun. Les descriptions de fonctionnalités reposent sur une inspection statique des JAR fournis. La compatibilité sur serveur actif, les performances de récupération, l'équilibrage et la précision anti-triche n'ont pas été testés dans ce processus de publication.

[Portfolio GitHub de Bardiya](https://github.com/FarlandGame) · [GitHub d'Ali](https://github.com/Alivexor) · [Toutes les versions](https://github.com/FarlandGame/Vexland_Manhunt/releases)
