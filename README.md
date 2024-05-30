# Classification d'Images de LEGO

## Table des matières
- [Description](#description)
- [Sujet](#sujet)
- [Objectifs](#objectif)
- [Sources](#sources)
- [Workflow](#workflow)
- [Hardware](#hardware)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Equipe](#equipe)
- [Remerciements](#remerciements)
- [Technologies](#technologies)

## Description
Bienvenue sur le dépôt GitHub de notre projet de groupe réalisé pendant notre formation en Data Analyse avec la Wild code School. Ce projet a été mené dans le cadre de notre cursus. Une des contarinte de ce projet était le temps limité à une trentaine d'heure.

## Sujet
Choisir un thème autour de la data (BI, ML, analyse, etc.), trouver un jeu de données approprié et réaliser un projet sur ce thème.

Nous avons choisi de travailler sur la classification d'images, avec un focus sur des images de LEGO. Le jeu de données que nous avons utilisé était composé de 40 000 images au format PNG, réparties en 16 catégories correspondant à 16 pièces de LEGO différentes. Nous avons finalement réalisé notre projet sur 7 classes différentes avec 800 images par classe soit 5600 images.

## Objectif
Entrainer un modèle de deep learning en utilisant Keras. Le but final était de permettre au système de classifier correctement une photo de LEGO en fonction de la catégorie correspondante.

## Sources
Jeu de donnée complet : https://www.kaggle.com/datasets/joosthazelzet/lego-brick-images/code  
[Jeu de données utilisé]() : [3001](), [3003](), [3004](), [3005](), [3010](), [3022](), [3037]()

## Workflow
1. Préparation des données  
1.1. Collecte des images de différentes pièces de LEGO  
1.2. Organisation des images en dossiers selon les classes  
1.3. Division des données en ensembles d'entraînement, de validation et de test  
1.4. Création d'un jeu de données de test à l'aide d'images 3D (3 à 4 images par pièce)

2. Préparation du modèle  
2.1. Chargement du modèle pré-entraîné  
2.2. Freeze des couches du modèle pré-entraîné  
2.3. Décision à tester : garder ou non certaines couches gelées  
2.4. Construction et Compilation du modèle personnalisé avec essai et choix des paramètres (nombre de neurones personnalisés, fonction d'activation, optimizer, fonction perte, nombre d'epochs, Taille des batchs)  
2.5. Évaluation du modèle  
2.6. Enregistrement du modèle

3. Préparation du notebook pour utilisation du modèle

## Hardware
La configuration du hardware pour l'entrainement des modèles était la suivante : 
- GPU : NVIDIA GeForce RTX 3060
- Processeur : Intel Core i7-14700KF
- RAM : 64 Go DDR5
- Stockage : SSD 1 To
- Système exploitation : Windows 11 (non optimale pour l'utilisation des bibliothèques)

## Installation
0. Prérequis d'installation
    
    ![python](img_readme/python-color.svg) Python <= 3.9
    
1. Clonez le dépôt:
    ```sh
    git clone https://github.com/Dim2960/lego_classification.git
    ```
2. Allez dans le répertoire du projet:
    ```sh
    cd lego_classification
    ```
3. Installez les dépendances:
    ```sh
    pip install -r requirements.txt
    ```

## Utilisation
Deux notebook sont à disposition . Ces notebook nous ont permis d'entrainer deux modele différents (VGG16 et EfficientNetB0) pour comparer les temps d'apprentissage, ainsi que la pertinence des résultats.
Les paramètres des modèles sont ajustables dans un des champs des notebook.
Un troisième notebook permet de tester le modèle. En donnant le chemin de l'image le modele classe la photo dans les différentes catégorie par probabilité.

## Equipe


| [DenToms](https://github.com/DenToms)  
| [Kelmain](https://github.com/Kelmain)  
| [Dim2960](https://github.com/Dim2960)

## Remerciements

- Merci à [Romain Lejeune](https://github.com/Vaelastraszz) pour l'aide apportée durant ce projet.

## Technologies
| Languages | Librairies python | Outils |
|-----------|------------------|--------|
| ![python](img_readme/python-color.svg) Python | ![numpy](img_readme/numpy-color.svg) numpy | ![jupiter](img_readme/jupyter-color.svg) Jupiter Notebook |
| | ![matplotlib](img_readme/python-color.svg) matplotlib | ![github](img_readme/github-color.svg) Github |
| | ![pillow](img_readme/python-color.svg) pillow | ![vscode](img_readme/visualstudiocode-color.svg) VS code |
| | ![scikit-learn](img_readme/scikitlearn-color.svg) scitkit-learn | ![colab](img_readme/googlecolab-color.svg) google colab |
| | ![tensorflow](img_readme/tensorflow-color.svg) Tensorflow | ![discord](img_readme/discord-color.svg) Discord |
| | ![keras](img_readme/keras-color.svg) Keras | ![kaggle](img_readme/kaggle-color.svg) Kaggle |

