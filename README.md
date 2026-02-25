# 🧠 Reconnaissance des Chiffres Manuscrits – Deep Learning

## 📌 Description du Projet

Ce projet s’inscrit dans le cadre du mini-projet en Machine Learning.  
L’objectif est de développer un programme en **Deep Learning** capable de reconnaître automatiquement des chiffres manuscrits (de 0 à 9).

Le modèle reçoit en entrée une image d’un chiffre manuscrit et prédit la classe correspondante.

---

## 📊 Dataset Utilisé : MNIST

Nous avons utilisé le dataset **[MNIST](https://www.kaggle.com/datasets)** (Modified National Institute of Standards and Technology).

### Caractéristiques du dataset :

- 70 000 images de chiffres manuscrits
- Images en niveaux de gris
- Taille : 28 × 28 pixels
- 60 000 images pour l'entraînement
- 10 000 images pour le test
- 10 classes (chiffres de 0 à 9)

Les images sont normalisées avant l'entraînement pour améliorer les performances du modèle.

---

## 🏗️ Modèles Implémentés

Deux modèles de Deep Learning ont été développés et comparés :

### 1️⃣ MLP (Multi-Layer Perceptron)

Un réseau de neurones entièrement connecté composé de :

- Une couche d’entrée (784 neurones)
- Une ou plusieurs couches cachées
- Une couche de sortie (10 neurones – Softmax)

**Caractéristiques :**

- Simple à implémenter
- Bonne performance
- Moins efficace pour exploiter la structure spatiale des images

---

### 2️⃣ CNN (Convolutional Neural Network)

Un réseau de neurones convolutionnel composé de :

- Couches de convolution
- Couches de pooling
- Couches fully connected
- Fonction d’activation ReLU
- Couche de sortie Softmax

**Caractéristiques :**

- Spécialement adapté aux images
- Meilleure extraction des caractéristiques
- Meilleure précision que le MLP

📌 Conclusion :  
Le modèle CNN donne de meilleures performances que le MLP sur le dataset MNIST.

---

## ⚙️ Étapes du Projet

1. Chargement du dataset MNIST  
2. Prétraitement des données (normalisation, reshaping)  
3. Division des données (train / test)  
4. Création des modèles (MLP et CNN)  
5. Entraînement des modèles  
6. Évaluation avec :
   - Accuracy
   - Matrice de confusion
   - Rapport de classification  
7. Comparaison des performances  

---

## 📈 Évaluation

Les modèles ont été évalués sur le dataset de test.

- Le MLP obtient une bonne précision.
- Le CNN obtient une précision plus élevée grâce aux couches convolutionnelles.

---

## 🖥️ Interface Interactive

Une interface graphique interactive a été développée avec **Gradio**.

**Fonctionnalités :**

- L’utilisateur peut dessiner un chiffre à la souris
- L’image est prétraitée automatiquement
- Le modèle prédit le chiffre en temps réel
- La probabilité de chaque classe peut être affichée

Cette interface permet de tester le modèle avec de nouvelles données (hors dataset MNIST).

---

## 🛠️ Technologies Utilisées

- Python  
- TensorFlow / Keras  
- NumPy  
- Matplotlib  
- Scikit-learn  
- Gradio  

---

## 🎯 Objectif Final

Comparer les performances de deux modèles de Deep Learning (MLP et CNN) pour déterminer celui qui offre le meilleur rendement dans la reconnaissance des chiffres manuscrits.

Le CNN est le modèle le plus performant pour ce problème.
