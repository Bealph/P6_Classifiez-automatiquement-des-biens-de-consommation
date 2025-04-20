P6: Classifiez automatiquement des biens de consommation


Ce projet, réalisé dans le cadre du parcours Data Scientist d'OpenClassrooms, vise à automatiser la classification des produits d'une marketplace e-commerce en fonction de leurs descriptions textuelles et images. L'objectif est d'améliorer l'expérience utilisateur en facilitant la mise en ligne des produits pour les vendeurs et la recherche pour les acheteurs, tout en préparant un passage à l'échelle.

Ce repository contient l'ensemble des livrables pour répondre aux deux itérations du projet : une étude de faisabilité pour le regroupement automatique des produits par catégorie et une classification supervisée des images avec collecte de données via une API.

Structure du projet.


Fichiers principaux :

- DIALLO_Alpha_1_notebook_pretraitement_feature_extraction_faisaibilite_082023.ipynb : Notebook contenant le prétraitement des données textuelles et images, l'extraction de features (texte : bag-of-words, Tf-idf, Word2Vec, BERT, USE ; image : SIFT, CNN Transfer Learning), la réduction dimensionnelle en 2D, la visualisation des clusters et la mesure de similarité pour évaluer la faisabilité du regroupement automatique par catégorie.
- DIALLO_Alpha_2_notebook_embeddings_082023.ipynb : Notebook dédié à l'exploration approfondie des approches d'embedding textuel (Word2Vec, BERT, USE) pour analyser leur performance dans la séparation des catégories.
- DIALLO_Alpha_3_notebook_traitement_avec_technique_recente_082023.ipynb : Notebook implémentant une classification supervisée des images avec data augmentation pour optimiser les performances du modèle.
- DIALLO_Alpha_4_script_Python_082023.py : Script Python pour tester l'API de collecte de produits, spécifiquement pour extraire des produits à base de "champagne".
- DIALLO_Alpha_5_API_082023.csv : Fichier CSV contenant les 10 premiers produits extraits via l'API, avec les champs foodId, label, category, foodContentsLabel, et image.
- DIALLO_Alpha_6_presentation_082023.pdf : Support de présentation (PDF) détaillant l'étude de faisabilité, la classification supervisée et le test de l'API (maximum 30 slides).
- first_10_champagne.csv : Fichier CSV contenant un exemple d'extraction des 10 premiers produits à base de "champagne" via l'API.

Données :

Les données utilisées incluent un jeu de produits avec descriptions textuelles et liens vers des images, fourni par l'entreprise. Aucune contrainte de propriété intellectuelle n'a été identifiée.

Objectifs du projet :

Première itération : Étude de faisabilité

Objectif : Démontrer la possibilité de regrouper automatiquement des produits de même catégorie à partir de leurs descriptions textuelles et images.

Méthodologie :

- Prétraitement : Nettoyage des textes (tokenisation, suppression des stop-words, etc.) et normalisation des images.
- Extraction de features :

  Texte : Bag-of-words (comptage simple, Tf-idf), embeddings (Word2Vec, BERT, USE).
  Image : Algorithmes SIFT et CNN Transfer Learning.
  Réduction dimensionnelle : Projection en 2D pour visualiser les clusters de produits par catégorie.
  Évaluation : Analyse visuelle des graphiques 2D et calcul de la similarité entre les catégories réelles et les clusters issus de la segmentation.
  Résultats : Les visualisations et mesures de similarité confirment la faisabilité du regroupement automatique, avec des performances variables selon les méthodes d'extraction.

- Deuxième itération : Classification supervisée et collecte de données

  Classification supervisée :

    Mise en œuvre d'un modèle de classification des images avec data augmentation pour améliorer la robustesse.
    Optimisation des performances via des techniques de régularisation et ajustement des hyperparamètres.

  Collecte de données :

    Test de l'API pour extraire des produits à base de "champagne".

- Exportation des 10 premiers produits dans un fichier CSV structuré.


Résultats principaux :

- L'étude de faisabilité montre que les embeddings BERT et USE, ainsi que le CNN Transfer Learning, offrent les meilleures performances pour le regroupement automatique.
- La classification supervisée avec data augmentation améliore significativement la précision du modèle sur les images.
- L'extraction via l'API a permis de collecter des données structurées sur les produits à base de "champagne", prêtes pour une intégration future.

Perspectives :

- Optimisation des modèles avec des hyperparamètres supplémentaires.
- Intégration d'autres sources de données via l'API pour élargir la gamme de produits.
- Déploiement du moteur de classification dans un environnement de production.
