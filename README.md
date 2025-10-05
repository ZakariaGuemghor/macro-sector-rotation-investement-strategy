![Image de couverture du projet](images/image_couverture.png)

# Impact des Régimes Macroéconomiques sur les Rendements des Différents Secteurs Économiques

## Introduction

La performance des différents secteurs de l'économie est liée au cycle économique global. Comprendre comment chaque secteur réagit aux divers régimes macroéconomiques tels que l'expansion, la récession, l'inflation ou les changements de politique monétaire est fondamental pour une allocation d'actifs tactique efficace. Les investisseurs cherchant à surperformer le marché doivent être capables d'identifier les secteurs les plus susceptibles de prospérer dans l'environnement économique anticipé.

Ce projet propose une étude empirique visant à quantifier la relation entre différents régimes macroéconomiques et les rendements des principaux secteurs de l'économie américaine. L'objectif est de fournir un cadre d'analyse clair qui peut servir d'outil d'aide à la décision pour les stratégies d'investissement, en mettant en évidence les secteurs qui ont historiquement bénéficié ou souffert sous des conditions économiques spécifiques.

**➡️ [Voir le Notebook : `macro_sector_rotation_analysis.ipynb`](./macro_sector_rotation_analysis.ipynb)**

---

## Objectif du Projet

L'objectif principal de ce projet est de mener une **étude empirique sur l'impact des régimes macroéconomiques sur les rendements des différents secteurs économiques**. Il ne s'agit pas de prédire le futur, mais d'analyser le passé pour identifier des tendances et des corrélations robustes qui peuvent guider les décisions d'allocation tactique.

Nous cherchons à répondre à la question suivante : **Quels secteurs performent le mieux (ou le moins bien) dans des environnements économiques distincts, définis par la croissance du PIB, l'inflation et la politique des taux d'intérêt ?** L'ambition est de transformer des données macroéconomiques complexes en une grille de lecture simple et exploitable pour les investisseurs.

---

## Structure du Projet et Méthodologie

Pour atteindre cet objectif, une méthodologie structurée a été élaborée, organisée en trois étapes principales formant une chaîne d'analyse logique.

#### 1. Collecte et Préparation des Données
La première étape consiste à construire une base de données historique cohérente à une fréquence trimestrielle. Cela inclut :
-   **Données Macroéconomiques :** Téléchargement des séries temporelles pour la croissance du PIB réel (`GDPC1`), l'inflation (`CPIAUCNS`) et les taux d'intérêt directeurs (`FEDFUNDS`).
-   **Données Sectorielles :** Téléchargement des indicateurs de performance historiques pour les principaux secteurs économiques (Production Manufacturière, Ventes au Détail, etc.).
-   **Transformation et Synchronisation :** Toutes les données sont agrégées à une fréquence trimestrielle. Les taux de croissance sont calculés pour chaque variable afin de mesurer leur dynamique.

#### 2. Identification des Régimes Macroéconomiques
La deuxième étape est consacrée à la classification de chaque trimestre de la période d'analyse dans un régime macroéconomique spécifique. Cette classification est basée sur un ensemble de règles empiriques appliquées à la dynamique des trois indicateurs clés :
-   **Régime de Croissance :** Basé sur l'accélération ou le ralentissement du taux de croissance du PIB (Expansion, Ralentissement, Récession, Reprise).
-   **Régime d'Inflation :** Basé sur le niveau et la direction du taux de croissance de l'inflation (Désinflation, Inflation Modérée, Inflation Élevée, etc.).
-   **Régime de Politique Monétaire :** Basé sur la direction du taux de croissance des taux d'intérêt (Hausse, Baisse, Maintien).

En combinant ces trois dimensions, nous obtenons une mosaïque de régimes macroéconomiques composites (par exemple, "Expansion économique avec maintien des taux et inflation modérée").

#### 3. Analyse de Corrélation et Interprétation
La dernière étape vise à quantifier la performance des secteurs au sein de chaque régime identifié.
-   **Calcul des Corrélations :** Une analyse de corrélation est menée pour mesurer la relation entre l'occurrence d'un régime macroéconomique spécifique et la performance (taux de croissance) de chaque secteur.
-   **Visualisation et Classement :** Les résultats sont présentés sous forme de graphiques en barres, classant les secteurs du plus positivement corrélé au plus négativement corrélé pour chaque régime.
-   **Synthèse :** Ces visualisations permettent d'identifier rapidement quels secteurs ont tendance à surperformer ou à sous-performer dans un contexte économique donné, fournissant ainsi des informations précieuses pour une allocation d'actifs tactique.