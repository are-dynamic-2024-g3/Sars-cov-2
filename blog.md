## Travail effectué 

=> Description hebdomadaire du travail effectué (variez les auteurs !)

### Semaine 1

Aujourd'hui pour bien débuter nous avons fais quelques recherches afin d'essayer de récuperer certaines informations essentielles au bon déroulement du code, tel que le R0, le taux d'immunité et le temps d'infection.
De plus nous avons commencez le codage, en créeant des mondes 2D alatoire(generate_spacial_world) avec des indivus sain représenté par des 0 et des None (qui est plus tardivemment remplacé par des 1) représentant par exemple des fronctière coupant les individus. Ce n'est pas tout ! En effet nous avons également codé Infection_world qui permet de piocher un individus au hasard et de lui infecter.

### Semaine 2

Cette semaine nous nous somme plus concentré sur le codage en codant plusieurs fonction. Tout d'abord la fonction "creation_parallèle" qui permet de creer un monde parallèle qui va être servit pour "desinfection", un fonction multifonctionnelle, car elle sert en réalité d'un compteur en se basant du monde parallèle d'un monde pour la durée d'infection, et en même temps de désinfecter quand la durée d'infection est atteint. Et en même temps, nous avons codé les fonction "voisins" utilisé dans "verif_voisin" qui permettent de de verifier si il y'a des individus infectable autour des individus infecté (ce code sert donc pour eviter des infections en boucle sur des individus déjà infecter ou encore sur des None qui ne sont pas des individus. 

### Semaine 3

De même, aujourd'hui nous nous sommes plus concentré sur le codage que sur la recherche. Nous avons implémenté en premier la fonction "tour" qui, comme sont nom indique faire un tour en infectant un individu utilisé avec verif_voisin et compèté avec désinfection. Comme notre projet était de se rapprocher de la réalité, nous avons également crée la fonction "déplacement" qui sert à changé de place entre 2 personne ce qui simule les déplacements telle que la migration. Et par la suite nous nous aidons de la fonction "tour" pour créer "tour_boucle" qui prend en plus le "nombre de tour" et la "fréquence de déplacement", en effet cette fonction permet de faire plusieurs tour correspondant à la variable "nombre de tour" complété par la "fréquence de déplament" faisant appel à la fonction déplacement.

### ...

<a href="index.html"> Retour à la page principale </a>
