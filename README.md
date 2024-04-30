# L’immunité post infection du SARS-CoV-2

Notre projet consiste à étudier la propagation du virus dans le temps et l'espace au sein de deux groupes distincts, l'un sans aucune vaccination et l'autre avec un taux de vaccination variable. Dans un premier temps le projet s'est majoritairement inspiré du virus Sars-CoV-2. Mais notre projet n'est pas seulement limité à celui-ci car la plus part des variables sont modifiables , telles que la durée d'infection , la vitesse de propagation, la durée de la vacination, etc...

## Post infection immunity from SARS-CoV-2

Our project is studying the virus spreading in time and space into two differents group, the first one without any vaccination and the other one with a adjustable vaccination rate. In the first time, our project was inspired by the Sars-Cov-2, But of course, our projet can going further because all our variable can be modified as like the the duration of infection, the spreading speed, the duration of vaccination, etc...

## Présentation de l'équipe

| Humain1 | Humain2 |
|-----|--|
| R.Antoine | M.Franck |


## Description synthétique du projet

**Problématique : Comment la présence d'un vaccin influe sur une population lors de la propagation d'un virus ?** 

**Hypothèse : Cela permet d'endiguer sa propagation mais une multitude de facteurs sont à prendre en compte.**

**Objectifs : Determiner l'incidence de la vaccination sur une population donnée en fonction des differents paramètres.**

**Critère(s) d'évaluation : Evaluer le taux de personnes infectées en fonction du temps et des differentes variables dans 2 groupes.**

## Présentation structurée des résultats

Présentation du choix de modélisation, des outils, du code et des résultats (tableaux, courbes, animations...) (**avec une analyse critique**).

Nous avons choisi de réaliser notre projet via jupyter notebook en python. 

Nous avons d'abord importé les bibliothèques utiles au projet : 
<img width="747" alt="biblio" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/7dd99020-ecf8-4095-8f08-77e21998f54d">

puis un code qui permet de générer des mondes aléatoires composés de cases vides et d'individus sains :

<img width="744" alt="creamonde" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/85506b05-6669-4550-89b1-a48d551b96a5">

Nous avons ensuite créer un code permettant d'infecter aléatoirement une case non vide dans le monde : 

<img width="629" alt="primoinfection" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/a0ef6ff5-fae5-4a8e-a765-149a05cf14b3">

Ainsi qu'un code pouvent faire une liste des voisins d'une case de coordonnée (x,y) et un autre qui permet d'analyser cette liste et de vérifier sur une case répondant au critères d'infections est encore disponible , ce qui nous à permis de créer une condition d'arrêt pour nous infections . 
Un autre code à été necessaire pour créer un autre tableau a 2dimension contenant une information très importante pour la suite du code : la durée depuis la quelle une personne est dans un état x ( infecté ou vacciné ) ce qui nous permet de contrôler quand une cellule arrive à la durée 
d'expiration de son état actuel. 
 une fois tous les codes réaliser nous avons fait un nouveau code permettant d'effectuer un tour complet de boucle dans une monde pour le moment contenant uniquement des cases vides , des individus saints et d'autres infectés : 
 
 <img width="741" alt="tour base" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/06a33b21-7229-49c5-ba6f-10ceb46c4bb9">

 puis nous avons réaliser la même chose pour une monde contenant aussi une autre possibilitée : une personne vaccinée. 

 ## TKINTER:

 Nous avons ensuite décidé de mettre à profit tout le travail réalisé plus tôt avec la bibliothèque *TKINTER* pour avoir une visualisation plus concrète des différents monde au cours du temps. 
 voici donc le code *TKINTER* utilisé pour réaliser cela: 
 <img width="592" alt="tk1" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/123e545f-02c9-4ff2-a741-8156c759855e">
ici nous commençons par créer les deux mondes sur une même base ainsi que leur parallèle contenant les informations de temps. 

<img width="563" alt="tk2" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/98b918e6-bd5f-40f9-9820-82207021182b">
Nous déclarons les différentes variables nécéssaire à la création de la fenetre *TKINTER* ainsi que de la zone de dessin. 

<img width="700" alt="tk3" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/3036fbd9-3423-4f88-a61d-fd05a3e4cc85">
Et voici le code qui nous permet de gerer la zone de dessin et de la mettre à jour de manière automatique en effectuant un tour de boucle à chaque actualisation.

voici deux exemple de ce que donne la fenetre tkinter avec les variables utiliser lors de chacunes des simunations.

Un cas avec une vaccination forte avec des paramètre élévés:

![Image Extreme](https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160223042/ae1f35ee-1d9e-46b1-9122-eb303fea1209)
![Gif_extreme](https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160223042/1eb39753-5a6c-4082-a212-e662b68a6d88)

Un cas ou la vaccination sur la population est plus faible:

![Image Soft](https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160223042/9ea82310-2ac4-405f-907b-ec8c89e0909b)
![Gif_soft](https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160223042/33d8df13-1a06-442f-aecb-7daf4e360c49)

2 tkinter : un vaccin faible : .GIF , un vaccin fort : 

expliquer que le vaccin fort pourrait totalement stopper l'infection si prise en compte de l'immun post infection .

Les Courbes:



## Compte rendu

### Semaine 1

Aujourd'hui pour bien débuter nous avons fais quelques recherches afin d'essayer de récuperer certaines informations essentielles au bon déroulement du code, tel que le R0, le taux d'immunité et le temps d'infection.
De plus nous avons commencez le codage, en créeant des mondes 2D aléatoire(generate_spacial_world) avec des indivus sain représenté par des 0 et des None (qui est plus tardivemment remplacé par des 1) représentant par exemple des fronctière coupant les individus. Ce n'est pas tout ! En effet nous avons également codé Infection_world qui permet de piocher un individus au hasard et de lui infecter.

### Semaine 2

Cette semaine nous nous somme plus concentré sur le codage en codant plusieurs fonction. Tout d'abord la fonction "creation_parallèle" qui permet de creer un monde parallèle qui va être servit pour "desinfection", un fonction multifonctionnelle, car elle sert en réalité d'un compteur en se basant du monde parallèle d'un monde pour la durée d'infection, et en même temps de désinfecter quand la durée d'infection est atteint. Et en même temps, nous avons codé les fonction "voisins" utilisé dans "verif_voisin" qui permettent de de verifier si il y'a des individus infectable autour des individus infecté (ce code sert donc pour eviter des infections en boucle sur des individus déjà infecter ou encore sur des None qui ne sont pas des individus. 

### Semaine 3

De même, aujourd'hui nous nous sommes plus concentré sur le codage que sur la recherche. Nous avons implémenté en premier la fonction "tour" qui, comme sont nom indique faire un tour en infectant un individu utilisé avec verif_voisin et compèté avec désinfection. Comme notre projet était de se rapprocher de la réalité, nous avons également crée la fonction "déplacement" qui sert à changé de place entre 2 personne ce qui simule les déplacements telle que la migration. Et par la suite nous nous aidons de la fonction "tour" pour créer "tour_boucle" qui prend en plus le "nombre de tour" et la "fréquence de déplacement", en effet cette fonction permet de faire plusieurs tour correspondant à la variable "nombre de tour" complété par la "fréquence de déplament" faisant appel à la fonction déplacement.

### ...







## Lien vers page de blog : <a href="blog.md"> C'est ici ! </a>
