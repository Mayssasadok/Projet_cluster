# Projet_cluster

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
 
• Maitriser l’API de twitter pour l’extraction des tweets
• Maitriser la partie NLP (natural language processing) avec NLTK en Python
• Appliquer les principes de nettoyage des données
• Classer les tweets : regrouper ensemble les tweets qui sont similaires. C’est une étape qui peut
  être considérée comme une étape 
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
-> Ordinateur portable 
-> Système d’exploitation : Windows 10 (64Bits)
-> Processeur :Intel Core i3
-> Mémoire Vive :4 GB

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

Clé consommateur (clé API)
Secret consommateur (secret API)
Jeton d'accès
Access Token Secret

Les données seront des tweets extraits de l'utilisateur. La première chose à faire est d'obtenir la clé du consommateur, le secret du consommateur, la clé d'accès et le secret d'accès du développeur Twitter facilement disponibles pour chaque utilisateur.
Ces clés aideront l'API pour l'authentification.


![api](https://user-images.githubusercontent.com/47771296/102277533-b605b080-3f28-11eb-8dc9-e5dffea6fcc7.PNG)

![text](https://user-images.githubusercontent.com/47771296/102278962-eea68980-3f2a-11eb-8907-727e195b80db.PNG)

## 5. Extraction de 10000 tweets 
![twwt](https://user-images.githubusercontent.com/47771296/102280086-c91a7f80-3f2c-11eb-827c-e3ca08bd69c7.PNG)

Les données utilisées sont extraites de Twitter à l'aide de Tweepy , une bibliothèque python permettant d'accéder à l'API Twitter.
## 6. Nettoyage des tweets
Les tweets contiennent des objets inutiles tels que des hashtags, des mentions, des liens et des signes de ponctuation qui peuvent affecter les performances d'un algorithme et doivent donc être supprimés. Tous les textes sont convertis en minuscules pour éviter que les algorithmes n'interprètent les mêmes mots avec des cas différents comme différents

Tokenisation, lemmatisation et suppression des mots vides
Les mots vides sont des mots couramment utilisés dont la présence dans une phrase a moins de poids que d'autres mots. Ils incluent des mots comme «et», «ou», «a» et.c.
La tokenisation est le processus de division d'une chaîne en une liste de jetons. Une phrase peut être réduite en mots et un mot peut être réduit en lettres à l'aide des tokenizers appropriés.

![token](https://user-images.githubusercontent.com/47771296/102285332-61693200-3f36-11eb-9273-7e69ef8a64fb.PNG)

La lemmatisation réduit un mot à sa forme racine. Par exemple, la forme de racine des « roches » est « roche ».
Les langues utilisées dans les tweets sont principalement l'anglais et le swahili. Ce dernier n'a aucun support donc nous ne travaillerons qu'avec le premier. Cela rend l'analyse paralysée d'une manière étant donné que les textes swahili seront ignorés.


###  *Suppression de ponctuation 

Utilisation de la variable punctuationdu package string. Avant d'utiliser, vous devez importer le package en utilisant la ligne import stringau début du fichier.

string.punctuationcontient tous les caractères de ponctuation pour ne pas avoir à les définir à chaque fois manuellement . 
![remove](https://user-images.githubusercontent.com/47771296/102283800-5eb90d80-3f33-11eb-985d-e8c1a58673ee.PNG)

