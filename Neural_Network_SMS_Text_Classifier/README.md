# Classification de SMS : Détection de Spam avec Deep Learning

## Description

Ce projet implémente un classificateur de SMS utilisant un réseau de neurones profond pour distinguer automatiquement les messages spam des messages légitimes (ham). Le modèle est construit avec TensorFlow/Keras et fait partie de la certification Machine Learning de **FreeCodeCamp**.

## Objectif

Développer un modèle de classification binaire capable d'identifier avec précision les SMS spam, en utilisant des techniques de traitement du langage naturel (NLP) et de deep learning.

## Dataset

Le dataset provient de **SMS Spam Collection** et contient des SMS étiquetés :

### Fichiers de données
- **train-data.tsv** : Données d'entraînement
- **valid-data.tsv** : Données de validation/test

### Structure des données
Chaque ligne contient :
- **label** : Classification (ham/spam)
- **message** : Contenu du SMS

### Distribution
Le dataset présente un déséquilibre de classes typique :
- **Ham (messages légitimes)** : ~87%
- **Spam (messages indésirables)** : ~13%

## Technologies Utilisées

- **TensorFlow 2.x / Keras** : Construction et entraînement du modèle
- **Pandas** : Manipulation des données
- **NumPy** : Calculs numériques
- **Matplotlib** : Visualisation des performances
- **Regular Expressions (re)** : Nettoyage du texte

##  Téléchargement des Données

```bash
wget https://cdn.freecodecamp.org/project-data/sms/train-data.tsv
wget https://cdn.freecodecamp.org/project-data/sms/valid-data.tsv
```

## Évaluation et Visualisation

### Métriques

- **Accuracy** : Taux de classification correcte
- **Loss** : Binary Crossentropy

### Graphiques

Le projet génère deux graphiques :
1. **Model Accuracy** : Évolution de la précision (train vs validation)
2. **Model Loss** : Évolution de la perte (train vs validation)

### Exemples de prédiction

```python
sample_texts = [
    "how are you doing today?",
    "WINNER! You have won $1000! Call now!",
    "Hey, want to grab lunch tomorrow?",
    "URGENT! Your account will be closed. Click here now!"
]
```

**Résultats attendus :**
- Message 1 : ham (score faible)
- Message 2 : spam (score élevé)
- Message 3 : ham (score faible)
- Message 4 : spam (score élevé)

**Critère de réussite** : Toutes les prédictions doivent correspondre aux labels attendus.

## Points Clés du Projet

1. **Preprocessing robuste** : Nettoyage systématique du texte
2. **Embeddings** : Représentation vectorielle dense des mots
3. **GlobalAveragePooling** : Agrégation efficace des séquences
4. **Régularisation** : Dropout pour éviter le surapprentissage
5. **Callbacks intelligents** : Optimisation automatique de l'entraînement

## Cas d'Usage

- Filtrage automatique de SMS
- Protection contre le phishing par SMS
- Modération de messages
- Systèmes de messagerie sécurisés
- Applications de télécommunication

## Améliorations Possibles

### Architecture
- **LSTM/GRU** : Réseaux récurrents pour capturer les dépendances temporelles
- **BiLSTM** : LSTM bidirectionnel pour contexte avant/arrière
- **Attention Mechanism** : Focaliser sur les mots importants
- **Transformers** : Architecture state-of-the-art (BERT, RoBERTa)

### Données
- **Augmentation** : Génération de variations de texte
- **Équilibrage** : Techniques pour gérer le déséquilibre de classes (SMOTE, class weights)
- **Features supplémentaires** : Longueur du message, nombre de majuscules, présence d'URL

### Preprocessing
- **Stemming/Lemmatization** : Réduction des mots à leur racine
- **Stop words removal** : Suppression des mots courants
- **N-grams** : Capture de séquences de mots

### Métriques
- **Precision/Recall** : Métriques plus adaptées aux classes déséquilibrées
- **F1-Score** : Moyenne harmonique precision/recall
- **Courbe ROC** : Analyse du trade-off sensibilité/spécificité
- **Matrice de confusion** : Visualisation détaillée des erreurs

## Licence

Ce projet est développé dans le cadre d'un challenge FreeCodeCamp.