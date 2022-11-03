# Projet Disaster Tweets : reconnaissance de tweets sur des catastrophes

## 1. Objectif

Twitter est devenu un important réseau de communication en cas d'urgence. L'omniprésence des smartphones permet aux gens d'annoncer une urgence qu'ils observent en temps réel. C'est pourquoi de plus en plus d'organismes s'intéressent à la surveillance programmatique de Twitter (par exemple, les organisations de secours en cas de catastrophe et les agences de presse).

Ainsi, le projet "Disaster Tweets" a pour but, à l'aide d'outils de deep learning, de reconnaître des tweets revêtant d'une vraie catastrophe, prenant ainsi en compte le contexte, exemple :
<ol>
  <li>"I would kill to eat"</li>
  <li>"I would kill him"</li>
</ol>
La (1) et la (2) possèdent le même mot clef "kill", le premier ne revêt cependant pas d'un caractère dangereux contrairement au deuxième.

## 2. Data overview

Le training set possède 7503 tweets répartis de la façon suivante :

![download](https://user-images.githubusercontent.com/96300465/199680269-ae864f0b-9325-4536-b222-9253620c14cd.png)

Le dataset de training est assez équilibré, cependant les données étant extraites du site Twitter, un pre-processing sur les caractères est nécessaire afin de pouvoir entraîner les algorithmes, avec <code>regex</code> pour le nettoyage des caractères spéciaux et <code>spacy</code> pour la lemmatisation.

## 3. Aperçu des résultats 

Pour témoigner de la qualité du pre-processing, un <code>wordcloud</code> a été effectué sur chacune des target du dataset de train :

Target = 0 (non-disaster tweet) :
![download](https://user-images.githubusercontent.com/96300465/199686110-3fa28cc7-1222-4e62-9bec-a01eb5af26a3.png)

Target = 1 (disaster tweet) :
![download](https://user-images.githubusercontent.com/96300465/199686127-c549e3d5-c79f-4637-8dcd-17b48b2fd6f2.png)

On retrouve des mots clef du champ lexical de la catastrophe dans le deuxième <code>wordcloud</code> que l'on ne retrouve pas dans le premier.

Ainsi, pour l'entrainement du modèle, le module <code>keras</code> de <code>TensorFlow</code> a été utilisé. Le modèle optimal comporte ainsi 4 couches dont deux fonctions d'activation, une relu et une sigmoid pour les résultats suivants :

![download](https://user-images.githubusercontent.com/96300465/199682061-9c33726a-cf4d-4b2e-b311-40020dc8cffa.png)

## 4. Crédits

Auteur : Jean Ivars, avec la participation d'<a href='https://github.com/Bebock'>Hélène</a>
