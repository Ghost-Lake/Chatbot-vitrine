# 🤖 Chatbot Java — SAE S1-01

> Chatbot de culture générale en Java capable de répondre en langage naturel, d'apprendre de nouvelles connaissances et de maintenir un contexte conversationnel.

---

## ✨ Fonctionnalités

- **Réponses en langage naturel** — analyse la question pour en extraire les mots-clés pertinents
- **Gestion du thésaurus** — rapproche les synonymes pour mieux comprendre les questions
- **Filtrage des mots-outils** — ignore les articles et prépositions pour se concentrer sur le sens
- **Mémoire contextuelle** — si une question ne contient que des mots-outils, elle est interprétée par rapport à la question précédente
- **Apprentissage à la volée** — si le chatbot ne connaît pas une réponse, il la demande et la sauvegarde automatiquement
- **Variété des formulations** — sélection aléatoire parmi plusieurs réponses candidates

---

## 🏗️ Architecture du projet

```
ProjetChatbot/
├── src/
│   ├── Chatbot.java          # Point d'entrée — boucle principale et logique conversationnelle
│   ├── Utilitaire.java       # Lecture des fichiers, construction des index, algorithmes de recherche
│   ├── Index.java            # Structure d'index inversé pour la recherche rapide
│   └── Thesaurus.java        # Gestion des synonymes
├── reponses.txt              # Base de données des réponses (~500 entrées)
├── questions-reponses.txt    # Association questions ↔ réponses idéales
├── mots-outils.txt           # Liste des mots à ignorer (à, de, le, est…)
└── thesaurus.txt             # Fichier de synonymes
```

---

## 🔧 Prérequis

- **Java JDK 11+**
- Un IDE Java (IntelliJ IDEA recommandé, le projet inclut le fichier `.iml`)

---

## 💬 Exemple d'utilisation

```
> J'attends tes questions de culture générale.
> Quelle est la capitale de la France ?
> La capitale de la France est Paris.

> Quel est son monument le plus célèbre ?
> La Tour Eiffel est le monument le plus emblématique de Paris.

> Au revoir.
> Au revoir.
```

Si le chatbot ne connaît pas la réponse :

```
> Qui a inventé le vélo ?
> Je ne sais pas.
> Je vais te l'apprendre.
> Je t'écoute.
[Baron Karl von Drais en 1817]
> Très bien, c'est noté.
```

---

## 👤 Auteur

Projet réalisé dans le cadre de la **SAE S1-01** — BUT Informatique 1ère année, IUT2 Grenoble.
