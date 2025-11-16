# Dépannage – Plus de son sur la Digigurdy

Ce guide vous aide à diagnostiquer les situations où **la Digigurdy n’émet plus de son**, alors qu’elle fonctionnait auparavant.

> Il couvre :
> - l’utilisation avec **sortie audio intégrée** (Tsunami/Trigger + casque/ampli),
> - l’utilisation comme **contrôleur MIDI**,
> - et le cas où la gurdy est restée en **mode MIDI** alors que du **son audio direct** est attendu.

---

## 1. Première question : comment attendez‑vous le son ?

Commencez par identifier le mode d’utilisation :

1. **Cas A – Vous souhaitez entendre le son directement depuis la Digigurdy**
   - Un **casque** ou des **enceintes amplifiées** sont branchés sur la **prise audio** de la gurdy.
   - Vous attendez d’entendre la vielle **sans PC, sans tablette**, ou avec PC/tablette uniquement pour l’alimentation.

2. **Cas B – Vous utilisez la Digigurdy comme contrôleur MIDI**
   - La Digigurdy est branchée en **USB** ou en **MIDI 5‑broches** vers un PC, iPad, iPhone, module externe…
   - Le son doit sortir de cet appareil externe (BS‑16i, DAW, expander…), et non directement de la gurdy.

Le chemin de dépannage dépend de ce choix.

---

## 2. Vérifications communes (dans tous les cas)

Avant de distinguer les cas A et B, vérifiez les points de base suivants :

1. **Alimentation**
   - La Digigurdy s’allume‑t‑elle normalement ? (écran allumé, menus visibles)
   - Le câble USB‑B est‑il bien branché des deux côtés ?
   - Si vous utilisez la **batterie interne**, est‑elle suffisamment chargée ?

2. **Fonctionnement interne de la gurdy**
   - Appuyez sur quelques touches à gauche.
   - Tournez la manivelle **ou** appuyez sur le bouton **auto‑crank**.
   - Vérifiez que l’écran affiche des notes qui changent lorsque vous appuyez sur les touches.
   - Si c’est le cas, **les touches et la logique interne fonctionnent**.

3. **Volume global**
   - Appuyez plusieurs fois sur `X + T-UP` (augmentation du volume).
   - Si le volume a été fortement réduit via `X + T-DOWN`, il peut être simplement devenu inaudible.

---

## 3. Cas A – Son direct (casque/ampli sur la Digigurdy)

### 3.1. Vérifier la chaîne audio simple

1. **Casque / ampli**
   - Le casque fonctionne‑t‑il sur un autre appareil ?
   - La fiche jack est‑elle correctement insérée dans la prise audio de la Digigurdy ?
   - Si vous utilisez un amplificateur ou des enceintes :
     - sont‑ils **amplifiés** ?
     - sont‑ils **allumés** ?
     - le volume n’est‑il pas à zéro ou en mode muet ?

2. **Volume côté Digigurdy**
   - Dans le menu pause → `Tuning` → `Volume` :
     - vérifiez que les volumes des canaux de **mélodie**, **bourdon** et **trompette** ne sont pas à 0,
     - pour un test, placez ces canaux à une valeur comprise entre **80 et 100**.

3. **Mute des cordes**
   - Certains réglages permettent de muter toutes les cordes via les boutons EX ou le menu pause.
   - Dans le menu pause, modifiez la combinaison de mute (via `A`/`B` ou les boutons EX configurés à cet effet) jusqu’à obtenir au moins :
     - **une corde de mélodie active**,
     - et, idéalement, un **bourdon** actif.

### 3.2. Vérifier le module Tsunami/Trigger et la carte microSD

1. **Carte microSD correctement insérée**
   - Si la Digigurdy a été ouverte, vérifiez que la **carte microSD** est correctement insérée dans le module Tsunami/Trigger.
   - Une carte absente ou mal insérée entraîne généralement **l’absence totale de son**.

2. **Contenu de la carte microSD**
   - Si des fichiers ont été ajoutés/supprimés ou si des tests ont été réalisés avec d’autres sons :
     - sauvegardez éventuellement le contenu existant,
     - formatez la carte ou supprimez **tous les fichiers**,
     - copiez **uniquement le contenu** du dossier `mono` ou `stereo` du ZIP Tsunami/Trigger fourni (pas le dossier lui‑même, uniquement les fichiers à la racine).

3. **Réglage de volume pour Tsunami/Trigger**
   - Dans le menu pause → `Tuning` → `Volume`, les valeurs 0–127 sont converties pour le module Tsunami/Trigger.
   - Pour un test, positionnez les canaux concernés à une valeur moyenne (par exemple 80) :
     - le **volume 112** correspond à un niveau « ligne » (niveau réel du fichier WAV),
     - au‑delà, le signal est sur‑amplifié.

---

## 4. Cas particulier – La gurdy est en mode MIDI alors que vous souhaitez un son audio

Il est possible que la Digigurdy soit configurée pour envoyer principalement du **MIDI** via la prise 5‑broches ou l’USB, tandis que la **sortie audio Tsunami/Trigger** n’est pas utilisée comme sortie principale.

### 4.1. Vérifier la configuration Entrée/Sortie

1. Ouvrez le **menu pause** (`X + A` ou bouton EX configuré à cet effet).
2. Accédez à **Other Options** → **Input/Output Configuration**.
3. Recherchez l’option **Secondary Output** (ou équivalent) :
   - elle détermine ce qui est utilisé en plus du MIDI USB,
   - selon la version du firmware, les choix possibles peuvent être :
     - `MIDI-OUT`,
     - `Trigger/Tsunami`,
     - ou un intitulé similaire.
4. Pour utiliser la **sortie audio**, assurez‑vous que :
   - la sortie secondaire (ou l’option correspondante) est réglée sur **Trigger/Tsunami** (ou équivalent audio),
   - et non pas uniquement sur **MIDI‑OUT**.

### 4.2. Exemple : alimentation USB via PC / iPad mais utilisation attendue du module audio

- Si le PC ou l’iPad reçoit le MIDI et qu’un logiciel est ouvert, il se peut que :
  - le son soit envoyé vers un autre périphérique (par exemple les haut‑parleurs du PC),
  - alors que le casque est branché sur la Digigurdy et non sur le périphérique de sortie audio du logiciel.

Pour vérifier que le **module audio interne de la gurdy** fonctionne correctement :

1. Débranchez temporairement le PC / iPad (ou fermez le logiciel audio).
2. Alimentez la gurdy avec un chargeur USB simple ou une powerbank.
3. Branchez un casque directement sur la sortie audio de la gurdy.
4. Jouez quelques notes :
   - si le son revient, le problème était lié à un **conflit de configuration ou de routage audio**.

---

## 5. Cas B – Utilisation de la Digigurdy comme contrôleur MIDI

### 5.1. Vérifier l’arrivée des messages MIDI

1. **Côté Digigurdy**
   - En jouant (touches + manivelle/auto‑crank), vérifiez que les notes changent bien sur l’écran.
   - Si oui, la partie interne de la Digigurdy fonctionne.

2. **Côté appareil MIDI (PC, tablette, etc.)**
   - Dans le logiciel (BS‑16i, DAW, etc.) :
     - vérifiez que la Digigurdy (ou l’adaptateur MIDI Bluetooth) est bien sélectionnée comme **source d’entrée MIDI**,
     - observez si un indicateur (LED, icône) signale la réception de messages MIDI lorsque vous jouez.

3. Si **aucun signal MIDI** n’apparaît dans le logiciel :
   - essayez un autre port USB ou un autre câble,
   - vérifiez l’adaptateur (Bluetooth ou interface MIDI 5‑broches).

### 5.2. Vérifier le son dans le logiciel

1. **Instrument chargé**
   - Assurez‑vous qu’un instrument (soundfont, VSTi, preset) est bien chargé sur le ou les canaux MIDI utilisés par la Digigurdy (en particulier le canal 1 pour la mélodie aiguë).

2. **Volume / Mute**
   - Dans BS‑16i ou votre DAW :
     - le canal est‑il en **mute** ?
     - le **volume** du canal et du master n’est‑il pas à zéro ?

3. **Périphérique audio de sortie**
   - Vérifiez que le son est dirigé vers les bonnes enceintes ou le casque attendu.
   - Si un casque Bluetooth est utilisé, faites un test avec un **casque filaire** pour éliminer un problème de configuration audio.

---

## 6. Réinitialiser proprement la configuration

Si de nombreux réglages ont été modifiés, il peut être plus simple de repartir d’une base saine.

1. **Charger un accordage standard**
   - Menu pause → `Load` → sélectionnez un accordage prédéfini (G/C ou D/G).
   - Testez le son.

2. **Réinitialiser tous les paramètres**
   - Éteignez puis rallumez la Digigurdy.
   - Dans le **menu de démarrage**, choisissez `Reset All Settings`.
   - Attention :
     - cette opération efface les accordages sauvegardés,
     - et réinitialise les boutons EX ainsi que divers réglages persistants.
   - Sélectionnez à nouveau un accordage standard et testez le son.

---

## 7. Si aucun son n’est toujours audible

Après l’ensemble de ces vérifications :

1. Notez pour votre diagnostic :
   - utilisez‑vous la **sortie audio** de la gurdy, le **MIDI**, ou les deux ?
   - l’écran réagit‑il correctement lorsque vous jouez (notes qui changent) ?
   - avez‑vous récemment :
     - mis à jour le firmware,
     - modifié la carte microSD,
     - changé de câbles ou d’appareil MIDI ?

2. Test minimal recommandé :
   - utilisez la configuration **la plus simple possible** :
     - Digigurdy + alimentation + casque sur la sortie audio,
     - sans PC, tablette ou logiciel audio ouvert.

3. Si aucun son n’est audible même dans cette configuration minimale :
   - un **problème matériel** est envisageable (prise jack, carte microSD, module Tsunami/Trigger, câbles internes, etc.).

Dans ce cas, conservez les informations suivantes et communiquez‑les au support ou à la communauté :

- modèle exact de votre Digigurdy,
- version de firmware si vous la connaissez,
- étapes déjà effectuées en suivant ce guide.

Ces éléments faciliteront un diagnostic plus poussé et une aide ciblée.
