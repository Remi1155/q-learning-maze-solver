# q-learning-maze-solver

Ce projet implémente un algorithme de **Q-Learning** pour entraîner un agent intelligent à naviguer dans un labyrinthe. L'objectif de l'agent est de trouver le chemin le plus efficace entre un point de départ et un objectif, tout en évitant les obstacles (murs).

## Fonctionnalités

* **Création du labyrinthe:** Le code définit un environnement de labyrinthe avec des obstacles et une destination finale.
* **Table Q:** Une matrice est utilisée pour stocker les valeurs Q, qui représentent la "qualité" d'une action dans un état donné.
* **Apprentissage par renforcement:** L'agent utilise une stratégie **epsilon-greedy** pour explorer le labyrinthe tout en exploitant les connaissances acquises.
* **Visualisation:** Le projet inclut des visualisations pour afficher le labyrinthe, les récompenses associées et le chemin optimal trouvé par l'agent après l'apprentissage.

## Comment ça marche

L'agent se déplace de manière itérative dans le labyrinthe. À chaque étape :
1.  Il observe son **état** (sa position actuelle).
2.  Il choisit une **action** (`haut`, `bas`, `gauche`, `droite`) basée sur la table Q.
3.  Il effectue l'action, passe à l'**état suivant**, et reçoit une **récompense** (positive ou nulle pour l'objectif, négative pour un mur).
4.  Il met à jour la valeur Q de son état et action en utilisant l'équation de Bellman.

Ce processus est répété sur de nombreux épisodes, ce qui permet à la table Q de converger vers les valeurs optimales, représentant le meilleur chemin.
