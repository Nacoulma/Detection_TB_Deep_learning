# Approche Deep Learning pour le diagnostic de la tuberculose à partir d’images radiographiques thoraciques.

<p>   La tuberculose pulmonaire (TBP) est une maladie infectieuse grave provoquée par la bactérie Mycobacterium tuberculosis. Selon l'Organisation Mondiale de la Santé (OMS), la tuberculose fait partie des dix principales causes de mortalité dans le monde. En 2020, on estime à 10 millions le nombre de nouveaux cas de tuberculose et à 1,5 million le nombre de décès liés à cette maladie. The major symptoms of tuberculosis are the cough that lasts more than three weeks, loss of appetite and unintentional weight loss, fever, chills, and night sweats. Most people die because of tuberculous mainly die because of the negligence of symptoms or not getting proper health treatment at the proper time. To fight against this problem and to save countless life I have created this convolutional neural network-based deep learning model.
  
Ce projet a pour objectif de détecter automatiquement la tuberculose pulmonaire à partir d’images radiographiques thoraciques (rayons X), en utilisant l’apprentissage profond et plus précisément avec les modèles pré-entraînés VGG16, MobileNet-V2 et DenseNet121.  

L’approche s’appuie sur le transfert de connaissances (`Transfer Learning`) à partir des modèles pré-entraînés sur ImageNet, afin d’adapter ses capacités à la classification binaire entre :
- 🟩 **Poumons sains**
- 🟥 **Poumons atteints de tuberculose**

Ce travail s’inscrit dans une démarche visant à aider les professionnels de santé dans le dépistage rapide et fiable de la tuberculose, notamment dans les zones à ressources limitées.

</p>
<h2>Libraries Used</h2>
<ul>
  <li>Tensorflow</li>
  <li>Keras</li>
  <li>Numpy</li>
  <li>Pandas </li>
  <li>Matplotlib</li>
  <li>Numpy</li>
  <li>Open CV</li>
  <li>Glob</li>
</ul> 

<p align="center">

## ⚙️ Architecture et approche

- **Architectures utilisées :** VGG16,MobileNet-V2,DenseNet (pré-entraînées sur ImageNet)
- **Technique :** Transfer Learning + Fine-Tuning
- **Environnement :** TensorFlow / Keras
- **Taille d’image :** 224x224 pixels
- **Optimiseur :** Adam
- **Fonction de perte :** Binary Crossentropy
- **Métriques :** Accuracy, AUC, F1-score

## 📊 Résultats principaux

| Modèle      | Accuracy | AUC  | Observation principale |
|--------------|-----------|------|--------------------------|
| **VGG16**    | **78 %**  | **0.85** | Meilleure performance globale, bonne stabilité |
| MobileNetV2  | 77.5 %    | 0.83 | Léger modèle, efficace mais moins discriminant |
| DenseNet     | 74 %      | 0.76 | Bonne convergence mais moins performant |

✅ **VGG16 a été retenu comme meilleur modèle** pour sa capacité à bien généraliser et à distinguer efficacement les cas positifs et négatifs de tuberculose.

## Données utilisées

Les données proviennent de jeux de données publics :

- Shenzhen Hospital (China) 
- Montgomery County (USA) 

🔒 Les données médicales ne sont pas incluses dans le dépôt pour des raisons éthiques.
Vous pouvez obtenir ces datasets via le site officiel de la National Library of Medicine (NLM) :
https://openi.nlm.nih.gov

## Perspectives d’amélioration

- Entraîner le modèle sur un plus grand volume d’images pour renforcer la robustesse.
- Intégrer une segmentation automatique des poumons avant la classification.
- Expérimenter avec des architectures plus récentes (EfficientNet, Vision Transformers).
- Créer une interface web interactive (ex. Streamlit ou Flask) pour le diagnostic assisté.
- Déployer le modèle sur appareil mobile (TensorFlow Lite).


# 📂 Jeu de Données – Détection de la Tuberculose à partir de Radiographies Thoraciques

Ce dossier est destiné à contenir les données utilisées pour l'entraînement, la validation et le test des modèles **VGG16** **MobileNet** et **DenseNet** appliqué à la détection automatique de la tuberculose pulmonaire à partir d’images de radiographies thoraciques.

---

## 🧠 Description du Dataset

Le jeu de données utilisé provient de plusieurs sources publiques, notamment les ensembles **Montgomery County** et **Shenzhen**, largement utilisés dans la recherche en détection de la tuberculose par apprentissage profond.

Le dataset est organisé en deux catégories principales :
- **TB (Tuberculosis)** : images présentant des signes radiographiques de tuberculose.
- **Normal** : images de radiographies pulmonaires normales.

Chaque image a été redimensionnée à **224 × 224 pixels**, conformément aux exigences d'entrée des (3) modèles.

---

## 📥 Téléchargement du Dataset

Les données complètes ne sont pas directement incluses dans ce dépôt GitHub en raison de leur taille.

Vous pouvez télécharger le dataset via le lien Google Drive ci-dessous 👇 :

👉 [**Télécharger le dataset (Google Drive)**](https://drive.google.com/drive/folders/1nPPuokBfUc3nZVdRysr5KU_BzMX9dLI8?usp=drive_link)

Une fois le téléchargement terminé, placez le dossier dans le répertoire racine du projet sous la structure suivante :


## Auteur

**Thierry Nacoulma**

</p>  
<h2>Model Details</h2>
<p> For the identification of tuberculosis, the model at its core uses convolutional and fully connected layers. The model consists of four convolutional layers for feature extraction from the chest x-ray, each followed by a max-pooling layer.  After the four convolutional and max-pooling layers, the model uses three dense layers for the classification task.</p>
<h2>Model Training</h2>
<p>The model was trained for 20 epochs with batch size equals 19. During the training process parse, the binary cross-entropy loss function was used along with the Adam optimizer. The dataset on which the model has trained has been downloaded from Kaggle.com (https://bit.ly/3vw3FJQ). </p>
<h2>Model Evaluation</h2>
<img src="https://github.com/NavinBondade/Tuberculosis_Detection_with_90_percent_accuracy/blob/main/Tuberculosis%20Detection%20with%2090%25%20accuracy/Graps%20and%20Images/loss.png" width="450" height="300">
<p>After training process the model has shown loss: 0.1270 and accuracy: 0.9445 for training data and loss: 0.4219 and accuracy: 0.8955 for validation data (this clearly shows that model trained perfectly without overfitting or underfitting)</p>
<h2>Conclusion</h2>
<p>In this project, I have created a convolution deep neural network architecture that correctly identifies tuberculosis infected chest x-ray with an impressive accuracy of 90 percent.</p>
