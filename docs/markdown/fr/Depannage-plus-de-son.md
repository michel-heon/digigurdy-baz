# Dépannage – Plus de son sur la Digigurdy

Ce guide t’aide à diagnostiquer le cas où **ta Digigurdy n’émet plus de son**, alors qu’elle fonctionnait auparavant.

> Il couvre à la fois :
> - l’utilisation avec **sortie audio intégrée** (Tsunami/Trigger + casque/ampli),
> - l’utilisation comme **contrôleur MIDI**,
> - et le cas particulier où la gurdy est restée en **mode MIDI uniquement** alors que tu attends du **son audio direct**.

---

## 1. Première question : comment attends‑tu le son ?

Identifie d’abord ce que tu es en train d’essayer de faire :

1. **Cas A – Tu veux entendre le son directement depuis la Digigurdy**
   - Tu as un **casque** ou des **enceintes amplifiées** branchées sur la **prise audio** de la gurdy.
   - Tu t’attends à entendre la vielle **sans PC, sans tablette**, ou PC/tablette seulement pour l’alimentation.

2. **Cas B – Tu veux utiliser la Digigurdy comme contrôleur MIDI**
   - Tu as la Digigurdy branchée en **USB** ou en **MIDI 5‑broches** vers un PC, iPad, iPhone, module externe…
   - Le son doit sortir de cet appareil externe (BS‑16i, DAW, expander…), pas directement de la gurdy.

Le chemin de dépannage dépend de ce choix.

---

## 2. Vérifications communes (dans tous les cas)

Avant de distinguer les cas A/B, vérifie ces points de base :

1. **Alimentation**
   - La Digigurdy s’allume‑t‑elle normalement ? (écran allumé, menus visibles)
   - Le câble USB‑B est‑il bien branché des deux côtés ?
   - Si tu utilises la **batterie interne**, est‑elle chargée ?

2. **La gurdy “joue‑t‑elle” du point de vue interne ?**
   - Appuie sur quelques touches à gauche.
   - Tourne la manivelle **ou** appuie sur le bouton **auto‑crank**.
   - Regarde l’écran : la note affichée change‑t‑elle quand tu appuies sur les touches ?
   - Si oui, **les touches et la logique interne fonctionnent**.

3. **Volume global**
   - Appuie plusieurs fois sur `X + T-UP` (volume +).
   - Si tu avais réduit le volume via `X + T-DOWN`, il est peut‑être simplement devenu inaudible.

---

## 3. Cas A – Tu veux du son direct (casque/ampli sur la Digigurdy)

### 3.1. Vérifier la chaîne audio simple

1. **Casque / ampli**
   - Ton casque fonctionne‑t‑il sur un autre appareil ?
   - Le jack est‑il bien enfoncé dans la prise audio de la Digigurdy ?
   - Si tu utilises un ampli/enceintes :
     - sont‑ils **amplifiés** ?
     - sont‑ils **allumés** ?
     - le volume de l’ampli n’est‑il pas à zéro ou en mute ?

2. **Volume côté Digigurdy**
   - Dans le menu pause → `Tuning` → `Volume` :
     - vérifie que les volumes des canaux de **mélodie**, **bourdon** et **trompette** ne sont pas à 0.
     - mets pour tester une valeur entre **80 et 100** pour les canaux importants.

3. **Mute des cordes**
   - Avec certains réglages, toutes les cordes peuvent être mutées via les boutons EX ou le menu pause.
   - Dans le menu pause, essaie de changer de combinaison de mute (avec `A`/`B` ou des boutons EX configurés pour ça) jusqu’à avoir au moins :
     - **une corde de mélodie active**,
     - et idéalement un **bourdon**.

### 3.2. Vérifier le module Tsunami/Trigger et la carte microSD

1. **La carte microSD est‑elle bien insérée ?**
   - Si tu as déjà ouvert la Digigurdy, vérifie que la **microSD** est bien enfoncée dans le module Tsunami/Trigger.
   - Une carte manquante ou mal insérée = souvent **aucun son**.

2. **Contenu de la microSD**
   - Si tu as ajouté/supprimé des fichiers ou essayé d’autres sons :
     - sauvegarde la carte au besoin,
     - formate‑la ou supprime **tous les fichiers**,
     - copie **uniquement le contenu** du dossier `mono` ou `stereo` fourni dans le ZIP Tsunami/Trigger du projet (pas le dossier lui‑même, juste les fichiers à la racine).

3. **Réglage de volume pour le Tsunami/Trigger**
   - Dans le menu pause → `Tuning` → `Volume`, les valeurs 0–127 sont aussi converties pour le Tsunami/Trigger.
   - Pour tester, mets le volume des canaux à une valeur moyenne (ex. 80) :
     - le **volume 112** correspond à un niveau « ligne » (niveau réel du WAV),
     - au‑dessus, c’est sur‑amplifié.

---

## 4. Cas particulier – La gurdy est en mode MIDI alors que tu veux de l’audio

Il est possible que la Digigurdy soit configurée pour envoyer principalement du **MIDI** sur la prise 5‑broches ou USB, et que la **sortie audio Tsunami/Trigger ne soit pas utilisée comme sortie principale**.

### 4.1. Vérifier la configuration Entrée/Sortie

1. Ouvre le **menu pause** (`X + A` ou bouton EX configuré pour ça).
2. Va dans **Other Options** → **Input/Output Configuration**.
3. Repère l’option **Secondary Output** (ou équivalent) :
   - elle détermine ce qui est utilisé en plus de l’USB MIDI.
   - selon le firmware, tu peux avoir des choix du type :
     - `MIDI-OUT`,
     - `Trigger/Tsunami`,
     - ou similaire.
4. Pour utiliser la **sortie audio**, assure‑toi que :
   - la sortie secondaire (ou l’option correspondante) est réglée sur **Trigger/Tsunami** (ou audio),
   - et non pas uniquement sur **MIDI‑OUT**.

### 4.2. Cas concret : tu alimentes via USB un iPad / PC mais tu veux le son du module audio

- Si ton PC / iPad reçoit du MIDI et qu’un logiciel est ouvert, il est possible que :
  - tu écoutes le mauvais périphérique (par ex. les haut‑parleurs du PC),
  - ou que tu attendes le son sur le casque branché à la Digigurdy alors que ton logiciel sort le son ailleurs.

Pour tester que le **module audio de la gurdy** fonctionne bien :

1. Débranche temporairement le PC / iPad (ou ferme le logiciel audio).
2. Alimente la gurdy avec un simple chargeur USB ou une powerbank.
3. Branche ton casque directement à la sortie de la gurdy.
4. Joue quelques notes :
   - si le son revient, ton problème était un **conflit de configuration / de sortie**.

---

## 5. Cas B – Tu utilises la Digigurdy comme contrôleur MIDI

### 5.1. Vérifier que le MIDI arrive bien

1. **Côté Digigurdy**
   - En jouant (touches + manivelle/auto‑crank), les notes changent‑elles sur l’écran ?
   - Si oui, la partie interne fonctionne.

2. **Côté appareil MIDI (PC, tablette…)**
   - Dans ton logiciel (BS‑16i, DAW, etc.) :
     - la Digigurdy (ou l’adaptateur MIDI Bluetooth) est‑elle bien sélectionnée comme **entrée MIDI** ?
     - vois‑tu une petite LED ou un indicateur qui clignote quand tu joues ?

3. Si **aucun signal MIDI** n’apparaît dans le logiciel :
   - teste un autre port USB ou un autre câble,
   - vérifie l’adaptateur (si Bluetooth ou MIDI 5‑broches).

### 5.2. Vérifier le son dans le logiciel

1. **Instrument chargé**
   - Un instrument (soundfont, VSTi, preset) est‑il bien chargé sur le (ou les) canal(aux) MIDI que la Digigurdy utilise (surtout canal 1 pour la mélodie aiguë) ?

2. **Volume / Mute**
   - Dans BS‑16i ou ton DAW :
     - le canal n’est‑il pas en **mute** ?
     - le **volume** du canal et du master n’est‑il pas à zéro ?

3. **Périphérique audio de sortie**
   - Le son sort‑il sur les bonnes enceintes / le bon casque ?
   - Si tu utilises un casque Bluetooth, teste avec un **casque filaire** pour éliminer un problème de configuration audio.

---

## 6. Réinitialiser proprement la configuration

Si tu as beaucoup bidouillé les réglages, il peut être plus simple de repartir d’une base saine.

1. **Charger un accordage standard**
   - Menu pause → `Load` → choisis un accordage prédéfini (G/C ou D/G).
   - Teste le son.

2. **Réinitialiser tous les paramètres**
   - Éteins puis rallume la Digigurdy.
   - Dans le **menu de démarrage**, choisis `Reset All Settings`.
   - Attention :
     - cela efface les accordages sauvegardés,
     - et réinitialise les boutons EX / options persistantes.
   - Rechoisis un accordage standard et teste à nouveau.

---

## 7. Si tu n’as toujours pas de son

Après toutes ces étapes, si tu n’entends toujours rien :

1. Note pour toi-même :
   - Utilises‑tu la **sortie audio** de la gurdy, le **MIDI**, ou les deux ?
   - L’écran réagit‑il bien quand tu joues (notes qui changent) ?
   - As‑tu récemment :
     - mis à jour le firmware,
     - modifié la carte microSD,
     - changé de câbles / appareil MIDI ?

2. Test rapide recommandé :
   - Essaye la configuration **la plus simple possible** :
     - Digigurdy + alimentation + casque sur la sortie audio,
     - aucun PC / tablette / logiciel ouvert.

3. Si même dans cette configuration minimale tu n’as aucun son :
   - il est possible qu’il y ait un **problème matériel** (prise jack, carte microSD, module Tsunami/Trigger, câbles internes, etc.).

Dans ce cas, garde ces informations et signale :
- ton modèle de Digigurdy,
- la version de firmware si tu la connais,
- ce que tu as déjà testé dans ce guide.

Cela aidera beaucoup pour un diagnostic plus poussé ou un support par le constructeur / la communauté.
