# Projet de Master 2 TIDE : Graph CNN study with an emphasis on ChebNet 

Utilisation de Convolution sur les Graphes
Bienvenue dans le répertoire GitHub du projet de Master 2 TIDE, qui explore l'utilisation de convolutions sur les graphes. Ce projet se concentre sur la modélisation de données non euclidiennes, typiquement représentées sous forme de graphes.

Nous nous intéressons particulièrement à ChebNet, une approche spectrale pour les réseaux de neurones convolutifs sur les graphes. Ce projet s'appuie sur l'article "Convolutional Neural Networks on Graphs with Fast Localized Spectral Filtering" que vous pouvez consulter ici : https://arxiv.org/abs/1606.09375.

## Objectifs de ce GitHub
1) Reproduction des Résultats de l'Article : Reprendre le code fourni dans le GitHub de l'article pour reproduire les résultats obtenus sur des jeux de données comme MNIST et 20News.


2) Nouveaux Cas d'Usage : Appliquer ChebNet à d'autres cas d'usage

## Contributions 

L'une des grosses diffucltés que nous avons rencontrés est que les auteurs de "Convolutional Neural Networks on Graphs with Fast Localized Spectral Filtering" ont initialement développé le modèle sur du TensorFlow version 1.0. Ce qui a été une grande diffucltés pour nous car il a fallut reprogrammer une grande partie du code sur du TensorFlow version 2.15. Ainsi la structure que nous avons utilisé est la même, il y a cependant beaucoup de changement sur les fonctions. C'est l'une des raisons que nous avons pas pu reproduire l'entière des résultats et également des résultats différents. Comme il y a une très grosse évolution entre la version de TensorFlow 1.0 et la version 2.0. 


## Structure du Répertoire GitHub

Afin de faciliter la navigation et la compréhension de ce projet, voici une description détaillée de l'arborescence du répertoire :

````
Graph_CNN_ChebNet/
│
├── model/ # Modèle de base utilisé dans l'article
│   ├── coarsening.py                  
│   ├── graph.py
│   ├── models.py 
│   └── utils.py             
│
├── Results_Pytorch/
│   ├── data_preprocessing.ipynb
│   ├── model_training.ipynb     
│   └── README.md                
│
├── Results_Tensorflow/
│   ├── 20news.ipynb
│   ├── mnist.ipynb 
│   └── usage.py
│   
├── .gitignore              
├── requirements.txt          
└── README.md            
````

### 
