# Tweets-Sentiment-Analysis-
Team members : SAFAA OUAHIB & THOMAS HARBERT

## Tweets sentiment Analysis using LSTM & BERT

Le traitement automatique de la langue est un domaine multidisciplinaire impliquant la linguistique, l'informatique et l'intelligence artificielle. Il vise à créer des outils de traitement de la langue naturelle pour diverses applications. Parmi ces applications, nous pouvons citer celles qui relèvent du traitement des réseaux sociaux. Les sites de médias sociaux, tels que Twitter, sont une source riche de nombreux types d'informations, notamment en matière de santé. Ce projet consiste à développer des modèles de classification des sentiments (positive, negative ou neutre) sur les réseaux sociaux avec trois architectures différentes (LSTM, BERT, et GPT), et à évaluer le meilleur d’entre eux.

Dataset est le site Kaggle:
training.1600000.processed.noemoticon.csv

## PRESENTATION

Le traitement automatique de la langue (TAL) constitue un domaine de recherche multidisciplinaire qui fusionne la linguistique, l'informatique et l'intelligence artificielle. Son objectif principal est de créer des outils capables de comprendre et de traiter le langage naturel pour une variété d'applications. L'une de ces applications concerne le traitement des réseaux sociaux, en particulier l'exploitation des données provenant de plateformes telles que Twitter, qui représentent une source riche d'informations, notamment dans le domaine de la santé.

Dans le cadre de ce projet, l'accent est mis sur le développement de modèles de classification des sentiments (positif, négatif ou neutre) appliqués aux contenus des réseaux sociaux. Trois architectures de modèles ont été explorées, à savoir LSTM (Long Short-Term Memory), BERT (Bidirectional Encoder Representations from Transformers) et enfin nous avons tenté d'utiliser les nouvelles technologies GPT (Generative Pre-trained Transformer). L'objectif est de comparer ces trois approches en termes d'efficacité dans la classification des sentiments.

Le processus comprend le développement et l'entraînement de modèles basés sur chaque architecture, suivi d'une évaluation pour déterminer les performances. Cette évaluation peut inclure des mesures telles que la précision, le rappel et la F-mesure. Les résultats obtenus permettront de guider le choix de la meilleure architecture pour la classification des sentiments dans le contexte des réseaux sociaux, offrant ainsi des perspectives précieuses pour des applications futures dans le domaine du TAL.

## PREREQUISITE
- Python 3
- re
- Numpy
- Pandas
- seaborn
- matplotlib.pyplot
- NLTK
- transformers
- Pytorch
- sklearn

## LSTM

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RavenMorgan/Tweets-Sentiment-Analysis-/blob/main/Sentiments_Analysis_with_LSTM_Model.ipynb)

LSTM, ou Long Short-Term Memory, est un type d'architecture de réseau de neurones récurrents (RNN) utilisé dans le domaine de l'apprentissage profond et de l'intelligence artificielle. Conçu pour résoudre le problème de la dépendance à long terme dans les séquences de données, LSTM est particulièrement efficace pour traiter et prévoir des informations dans des séquences temporelles, telles que des séquences de mots dans le langage naturel ou des séries temporelles dans la prédiction de valeurs.

### Overview: 
1) *Import et load dataset*
2) *Data processing*
    1) *Tokenization*
    2) *Padding*
    3) *Data splitting*
    4) *Encoder*
7) *Embedding*
8) *Modeling*
9) *Evaluation*

### Guide d'utilisation:
Cliquez sur le bouton "Ouvrir dans Colab" et suivez les instructions sur le notebook.

Vous pouvez également cloner le dépôt sur votre machine locale en utilisant la commande suivante :
git clone https://github.com/RavenMorgan/Tweets-Sentiment-Analysis-.git

### Résultats :

Visualisation graphique de la précision et de la perte :
![image](https://github.com/RavenMorgan/Tweets-Sentiment-Analysis-/assets/93980956/a2b80c1f-4f1f-4790-8b3b-3d5cb6fe9af9)

Matrice de confusion :
![image](https://github.com/RavenMorgan/Tweets-Sentiment-Analysis-/assets/93980956/96e12e73-b57c-4ec7-98f7-c5d71380572c)

Scores :
|           | Precision | Recall | F1-Score | Support  |
|-----------|-----------|--------|----------|----------|
| Class 0   |   0.79    |  0.78  |   0.78   | 160542   |
| Class 1   |   0.78    |  0.79  |   0.78   | 159458   |
|-----------|-----------|--------|----------|----------|
| Accuracy  |           |        |   0.78   | 320000   |
| Macro Avg |   0.78    |  0.78  |   0.78   | 320000   |
| Weighted Avg | 0.78    |  0.78  |   0.78   | 320000   |


## BERT: 

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RavenMorgan/Tweets-Sentiment-Analysis-/blob/main/Sentiments_Analysis_with_BERT_Model.ipynb)

BERT, ou Bidirectional Encoder Representations from Transformers, est un modèle de langage préentraîné qui a révolutionné le domaine du traitement du langage naturel (NLP). Il a été introduit par Google en 2018. La particularité de BERT réside dans sa capacité à capturer la signification contextuelle des mots dans une phrase en utilisant un contexte bidirectionnel.

### Overview : 

Ce dépôt contient le code pour un modèle d'analyse de sentiment utilisant BERT (Bidirectional Encoder Representations from Transformers). Le modèle est entraîné sur un ensemble de données pour la classification des sentiments.

1) Data preparing 
2) Tokenization
3) Model Training ( a small version of BERT Model  for sequenceClassificaton )
4) Evaluation (accuracy = 0.97 , loss = 0.10)
5) Interference / predictions

### Guide d'utilisation:
Cliquez sur le bouton "Ouvrir dans Colab" et suivez les instructions sur le notebook.

Vous pouvez également cloner le dépôt sur votre machine locale en utilisant la commande suivante :
git clone https://github.com/RavenMorgan/Tweets-Sentiment-Analysis-.git

## CONCLUSION

En conclusion, les résultats de notre projet de recherche indiquent que parmi les architectures de modèles de classification des sentiments examinées, BERT se distingue en offrant une précision exceptionnelle. Les mesures d'évaluation, notamment le Test loss (perte lors de l'évaluation) de 0.1367 et la Test accuracy (précision lors de l'évaluation) de 0.9630, démontrent la performance remarquable de BERT dans la tâche de classification des sentiments sur les réseaux sociaux.

Cette précision élevée suggère que BERT a une capacité unique à saisir les nuances et le contexte dans le langage naturel, ce qui est essentiel pour comprendre les sentiments exprimés sur les plateformes de médias sociaux comme Twitter. Ces résultats encouragent l'adoption de BERT dans des applications réelles où la compréhension précise des sentiments est cruciale, que ce soit dans le domaine de la santé, du marketing ou d'autres secteurs où l'analyse des opinions en ligne revêt une importance stratégique.

Il est important de noter que bien que BERT se soit démarqué dans cette étude, le choix de l'architecture du modèle dépendra toujours du contexte spécifique de l'application et des exigences particulières du projet. En fin de compte, cette recherche ouvre la voie à des améliorations continues dans le domaine du traitement automatique de la langue et souligne l'importance de choisir des modèles adaptés aux tâches spécifiques pour garantir des performances optimales.
