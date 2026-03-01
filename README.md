Voici le contenu du fichier README.md au format text brut, rédigé en français et respectant scrupuleusement les informations de votre mémoire.

Reconnaissance d'Entités Nommées (REN) sur un corpus de poèmes (XIXe - XXe)
🎓 Contexte du Projet
Ce projet est un mémoire de Master 1 Sciences du Langage, parcours Langue et Informatique réalisé à Sorbonne Université.
+1


Titre du mémoire : Reconnaissance d'Entités Nommées sur un corpus de poèmes des XIXe et XXe siècles.


Auteurs : Marina CARVALHO LOPES & Ruixing ZHENG.


Direction : Caroline KOUDORO-PARFAIT, Ljudmila PETKOVIC et Gaël LEJEUNE.


Année universitaire : 2024-2025.

🎯 Objectifs de la recherche
L'objectif est d'évaluer la pertinence des outils de Traitement Automatique du Langage Naturel (TALN) pour la reconnaissance d'entités nommées dans un contexte littéraire poétique. L'étude analyse comment des modèles conçus pour des domaines contemporains peuvent enrichir les méthodes classiques d'analyse littéraire.
+1

🛠️ Outils et Méthodologie
Les expérimentations ont comparé plusieurs modèles de l'état de l'art:
+1


spaCy (sm & lg) : Modèles rapides utilisés comme référence pour la tokenisation et la REN.
+2


Stanza : Boîte à outils neuronale de Stanford utilisée pour son modèle francophone.
+2


CamemBERT : Modèle basé sur RoBERTa, utilisant la version fine-tunée Jean-Baptiste/camembert-ner.
+1


FlauBERT : Utilisé pour la tokenisation et combiné avec CamemBERT pour la REN.
+1

📂 Corpus
Le corpus est constitué de 10 œuvres numérisées provenant de Gallica (BnF):
+1


XIXe siècle : Hugo, Desbordes-Valmore, D'Arbouville, Verlaine, Rimbaud, Vivien.


XXe siècle : Apollinaire, Noailles, Loiseau, Sauvage.


Contraintes : Les textes comportent du bruit généré par la reconnaissance optique de caractères (OCR) avec des taux variant de 77% à 99%.
+2

📊 Résultats clés

Performance : spaCy (sm) et (lg) sont les plus rapides (environ 70s), tandis que CamemBERT est le plus lent (1772s) et le plus conservateur.
+2


Intersection : 27,6% des entités sont reconnues par les quatre modèles simultanément, ce qui suggère une forte fiabilité pour ces segments.


Hapax : Les mots uniques (62,43% du corpus) constituent un défi majeur pour les outils de REN.
+2


Transition thématique : L'analyse quantitative montre un passage d'une poésie marquée par l'orientalisme au XIXe siècle à une prédominance de la ruralité au XXe siècle.

📁 Structure du dépôt

Corpus/ : Textes bruts (.txt) issus de l'OCR de Gallica.


scripts/ : Notebooks Python (.ipynb) pour le traitement, l'annotation et les graphiques.


output/ : Résultats des extractions d'entités au format JSON.

Latex/ : Sources du mémoire et de la documentation associée.

zipf.ipynb : Analyse statistique de la distribution des mots du corpus.

🚀 Perspectives
Le travail propose d'entraîner spécifiquement FlauBERT sur des corpus poétiques annotés et de créer une "vérité de terrain" (gold standard) pour évaluer les performances via la F-mesure.
