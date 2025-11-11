# Approche Deep Learning pour le diagnostic de la tuberculose à partir d’images radiographiques thoraciques.

<p>   La tuberculose pulmonaire (TBP) est une maladie infectieuse grave provoquée par la bactérie Mycobacterium tuberculosis. Selon l'Organisation Mondiale de la Santé (OMS), la tuberculose fait partie des dix principales causes de mortalité dans le monde. En 2020, on estime à 10 millions le nombre de nouveaux cas de tuberculose et à 1,5 million le nombre de décès liés à cette maladie. Les principaux symptômes de la tuberculose sont une toux qui dure plus de trois semaines, une perte d'appétit et une perte de poids involontaire, de la fièvre, des frissons et des sueurs nocturnes. La plupart des personnes qui meurent de la tuberculose décèdent principalement parce qu'elles ont négligé les symptômes ou n'ont pas reçu de traitement médical approprié au moment opportun. Pour lutter contre ce problème et sauver d'innombrables vies, j'ai créé ce modèle d'apprentissage profond basé sur un réseau neuronal convolutif.

Traduit avec DeepL.com (version gratuite)
  
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


