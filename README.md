# Graph CNN study with an emphasis on ChebNet 
#### Réalisé par : Legrosse Alexandre, Mobasso Guilhem et Lazizi Célia

Bienvenue dans le répertoire GitHub du projet de Master 2 TIDE, qui explore l'utilisation de convolutions sur les graphes. Ce projet se concentre sur la modélisation de données non euclidiennes, typiquement représentées sous forme de graphes.

Nous nous intéressons particulièrement à ChebNet, une approche spectrale qui utilise les filtres spectraux basés sur les polynômes de Chebyshev pour les réseaux de neurones convolutifs sur les graphes. Ce projet s'appuie sur l'article "Convolutional Neural Networks on Graphs with Fast Localized Spectral Filtering" que vous pouvez consulter ici : [https://arxiv.org/abs/1606.09375].

## Objectifs de ce GitHub
1) Reproduction des résultats de l'Article : Reprendre l'implémentation fournie dans le GitHub de l'article pour reproduire les résultats obtenus sur des jeux de données notamment 20News et RCV1.
2) Utilisation des récents travaux avec l'utilisation de torch_geometric et des jeux de données DeezerEurope et MNISTSuperpixels. 

## Méthodologie 

En premier lieu, nous avons utilisé l'implémentation des filtres spectraux basés sur les polynômes de Chebyshev disponible sur le GitHub de l'article : [https://github.com/mdeff/cnn_graph]. Une difficulté majeure a été l'initialisation du modèle avec TensorFlow 1.0, nécessitant une reprogrammation pour le porter sur TensorFlow 2.15. Bien que nous ayons conservé la structure de base, de nombreux changements de fonctions étaient nécessaires, ce qui a entraîné des différences dans les résultats obtenus. L'évolution entre TensorFlow 1.0 et 2.0 explique en partie ces variations. 

Le modèle mis à jour pour TensorFlow 2.0 se trouve dans `Graph_CNN_ChebNet/lib/` et les résultats correspondants dans `Graph_CNN_ChebNet/Results_Tensorflow/`.

## Implémentation avec PyTorch Geometric

Ensuite, nous avons utilisé l'implémentation de ChebNet fournie par `torch_geometric` : [https://pytorch-geometric.readthedocs.io/en/latest/generated/torch_geometric.nn.conv.ChebConv.html]. Les résultats de ce modèle sont disponibles dans `Graph_CNN_ChebNet/Results_Pytorch/`.

## Structure du Répertoire GitHub

Voici une description de l'arborescence du répertoire :

````
Graph_CNN_ChebNet/
│
├── model/ # Implémentation officiel du GitHub de ChebNet
│   ├── coarsening.py                  
│   ├── graph.py
│   ├── models.py 
│   └── utils.py             
│
├── Results_Pytorch/ # Résultats provenant de l'implémentation ChebNet
│   ├── DeezerEurope.ipynb
│   ├── MNISTSuperpixels.ipynb     
│                 
├── Results_Tensorflow/ # Résultats provenant de l'implémentation de l'article 
│   ├── 20news.ipynb
│   ├── mnist.ipynb 
│   ├── rcv1.ipynb 
│   └── usage.py
│   
├── .gitignore              
├── requirements.txt          
└── README.md            
````
### 

## Installer

1. Clone this repository.
   ```sh
   git clone https://github.com/Alexx776/Graph_CNN_ChebNet
   cd Graph_CNN_ChebNet
   ```

2. Installer les dépendances. 
   ```sh
   pip install -r requirements.txt  
   ```

Remarque importante : Les résultats ne sont pas reproductibles à l'état au vu de la configuration du modèle, un update de ce repo est à envisager.