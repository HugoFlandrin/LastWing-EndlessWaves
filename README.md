# 🚀 Last Wing: Endless Waves

**Un shoot'em up vertical qui ne vous laisse jamais souffler.** Les vagues d'ennemis ne s'arrêtent pas, elles s'intensifient : à vous de tenir, de ramasser les bons bonus au bon moment et de battre votre propre record.

Jouable **directement dans le navigateur**, sur ordinateur comme sur mobile. Pas d'installation, pas de compte : une partie commence en quelques secondes.

<p align="center">
  <a href="https://hugoflandrin.github.io/LastWing-EndlessWaves">
    <img src="docs/media/lastwing-banner.png" alt="Last Wing: Endless Waves" width="360">
  </a>
</p>

<p align="center">
  <a href="https://hugoflandrin.github.io/LastWing-EndlessWaves"><b>▶ Jouer à Last Wing dans le navigateur</b></a>
</p>

---

## Pourquoi vous allez y rester

- **Une difficulté qui monte sans plafond brutal.** Chaque partie suit une courbe d'intensité unique : elle règle en même temps le rythme des vagues, la solidité des ennemis, la vitesse de défilement, la fréquence des bonus et même le tempo de la musique, qui accélère légèrement au fil de la partie. Vous *sentez* la pression monter.
- **Dix types d'ennemis qui obligent à changer de tactique** : classiques, rapides, blindés, tireurs, plongeurs, ennemis qui se divisent en fragments, qui zigzaguent, tireurs d'élite, tirs en éventail.
- **Des ennemis d'élite**, reconnaissables à leur aura dorée : plus coriaces, plus rentables, et ils lâchent toujours un bonus de qualité.
- **Onze bonus à enchaîner** : cadence de tir, tir multiple, double tir, bouclier, soin, aimant à pièces, ralenti, bombe (une onde de choc qui balaie ennemis et projectiles), dégâts accrus, drone allié et multiplicateur de score. Les drops ne sont pas purement aléatoires : un système de garanties évite les longues séries de malchance.
- **Trois niveaux de difficulté** (Facile, Moyen, Difficile) pour les parties sans fin.
- **Trois modes** : partie solo sans fin (par défaut), coopération à deux joueurs sur le même clavier (PC uniquement), et une partie chronométrée pour un défi court.
- **Un cycle jour et nuit**, de la musique d'ambiance, des effets sonores soignés et un réglage du son accessible en un clic.
- **Un jeu qui respecte votre onglet** : si vous changez de page, tout se met en pause (jeu, musique, effets) et reprend exactement là où vous étiez.

## 🎬 Démo

https://github.com/user-attachments/assets/259d577b-21b6-42ae-bc3f-2ba4540d8e6b

## Le moteur

Last Wing ne repose pas sur un moteur du commerce : il tourne sur un **moteur 2D écrit sur mesure en C++**, qui produit aussi bien une version navigateur qu'une version Windows ou Android à partir d'un même code.

L'architecture, les choix techniques et leurs raisons sont présentés dans un dépôt dédié : **[HugoFlandrin/2D-Game-Engine](https://github.com/HugoFlandrin/2D-Game-Engine)**.

---

## Histoire du jeu

Last Wing est né d'un [moteur 2D écrit sur mesure](https://github.com/HugoFlandrin/2D-Game-Engine). Un platformer inspiré de Mario a servi à valider ses briques de base : physique, collisions, scènes, audio, interface. D'abord nommé Space Shooter, le shoot'em up avait pour objectif initial de servir de miroir au platformer : deux démos moteurs, l'une sur PC, l'autre sur mobile. Au fil de son développement, je me suis pris d'affection pour Space Shooter, qui a fini par devenir un véritable jeu, jusqu'à remplacer le platformer sur PC. Plus tard renommé Last Wing: Endless Waves, j'ambitionne de faire de ce jeu une application mobile gratuite, disponible sur tous les appareils Android (puis iOS dans un second temps).

La version web, publiée en bêta, a été jouée et commentée par des testeurs. Leurs retours ont dicté un long chantier d'équilibrage :

- un **choix de difficulté** avant la partie ;
- une **difficulté qui monte progressivement** plutôt que de plafonner ;
- des **ennemis d'élite** et de **nouveaux ennemis** pour varier le jeu ;
- des **bonus plus lisibles** et plus utiles (bombe, drone, multiplicateur de score, ralenti) ;
- une **sensation de progression** : défilement plus rapide, musique qui accélère, cycle jour et nuit.

Dans un second temps, le moteur a été **étendu pour devenir multi-plateforme** : le jeu, qui tournait sur Windows et sur le Web, produit désormais aussi une build **Android**, signée et validée sur un vrai téléphone.

<!-- HISTOIRE PERSONNELLE : ajouter ici, si souhaité, quelques lignes sur l'idée de départ, l'envie de faire ce jeu et le parcours qui y a mené. -->

---

## Et ensuite ?

- **Android** : la build existe et tourne à 60 images par seconde sur téléphone. Reste à la publier sur les boutiques d'applications.
- **iOS** : le moteur est conçu pour l'accueillir, il reste à le porter et à valider le jeu sur appareil.
- **Nouveau mode de jeu** avec des **mini-boss**, volontairement mis de côté jusqu'ici pour ne pas alourdir le mode sans fin.

---

## Contenu de ce dépôt

Uniquement la build web compilée, sans aucun code source :

- `index.html` : la page qui héberge le jeu
- `index.js`, `index.wasm`, `index.data` : le jeu (WebAssembly), son code d'amorçage et ses ressources
- `coi-serviceworker.js` : un petit fichier qui supprime un ancien service worker que certains joueurs peuvent encore avoir d'une version de test. Il ne fait rien d'autre et doit rester en place.

---

## Crédits

- Conception et développement : Hugo Flandrin
- Musique : *Sweet 70s* de Clement Panchout
- Police : Kenney Pixel (Kenney)

---

## Licence

**Copyright © 2026 Hugo Flandrin. Tous droits réservés.**

Last Wing: Endless Waves est un jeu propriétaire. Ce dépôt ne publie que sa version jouable dans le navigateur.

- Vous pouvez **jouer** au jeu en ligne et le **partager par un lien** vers sa page.
- Sauf autorisation écrite de l'auteur, il est **interdit** de copier, redistribuer ou héberger ailleurs les fichiers de ce dépôt, de les modifier, d'en extraire les ressources (images, sons, polices), ou de les décompiler, désassembler ou en faire de l'ingénierie inverse.
- Le code source du jeu et de son moteur n'est pas publié et n'est couvert par aucune licence ouverte.

**Composants tiers.** Le jeu s'appuie sur des bibliothèques et des ressources libres ou tierces, dont VRSFML et SDL3 (le rendu et le fenêtrage), Box2D (la physique), miniaudio (l'audio) et FreeType (les polices). Chacune reste soumise à sa propre licence, qui s'applique à elle seule et non à l'ensemble du jeu. La musique *Sweet 70s* reste la propriété de son auteur, Clement Panchout. La police Kenney Pixel reste soumise à la licence de son auteur.
