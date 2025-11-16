# Commandes Digigurdy – Aide-mémoire

> **Note** : Ce document est un aide-mémoire rapide basé sur le `User-Guide` officiel de la Digigurdy. Il récapitule les commandes et menus les plus utilisés (en particulier le *menu pause*, c'est-à-dire le grand menu de réglages accessible pendant le jeu avec `X + A` ou un bouton EX configuré), sans détailler toutes les explications du guide complet.

Ce document résume les commandes et actions décrites dans le `User-Guide` de la Digigurdy.

![Disposition des touches](https://raw.githubusercontent.com/wiki/bazmonk/digigurdy-baz/keys.jpeg)

| Fonctionnalité / Cas d'usage | Commande / Contrôle | Courte description |
| --- | --- | --- |
| Sélectionner un élément de menu | Touches `1` à `6` | Permettent de choisir les options affichées à l'écran dans les menus (pause, démarrage, etc.). |
| Revenir au menu précédent | Touche `X` | Annule ou quitte la sélection en cours et remonte d'un niveau de menu. |
| Navigation dans le menu pause | Touches `A` et `B` | Utilisées dans le menu pause, notamment pour faire défiler certaines options (dont les combinaisons de muting). |
| Ouvrir le menu pause pendant le jeu | `X + A` ou bouton `EX1` (par défaut) | Coupe les notes en cours et affiche le menu pause. |
| Changer d'option de capo | Touche `Capo` ou `X + B` | Fait défiler les différentes positions de capo pour drone/trompette. |
| Transposer les cordes (pendant le jeu) | Boutons `Tpose Up/Down` | Transpose les cordes par demi-tons, jusqu'à une octave au-dessus ou au-dessous du tuning choisi. |
| Transposer par combinaison de touches | `1 + T-UP/DOWN` | Transpose vers le haut ou le bas sans utiliser les boutons EX. |
| Ajuster le volume général | `X + T-UP/DOWN` | Augmente ou diminue le volume par pas prédéfinis. |
| Activer/désactiver le son des cordes | Bouton `Auto-crank` ("big button") | Simule la manivelle : active ou coupe les cordes comme si on tournait la manivelle. |
| Ajuster la sensibilité de la trompette (bourdon/coup) | Potentiomètre `Buzz Sensitivity` | Règle la vitesse de manivelle nécessaire pour déclencher le bourdon de trompette (coup) (sensibilité plus ou moins forte). |
| Mettre les cordes de mélodie en sourdine | Bouton `EX2` (par défaut) | Fait défiler les combinaisons de mise en sourdine pour les cordes de mélodie. |
| Mettre les drones/trompette en sourdine | Bouton `EX3` (par défaut) | Fait défiler les combinaisons de mise en sourdine pour drone et trompette. |
| Charger un accordage prédéfini ou sauvegardé | Menu `Load` | Permet de charger un des 4 préréglages (G/C, D/G) ou des 4 accordages personnalisés. |
| Sauvegarder la configuration actuelle | Menu `Save` | Enregistre l'accordage, la transposition, le capo et le volume des canaux dans un des 4 emplacements. |
| Démarrer un accordage guidé | Menu `Tuning` → `Guided Tuning` | Assistant pas-à-pas proposant des combinaisons de notes réalistes pour chaque corde. |
| Régler manuellement les notes de chaque corde | Menu `Tuning` → `Manual Tuning` | Donne un contrôle complet sur la note de chaque corde et sur le son de bourdon/coup. |
| Régler le volume MIDI de chaque canal | Menu `Tuning` → `Volume` | Ajuste le volume MIDI (0–127) des 6 canaux (mélodies, drone, trompette, key-click/bourdon/coup). |
| Ajouter un second ton à une corde (expérimental) | Menu `Tuning` → touche `6` (Secret Fun Menu) | Ajoute une quarte, une quinte ou une octave en dessous à une corde ; peut être sauvegardé dans un slot. |
| Relancer la détection de manivelle | Menu `Other Options` → `Crank Detection` | Recalibre la détection de la manivelle (modèles à manivelle engrenée). |
| Configurer les boutons EX et assimilés | Menu `Other Options` → `EX Button Configuration` | Assigne à EX1–EX3, EX4–EX6 (tpose/capo) et `Big` différentes fonctions (mute, transpose, volume, etc.). |
| Changer la notation et l'écran de jeu | Menu `Other Options` → `Screen Configuration` | Choix du type de notation (scientifique, solfège, combo), indicateur de bourdon/coup, et style d'affichage pendant le jeu. |
| Configurer les sorties MIDI/audio | Menu `Other Options` → `Input/Output Configuration` | Choix de la sortie secondaire (MIDI OUT ou Trigger/Tsunami), vibrato MIDI, Buzz LED, pédale accessoire. |
| Afficher les écrans "À propos" | Menu `Other Options` → `About Digigurdy` | Affiche les écrans de titre et de remerciements ; avancer avec la touche `X`. |
| Accéder à l'aide en ligne | Menu `Help` | Affiche un QR code menant à ce guide utilisateur. |
| Effacer la mémoire (sauvegardes et réglages persistants) | Menu de démarrage → `Other Options` → `Clear EEPROM` | Réinitialise tous les slots de sauvegarde et remet les options persistantes à zéro. |
| Activer/désactiver le contrôle de scènes BS-16i | Menu de démarrage → `Other Options` → `Scene Control` | Permet à la Digigurdy d'envoyer des changements de programme pour basculer entre scènes BS-16i lors du changement de tuning. |
| Activer un vibrato automatique sur les mélodies (MIDI) | Menu `Other Options` → `Input/Output Configuration` → `MIDI Melody Vibrato` | Définit la valeur de modulation constante envoyée sur les canaux de mélodie pour simuler un vibrato. |
| Activer ou désactiver la LED de bourdon/coup | Menu `Other Options` → `Input/Output Configuration` → `Buzz LED` | Active ou coupe le témoin lumineux de bourdon/coup, si présent dans le matériel et la compilation. |
| Activer la pédale accessoire | Menu `Other Options` → `Input/Output Configuration` → `Accessory Pedal` | Active la prise de pédale pour contrôler la modulation (vibrato) ; désactivée par défaut au démarrage. |

## Lexique des termes

Ce tableau regroupe quelques termes anglais utilisés dans l'interface de la Digigurdy et leur équivalent dans ce document.

| Terme interface (anglais) | Terme utilisé ici (français) | Commentaire |
| --- | --- | --- |
| Tuning | Accordage | Réglage des notes de chaque corde. |
| Guided Tuning | Accordage guidé | Assistant de choix d'accord pour chaque corde. |
| Manual Tuning | Accordage manuel | Réglage direct de la note de chaque corde. |
| Buzz / Coup | Bourdon / coup | Son caractéristique de la trompette lorsqu'on accélère la manivelle. |
| Buzz Sensitivity | Sensibilité de bourdon/coup | Potentiomètre réglant la vitesse nécessaire pour déclencher le bourdon/coup. |
| Buzz LED | LED de bourdon/coup | Témoin lumineux indiquant qu'un bourdon/coup est déclenché. |
| Mute (strings) | Mettre en sourdine | Action de rendre silencieuse une ou plusieurs cordes (mélodie, drone, trompette). |
