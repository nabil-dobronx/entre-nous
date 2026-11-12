# 🎲 Entre Nous — mini-jeux à plusieurs

Site de mini-jeux à jouer entre amis, chacun sur son téléphone. L'hôte crée une partie, partage le lien + code, et tout le monde joue en temps réel.

## Jeux
- 🎯 **La demi-roue** (façon « Longueur d'onde ») — un indice, une aiguille, une cible cachée entre deux extrêmes
- 💞 **Qui de nous deux ?** — version couple, 178 questions en 4 thèmes
- 🧠 **Même réponse** — « Quel est mon plat préféré ? » / « Quel est son plat préféré ? »
- ⚖️ **Tu préfères ?**
- 👑 **Qui est le plus susceptible de… ?**
- 🕵️ **L'Imposteur** (Undercover / Mister White)

## Avatars
Chaque joueur choisit un emoji ou met sa propre photo (recadrée et compressée automatiquement).

## Technique
Une seule page HTML statique (GitHub Pages). La synchro temps réel passe par un relais MQTT public (broker.emqx.io, avec HiveMQ et Mosquitto en secours) : aucun compte ni serveur à gérer. Les messages d'une partie sont visibles de quiconque connaît le code — c'est fait pour des jeux entre amis, n'y mettez rien de confidentiel.
