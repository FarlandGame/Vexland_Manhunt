# Vexland_Manhunt — 1.9.11 / 1.6.4

> Guide des versions archivées · [1.13.1 →](../../README.fr.md)

[English](README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**Une expérience Minecraft complète opposant les Runner aux Hunter, créée conjointement par [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) et [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt réunit la préparation des parties, les rôles des équipes, le début de la poursuite, le suivi, la progression, les récompenses, les résultats et l'administration dans un seul plugin pour serveur Paper. Les Runner tentent de vaincre l'Ender Dragon, tandis que les Hunter cherchent à éliminer le dernier Runner. Le plugin prend en charge plusieurs Runner et maintient la poursuite malgré les morts, réapparitions, changements de dimension et reconnexions. Son centre de contrôle `/mhgui` permet aux administrateurs de gérer une partie par des menus, avec des messages et des guides traduits pour les joueurs.

## Téléchargements et compatibilité

| Version du plugin | Téléchargement | Environnement cible |
| --- | --- | --- |
| **1.9.11** — version actuellement fournie | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Paper **1.21.11**, Java **21** |
| **1.6.4** — version antérieure | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Paper **1.21.11**, Java **21** |

**1.6.4 et 1.9.11 sont les numéros de version du plugin.** Les deux versions fournies déclarent l'API Minecraft `1.21.11` et des fichiers de classes Java 21. Ce sont des plugins serveur pour Minecraft Java Edition. [Les exigences Java de Paper selon la version](https://docs.papermc.io/paper/getting-started/) indiquent également Java 21 pour Paper 1.21.11. Aucune dépendance supplémentaire à un autre plugin n'est déclarée dans les descripteurs fournis.

Il s'agit des **versions originales pour serveur personnel, dotées d'un accès administratif élevé propre aux créateurs**, conservées exactement telles qu'elles ont été fournies. Le guide ci-dessous présente les commandes publiques de Manhunt.

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

## Quoi de neuf dans la version 1.9.11 ?

Ces changements ont été identifiés en comparant les deux versions fournies, notamment leurs métadonnées, ressources de messages et classes compilées.

| Ajout ou changement | Comportement dans la version 1.9.11 |
| --- | --- |
| **Smart Hunter Kit V3** | Les kits de réapparition adaptatifs tiennent compte de l'équipement des Runner, des équipes et du contexte de partie. Le système vise à maintenir les kits Hunter sous la moyenne de l'équipement Runner ; il se règle avec `/mhkit` ou l'interface. |
| **Point d'apparition automatique dans l'Overworld** | Déplace le point d'apparition du monde près d'un Runner admissible dans l'Overworld à intervalle choisi : désactivé, 5, 10, 15, 20 ou 30 minutes. Le système choisit une surface sûre et ignore les cas inadaptés. |
| **Pause et reprise** | `/mhpause` suspend le jeu ainsi que les minuteurs, le suivi et le déplacement du point d'apparition ; `/mhresume` les reprend. Le temps de pause est retiré du temps actif de partie. |
| **Récupération après redémarrage ou plantage** | Une couche de récupération restaure l'état, les rôles, les cibles des boussoles, la progression, les minuteurs de récompense/mort et les reconnexions grâce aux instantanés principaux/de secours, aux sauvegardes périodiques et à celles de l'arrêt. |
| **Réglages de reconnexion des Runner** | Une fenêtre configurable remplace les 60 minutes fixes précédentes. Valeur initiale : 15 minutes, avec 10 secondes de protection au retour. L'indisponibilité du serveur est exclue ; l'expiration peut transformer le Runner en Hunter ou terminer la partie. |
| **Administration élargie** | Change les rôles en cours de partie tout en préservant le dernier Runner ; actions sur un joueur choisi, téléportation/immobilisation d'équipes, resynchronisation d'état et raccourcis facilitent la gestion. |
| **Réinitialisation confirmée des réglages** | Deux clics en huit secondes appliquent Smart Kit ACTIVÉ, apparition automatique toutes les 15 minutes et reconnexion de 15 minutes. Cela diffère d'une installation neuve, où l'apparition automatique est DÉSACTIVÉE. |
| **VexAC 3.0** | Contrôles de mouvement, combat, AutoClick, vélocité/recul et construction ; activation générale ou par groupes, journal de preuves, alertes administrateurs et exemptions liées à l'environnement/au lag. |
| **Ultra Deep Debug v4** | `/mhdebug` fournit des diagnostics de machine à états, interface, kits/tests de charge synthétiques, paramètres de traduction, aller-retour de récupération et intégrité. |
| **Affichages étendus** | Progression plus détaillée, visuels de santé du dragon, résultats MVP/dégâts/distances et ping dans TAB. |
| **Changements de commandes** | Ajoute `/mhkit`, `/mhspawn`, `/mhpause`, `/mhresume` et `/mhdebug` ; retire `/mhnone` ; adapte `/mhhelp` au joueur/administrateur et ajoute des alias de `/trash`. |
| **Davantage de messages traduits** | Les ressources passent de 446 à 683 clés de messages par langue. |

Les contrôles intégrés de VexAC couvrent Fly, Speed, Timer, Phase, Step, NoSlow, GroundSpoof, Reach, KillAura, AimAssist, wall-hit, BadPackets, les motifs temporels AutoClick, le recul modifié, Scaffold, Tower, FastPlace, Nuker et la portée sur les blocs. Son interface indique un mode de surveillance uniquement, mais le code compilé contient aussi des chemins d'expulsion ; vérifiez la modération réelle sur un serveur de test avant de vous fier à cette indication. La version antérieure propose à la place les anciens contrôles Anti AutoClick et Anti Fly.

## Installation et utilisation complètes avec `/mhgui`

### 1. Installer une version sur le serveur

Arrêtez votre serveur **Paper 1.21.11 / Java 21**. Placez un JAR téléchargé dans son dossier `plugins/`. Ne gardez qu'une seule version de VexLandManhunt installée à la fois. Effectuez un redémarrage complet après le remplacement d'une version. Le nom interne du plugin reste `VexLandManhunt` ; le nom public du projet est `Vexland_Manhunt`.

### 2. Ouvrir le centre de contrôle

Connectez-vous comme administrateur avec **OP** ou la permission **`vexland.admin`**, puis saisissez :

```text
/mhgui
```

Les instructions suivantes couvrent l'interface publique du plugin **1.9.11**, avec les noms anglais de ses boutons. Les libellés suivent la langue sélectionnée sur le serveur. Pour utiliser toute l'interface, employez un compte **OP** de confiance : la permission du descripteur permet d'ouvrir la commande, mais certains gestionnaires de l'interface vérifient OP plus strictement. L'inventaire principal comporte cinq rangées de neuf emplacements. Survolez un bouton pour lire sa description et son réglage actuel. La plupart utilisent un clic normal ; les actions spéciales et confirmations sont expliquées ci-dessous. Le menu plus petit de 1.6.4 est présenté à la fin.

#### Préparer votre première partie

1. Ouvrez **Player Roles**. Cliquez sur la tête de chaque participant jusqu'à obtenir le bon rôle affiché. Dans 1.9.11, le rôle alterne entre **Runner** et **Hunter** ; un participant sans rôle devient Runner au premier clic. Les clics gauche/droit/avec Maj ne sont pas des raccourcis distincts pour choisir le rôle. Utilisez **Previous Page**, **Next Page** et **Back to Control Center** si nécessaire.
2. Affectez au moins un Runner et un Hunter. La procédure de démarrage peut transformer les joueurs connectés encore sans rôle en Hunter ; attribuer explicitement tous les rôles clarifie les équipes.
3. Cliquez sur **Friendly Fire** pour autoriser ou interdire les dégâts entre coéquipiers. Vérifiez l'indicateur ON/OFF après le clic.
4. Cliquez sur **Language** pour choisir la langue de tout le serveur. Ce réglage concerne les messages, interfaces, avis et guides de tous les joueurs, pas seulement le vôtre.
5. Examinez **Smart Hunter Kit**, **Auto World Spawn** et **Anti-Cheat**. Le bouton du livre donne accès au guide administrateur pour des explications en jeu.
6. Vérifiez que **Server Freeze** est désactivé, puis cliquez sur **Start Match**. Le démarrage prépare les joueurs et inventaires, lance la présentation et la roulette aléatoire de délai des Hunter, puis commence la chasse. Avant de démarrer, conservez les objets nécessaires en dehors des inventaires des participants.

#### Boutons principaux du centre de contrôle

Les positions comptent les rangées de haut en bas et les colonnes de gauche à droite. Elles décrivent la disposition finale décorée de 1.9.11.

| Position | Bouton anglais | Fonction |
|---|---|---|
| Rangée 2, colonne 2 | Player Roles | Ouvre le menu paginé des têtes de joueurs Runner/Hunter. |
| Rangée 2, colonne 3 | Target Player | Parcourt les autres joueurs connectés pour les actions administratives ciblées. Vérifiez le nom actuel. |
| Rangée 2, colonne 4 | Friendly Fire | Active ou désactive les dégâts entre coéquipiers. |
| Rangée 2, colonne 5 | Match Info | Envoie un bref rapport d'état, équipes, tirs alliés et cible choisie. |
| Rangée 2, colonne 6 | Start Match | Exécute le démarrage normal et la séquence d'avance aléatoire. |
| Rangée 2, colonne 7 | Full Heal | Restaure la santé de tous les joueurs connectés. |
| Rangée 2, colonne 8 | Reset Match | Réinitialise entièrement la partie. Différent de Reset Settings. |
| Rangée 3, colonne 2 | Full Hunger | Restaure nourriture et saturation de tous les joueurs connectés. |
| Rangée 3, colonne 3 | Release Hunters | Libère les Hunter en attente avant la fin de l'avance. |
| Rangée 3, colonne 4 | Clear Effects | Retire les effets de potion de tous les joueurs connectés. |
| Rangée 3, colonne 5 | Server Freeze | Active ou désactive l'immobilisation globale ; les joueurs ordinaires sans OP sont immobilisés. |
| Rangée 3, colonne 6 | Clear Target Inventory | Vide l'inventaire, l'armure et la main secondaire du joueur choisi après confirmation. |
| Rangée 3, colonne 7 | Teleport Everyone | Amène tous les joueurs connectés à votre position actuelle. |
| Rangée 3, colonne 8 | Kill Target | Tue le joueur choisi après confirmation ; les règles normales de mort peuvent affecter la partie. |
| Rangée 4, colonne 2 | Anti-Cheat | Ouvre les contrôles de sécurité VexAC. |
| Rangée 4, colonne 3 | Freeze Target | Active ou désactive l'immobilisation individuelle du joueur choisi. |
| Rangée 4, colonne 4 | Emergency Restore | Restaure santé, nourriture et saturation de tous les joueurs connectés. |
| Rangée 4, colonne 5 | Freeze Team | Clic gauche : Runner ; clic droit : Hunter ; clic avec Maj : retirer les immobilisations individuelles/d'équipes. |
| Rangée 4, colonne 6 | Set Day | Passe votre monde actuel au jour. |
| Rangée 4, colonne 7 | Clear Weather | Arrête pluie et orage dans votre monde actuel. |
| Rangée 4, colonne 8 | Language | Ouvre le sélecteur global de langue. |
| Rangée 5, colonne 2 | Smart Hunter Kit | Active ou désactive les kits adaptatifs de réapparition Hunter ; affiche ON/OFF. |
| Rangée 5, colonne 3 | Clear Dropped Items | Supprime les entités d'objets au sol de votre monde actuel. |
| Rangée 5, colonne 4 | Pause Match / Resume Match | Suspend ou reprend le jeu actif et les minuteurs de partie. |
| Rangée 5, colonne 5 | Emergency Sync | Resynchronise rôles, boussoles et état d'exécution associé. |
| Rangée 5, colonne 6 | Reset Settings | Restaure les réglages équilibrés après confirmation par deux clics. |
| Rangée 5, colonne 7 | Close | Ferme le centre de contrôle. |
| Rangée 5, colonne 8 | Auto World Spawn | Ouvre le choix d'intervalle d'apparition automatique dans l'Overworld. |
| Rangée 5, colonne 9 | Manhunt Administrator Guide | Donne le livre d'administration traduit. |

Le verre décoratif et les objets de titre/état ne sont pas des boutons de jeu.

#### Rôles et cibles sélectionnées

**Player Roles** modifie l'équipe Manhunt réelle d'un participant. Cliquez sur sa tête et lisez le rôle actualisé. Pendant STARTING/RUNNING, l'interface autorise les changements Runner/Hunter, mais refuse de transformer le dernier Runner en Hunter. Cela préserve le camp Runner de la partie en cours. Changez les rôles de manière réfléchie : l'état d'exécution des équipes et les boussoles sont synchronisés ensuite.

**Target Player** est distinct : il choisit quelqu'un pour Freeze Target, Clear Target Inventory ou Kill Target, sans modifier son équipe. Parcourez les joueurs jusqu'à voir le bon nom. Si une cible enregistrée devient indisponible, le code peut utiliser le premier autre joueur connecté ; vérifiez donc toujours le nom immédiatement avant une action ciblée. Si personne d'autre n'est connecté, il indique qu'aucune cible n'est disponible.

**Clear Target Inventory** et **Kill Target** nécessitent deux clics sur la même action pour la même cible en **cinq secondes**. Le premier arme la confirmation et identifie la cible ; le second exécute l'action. Changer de cible ou attendre trop longtemps impose une nouvelle confirmation. Vider un inventaire supprime son contenu ; tuer un Runner peut modifier ou terminer la partie selon les règles normales de mort.

**Freeze Team** propose les seuls raccourcis souris propres aux équipes dans ce menu : un clic gauche normal choisit les Runner, un clic droit normal les Hunter et un clic avec Maj retire toutes les immobilisations individuelles/d'équipes gérées par cet outil. Le réglage global Server Freeze est séparé et doit être désactivé séparément si les joueurs restent immobilisés.

#### Smart Hunter Kit

Cliquez sur **Smart Hunter Kit** pour activer ou désactiver les kits adaptatifs de réapparition Hunter. Le bouton affiche l'état actuel. Lorsque la fonction est active, un Hunter qui réapparaît peut recevoir un kit adapté à l'équipement Runner et au contexte de partie ; le guide fourni le décrit comme inférieur à la moyenne des Runner. Lorsqu'elle est désactivée, les Hunter ne reçoivent aucun kit automatique après leur mort. Cela ne désactive pas la boussole de suivi.

Pour définir directement l'état plutôt que l'inverser, utilisez `/mhkit on`, `/mhkit off` ou `/mhkit status`. La valeur de repli observée dans une nouvelle configuration est ACTIVÉ.

#### Auto World Spawn

Cliquez sur **Auto World Spawn**, puis choisissez **OFF**, **5 minutes**, **10 minutes**, **15 minutes**, **20 minutes** ou **30 minutes**. Le choix est enregistré et ramène à `/mhgui` ; **Back** revient sans choisir de nouvel intervalle.

Lorsque la fonction est active, le système cherche périodiquement une surface sûre dans l'Overworld près d'un Runner actif de cette dimension et y déplace le point d'apparition du monde. Il ignore le déplacement si aucun Runner n'est dans l'Overworld ou si aucun emplacement sûr n'est trouvé. La valeur de repli initiale est DÉSACTIVÉ. Les mêmes réglages existent avec `/mhspawn off`, `/mhspawn 15` ou `/mhspawn status`, en remplaçant 15 par tout intervalle pris en charge.

#### Pause, reconnexion et récupération

**Pause Match** est disponible lorsque la partie est RUNNING. Il suspend les systèmes de jeu, mouvements/interactions, minuteurs, suivi et déplacement du point d'apparition. **Resume Match** les reprend en compensant le temps de pause. Server Freeze immobilise seulement les joueurs et ne remplace pas une pause de l'horloge de partie.

La fenêtre de reconnexion des Runner est configurable, avec une valeur initiale de repli de **15 minutes**. Une reconnexion à temps restaure l'état Runner et donne dix secondes de protection au retour. Le temps d'arrêt du serveur ne consomme pas la durée de reconnexion sauvegardée. Les places Runner expirées deviennent Hunter ; l'expiration du dernier Runner peut donner la victoire aux Hunter.

L'interface fournie de 1.9.11 n'a **pas de sélecteur distinct de durée de reconnexion**. Pour la personnaliser, arrêtez le serveur, modifiez `plugins/VexLandManhunt/config.yml`, conservez ses autres réglages et définissez :

```yaml
features:
  custom-reconnect-minutes: 15
```

Redémarrez après modification. Les valeurs inférieures à une minute sont ramenées à une minute. **Reset Settings** restaure cette valeur à 15 minutes. La version compilée sauvegarde aussi les états de partie/reconnexion et des instantanés de secours pour les redémarrages/plantages ; laissez le plugin gérer ces fichiers plutôt que de les modifier pendant le jeu.

#### Reset Settings et Reset Match

**Reset Settings** nécessite deux clics en **huit secondes**. Le premier arme la confirmation ; le second restaure **Smart Kit ACTIVÉ**, **Auto Spawn toutes les 15 minutes**, **Reconnexion 15 minutes** et une **avance aléatoire**. Cela diffère d'une nouvelle installation, où Auto World Spawn est DÉSACTIVÉ par défaut de repli. Cette action modifie la configuration ; elle ne remplace pas la réinitialisation complète de partie.

**Reset Match** effectue la réinitialisation existante : il nettoie l'état et les objets temporaires, puis ramène les joueurs au point d'apparition de l'Overworld pour une nouvelle manche. Son bouton principal n'utilise pas la confirmation à deux clics de Reset Settings. **Start Match** peut préparer/vider les inventaires des participants. Vérifiez quel contrôle de réinitialisation/démarrage vous souhaitez utiliser avant de cliquer.

#### Contrôles de langue et d'anti-triche

**Language** ouvre le sélecteur global. Cliquez sur la langue souhaitée. Les deux versions contiennent anglais, persan, arabe, espagnol, français, allemand, russe, chinois simplifié, hindi et portugais. La sélection est partagée par le serveur et enregistrée. La documentation README japonaise n'ajoute pas le japonais au sélecteur en jeu du plugin.

**Anti-Cheat** ouvre **VexAC Security**. **VexAC Master** active/désactive le moteur interne ; **Movement**, **Combat**, **AutoClick**, **Velocity / AntiKB** et **World / Scaffold** activent/désactivent chacun leur groupe. **Anti X-Ray** inverse le réglage Anti-Xray de Paper ; redémarrez pour appliquer ce changement. Les cases d'état, de journal de preuves et de modèle de détection expliquent les systèmes actuels. **Back to Control Center** ramène au menu principal.

L'interface décrit une modération de surveillance uniquement, mais l'inspection statique conserve un chemin d'expulsion basé sur un seuil. Considérez le texte affirmant l'absence d'expulsions comme une divergence entre implémentation et documentation, et vérifiez la modération sur un serveur contrôlé avant de vous y fier.

#### Guide en jeu et dépannage

Cliquez sur **Manhunt Administrator Guide** ou utilisez `/mhhelp` pour recevoir un guide traduit. Dans 1.9.11, les joueurs peuvent utiliser `/mhhelp` pour leur guide adapté au rôle. Les Hunter font un clic droit sur leur boussole pour choisir un Runner ; cette interface de suivi est distincte du sélecteur administratif Target Player.

Si un rôle ou une boussole semble désynchronisé, **Emergency Sync** actualise l'état d'exécution associé. **Match Info** aide à vérifier les équipes et l'état. Si le démarrage échoue, vérifiez que la partie est prête, que le gel du serveur est désactivé et qu'une équipe Runner/Hunter existe. Après remplacement du JAR, préférez un redémarrage complet à `/reload`. `/mhdebug` est une commande de diagnostic administrateur de 1.9.11 ; sa présence ne signifie pas que ces versions ont réussi des tests sur un serveur actif.

#### Utiliser l'ancien centre de contrôle de 1.6.4

1.6.4 conserve **Player Roles**, **Friendly Fire**, **Start Match**, **Reset Match**, **Release Hunters Now**, **Server Lock**, **Teleport Everyone To Me**, **Heal & Feed Everyone**, **Match Status**, le choix de langue, **Anti Cheat** et un guide administrateur. Ses rôles suivent le cycle **None → Runner → Hunter** ; les changements sont verrouillés pendant le démarrage et la partie.

Son menu anti-triche contient les anciens **Anti AutoClick** (règle de 30 CPS avec avertissements/expulsions), **Anti Fly** et **Anti X-Ray** de Paper. Sa fenêtre de reconnexion Runner est fixée à **60 minutes**. L'activation Smart Hunter Kit V3, le sélecteur Auto World Spawn, pause/reprise, la confirmation Reset Settings et les outils supplémentaires ciblant joueurs/monde décrits plus haut appartiennent à 1.9.11 et ne doivent pas être attendus dans l'ancien menu.

Ce guide a été établi à partir des métadonnées JAR fournies, des textes de langue/aide intégrés et du désassemblage statique. L'interface n'a pas été exécutée sur un serveur Minecraft actif pendant cette inspection.

### 3. Jouer la poursuite

Les Runner s'échappent pendant l'avance aléatoire et progressent vers la victoire contre l'Ender Dragon. Les Hunter attendent leur libération, puis font un clic droit sur la boussole pour choisir un Runner. Les cibles peuvent changer en cours de partie, y compris lorsque la poursuite traverse les dimensions. Utilisez `/teammsg <message>` pour parler uniquement à votre équipe et `/mhhelp` pour le guide de rôle traduit de 1.9.11.

Si un Runner meurt, les autres continuent et le joueur tombé devient Hunter. Un Hunter peut réapparaître et reprendre le suivi. La mort du dernier Runner ou l'expiration de sa reconnexion peut donner la partie aux Hunter ; la défaite de l'Ender Dragon la termine pour les Runner.

### 4. Mettre en pause, terminer et préparer une autre partie

Dans 1.9.11, mettez en pause avec `/mhpause` et reprenez avec `/mhresume`. Utilisez `/mhrelease` pour libérer les Hunter avant la fin du compte à rebours. Pour une nouvelle partie, utilisez la réinitialisation complète du centre de contrôle ou `/mhreset` ; elle nettoie l'état et les objets temporaires et ramène les joueurs au point d'apparition de l'Overworld. Modifier l'Anti-Xray de Paper exige un redémarrage.

## Réglages par défaut de 1.9.11

Les valeurs de repli observées pour une configuration neuve sont :

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` signifie que le déplacement automatique du point d'apparition est désactivé. L'action confirmée de réinitialisation de l'interface fixe plutôt cet intervalle à 15 minutes. Utilisez l'interface ou `/mhkit` et `/mhspawn` pour les réglages correspondants.

## Référence des commandes publiques

Les commandes administrateur ci-dessous utilisent `vexland.admin`, accordée par défaut aux OP. Discussion d'équipe, poubelle et vision nocturne n'ont pas de permission de descripteur ; `/mhhelp` devient un guide joueur/administrateur dans 1.9.11.

| Commande | Fonction | Disponibilité |
| --- | --- | --- |
| `/mhgui` | Ouvrir le centre de contrôle | Les deux versions |
| `/mhstart` | Exécuter la séquence complète de démarrage | Les deux versions |
| `/mhreset` | Réinitialiser complètement la partie | Les deux versions |
| `/mhrelease` | Libérer les Hunter en avance | Les deux versions |
| `/mrunner <player>` | Affecter un Runner | Les deux versions |
| `/mhunter <player>` | Affecter un Hunter | Les deux versions |
| `/mhnone <player>` | Retirer un rôle | 1.6.4 seulement |
| `/teammsg <message>` | Envoyer un message privé à l'équipe | Les deux versions |
| `/trash` | Ouvrir l'inventaire jetable de 54 emplacements | Les deux ; alias 1.9.11 : `/mhtrash`, `/vextrash` |
| `/nv` | Activer ou désactiver la vision nocturne personnelle | Les deux versions |
| `/mhlang` | Ouvrir le sélecteur global de langue | Les deux ; administrateur |
| `/mhhelp` | Recevoir un guide traduit | 1.6.4 administrateur uniquement ; 1.9.11 guide joueur/administrateur |
| `/mhkit <on\|off\|toggle\|status>` | Configurer les kits Smart Hunter | 1.9.11 |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Configurer le déplacement automatique du point d'apparition | 1.9.11 |
| `/mhpause` | Mettre la partie active en pause | 1.9.11 |
| `/mhresume` | Reprendre la partie en pause | 1.9.11 |
| `/mhdebug` | Exécuter les diagnostics internes | 1.9.11 |

## Langues en jeu et langues de documentation

Les deux versions proposent **10 langues en jeu** : anglais, persan, arabe, espagnol, français, allemand, russe, chinois simplifié, hindi et portugais. Un administrateur choisit la **langue globale du serveur** avec `/mhlang` ; messages, menus, avis et guides suivent cette sélection, enregistrée dans `language.txt`.

La documentation GitHub est publiée en **18 langues, sans édition de documentation arabe**. Les traductions README japonaises, turques et les autres langues supplémentaires aident à comprendre le projet ; elles n'ajoutent aucune langue en jeu à ces JAR originaux.

## Historique et prochaine version

[CHANGELOG.md](../../../CHANGELOG.md) décrit les différences entre les versions téléversées. La version supplémentaire dotée d'une fonction spectateur dédiée est **en attente de réception pour une future publication**. Les références existantes au mode Spectator de Minecraft standard n'établissent pas la présence de cette nouvelle fonction dans les deux téléchargements fournis. Chaque version reçue ultérieurement aura son téléchargement, sa somme de contrôle et ses notes de changements après comparaison avec la précédente.

## Un défi humoristique à Dream

Une petite taquinerie Minecraft de Bardiya 😄

> « Pfff… Ali et moi avons créé un plugin Manhunt cent fois meilleur que celui de Dream, mais Dream a peur et ne veut pas jouer avec le nôtre ! »

## Créateurs et périmètre du projet

**Créé conjointement par [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) et [Ali · Alivexor](https://github.com/Alivexor).** Les deux pseudonymes sont également enregistrés comme auteurs dans les descripteurs originaux du plugin.

Ce dépôt présente les versions compilées originales, leur documentation et leurs notes de version comme un projet de portfolio commun. Les descriptions de fonctionnalités reposent sur une inspection statique des JAR fournis. La compatibilité sur serveur actif, les performances de récupération, l'équilibrage et la précision anti-triche n'ont pas été testés dans ce processus de publication.

[Portfolio GitHub de Bardiya](https://github.com/FarlandGame) · [GitHub d'Ali](https://github.com/Alivexor) · [Toutes les versions](https://github.com/FarlandGame/Vexland_Manhunt/releases)
