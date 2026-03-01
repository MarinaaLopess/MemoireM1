# Reconnaissance d'Entités Nommées (REN) sur un corpus de poèmes (XIXe - XXe)

## 🎓 Contexte du Projet
[cite_start]Ce projet est un mémoire de **Master 1 Sciences du Langage, parcours Langue et Informatique** réalisé à **Sorbonne Université**[cite: 6, 7, 41].

* [cite_start]**Titre du mémoire** : Reconnaissance d'Entités Nommées sur un corpus de poèmes des XIXe et XXe siècles[cite: 8, 9].
* [cite_start]**Auteurs** : Marina CARVALHO LOPES & Ruixing ZHENG[cite: 10].
* [cite_start]**Direction** : Caroline KOUDORO-PARFAIT, Ljudmila PETKOVIC et Gaël LEJEUNE[cite: 11, 12].
* [cite_start]**Année universitaire** : 2024-2025[cite: 13].

## 🎯 Objectifs de la recherche
[cite_start]L'objectif est d'évaluer la pertinence des outils de Traitement Automatique du Langage Naturel (TALN) pour la reconnaissance d'entités nommées dans un contexte littéraire poétique[cite: 19]. [cite_start]L'étude analyse comment des modèles conçus pour des domaines techniques ou contemporains peuvent enrichir les méthodes classiques d'analyse littéraire[cite: 20].

## 🛠️ Outils et Méthodologie
[cite_start]Les expérimentations ont comparé plusieurs modèles de l'état de l'art[cite: 21]:
* [cite_start]**spaCy (sm & lg)** : Modèles rapides utilisés comme référence pour la tokenisation et la REN[cite: 84, 161, 191].
* [cite_start]**Stanza** : Boîte à outils neuronale de Stanford utilisant un modèle francophone intégré[cite: 238, 240, 246].
* [cite_start]**CamemBERT** : Modèle basé sur RoBERTa, utilisant la version fine-tunée `Jean-Baptiste/camembert-ner`[cite: 223, 233].
* [cite_start]**FlauBERT** : Utilisé pour la tokenisation et combiné avec CamemBERT pour la REN[cite: 21, 544].

## 📂 Corpus
[cite_start]Le corpus est constitué de 10 œuvres numérisées provenant de **Gallica (BnF)**[cite: 139]:
* [cite_start]**XIXe siècle** : Hugo, Desbordes-Valmore, D'Arbouville, Verlaine, Rimbaud, Vivien[cite: 140, 183].
* [cite_start]**XXe siècle** : Apollinaire, Noailles, Loiseau, Sauvage[cite: 140, 183].
* [cite_start]**Contraintes** : Les textes comportent du bruit généré par l'OCR avec des taux variant de 77,85% à 99,96%[cite: 168, 183].

## 📊 Résultats clés
* [cite_start]**Performance** : Les modèles spaCy sont les plus rapides (env. 70s), tandis que CamemBERT est le plus lent (1772,7s)[cite: 279, 283, 285].
* [cite_start]**Intersection** : 27,6% des entités (7 100) sont reconnues par les quatre modèles simultanément, indiquant une forte fiabilité[cite: 371, 387].
* [cite_start]**Hapax** : Les mots uniques (62,43% du corpus) constituent un défi majeur pour les outils de REN[cite: 24, 450, 540].
* [cite_start]**Transition thématique** : L'analyse montre un passage d'une poésie marquée par l'**orientalisme** au XIXe siècle à une prédominance de la **ruralité** au XXe siècle[cite: 513, 514, 515].

## 📁 Structure du dépôt
* [cite_start]`Corpus/` : Textes bruts (.txt) issus de l'OCR de Gallica[cite: 172, 173].
* [cite_start]`scripts/` : Notebooks Python pour le traitement, l'annotation et les graphiques[cite: 175, 532].
* [cite_start]`output/` : Résultats des extractions d'entités au format JSON[cite: 533].
* `Latex/` : Sources du mémoire et de la documentation associée.
* `zipf.ipynb` : Analyse statistique de la distribution des mots du corpus.

## 🚀 Perspectives
[cite_start]Le travail propose d'entraîner spécifiquement FlauBERT sur des corpus poétiques annotés [cite: 25, 548] [cite_start]et de créer une "vérité de terrain" (gold standard) pour évaluer les performances via la F-mesure[cite: 25, 551].
