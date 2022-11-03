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

## 4. Crédits

Auteur : Jean Ivars, avec la participation de <a href='https://github.com/Bebock'>Hélène</a>
