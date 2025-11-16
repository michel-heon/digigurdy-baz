# FAQ Digigurdy (FR)

> Pour les problèmes de son (plus de son, mode MIDI vs audio, etc.), voir aussi : [Dépannage – Plus de son sur la Digigurdy](Depannage-plus-de-son.md).

## 1. Qu’est‑ce que la Digigurdy et de quoi ai‑je besoin pour l’utiliser ?

La Digigurdy est une vielle à roue électronique qui agit comme un contrôleur MIDI (et, selon le modèle, comme un lecteur d’échantillons audio via Tsunami/Trigger). Pour l’utiliser, il vous faut :

- une source d’alimentation (USB ou batterie 18650 interne),
- un appareil qui lit le MIDI (PC, tablette, smartphone, module externe),
- un logiciel ou un module sonore (par exemple BS‑16i sur iOS, un sampler sur PC, etc.).

---

## 2. Comment mettre à jour le firmware / code de ma Digigurdy ?

Vous pouvez télécharger une version pré‑compilée (fichier `.hex`) depuis le dépôt GitHub, puis la téléverser avec votre ordinateur. Le guide d’installation par fichier hex se trouve ici :

<https://github.com/bazmonk/digigurdy-baz/wiki/install-by-hex>

---

## 3. Quels types d’alimentation puis‑je utiliser ?

- Port USB‑B (depuis un chargeur, un PC, une powerbank, etc.),
- batterie interne basée sur une cellule 18650 *non protégée*,
- certains téléphones / tablettes USB‑C capables de fournir du courant.

La consommation est typiquement 130–240 mA, bien en dessous de la limite USB de 500 mA.

---

## 4. Comment installer et charger la batterie 18650 interne ?

1. Acheter une 18650 **non protégée**.
2. Dévisser le couvercle de la Digigurdy pour sortir le module de powerbank.
3. Insérer la batterie dans le logement prévu (en respectant la polarité).
4. Replacer le module et revisser.
5. Charger la batterie avec un câble micro‑USB.

Une charge complète donne environ 15 h de jeu.

---

## 5. Ma tablette ou mon téléphone peut‑il alimenter directement la Digigurdy ?

- Les appareils USB‑C récents le peuvent souvent, mais pas tous.
- Les anciens iPad avec connecteur Lightning, par exemple, ne fournissent pas assez de courant.

Dans ce cas, un « adaptateur appareil photo » Apple ou équivalent (avec alimentation externe + USB) est recommandé.

---

## 6. À quoi sert l’option « Reset All Settings » au démarrage ?

Cette option efface tous les paramètres persistants et rétablit les valeurs par défaut (y compris les préréglages sauvegardés).

Elle est **fortement recommandée après une mise à jour du firmware** pour éviter des comportements erratiques liés à des changements de structure mémoire.

---

## 7. Comment connecter la Digigurdy en MIDI via USB ?

Branchez la prise USB‑B de la Digigurdy sur :

- un ordinateur,
- un iPad (via adaptateur si nécessaire),
- ou un smartphone compatible OTG/USB‑C.

Le même câble sert à l’alimentation et au transport des messages MIDI. Dans votre logiciel audio (DAW, BS‑16i, etc.), sélectionnez la Digigurdy comme périphérique MIDI d’entrée.

---

## 8. Comment utiliser la sortie MIDI 5‑broches et le MIDI Bluetooth ?

La prise MIDI‑OUT 5 broches envoie le même flux MIDI que l’USB. Vous pouvez y brancher :

- un synthétiseur ou expander matériel,
- un adaptateur MIDI Bluetooth.

Avec un adaptateur Bluetooth et la batterie interne, vous obtenez une solution presque entièrement sans fil.

---

## 9. Pourquoi éviter les écouteurs / casques Bluetooth ?

Les casques Bluetooth introduisent une latence audio perceptible, ce qui rend le jeu peu confortable.

Le MIDI Bluetooth fonctionne bien car il transporte très peu de données, mais l’audio Bluetooth reste trop lent dans la plupart des cas, sauf éventuellement avec certains couples AirPods / appareil Apple.

---

## 10. Qu’est‑ce que BS‑16i et pourquoi est‑il recommandé ?

BS‑16i est une application iOS qui lit des soundfonts (fichiers SF2) et sert de synthétiseur/échantillonneur MIDI :

- peu coûteuse,
- stable,
- compatible avec USB MIDI et MIDI Bluetooth.

Elle est devenue la solution « standard » recommandée pour la Digigurdy sur iPad/iPhone.

---

## 11. Quelles sont les options pour utiliser un PC Windows comme lecteur de sons MIDI ?

Il est possible d’utiliser un PC Windows avec :

- un pilote MIDI,
- un VSTi (synthétiseur virtuel),
- ou un lecteur de soundfont dédié.

Une procédure détaillée est décrite dans le document `midi-on-win` indiqué dans le guide (`./midi-on-win`).

---

## 12. Où trouver les soundfonts de hurdy‑gurdy pour la Digigurdy ?

Les soundfonts dédiées (issues du projet MIDIgurdy) se trouvent dans le répertoire `soundfonts/` du dépôt GitHub du projet.

Vous pouvez les charger dans BS‑16i ou dans n’importe quel lecteur de soundfont compatible.

---

## 13. Quels canaux MIDI la Digigurdy utilise‑t‑elle ?

Par défaut :

1. Mélodie aiguë
2. Mélodie grave
3. Trompette
4. Bourdon
5. Bourdon/coup (buzz)
6. Clic des touches

Votre échantillonneur doit être configuré pour que chaque canal produise le son souhaité.

---

## 14. Comment utiliser les échantillonneurs Tsunami ou Trigger intégrés ?

Si votre Digigurdy est équipée d’un Tsunami ou Trigger :

- elle peut fournir un **signal audio de niveau ligne** directement vers des enceintes amplifiées ou un casque,
- les sons sont stockés sur une carte microSD dans le module.

Vous pouvez jouer même sans appareil externe pour le son, tant que le module audio est configuré et alimenté.

---

## 15. Comment installer les fichiers sur la carte microSD du Tsunami/Trigger ?

1. Retirez la carte microSD du module.
2. Connectez‑la à un PC.
3. Supprimez tous les fichiers présents.
4. Extrayez le ZIP Tsunami/Trigger fourni dans le dépôt.
5. Copiez **le contenu** du dossier `mono` ou `stereo` (pas le dossier lui‑même) à la racine de la carte.
6. Éjectez proprement puis réinsérez la carte dans le module.

---

## 16. À quoi servent les différents boutons de la Digigurdy ?

- **1–6** : sélection dans les menus.
- **X** : retour / annulation dans les menus.
- **A / B** : navigation supplémentaire (menu pause, mise en sourdine, etc.).
- **Tpose Up/Down** : transposition en demi‑tons.
- **Capo** : changement de capo (bourdon/trompette).
- **EX1–EX3** : boutons configurables (mise en sourdine, pause, transposition, etc.).
- **Auto‑crank (Big)** : simule la rotation de la roue (cordes on/off).
- **Potentiomètre de bourdon/coup** : règle la sensibilité du bourdon/coup de trompette.

---

## 17. Quelles sont les combinaisons de touches « cachées » importantes ?

- `X + A` : ouvre le menu pause pendant le jeu.
- `X + B` : fait défiler les options de capo.
- `1 + T-UP/DOWN` : transpose vers le haut/bas.
- `X + T-UP/DOWN` : augmente / diminue le volume global.

---

## 18. Comment fonctionne la détection de la manivelle ?

Au démarrage, les modèles à manivelle à engrenages détectent automatiquement si la manivelle est connectée.

Il est recommandé de ne pas bouger la manivelle pendant ce test.

Si nécessaire, la détection peut être relancée depuis le menu « Autres options » du menu pause (option « Crank Detection »).

---

## 19. Comment choisir, charger et sauvegarder un accordage ?

- **Charger** : dans le menu pause → « Load », vous pouvez choisir :
  - un des 4 accordages prédéfinis (G/C, D/G, etc.),
  - ou un des 4 accordages personnalisés.
- **Sauvegarder** : dans le menu pause → « Save », vous enregistrez :
  - l’accordage,
  - la transposition/capo,
  - le volume par canal,
  dans l’un des 4 emplacements de sauvegarde.

Les états de mise en sourdine ne sont pas sauvegardés avec l’accordage.

---

## 20. Quelle est la différence entre accordage guidé et accordage manuel ?

- **Guidé** : vous sélectionnez une base (G/C ou D/G), puis la Digigurdy propose des choix cohérents pour chaque corde, inspirés des vielles acoustiques.
- **Manuel** : vous choisissez directement la note de chaque corde et du son de bourdon/coup, sans contrainte, pour des configurations totalement personnalisées.

---

## 21. Comment régler le volume de chaque canal ?

Dans le menu Accordage → « Volume », vous pouvez régler le volume MIDI (0–127) de chaque canal :

- 2 canaux de mélodie,
- trompette,
- bourdon,
- bourdon/coup,
- clic des touches.

La valeur par défaut est 70. Ce volume est **en plus** du volume interne de votre sampler (BS‑16i, etc.).

---

## 22. Comment fonctionne le bourdon/coup de trompette ?

Le bourdon/coup se déclenche lorsque la vitesse de rotation de la manivelle dépasse un certain seuil.

Le potentiomètre de bourdon/coup ajuste cette sensibilité :

- tourné à fond dans le sens horaire → sensibilité minimale (bourdon/coup presque désactivé),
- tourné dans l’autre sens → bourdon/coup plus facile à déclencher.

---

## 23. Comment utiliser la transposition (Tpose) et le capo pendant le jeu ?

- **Transposition (Tpose)** : déplace toutes les notes par demi‑tons jusqu’à ±1 octave autour de l’accordage de base.
- **Capo** : déplace la hauteur des bourdons/trompette par sauts de tons entiers (0, +2, +4 demi‑tons, etc.), comme un vrai capo sur une vielle.

Il est également possible d’utiliser les combinaisons de touches `1 + T-UP/DOWN` et `X + B`.

---

## 24. À quoi sert le « menu secret amusant » ?

Depuis le menu Accordage principal, appuyez sur la touche « 6 » (même si aucune option 6 n’est affichée).

Vous pouvez alors ajouter :

- une quarte,
- une quinte,
- ou une octave inférieure

à n’importe quelle corde, créant des doublures (drones, intervalles, etc.).

Ces réglages sont sauvegardés si vous enregistrez un accordage dans un emplacement.

---

## 25. Comment configurer les boutons EX, Tpose, Capo et Auto‑crank ?

Dans le menu « Autres options » → « EX Button Configuration », vous pouvez attribuer à chaque bouton (EX1–EX3, et aussi Tpose/Capo/Big dans les versions 2.4+ et 2.5+) des fonctions telles que :

- ouvrir le menu pause,
- activer/désactiver certaines cordes (mise en sourdine / retour du son),
- augmenter/diminuer le volume,
- transposer vers le haut/bas,
- faire défiler les réglages de capo,
- activer/désactiver l’auto‑crank, etc.

Ces réglages sont persistants et indépendants des emplacements d’accordage.

---

## 26. Quelles options de notation sont disponibles sur l’écran ?

Dans « Screen Configuration », vous pouvez choisir :

- **Scientific/ABC** : C4, D4, etc.
- **Solfege/DoReMi** (do fixe) : Do4, Ré4, etc.
- **Combo** : les deux à la fois, par exemple « C4/DO4 ».

---

## 27. Quels types d’écran de jeu puis‑je afficher pendant que je joue ?

Toujours dans « Screen Configuration », vous pouvez choisir parmi :

- grande note bitmap + portée,
- grande note texte + portée,
- uniquement la note bitmap,
- uniquement la note texte,
- uniquement la portée,
- écran vide.

---

## 28. Comment activer le vibrato MIDI de mélodie et la pédale accessoire ?

Dans « Input/Output Configuration » :

- **MIDI Melody Vibrato** : règle une valeur de modulation constante sur les canaux de mélodie (par exemple 16 pour un léger vibrato dans BS‑16i).
- **Accessory Pedal** : active l’entrée pédale (si le support matériel et logiciel est présent). Elle est **désactivée par défaut à chaque démarrage** pour éviter des effets indésirables lorsqu’aucune pédale n’est branchée.

---

## 29. Que fait l’option « Clear EEPROM » au démarrage ?

« Clear EEPROM » :

- efface tous les emplacements d’accordage sauvegardés,
- réinitialise la configuration des boutons EX,
- remet diverses options persistantes à leurs valeurs par défaut.

Cette option est à utiliser après une mise à jour majeure ou si la configuration semble corrompue et qu’il est nécessaire de repartir d’une base saine.

---

## 30. Comment fonctionne le « Scene Control » avec BS‑16i ?

Le Scene Control permet de synchroniser :

- le choix d’un accordage sur la Digigurdy,
- avec le chargement automatique d’une « scène » BS‑16i.

Principe :

1. Dans BS‑16i, créez une scène (choix d’instruments, effets, volumes, etc.).
2. Dans Settings → Scenes → Assignment, assignez un numéro à chaque scène.
   - 0–3 → accordages prédéfinis de la Digigurdy,
   - 4–7 → emplacements d’accordage sauvegardés.
3. Dans Settings → CoreMIDI, activez « Switch Scenes with Program Change » (Omni ou Channel 1).
4. Dans la Digigurdy, activez « Scene Control » dans le menu de démarrage.

À partir de là, changer d’accordage sur la Digigurdy déclenchera automatiquement le changement de scène correspondant dans BS‑16i.
