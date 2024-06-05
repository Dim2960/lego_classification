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
1.1. Collecte des images de différentes pièces de LEGO (voir sources)  
1.2. Organisation des images en dossiers selon les classes  
1.3. Redimensionnement des images du dataset (dataset_preparation.ipynb)  
1.4. Définition des paramètres de data augmentation (train_model_***.ipynb)  
1.5. Division des données en ensembles d'entraînement, de validation et de test (train_model_***.ipynb)  
1.6. Création manuellement d'un jeu de données de test à l'aide d'images 3D en .dae (3 à 4 images par pièce) (https://imagetostl.com/fr/visualiser-dae-en-ligne#google_vignette)  

2. Préparation du modèle  
2.1. Chargement du modèle pré-entraîné  
2.2. Freeze des couches du modèle pré-entraîné  
2.3. Décision à tester : garder ou non certaines couches gelées  
2.4. Construction et Compilation du modèle personnalisé avec essai et choix des paramètres (nombre de neurones personnalisés, fonction d'activation, optimizer, fonction perte, nombre d'epochs, Taille des batchs)  
2.5. Évaluation du modèle  avec les metrix val_accuracy, val_loss et une matrice de confusion
2.6. Enregistrement du modèle

3. Préparation et utilisation du modèle  
3.1. Preparation des images à tester (image_test_preparation.ipynb)  
3.2. Utilisation du modèle sur les images de test différentes du dataset (test_model.ipynb)  

## Hardware

La configuration du hardware pour l'entrainement des modèles était la suivante : 
- GPU : NVIDIA GeForce RTX 3060
- Processeur : Intel Core i7-14700KF
- RAM : 64 Go DDR5
- Stockage : SSD 1 To
- Système exploitation : Windows 11

## Installation

0. Prérequis d'installation
    
    ![python](img_readme/python-color.svg) Python == 3.9
    
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

1. Préparation du dataset : dataset_preparation.ipynb  
2. Entrainnement des modèles : train_model_***.ipynb  
3. Préparation de l'image de test : image_test.ipynb  
4. Utilisation des modèles : test_model.ipynb  

## Perspective d'amélioration / évolution

* Préparation automatisée des images de test pour utilisation du modèle  
* Utilisation d'image réel de Lego pour tester les modèles
* Utilisation de deux images à des angles de vues différentes pour améliorer la fiabilité de prédiction

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

