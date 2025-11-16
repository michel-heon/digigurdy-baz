# Guide Utilisateur Digigurdy

Ce document décrit la configuration générale et l'utilisation de la Digigurdy.

Pour un démarrage très simple pas à pas, voir : [Ma première utilisation de la Digigurdy](Ma-premiere-utilisation-de-la-digigurdy.md).

Pour des questions courantes, voir aussi la [FAQ Digigurdy (FR)](FAQ-fr.md).

_(Ce guide couvre la version 2.5 du code. Certaines fonctionnalités peuvent ne pas être présentes, ou avoir changé, depuis la dernière mise à jour de ce document.)_

- [Guide Utilisateur Digigurdy](#guide-utilisateur-digigurdy)
  * [Premiers Pas](#premiers-pas)
    + [Installation](#installation)
    + [Alimentation](#alimentation)
    + [Premier Démarrage](#premier-démarrage)
    + [Configuration MIDI](#configuration-midi)
      - [BS-16i](#bs-16i)
      - [Options PC Windows](#options-pc-windows)
      - [Soundfonts](#soundfonts)
      - [Canaux MIDI](#canaux-midi)
    + [Support Tsunami/Trigger](#support-tsunamitrigger)
  * [Commandes](#commandes)
    + [Combinaisons de touches](#combinaisons-de-touches)
  * [Jeu](#jeu)
  * [Le Menu Pause](#le-menu-pause)
    + [Charger](#charger)
    + [Sauvegarder](#sauvegarder)
    + [Accordage](#accordage)
      - [Accordage guidé](#accordage-guidé)
      - [Accordage manuel](#accordage-manuel)
      - [Volume](#volume)
      - [Le menu secret amusant](#le-menu-secret-amusant)
    + [Autres options](#autres-options)
      - [Configuration des boutons EX](#configuration-des-boutons-ex)
      - [Configuration de l'écran](#configuration-de-lécran)
      - [Configuration Entrée/Sortie](#configuration-entréesortie)
    + [Aide](#aide)
  * [Menu de démarrage](#menu-de-démarrage)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>(Généré avec markdown-toc)</a></i></small>

***

## Premiers Pas

### Installation

Si vous êtes ici pour mettre à jour le code de votre Digi-Gurdy, rendez‑vous [ici](https://github.com/bazmonk/digigurdy-baz/wiki/install-by-hex) pour les instructions sur le téléversement d'une des versions pré‑compilées. C'est un processus assez simple avec votre ordinateur, et il existe même [une vidéo de John Dingley](https://www.youtube.com/watch?v=XpZLFBAtYpw) qui le montre étape par étape.

### Alimentation

Les gurdies produites après octobre 2022 utilisent un connecteur USB‑B (la prise carrée utilisée par les imprimantes) pour se connecter à une source d'alimentation USB.

En plus d'un chargeur USB ou d'une batterie externe standard, la Digi-Gurdy inclut également une batterie interne. Pour l'utiliser, vous devrez acheter une batterie *18650 non protégée* ("non protégée" est important, les batteries protégées sont un peu trop grandes), dévisser le couvercle pour retirer le module d'alimentation, et y installer la batterie. Elle se recharge avec un câble microUSB et devrait fournir environ 15 heures de jeu par charge.

Les tablettes et téléphones plus récents avec USB‑C devraient également pouvoir alimenter une Digi-Gurdy. Elle consomme environ 130/240 mA (mode MIDI/Trigger), bien en dessous de la limite standard USB de 500 mA. Toutefois, certains appareils ne sont pas conçus pour alimenter des périphériques via leur port de charge et ne pourront pas le faire. Les anciens iPad avec connecteur Lightning, par exemple, ne peuvent pas alimenter la gurdy seuls. Pour ce type d'appareils, il existe des « adaptateurs appareil photo » qui fournissent des ports pour brancher la Digi-Gurdy et un câble d'alimentation sur votre tablette/appareil : ceux‑ci devraient fonctionner.

Il n'y a pas d'interrupteur marche/arrêt : brancher l'alimentation l'allume, débrancher l'alimentation l'éteint. Le Trigger/Tsunami s'allume et s'éteint automatiquement en interne selon que vous l'utilisez ou non.

### Premier Démarrage

Après la mise sous tension de la gurdy, le menu de démarrage s'affiche. **Si c'est la première fois que vous lancez une nouvelle version**, l'option 4 propose "Reset All Settings" (réinitialiser tous les réglages). Cela efface la mémoire de la gurdy et rétablit certains paramètres par défaut. Cette opération est recommandée après une mise à jour pour éviter un comportement instable. Elle efface aussi tous les préréglages enregistrés : à utiliser en connaissance de cause.

### Configuration MIDI

La Digi-Gurdy est un contrôleur MIDI. Elle se connecte à un échantillonneur/synthétiseur MIDI (comme l'application BS-16i sur iOS, ou GarageBand sur Mac) pour produire le son. Il existe deux façons de connecter votre gurdy en MIDI :

* **USB** – en plus de l'alimentation, le câble USB transporte aussi les données MIDI standard. Si vous branchez la gurdy sur un iPad, un ordinateur, etc. pour l'alimenter, vous pouvez aussi recevoir le MIDI via ce câble.

* **Prise MIDI** – la gurdy possède une prise standard MIDI‑OUT à 5 broches. Tout appareil MIDI avec une entrée MIDI‑IN devrait pouvoir la recevoir.
  * **Bluetooth** – une utilisation courante de cette prise est la connexion d'un adaptateur MIDI Bluetooth. Ces petits appareils coûtent environ 50 USD en ligne et sont très pratiques en combinaison avec la batterie interne, permettant une utilisation quasiment sans fil, avec un téléphone ou une tablette qui fournit l'audio.

Il **n'est pas recommandé d'utiliser des écouteurs ou casques Bluetooth pour jouer.** Vous constaterez que la latence est perceptible. Le MIDI représente _très_ peu de données par rapport à l'audio : c'est pourquoi le MIDI Bluetooth fonctionne avec très peu de délai, alors que l'audio Bluetooth non. Vous pouvez essayer, et il existe des codecs à faible latence, mais d'après mon expérience, soit la latence reste trop élevée, soit la qualité audio est médiocre (le son à faible latence est surtout une fonctionnalité de jeu vidéo). Je trouve que le plus simple et le plus « sans fil » est d'utiliser des écouteurs filaires branchés sur mon téléphone dans ma poche, combinés au MIDI Bluetooth.

Au moins un utilisateur a rapporté que des AirPods associés à un appareil Apple offrent une latence suffisamment faible pour être acceptable. Votre expérience peut varier.

#### BS-16i

L'échantillonneur MIDI qui fait le plus office de « standard » pour la Digigurdy est BS-16i, disponible sur iOS. Il offre de nombreuses fonctionnalités, est peu coûteux et fonctionne très bien avec le MIDI Bluetooth ou USB.

#### Options PC Windows

Michael Coene a partagé sur Facebook sa méthode pour utiliser son PC sous Windows pour la lecture audio. [Voir ici](./midi-on-win).

#### Soundfonts

Avec le MIDI, vous pouvez configurer les canaux pour obtenir pratiquement n'importe quel son. La soundfont de gurdy (ainsi que d'autres sons que vous pourriez vouloir essayer) se trouve [ici, dans ce dépôt](https://github.com/bazmonk/digigurdy-baz/tree/main/soundfonts). Un grand merci au projet MIDIgurdy qui les a créées à l'origine et les a rendues disponibles au public.

Votre échantillonneur (comme BS-16i) peut aussi inclure beaucoup d'autres sons à expérimenter.

#### Canaux MIDI

La Digigurdy utilise les canaux suivants :

1. Mélodie aiguë
2. Mélodie grave
3. Trompette
4. Bourdon
5. Buzz
6. Clic de touches

### Support Tsunami/Trigger

Si votre gurdy possède un échantillonneur wav Tsunami ou Trigger intégré (les modèles de digigurdy.com incluent des Triggers intégrés depuis environ mars 2023), elle peut sortir l'audio directement vers des écouteurs ou des enceintes amplifiées.

Les cartes Tsunami et Trigger fournissent un _signal audio de niveau ligne_. Celui‑ci n'est pas assez puissant pour piloter de grandes enceintes seul : des enceintes amplifiées sont recommandées pour tout ce qui est plus grand que des écouteurs.

Dans ce dépôt se trouvent des fichiers ZIP pour le Tsunami et le Trigger, qui contiennent les fichiers WAV et les fichiers de configuration nécessaires à leur fonctionnement. Pour les installer, retirez la carte microSD du Tsunami/Trigger, connectez‑la à un ordinateur, supprimez tous les fichiers de la carte, puis copiez le contenu du dossier `mono` ou `stereo` à l'intérieur du fichier ZIP (celui qui est présent) directement à la racine de la carte microSD. Ne copiez pas le dossier `mono`/`stereo` lui‑même, seulement son contenu. Éjectez ensuite la carte et réinsérez‑la dans la carte Tsunami/Trigger.

**REMARQUE : si vous installez vous‑même un module Trigger, il doit disposer d'un firmware à jour (1.3 ou supérieur). Les versions de firmware plus anciennes sont confirmées comme ne fonctionnant pas.**

***

## Commandes

Toutes les Digi-Gurdies ne possèdent pas l'ensemble des boutons présentés ici (ils sont mentionnés ci‑dessous). Pas d'inquiétude ! Voir la section suivante pour les « combinaisons de touches cachées » qui donnent accès à beaucoup de ces fonctions. Toutes les options sont disponibles, que vous ayez ou non ces boutons supplémentaires, soit via des combinaisons de touches, soit via le menu pause.

![keybox pic](https://raw.githubusercontent.com/wiki/bazmonk/digigurdy-baz/keys.jpeg)

* **Touches 1‑6** – pour sélectionner les éléments de menus
* **Touche X** – revient en arrière dans la plupart des menus
* **Touches A et B** – utilisées dans le menu pause, et aussi pour les combinaisons de touches ci‑dessous
* **Tpose Up/Down, Capo** _(les tout premiers modèles n'ont pas ces boutons)_ – pendant le jeu, ils servent à transposer les cordes et à faire défiler les options de capo (plus de détails plus loin)
* **EX1–EX3** _(les modèles à manivelle à engrenages n'ont pas ces boutons)_ – ces boutons ont un comportement configurable, mais par défaut :
  * EX1 ouvre le menu pause pendant le jeu
  * EX2 fait défiler les combinaisons de mute des cordes de mélodie
  * EX3 fait défiler les combinaisons de mute du bourdon et de la trompette
* **Auto-crank** (le « gros bouton ») – ce bouton active ou coupe les cordes comme si vous tourniez la manivelle.
* **Sensibilité du buzz** _(les modèles portables sans manivelle n'ont pas ce bouton)_ – ce potentiomètre ajuste la vitesse de manivelle nécessaire pour déclencher le buzz/coup de trompette. Il peut avoir une LED qui s'allume lorsque vous buzzez (les modèles antérieurs aux pédales accessoires possédaient cette LED).

### Combinaisons de touches

Il existe des combinaisons de touches « secrètes » qui étaient utilisées sur les anciens modèles qui n'avaient pas tous les boutons EX et transpose/capo. Elles sont toujours disponibles :

* **`X + A`** ouvre le menu pause pendant le jeu
* **`X + B`** fait défiler les options de capo
* **`1 + T-UP/DOWN`** transpose vers le haut/bas
* **`X + T-UP/DOWN`** augmente/diminue le volume

***

## Jeu

Si vous avez une manivelle à engrenages, après les écrans de démarrage la gurdy détectera si la manivelle est attachée. Ne touchez pas à la manivelle pendant ce test, car cela peut le perturber. Si vous le faites, vous pourrez relancer la détection depuis le menu pause.

Au démarrage, vous devrez charger ou choisir un accordage à utiliser. (Voir plus loin.)

Une fois connectée à votre échantillonneur MIDI (ou après avoir branché un haut‑parleur sur la sortie audio du Tsunami), vous êtes prêt à jouer ! Elle fonctionne comme une vielle à roue (mais pratique et juste). Tournez la manivelle ou appuyez sur le bouton `auto-crank` pour jouer. Par défaut, la note en cours jouée par la corde de mélodie aiguë est affichée à l'écran, ainsi que sa position sur une portée en clé de sol. Quand vous ne jouez pas, un écran d'état affiche la transposition actuelle, le capo, l'accordage et les cordes muettes.

_(Manivelle optique uniquement :)_ si vous utilisez la manivelle, le volume variera légèrement selon la vitesse de rotation (comme sur une vraie vielle).

En tournant très vite, vous déclenchez le buzz/coup de la trompette. À tout moment, vous pouvez ajuster la sensibilité du buzz à l'aide du potentiomètre. Quand il est tourné à fond dans le sens horaire (sensibilité minimale), le buzz est pratiquement désactivé.

_(Seules les gurdies postérieures à nov. 2022 disposent d'une prise accessoire.)_ Si vous utilisez une pédale accessoire de vibrato et qu'elle est activée (voir la section « Autres options » ci‑dessous), elle ajuste l'intensité de l'effet de modulation de votre échantillonneur MIDI, ce qui, avec BS-16i, produit un effet de vibrato sur les canaux de mélodie.

Pendant le jeu, vous pouvez ajuster la transposition des cordes avec les boutons `Tpose` (ou la combinaison de touches) par demi‑tons, sur une octave vers le haut ou vers le bas à partir de l'accordage choisi. Vous pouvez également mettre un capo sur les cordes de bourdon/trompette de un ou deux tons entiers (comme le permettraient de vrais capos sur une vielle) à l'aide du bouton `Capo` ou de la combinaison de touches.

Les options de boutons EX sont aussi disponibles pendant le jeu, par exemple pour muter certaines cordes à la volée. _(Modèles à manivelle optique uniquement.)_

Le menu pause est accessible en appuyant sur `X+A`, ou via un bouton EX (`EX1` par défaut). Toute note en cours est alors arrêtée.

***

## Le Menu Pause

Le menu pause permet d'accéder à tous les autres réglages de la Digigurdy. Dans tous les menus, les sélections se font avec les touches `1–6` et `X`, les fonctions étant indiquées à l'écran. Dans le menu pause principal, les touches `A` et `B` font également défiler les combinaisons de mute.

### Charger

Le menu Charger permet de charger l'un des quatre accordages prédéfinis pour les gurdies en G/C et D/G, ainsi que jusqu'à quatre accordages personnalisés que vous pouvez créer vous‑même pour y accéder facilement.

### Sauvegarder

Le menu Sauvegarder sert à enregistrer votre configuration actuelle dans l'un des quatre emplacements de sauvegarde. En plus de l'accordage de chaque corde, la transposition/capo actuelle et le volume de chaque corde/canal sont également enregistrés dans cet emplacement. Les réglages de mute ne font _pas_ partie des paramètres d'accordage.

_Remarque : définir un accordage (comme décrit plus bas) ne le sauvegarde PAS ! Vous devez enregistrer votre configuration séparément si vous voulez la conserver pour plus tard._

### Accordage

Le menu Accordage permet d'ajuster l'accordage des cordes/canaux et le volume. L'accordage peut se faire de deux façons : guidée ou manuelle.

#### Accordage guidé

Pour l'accordage guidé, sélectionnez G/C ou D/C pour commencer, puis suivez les instructions à l'écran. Pour chaque corde, vous aurez un ensemble de choix qui fonctionnent bien ensemble et qui pourraient se retrouver sur de vraies vielles à roue.

#### Accordage manuel

Ce mode vous donne un contrôle total sur l'accordage des quatre cordes et du son de buzz (la note de clic de touches n'est pas ajustable). Vous pouvez d'abord choisir un accordage guidé, puis le modifier ensuite ici, ou aller directement dans ce menu et définir chaque note explicitement.

#### Volume

Les six canaux disposent chacun d'un réglage de volume indépendant. Il s'agit du volume MIDI (un nombre entre 0 et 127), distinct du volume de canal (le volume maximum potentiel du canal à volume MIDI 127) dans BS-16i ou votre échantillonneur MIDI. La valeur par défaut utilisée ici est 70.

Si votre échantillonneur MIDI permet de régler le volume, vous n'aurez généralement pas besoin de modifier ce volume‑ci.

_(Modèles Tsunami/Trigger :)_ le contrôle de volume s'applique également au Tsunami. En interne, la valeur 0–127 est convertie automatiquement dans l'échelle de volume utilisée par Tsunami. Le volume 112 correspond au niveau ligne (aussi fort que le fichier WAV d'origine). Au‑dessus, le signal est sur‑amplifié.

#### Le menu secret amusant

En appuyant sur le bouton « 6 » depuis le menu Accordage principal (alors qu'aucune option 6 n'est affichée), vous accédez à mon écran secret amusant ! Ici, vous pouvez ajouter une seconde voix à n'importe quelle corde : une quarte, une quinte ou une octave en dessous. Si vous enregistrez dans un emplacement alors que ces options sont activées, elles seront mémorisées dans cette sauvegarde.

Si vous ne sauvegardez pas dans un emplacement, ces réglages disparaîtront au prochain redémarrage.

Est‑ce utile ? Je ne sais pas. Est‑ce que ça sonne bien ? Certains réglages oui (essayez l'octave) ! Est‑ce amusant à utiliser ? Bien sûr !

### Autres options

Diverses options sont disponibles ici :

* **Détection de manivelle** (**modèles à manivelle à engrenages**) – sélectionnez cette option pour relancer la routine de détection de manivelle. Si vous souhaitez détacher/rattacher votre gurdy de/à son corps, faites‑le d'abord, puis lancez cette option.
* **Configuration des boutons EX** – voir ci‑dessous.
* **Configuration de l'écran** – voir ci‑dessous.
* **Configuration Entrée/Sortie** – voir ci‑dessous.
* **À propos de la Digigurdy** – affiche l'écran de titre/à propos, ainsi qu'un simple écran de remerciements pour les personnes ayant particulièrement aidé ce projet. Appuyez sur la touche `X` pour faire défiler les écrans.

#### Configuration des boutons EX

Les trois boutons `EX` peuvent être configurés pour réaliser différentes fonctions selon vos besoins. Ces réglages sont sauvegardés immédiatement, persistent entre les redémarrages et sont indépendants des emplacements de sauvegarde d'accordage. Effacer l'EEPROM réinitialise ces réglages.

_Nouveau en 2.4 :_ les boutons de transposition et de capo sont aussi configurables et apparaissent comme EX4, EX5 et EX6 dans ce menu.

_Nouveau en 2.5 :_ le bouton d'auto-crank est maintenant aussi configurable et apparaît comme « Big » dans ce menu.

Fonctions disponibles pour les boutons EX :
* Ouvrir le menu pause
* Faire défiler les combinaisons de mute des cordes de mélodie
* Faire défiler les combinaisons de mute du bourdon et de la trompette
* Basculer le mute du bourdon
* Basculer le mute de la trompette
* Baisser le volume
* Augmenter le volume
* Transposer vers le bas
* Transposer vers le haut
* Faire défiler les capos 0, +2, +4 demi‑tons
* Auto-crank (son on/off)

#### Configuration de l'écran

Nouvelles options de configuration d'affichage depuis la version 2.2.0 :

* **Notation** – choisir entre différentes notations de hauteur :
  * **Scientifique/ABC** – do central = C4.
  * **Solfège/DoRéMi** – solfège « do fixe », le do central s'affiche "Do4".
  * **Combo** – les notes sont affichées dans les deux notations. Le do central s'affiche « C4/DO4 ».
* **Activer/Désactiver l'indicateur de buzz** – si activé, un fin cadre rectangulaire clignote à l'écran lorsqu'un buzz est détecté. Ce réglage est persistant et constitue une alternative à la LED de buzz pour les modèles qui n'en ont pas.
* **Choisir l'écran de jeu** – choisir entre six affichages pendant que la gurdy joue :
  * Une grande note bitmap (notation ABC) + une portée affichant la note
  * Une grande note textuelle (correspondant à la notation choisie) + une portée
  * Uniquement la note bitmap, centrée
  * Uniquement la note textuelle, centrée
  * Uniquement la portée, centrée
  * Écran vide

#### Configuration Entrée/Sortie

* **Sortie secondaire** – en plus du MIDI USB, vous pouvez choisir entre l'utilisation de la prise MIDI‑OUT comme seconde sortie, ou d'une sortie audio Trigger/Tsunami.
* **Vibrato de mélodie MIDI** – en mode MIDI, une valeur de modulation constante peut être envoyée sur les cordes de mélodie, pour simuler un vibrato sur les touches. Vous pouvez régler ici l'intensité (ou désactiver la fonction). Personnellement, j'utilise la valeur 16 si vous voulez essayer. La valeur par défaut est 0.
* **LED de buzz** – si votre gurdy dispose d'une LED d'indication de buzz/coup, vous pouvez l'activer ou la désactiver ici. Ce réglage est persistant. Si votre version du code n'a pas le support LED activé à la compilation, cette option n'apparaîtra pas.
* **Pédale accessoire** – si votre gurdy possède une prise pédale accessoire, vous pouvez l'activer ici. Elle est désactivée par défaut à chaque mise sous tension, car l'activer sans pédale branchée provoque un comportement étrange. Si votre version du code n'intègre pas le support de la pédale, cette option n'apparaîtra pas.

### Aide

L'option « Aide » affiche un QR code. Vous pouvez le scanner avec n'importe quel smartphone pour obtenir un lien vers ce Guide Utilisateur.

***

## Menu de démarrage

Lorsque vous allumez la gurdy, l'écran de démarrage possède son propre menu « Autres options » avec des options spécifiques au démarrage :

* **Effacer l'EEPROM** – efface tous les emplacements de sauvegarde et réinitialise les boutons EX ainsi que divers réglages persistants à leurs valeurs par défaut. Cette opération est également recommandée après la mise à jour du code de votre Digigurdy, car la structure mémoire peut avoir changé.
* **Contrôle de scène** – BS-16i permet d'enregistrer vos réglages dans des profils appelés « scènes ». C'est pratique pour avoir une configuration pour un son de gurdy, une autre pour une cornemuse ou un autre instrument, une configuration pour un morceau particulier, etc. BS-16i peut être configuré pour changer de scène automatiquement lorsqu'il reçoit un signal MIDI particulier. Si le contrôle de scène est activé, la Digigurdy enverra ce signal lorsqu'on passe à un accordage prédéfini ou sauvegardé. En configurant cela, vous pouvez changer automatiquement d'« instrument » ou de configuration complète simplement en sélectionnant un accordage. Ce réglage persiste entre les redémarrages.
  * Fonctionnement : dans BS-16i, créez une « scène ». Choisissez les instruments et effets souhaités, etc.
  * Dans le menu Settings->Scenes->Assignment, assignez‑la à un numéro. Les numéros 0–3 correspondent aux quatre accordages prédéfinis de la gurdy, et les numéros 4–7 correspondent aux quatre emplacements d'accordages sauvegardés.
  * Dans Settings->CoreMIDI, activez l'option "Switch Scenes with Program Change". Vous pouvez utiliser "Omni" ou "Channel 1" (la Digigurdy enverra sur le canal 1).
  * Enfin, dans l'écran d'options de la Digigurdy, activez le contrôle de scène (Scene Control).
