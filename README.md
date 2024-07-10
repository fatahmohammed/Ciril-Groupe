# 🌱 Ciril-Group-Simulation-Feu-En-Foret 🌱
# 👋 FATAH Mohammed 👋
# Simulation de propagation de feu

Ce projet simule la propagation du feu dans une image Sat en utilisant un modèle probabiliste Rendomiser et condition Climatique.

![Description de la vidéo](https://github.com/fatahmohammed/Ciril-Groupe/blob/main/Applicatin%20Vid%C3%A9o.png)
# [Regarder la vidéo](https://www.youtube.com/watch?v=lr0V1TrIKwA)

![Description de la vidéo](https://github.com/fatahmohammed/Ciril-Groupe/blob/main/Code%20vid%C3%A9o.png)
# [Regarder la vidéo](https://www.youtube.com/watch?v=4ObO7wQ9HJw)

## Algorithme

L'algorithme suit les étapes suivantes :

1. **Initialisation** :
    - Créer une grille de taille définie où chaque case est initialement un ARBRE.
    - Définir la probabilité `p` de propagation du feu à une case adjacente.
    - Placer quelques cases initiales en état EN_FEU pour démarrer la simulation.

2. **Simulation** :
    - Pour chaque tour de simulation :
        - Identifier Si les positions des cases actuellement en feu `(x, y)`.
        - Pour chaque case `(X, Y)` en feu :
            - Passer l'état de la case à `CENDRE`.
            - Récupérer les positions adjacentes `ADJX, ADJY` des 4 cases voisines (haut, bas, gauche, droite).
            - Pour chaque case adjacente `(ADJX, ADJY)` :
                - Si `(ADJX, ADJY)` est une position valide dans la grille et que la case `[ADJX, ADJY]` est un `ARBRE` et que `Class A ou Class B < p` (où `A  ou B` est un nombre aléatoire ou Conditioner pour le principe de simulation ) :
                    - Passer l'état de la case adjacente à `EN_FEU`.
                - Fin Si
            - Fin Pour
        - Fin Pour
    - Fin Si
- Fin

# Présentation du projet 


## ⚡ Structure du Projet

Dans ce projet, j'ai structuré l'organisation de manière efficace. Voici la structure du projet :

- **`src/main/java/ `** Contient tout le code source du projet ainsi que les ressources nécessaires.
- **`com/fatah/simulationfeuenforet/`**  Paquetage principal du projet.
- **`frame/`**  Contient la classe relatives à l'interface utilisateur `JFrame`.
- **`grille/`**  Contient les classes de gestion de la grille de simulation et une interface extensible pour chaque idé a l'avenir sans toucher le code initiale .
- **`image/`**  Contient la classe pour enregistrer un état de simulation.
- **`simulation/`**  Contient la classe de la simulation de propagation de feu sur la grille en shousissant la stratigie avec la quelle je lance la simulation.
- **`ZoneDetection et PointParCercle/`** sont deux classes, l'une pour la détection des zones sur l'image et l'autre pour entourer les points sélectionnés sur l'image.
## ⚡ Prérequis

- Avant de commencer, assurez-vous d'avoir Java JDK 17 ou + installé sur votre système.
- Maven installé
- Configuration OpenCV pour ``opencv-4100.jar`` dans le project Structure --> Module --> dependencies : ajouter le jar. Et ``opencv_java4100.dll`` copie ce fichier .dll dans le repertoire C: 
- ## ⚡ Configuration

Avant d'exécuter les tests, assurez-vous de recharger Maven pour télécharger les dépendances nécessaires en exécutant la
commande suivante :

## ⚡ Installation

1. Clonez ce dépôt sur votre machine locale.
2. Importez le projet dans votre environnement de développement Java préféré IntelliJ IDEA.
3. Configurez les dépendances nécessaires .
4. Exécutez. `MainImageSat` .

