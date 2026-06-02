<div align="center">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/Terminal-4D4D4D?style=for-the-badge&logo=windows-terminal&logoColor=white" alt="Terminal" />
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" alt="Status" />

  <h1>🤖 Chatbot Java — SAE S1-01</h1>
  <p>
    <i>Chatbot de culture générale en Java capable de répondre en langage naturel, d'apprendre de nouvelles connaissances et de maintenir un contexte conversationnel.</i>
  </p>
</div>

<br />

## 📖 Table des matières
- [À propos du projet](#-à-propos-du-projet)
- [Fonctionnalités](#-fonctionnalités)
- [Objectifs et Compétences](#-objectifs-et-compétences)
- [Architecture du projet](#-architecture-du-projet)
- [Prérequis et Utilisation](#-prérequis-et-utilisation)
- [Cadre du Projet (PPP)](#-cadre-du-projet-ppp)

---

## 🚀 À propos du projet

Ce projet est un chatbot de culture générale développé en Java. Il répond à des questions en langage naturel en s'appuyant sur une base de données de questions-réponses stockée dans des fichiers texte (environ 500 entrées).

Pour améliorer la pertinence de ses réponses, il filtre les mots-outils (articles, prépositions…) afin de se concentrer sur le sens, et utilise un thésaurus pour rapprocher les synonymes. Il gère également le contexte conversationnel : une question composée uniquement de mots-outils est interprétée en lien avec la question précédente. Enfin, lorsqu'il ne connaît pas une réponse, il peut l'apprendre directement depuis la conversation et la sauvegarder.

---

## ✨ Fonctionnalités

- **Réponses en langage naturel** : Analyse la question pour en extraire les mots-clés pertinents.
- **Gestion du thésaurus** : Rapproche les synonymes pour mieux comprendre les questions de l'utilisateur.
- **Filtrage des mots-outils** : Ignore les articles et prépositions pour se concentrer sur les termes importants.
- **Mémoire contextuelle** : Si une question ne contient que des mots-outils, elle est interprétée par rapport à la question précédente.
- **Apprentissage à la volée (Dynamique)** : Si le chatbot ne connaît pas une réponse, il la demande et la sauvegarde automatiquement.
- **Variété des formulations** : Sélection aléatoire parmi plusieurs réponses candidates.

---

## 🎯 Objectifs et Compétences

### Objectifs du projet
Le projet visait à mettre en œuvre les concepts d'algorithmique et de développement Java pour créer un outil interactif en langage naturel capable de rechercher efficacement des informations, d'analyser du texte, et de s'auto-alimenter en données.

### Compétences, Techniques et Savoir-faire Acquis
- **Java et POO (Programmation Orientée Objet)** : Structuration du code et séparation des responsabilités.
- **Algorithmique et Traitement de texte** : Implémentation d'un système de recherche via un index inversé.
- **Gestion de fichiers** : Lecture, écriture et manipulation dynamique de bases de données textuelles (fichiers `.txt`).
- **Mémoire Contextuelle** : Mise en place de logiques permettant au programme de se "souvenir" de l'état précédent.
- **Apprentissage Dynamique** : Capacité à faire évoluer les fichiers de données du programme à l'exécution.

---

## 🏗️ Architecture du projet

```text
ProjetChatbot/
├── src/
│   ├── Chatbot.java          # Point d'entrée : boucle principale et logique conversationnelle
│   ├── Utilitaire.java       # Lecture des fichiers, construction des index, algorithmes de recherche
│   ├── Index.java            # Structure d'index inversé pour la recherche rapide
│   └── Thesaurus.java        # Gestion des synonymes
├── reponses.txt              # Base de données des réponses (~500 entrées)
├── questions-reponses.txt    # Association questions ↔ réponses idéales
├── mots-outils.txt           # Liste des mots à ignorer (à, de, le, est…)
└── thesaurus.txt             # Fichier de synonymes et concepts similaires
```

---

## 💬 Prérequis et Utilisation

### Prérequis
- **Java JDK 11** (ou supérieur).
- Un IDE Java (IntelliJ IDEA recommandé, le projet inclut le fichier `.iml`).

### Exemple d'interaction
```text
> J'attends tes questions de culture générale.
> Quelle est la capitale de la France ?
> La capitale de la France est Paris.

> Quel est son monument le plus célèbre ?
> La Tour Eiffel est le monument le plus emblématique de Paris.

> Au revoir.
> Au revoir.
```

**Si le chatbot ne connaît pas la réponse :**
```text
> Qui a inventé le vélo ?
> Je ne sais pas.
> Je vais te l'apprendre.
> Je t'écoute.
[Baron Karl von Drais en 1817]
> Très bien, c'est noté.
```

---

## 🎓 Cadre du Projet

Projet réalisé dans le cadre de la **SAE S1-01** (BUT Informatique 1ère année, IUT2 Grenoble).

- **Travail en groupe** : Ce projet a été réalisé en binôme (**équipe de 2 personnes**).
- **Travail individuel dans le groupe** : Au sein de l'équipe, je me suis spécifiquement occupé de :
  - **La gestion et le filtrage des mots-outils** entrés par l'utilisateur, afin d'optimiser la compréhension du chatbot.
  - **L'implémentation et la gestion du thésaurus** (`Thesaurus.java` / `thesaurus.txt`), permettant l'association des synonymes pour une meilleure analyse des requêtes.
