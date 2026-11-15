# 🎲 Entre Nous — mini-jeux à plusieurs

Site de mini-jeux à jouer entre amis, chacun sur son téléphone. L'hôte crée une partie, partage le lien + code, et tout le monde joue en temps réel.

## Jeux
- 🎯 **La demi-roue** (façon « Longueur d'onde ») — un indice, une aiguille, une cible cachée entre deux extrêmes
- 💞 **Qui de nous deux ?** — version couple, 178 questions en 4 thèmes
- 🧠 **Même réponse** — « Quel est mon plat préféré ? » / « Quel est son plat préféré ? »
- ⚖️ **Tu préfères ?**
- 👑 **Qui est le plus susceptible de… ?**
- 🕵️ **L'Imposteur** (Undercover / Mister White)
- 🧩 **Quiz** — QCM chronométré, bonus au plus rapide
- ✅ **Vrai ou Faux** — avec l'explication à chaque réponse
- 💯 **C'est un 10 mais…** — une note parfaite, un défaut qui gâche tout : chacun redonne sa note de 0 à 10
- 🔑 **Mot de passe** — chacun son tour fait deviner sa série de mots (1re lettre donnée), un seul mot par indice, 5 → 1 pt
- 🔍 **Qui suis-je ?** — indices progressifs, moins d'indices = plus de points

Chaque jeu propose des catégories au choix : 🎲 Général, 🚂 Honkai: Star Rail, ⚔️ Genshin Impact, 🍙 Manga / Animé, 🎵 Musique, ⚽ Sport, 🎤 Rap FR (plus de 3 700 questions au total, thème affiché en haut de chaque question).

## Parties
L'hôte choisit le nombre de manches (5, 10, 15, 20, 30 ou illimité) et les catégories. À la fin : podium, classement de la partie et total de la soirée, puis « Rejouer » ou « Changer de jeu ». Le menu ☰ permet de terminer une partie à tout moment.

## Avatars
Chaque joueur choisit son avatar parmi 12 images intégrées à la page.

## Technique
Une seule page HTML statique (GitHub Pages). La synchro temps réel passe par un relais MQTT public (broker.emqx.io, avec HiveMQ et Mosquitto en secours) : aucun compte ni serveur à gérer. Les messages d'une partie sont visibles de quiconque connaît le code — c'est fait pour des jeux entre amis, n'y mettez rien de confidentiel.
