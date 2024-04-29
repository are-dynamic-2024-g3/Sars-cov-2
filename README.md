# L’immunité post infection du SARS-CoV-2

Notre projet consiste à étudier la propagation du virus dans le temps et l'espace au sein de deux groupes distincts, l'un sans aucune vaccination et l'autre avec un taux de vaccination variable. Dans un premier temps le projet s'est majoritairement inspiré du virus Sars-CoV-2. Mais notre projet n'est pas seulement limité à celui-ci car nos variables sont modifiable telles que la durée d'infection (sans compté la mortalité), la vitesse de propagation, la durée de la vacination, etc...

## Post infection immunity from SARS-CoV-2

Our project is studying the virus spreading in time and space into two differents group, the first one without any vaccination and the other one with a adjustable vaccination rate. In the first time, our project was inspired by the Sars-Cov-2, But of course, our projet can going further because all our variable can be modified as like the the duration of infection, the spreading speed, the duration of vaccination, etc...

## Présentation de l'équipe

| Humain1 | Humain2 |
|-----|--|
| R.Antoine | M.Franck |


## Description synthétique du projet

**Problématique : Comment la présence d'un vaccin influe sur une population lors de la propagation d'un virus ?** 

**Hypothèse : Cela permet d'endiguer sa propagation mais une multitude de facteurs sont a prendre en compte.**

**Objectifs : Determiner l'incidence de la vaccination sur une population donnée en fonction des differents paramètres**

**Critère(s) d'évaluation : Evaluer le taux de personnes infecté en fonction du temps et des differentes variables dans 2 groupes**

## Présentation structurée des résultats

Présentation du choix de modélisation, des outils, du code et des résultats (tableaux, courbes, animations...) (**avec une analyse critique**).
Nous avons choisis de réaliser notre projet via jupyter notebook en python. Nous avons d'abord importer les bibliothèques utile au projet : IMG
puis un code qui permet de generer des mondes aléatoire composé de case vide et d'individus sains : IMG



2 tkinter : un vaccin faible : .GIF , un vaccin fort : .GIF .
expliquer que le vaccin fort pourrait totalement stopper l'infection si prise en compte de l'immun post infection .
## Travail effectué 

### Semaine 1

Aujourd'hui pour bien débuter nous avons fais quelques recherches afin d'essayer de récuperer certaines informations essentielles au bon déroulement du code, tel que le R0, le taux d'immunité et le temps d'infection.
De plus nous avons commencez le codage, en créeant des mondes 2D aléatoire(generate_spacial_world) avec des indivus sain représenté par des 0 et des None (qui est plus tardivemment remplacé par des 1) représentant par exemple des fronctière coupant les individus. Ce n'est pas tout ! En effet nous avons également codé Infection_world qui permet de piocher un individus au hasard et de lui infecter.

### Semaine 2

Cette semaine nous nous somme plus concentré sur le codage en codant plusieurs fonction. Tout d'abord la fonction "creation_parallèle" qui permet de creer un monde parallèle qui va être servit pour "desinfection", un fonction multifonctionnelle, car elle sert en réalité d'un compteur en se basant du monde parallèle d'un monde pour la durée d'infection, et en même temps de désinfecter quand la durée d'infection est atteint. Et en même temps, nous avons codé les fonction "voisins" utilisé dans "verif_voisin" qui permettent de de verifier si il y'a des individus infectable autour des individus infecté (ce code sert donc pour eviter des infections en boucle sur des individus déjà infecter ou encore sur des None qui ne sont pas des individus. 

### Semaine 3

De même, aujourd'hui nous nous sommes plus concentré sur le codage que sur la recherche. Nous avons implémenté en premier la fonction "tour" qui, comme sont nom indique faire un tour en infectant un individu utilisé avec verif_voisin et compèté avec désinfection. Comme notre projet était de se rapprocher de la réalité, nous avons également crée la fonction "déplacement" qui sert à changé de place entre 2 personne ce qui simule les déplacements telle que la migration. Et par la suite nous nous aidons de la fonction "tour" pour créer "tour_boucle" qui prend en plus le "nombre de tour" et la "fréquence de déplacement", en effet cette fonction permet de faire plusieurs tour correspondant à la variable "nombre de tour" complété par la "fréquence de déplament" faisant appel à la fonction déplacement.

### ...







## Lien vers page de blog : <a href="blog.md"> C'est ici ! </a>
