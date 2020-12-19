# Projet_cluster


[![Binder](https://mybinder.org/badge_logo.svg)](https://gesis.mybinder.org/binder/v2/gh/Mayssasadok/Projet_cluster/6d2ed1a579f44310d29abe827bbfd94a2fc05f4f)

![imgisi](https://user-images.githubusercontent.com/47771296/102260350-9d899c00-3f10-11eb-945d-172dd56f2184.PNG)

 ##  Université de Sousse : Institut Supérieur d’Informatique et des Techniques de Communication  d’Hammam Sousse - Cycle Ingénieur en Téléinformatique

  ### Réalisé par Sadok Mayssa 3DNI2 
  
 ## Projet–Fouille de Données
                 Thème : Classification des Tweets
 
   ![tww](https://user-images.githubusercontent.com/47771296/102263048-22c28000-3f14-11eb-911e-124ca8040025.jpg)
   
   
### cadre de projet : 
   
Durant le 3éme année cycle d’ingénieur  au sein de l’institut supérieur d’informatique et de télécommunication de hammem Sousse 
nous somme appelés à réaliser le projet intutilé "classification des tweets". 
le projet portera sur la classification selon plusieurs étapes . 
   
 ### Objectifs :
 
##### • Maitriser l’API de twitter pour l’extraction des tweets
##### • Maitriser la partie NLP (natural language processing) avec NLTK en Python
##### • Appliquer les principes de nettoyage des données
##### • Classer les tweets : regrouper ensemble les tweets qui sont similaires. C’est une étape qui peut
 #####  être considérée comme une étape 
  # I. Partie théorique 
 ##  1. Tweeter
Twitter est un réseau social populaire où les utilisateurs partagent des messages appelés tweets. Twitter nous permet d'exploiter les données de tout utilisateur en utilisant l'API Twitter ou Tweepy
## 2. Le clustering 
le clustering est une méthode d'analyse statistique utilisée pour organiser des données brutes en silos homogènes. 

A l'intérieur de chaque grappe, les données sont regroupées selon une caractéristique commune. 

L'outil d'ordonnancement est un algorithme qui mesure la proximité entre chaque élément à partir de critères définis.
Exemple de cluster : kameans

# II. Partie Pratique 
## 1. Evironnement de travail : 
 ### * Environnement logiciel :
 Jupyter est une application web utilisée pour programmer dans plus de 40 langages de programmation, dont Python, Julia, Ruby, R, ou encore Scala2. Jupyter est une évolution du projet IPython. Jupyter permet de réaliser des calepins ou notebooks, c'est-à-dire des programmes contenant à la fois du texte en markdown et du code en Julia, Python, R... Ces calepins sont utilisés en science des données pour explorer et analyser des données.
      
![jup](https://user-images.githubusercontent.com/47771296/102266998-8bf8c200-3f19-11eb-9cc7-bfc34dbad880.PNG)
 ### * Environnement matériel  :
#####  -> Ordinateur portable 
 ##### -> Système d’exploitation : Windows 10 (64Bits)
#####  -> Processeur :Intel Core i3
#####  -> Mémoire Vive :4 GB

## 2. création d'un compte tweeterdevelopper 
### * Création de compte 
![dev1](https://user-images.githubusercontent.com/47771296/102264973-ad0be380-3f16-11eb-9805-807b79305781.PNG)


![dev2](https://user-images.githubusercontent.com/47771296/102265447-6a96d680-3f17-11eb-8b69-2fc6a20ef3cc.PNG)

### * Sauvgarde des clés
  
  ![saugarde](https://user-images.githubusercontent.com/47771296/102266112-4c7da600-3f18-11eb-9682-a188fd5e26bf.PNG)
 ##  3. Installation des bibliothéques 
 ### * Tweepy
 Tweepy prend en charge l'accès à Twitter via l'authentification de base et la nouvelle méthode, OAuth. Twitter a cessé d'accepter l'authentification de base, donc OAuth est désormais le seul moyen d'utiliser l'API Twitter.
 
 ![ins1](https://user-images.githubusercontent.com/47771296/102269451-f0695080-3f1c-11eb-9cab-c4b683572f82.PNG)
 ### * Spacy
 SpaCy est une bibliothèque logicielle Python de traitement automatique des langues 
La bibliothèque SpaCy permet d'effectuer les opérations d'analyse suivantes3 sur des textes dans plus de 50 langues
![spacy](https://user-images.githubusercontent.com/47771296/102271021-0b3cc480-3f1f-11eb-81c0-4a5990d84813.PNG)
### * Importation des bibliothéques 
![les bibliothéque](https://user-images.githubusercontent.com/47771296/102272178-a71b0000-3f20-11eb-91ac-9b73cbeae76b.PNG)

## 4. Authentification et Affichage des tweets 
À partir de compte tweeter develloper qu'ona  créer, ona enregistrer les informations suivantes dans un script appelé credentials.py:

* Clé consommateur (clé API)
* Secret consommateur (secret API)
* Jeton d'accès
* Access Token Secret

Les données seront des tweets extraits de l'utilisateur. La première chose à faire est d'obtenir la clé du consommateur, le secret du consommateur, la clé d'accès et le secret d'accès du développeur Twitter facilement disponibles pour chaque utilisateur.
Ces clés aideront l'API pour l'authentification.


![api](https://user-images.githubusercontent.com/47771296/102277533-b605b080-3f28-11eb-8dc9-e5dffea6fcc7.PNG)

![ccc](https://user-images.githubusercontent.com/47771296/102531553-c477d780-40a2-11eb-8ca7-fc0126144fa5.PNG)

## 5. Extraction de 10000 tweets 

![extra](https://user-images.githubusercontent.com/47771296/102533231-6d273680-40a5-11eb-85eb-188723f65516.PNG)


Les données utilisées sont extraites de Twitter à l'aide de Tweepy , une bibliothèque python permettant d'accéder à l'API Twitter.

![bbb](https://user-images.githubusercontent.com/47771296/102531000-fd637c80-40a1-11eb-968e-688a6fc7a692.PNG)
## 6. Stockage de tweet dans un fichier.CSV

![stockage](https://user-images.githubusercontent.com/47771296/102532199-e58cf800-40a3-11eb-8275-314488a0b1d4.PNG)

affichage des caractéristiques des tweets 

![caracte](https://user-images.githubusercontent.com/47771296/102532806-ce9ad580-40a4-11eb-8aa9-8b4e30cfb11d.PNG)

## 7. Nettoyage des tweets
Les tweets contiennent des objets inutiles tels que des hashtags, des mentions, des liens et des signes de ponctuation qui peuvent affecter les performances d'un algorithme et doivent donc être supprimés. Tous les textes sont convertis en minuscules pour éviter que les algorithmes n'interprètent les mêmes mots avec des cas différents comme différents

Tokenisation, lemmatisation et suppression des mots vides
Les mots vides sont des mots couramment utilisés dont la présence dans une phrase a moins de poids que d'autres mots. Ils incluent des mots comme «et», «ou», «a» et.c.

## La tokenisation:
est le processus de division d'une chaîne en une liste de jetons. Une phrase peut être réduite en mots et un mot peut être réduit en lettres à l'aide des tokenizers appropriés.


![tok](https://user-images.githubusercontent.com/47771296/102677380-6cc09580-41a2-11eb-9b5e-d7f7fbc9ffcd.PNG)

![token](https://user-images.githubusercontent.com/47771296/102677130-36cee180-41a1-11eb-96ca-a30b9315540b.PNG)

## La lemmatisation:
réduit un mot à sa forme racine. Par exemple, la forme de racine des « roches » est « roche ».
Les langues utilisées dans les tweets sont principalement l'anglais et le swahili. Ce dernier n'a aucun support donc nous ne travaillerons qu'avec le premier. Cela rend l'analyse paralysée d'une manière étant donné que les textes swahili seront ignorés.

![lemmm](https://user-images.githubusercontent.com/47771296/102677212-b52b8380-41a1-11eb-84b8-5a69cad3a698.PNG)

###  *Suppression de ponctuation 

Utilisation de la variable punctuationdu package string. Avant d'utiliser, vous devez importer le package en utilisant la ligne import stringau début du fichier.

string.punctuationcontient tous les caractères de ponctuation pour ne pas avoir à les définir à chaque fois manuellement .

![remove](https://user-images.githubusercontent.com/47771296/102283800-5eb90d80-3f33-11eb-985d-e8c1a58673ee.PNG)

### -> Résultat 

![supresion](https://user-images.githubusercontent.com/47771296/102676622-b5764f80-419e-11eb-80e3-edbcd628bac2.PNG)

### * La bibliothéque NLTK

Il existe dans la librairie NLTK une liste par défaut des stopwords dans plusieurs langues, notamment le français.
Mais nous allons faire ceci d'une autre manière : on va supprimer les mots les plus fréquents du corpus et considérer qu'il font partie du vocabulaire commun et n'apportent aucune information. 
Ensuite on supprimera aussi les stopwords fournis par NLTK.
La première manipulation souvent effectuée dans le traitement du texte est la suppression de ce qu'on appelle en anglais
les stopwords. Ce sont les mots très courants dans la langue étudiée ("et", "à", "le"... en français) 
qui n'apportent pas de valeur informative pour la compréhension du "sens" d'un document et corpus. 
Il sont très fréquents et ralentissent notre travail : nous souhaitons donc les supprimer.


![stopword](https://user-images.githubusercontent.com/47771296/102288568-0d158080-3f3d-11eb-81c9-8f32072b07ec.PNG)

le mots les mots le plus courants dans la langue anglaise 

![en](https://user-images.githubusercontent.com/47771296/102289024-ffacc600-3f3d-11eb-8898-8a1ac333b94c.PNG)

### * la stemming
La stemming est une sorte de normalisation des mots. La normalisation est une technique dans laquelle un ensemble de mots dans une phrase est converti en une séquence pour raccourcir sa recherche. Les mots qui ont le même sens mais qui présentent des variations selon le contexte ou la phrase sont normalisés.*


![nn](https://user-images.githubusercontent.com/47771296/102289408-e6584980-3f3e-11eb-98c9-891ddfc43244.PNG)
## Résultat : 
![stemming](https://user-images.githubusercontent.com/47771296/102677074-e8b9de00-41a0-11eb-9ed9-d55359bd0695.PNG)



![jjj](https://user-images.githubusercontent.com/47771296/102292160-ea876580-3f44-11eb-891b-cebf69c4091d.PNG)
###  L'ensemble de données après le nettoyage 
![apres nett](https://user-images.githubusercontent.com/47771296/102536097-67cbeb00-40a9-11eb-839d-0794191fb148.PNG)

### --> les  tweets  aprés les nettoyage sont stokées dans une une autre fichier.CSV 

![stockage aprés](https://user-images.githubusercontent.com/47771296/102558662-3ca7c280-40ce-11eb-8666-18192848f6e6.PNG)

### Suppression de hashtag
Les tweets contiennent des objets inutiles tels que des hashtags, des mentions, des liens et des signes de ponctuation qui peuvent affecter les performances d'un algorithme et doivent donc être supprimés. Tous les textes sont convertis en minuscules pour éviter que les algorithmes n'interprètent les mêmes mots avec des cas différents comme différents

![supphas](https://user-images.githubusercontent.com/47771296/102560035-8c3bbd80-40d1-11eb-8c2a-959344530705.PNG)
![lemm](https://user-images.githubusercontent.com/47771296/102560265-1d129900-40d2-11eb-854f-442193ad057a.PNG)

### Extraction des feautres 
Convertir une collection de documents texte en une matrice de nombres de jetons.
CountVectorizer implémente à la fois la tokenisation et le comptage des occurrences dans une seule classe . 
fit_transform () est utilisé sur les données d'entraînement afin que nous puissions mettre à l'échelle les données d'entraînement et également apprendre les paramètres de mise à l'échelle de ces données

![extraction des feautres](https://user-images.githubusercontent.com/47771296/102561835-f8b8bb80-40d5-11eb-99cd-5603755e91e5.PNG)

### K-means clustering 

Le clustering K-Means est un algorithme d'apprentissage automatique non supervisé. Contrairement aux algorithmes traditionnels d'apprentissage automatique supervisé, K-Means tente de classer les données sans avoir d'abord été formé avec des données étiquetées. Une fois l'algorithme exécuté et les groupes définis, toute nouvelle donnée peut être facilement affectée au groupe le plus pertinent.
WCSS est défini comme la somme de la distance au carré entre chaque membre du cluster et son centre de gravité .

![kmeans](https://user-images.githubusercontent.com/47771296/102563322-45ea5c80-40d9-11eb-9a4d-30df1e5e83a2.PNG)
![gg](https://user-images.githubusercontent.com/47771296/102563684-1f78f100-40da-11eb-9755-19a1e7636ab6.PNG)

Nous représentons la relation entre le nombre de clusters et la somme des carrés au sein des clusters (WCSS), puis nous sélectionnons le nombre de clusters où le changement de WCSS commence à se stabiliser (méthode du coude)

![rep](https://user-images.githubusercontent.com/47771296/102563848-826a8800-40da-11eb-9d47-ba53fbcf22e6.PNG)

### Affichage des termes par  cluster 

![term](https://user-images.githubusercontent.com/47771296/102564240-4a177980-40db-11eb-8134-f62bf94c1122.PNG)

## Exemple : 

![Exe](https://user-images.githubusercontent.com/47771296/102564485-d6c23780-40db-11eb-9baa-422368aaee8f.PNG)

### Affichage des tweets de chaque cluster : 

![ff](https://user-images.githubusercontent.com/47771296/102607194-2595be80-4128-11eb-9ab5-fb6c593be93e.PNG) 

 ### Resultats :
 
![kk](https://user-images.githubusercontent.com/47771296/102607324-67bf0000-4128-11eb-8fdb-9599a506fe28.PNG)

#### Ensembles de mots


##  --> Le bloc ci-dessous représente des mots liés à l'économie. Il existe 3 autres ensembles de ce type ( social_related_words , health_related_words et culture_related_words ) pour les 3 groupes restants : 

![cc](https://user-images.githubusercontent.com/47771296/102608088-9f7a7780-4129-11eb-9188-795fd0b0c465.PNG)

![vv](https://user-images.githubusercontent.com/47771296/102608540-51b23f00-412a-11eb-9177-35ad477e60ce.PNG)

Tout comme les tweets, ils doivent subir un pré-traitement. La fonction fournie utilisée sur les tweets est appliquée sur les sets 

![oo](https://user-images.githubusercontent.com/47771296/102608733-a950aa80-412a-11eb-8e79-78e6edfd9c29.PNG)

Les doublons sont également supprimés:

![ppp](https://user-images.githubusercontent.com/47771296/102609210-64794380-412b-11eb-9057-4cdadf52faf5.PNG)

### Scores de similarité Jaccard

![rrr](https://user-images.githubusercontent.com/47771296/102609396-b0c48380-412b-11eb-91a9-66fe5f632e80.PNG)

### Trame de données en cluster
Nous souhaitons créer une base de données contenant le nombre total de tweets par catégorie et par personne. Une base de données 4D avec la colonne d'index remplie d'utilisateurs, et 3 autres colonnes contenant le nombre total de tweets de l'utilisateur dans les classes sociales, culturelles, sanitaires et économiques.
Cela peut être réalisé d'abord en créant un bloc de données contenant les scores Jaccard pour chaque tweet pour chaque catégorie, puis en attribuant un tweet à une catégorie en fonction du score le plus élevé et enfin en regroupant les tweets par nom d'utilisateur et somme des tweets.

![mmm](https://user-images.githubusercontent.com/47771296/102610545-aa370b80-412d-11eb-84c7-51a382516eae.PNG)

#### Scores de similarité Jaccard

![sccc](https://user-images.githubusercontent.com/47771296/102612574-40206580-4131-11eb-8409-9201d5d20e26.PNG)

#### Matrice des tweets 

![ex](https://user-images.githubusercontent.com/47771296/102613063-1d428100-4132-11eb-806f-687b1bf225c8.PNG)

#### volumes de tweets dans les différentes catégories:

![ll](https://user-images.githubusercontent.com/47771296/102614163-0b61dd80-4134-11eb-8102-a6ecd5c8b5ae.PNG)
![vvv](https://user-images.githubusercontent.com/47771296/102614258-31877d80-4134-11eb-8788-299fd7fa5841.PNG)

## Intérprétation 

La santé a le plus grand pourcentage. Cela pourrait être le résultat de la pandémie actuelle dont tout le monde parle.
Les données peuvent être utilisées pour de nombreuses analyses et de belles visualisations, mais l'objectif de l'article est l'analyse de cluster.

## Conclusion 
Le traitement du langage naturel est un vaste domaine et il y a tellement plus à faire sur les données pour obtenir des informations plus précises et utiles. 




