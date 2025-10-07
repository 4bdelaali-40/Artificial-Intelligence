# Cats Dogs Classifier 

## Description

Ce projet implémente une solution de classification d'images (chats vs chiens) en utilisant un réseau de neurones convolutifs (CNN) avec TensorFlow / Keras. on a appliquer des transformations sur les images et de l'augmentation, construit un modèle CNN, l'entraîne, puis évalue et sauvegarde le modèle.

## Objectifs

* Télécharger et préparer le dataset `cats_and_dogs` (fourni par freeCodeCamp).
* Construire un pipeline de prétraitement d'images.
* Définir et entraîner un modèle CNN simple avec Keras.
* Évaluer les performances.

## Prérequis

* Python 3.8+ recommandé
* Bibliothèques (voir `requirements.txt` exemple ci-dessous) :

  * tensorflow
  * numpy
  * matplotlib
  * pillow (PIL)
  * (optionnel) google-colab (si vous utilisez Colab)

## Structure du notebook

Le notebook contient les sections principales suivantes (ordre observé) :

1. Téléchargement et extraction du dataset
2. Définition des chemins (`PATH`, `train_dir`, `validation_dir`, ...)
3. Visualisation d'exemples d'images
4. Variables de prétraitement et d'entraînement (taille d'image, batch, etc.)
5. Création des `ImageDataGenerator` (rescaling, augmentation pour l'entraînement)
6. Définition du modèle CNN (Keras Sequential)
7. Compilation du modèle
8. Entraînement du modèle
9. Évaluation / visualisation des courbes d'entraînement

## Paramètres importants

* Taille des images : 150*150
* `batch_size` : 128
* `epochs` : 50

## Résultats

* accuracy : 78%
* loss : 0.5

## Suggestions d'améliorations

* Essayer des architectures pré-entraînées (transfer learning : MobileNet, VGG16, ResNet) pour de meilleures performances.
* Ajouter un pipeline de test indépendant et une métrique de confusion matrix.
* Enregistrer les checkpoints et utiliser `EarlyStopping` pour éviter l'overfitting.
* Expérimenter avec d'autres techniques d'augmentation (rotation, zoom, flip, brightness).