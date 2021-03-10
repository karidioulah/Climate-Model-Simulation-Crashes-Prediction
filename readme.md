# Projet Machine Learning 2020
![Imgur](https://i.imgur.com/VfCBHQo.png?1)


**Réalisé par:  Homar KARIDIOULA (Apprenant Data Scientist Sigma-Clermont)** 

##  Sommaire: 
[I. Présentation](#presentation) <br>
[II. Initialisation et Chargement des données](Voir NoteBook)(#initialisation) <br>
[III. Exploration des donnéess](Voir NoteBook)(#exploration) <br>
[IV. Algorithmes d'apprentissage](Voir NoteBook)(#algorithmes)<br>
[V. Exploitation des Modèles](Voir NoteBook)(#Model_exploitation)<br>
[VI. Conclusion](#conclusion)    <br>

## [I.  Présentation du projet](#sommaire) 

Dans cadre de la formation du Mastère Spécialisé Data Science pour l'Ingénierie, nous avons eu à découvrir et apprendre différents concepts lié à la Data Science. Au nombre de ces concepts, nous avons le Machine Learning qui a constitué tout un cours à travers lequel nous avons étudié différents algorithmes d'apprentissage machine. Ce projet à pour but de mettre en pratique les notions étudiées dans ce cours, en apppliquant les algorithmes à des problèmes de vie réelle. Ainsi le présent projet consiste à faire des prédictions sur des résultats de simulation d'un modèle climatique.

#### 1. Information sur le Dataset 

Le Dataset contient des enregistrements d'un ensemble de simulation de l'incertitude des modèles climatiques.
Les variables ont été construites en utilisant une méthode d'hypercube latin dans le système logiciel UQ Pipeline de LLNL pour échantillonner les incertitudes de 18 paramètres du modèle dans le cadre de la composante POP2 (Parallel Ocean Program) du modèle du système climatique (CCSM4).
Trois ensembles hypercubiques latins distincts ont été réalisés, chacun contenant 180 données de simulations. 46 des 540 simulations ont échoué pour des raisons numériques à des combinaisons de valeurs de paramètres.

L'objectif est d'utiliser les algorithmes Machine Learning de classification pour prédire les résultats des simulations (échec ou réussite) à partir des valeurs des paramètres d'entrée, et d'utiliser l'analyse de sensibilité et la sélection des caractéristiques pour déterminer les causes des accidents de simulation.
Vous pourriez obtenir plus de détails sur les données en cliquant sur le lien [suivant](http://archive.ics.uci.edu/ml/datasets/Climate+Model+Simulation+Crashes)


#### 2. Information sur les variables 

L'objectif est de prédire les résultats des simulations de modèles climatiques (colonne 21, échec ou réussite) en fonction des valeurs des paramètres d'entrée des modèles climatiques (colonnes 3-20).

* Colonne 1 : ID de l'étude de l'hypercube latin (de l'étude 1 à l'étude 3)
* Colonne 2 : ID de la simulation (de 1 à 180)
* Colonnes 3-20 : valeurs de 18 paramètres du modèle climatique mis à l'échelle dans l'intervalle [0, 1].
* Colonne 21 : résultat de la simulation (0 = échec, 1 = succès)


#### 3. Modélisation du problème

Au regard de l'objectif, nous somme en présence d'un problème de classification qui consiste à déterminer la classe (0 ou 1), qui correspond au résultat d'une simulation. 
Nous aurons donc le modèle suivant:

   * Modèle: 
        > X : colonnes 3 à 21, variable de prédiction <br>
        > Y : colonne 21 varibles prédite

   * Données d'apprentissage et de test:
Nous partagerons nos données en deux types de données: **les données d'apprentissage (X_train)** qui constituerons **80%** des données initiales et **les données de test (y_train)** qui constituerons **20%** restants. 
Nous utiliserons plutard les données de test  X_test et y_test pour effectuer la prédiction. 

#### 4.  Algorithmes d'apprentissage: 

Plusieurs algorithmes de classification peuvent être utilisés pour répondre à notre problème. Dans un premier temps, Nous utiliserons quelques unes d'entre elles pour effectuer l'apprentissage de notre modèle et évaluerons leur performance pour ne  retenir les meilleurs. 
Après nous procédérons à la configuration des hyperparamètres des modèles retenus en vue de les rendre plus performants.
Merci de voir le note pour les autres sections du sommaire.


## [VI. Conclusion](#sommaire) <a name='conclusion'><a>
Dans ce projet nous avons étudié un problème de classification binaire. Nous avons débuté par le chargement de nos données et effectué quelques traitements sur ces données avant de réaiser une étude comparative de huit classifiers. La comparaison effectuée, nous avons cinq classifiers qui avaient les scores d'accuracy les plus élevés. Nous avons également pu voir d'autre méthode d'évalutaion notamment le learning curve et ROC curve qui apportent les informations sur la précision des diffierents classifiers. <br>
Nous avions un dataset un peu déséquilibré que et nous avons utilisé une technique de resampling pour reéchantilloner nos données et nous avons remarqué une amélioration de certains classifiers cependant on pouvait voir au niveau des learning curve que les modèles étaient trop adptés qux données d'apprentissage alors nous avons décidé ne pas utilisés les modèles issus de cette approche.<br>
Au final nous retenons que ce projet nous a permis de mettre en pratique beaucoup de notions liées au Machine Learning et il nous a également permis de voir des concepts avancés liés à la performance des algorithmes de classification.




