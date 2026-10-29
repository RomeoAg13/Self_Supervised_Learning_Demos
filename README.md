# Self-Supervised Learning — Computer Vision

## Contexte

Ce projet a été réalisé dans le cadre du **Master 2 Vision et Machine Intelligente (VMI)** à l'Université Paris Cité.

L'objectif de ce TP est de comprendre et comparer différentes méthodes d'**apprentissage auto-supervisé (Self-Supervised Learning)** appliquées à la vision par ordinateur.

Le principe est d'entraîner un réseau neuronal à apprendre des représentations visuelles à partir de tâches prétextes, sans utiliser directement les labels des images.

## Méthodes étudiées

- **Context Encoder** : reconstruction d'une partie masquée de l'image.
- **RotNet** : prédiction de la rotation appliquée à une image.
- **SimCLR** : apprentissage contrastif entre différentes vues d'une même image.
- **Relative Patch Position Prediction** : implémentation d'une tâche prétexte consistant à prédire la position relative de deux patchs.

Pour cette dernière méthode, j'ai développé un CNN à poids partagés, entraîné sur des paires de patchs extraits des images.

## Jeux de données

- **CIFAR-10** : entraînement et évaluation.
- **CINIC-10** : étude de la généralisation sur un autre jeu de données.

## Résultats

La méthode de prédiction de position relative atteint **29,69 % d'accuracy sur CIFAR-10 Test**, pour une classification parmi huit positions possibles.

L'objectif final est de comparer les représentations apprises par les quatre méthodes sur des tâches de classification d'images.

## Technologies

Python · PyTorch · Torchvision · Google Colab
