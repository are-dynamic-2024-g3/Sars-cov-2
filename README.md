## L'influence du vaccin sur la population lors de la propagation d'un virus

Notre projet consiste à étudier la propagation du virus dans le temps et l'espace au sein de deux groupes distincts, l'un sans aucune vaccination et l'autre avec un taux de vaccination variable. Dans un premier temps le projet s'est majoritairement inspiré du virus Sars-CoV-2. Mais notre projet n'est pas seulement limité à celui-ci car la plupart de nos facteurs sont modifiables , telles que la durée d'infection , la vitesse de propagation, la durée de la vacination, etc... Ainsi notre projet ne sera pas seulement limité par un seul virus.

## The Vaccine influence on the population during the spread of a virus

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

## Présentation structurée du code et des résultats:

Nous avons choisi de réaliser notre projet via jupyter notebook en python. 

Nous avons d'abord importé les bibliothèques utiles au projet: 

<img width="747" alt="biblio" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/7dd99020-ecf8-4095-8f08-77e21998f54d">


puis un code qui permet de générer des mondes aléatoires composés de cases vides et d'individus sains:

<img width="744" alt="creamonde" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/85506b05-6669-4550-89b1-a48d551b96a5">


Nous avons ensuite crée un code permettant d'infecter aléatoirement une case non vide dans le monde: 

<img width="629" alt="primoinfection" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/a0ef6ff5-fae5-4a8e-a765-149a05cf14b3">


Ainsi qu'un code pouvant faire une liste des voisins d'une case de coordonnée (x,y) et un autre qui permet d'analyser cette liste et de vérifier si une case répondant aux critères d'infections est encore disponible , ce qui nous à permis de créer une condition d'arrêt pour nos infections . 
Un autre code à été necessaire pour créer un autre tableau à 2 dimensions contenant une information très importante pour la suite du code : la durée depuis laquelle une personne est dans un état x ( infecté ou vacciné ) ce qui nous permet de contrôler quand une cellule arrive à la durée d'expiration de son état actuel. 
 une fois tous les codes réalisé nous avons fait un nouveau code permettant d'effectuer un tour complet de boucle dans une monde pour le moment contenant uniquement des cases vides , des individus sains et d'autres infectés : 
 
 <img width="741" alt="tour base" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/06a33b21-7229-49c5-ba6f-10ceb46c4bb9">


 puis nous avons réalisé la même chose pour une monde contenant aussi une autre possibilité : une personne vaccinée. 

 ## TKINTER:

 Nous avons ensuite décidé de mettre à profit tout le travail réalisé plus tôt avec la bibliothèque *TKINTER* pour avoir une visualisation plus concrète des différents mondes au cours du temps. 
 voici donc le code *TKINTER* utilisé pour réaliser cela: 
 
  
  <img width="592" alt="tk1" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/123e545f-02c9-4ff2-a741-8156c759855e">

Ici nous commençons par créer les deux mondes sur une même base ainsi que leur parallèle contenant les informations de temps. 


<img width="563" alt="tk2" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/98b918e6-bd5f-40f9-9820-82207021182b">

Nous déclarons les différentes variables nécéssaires à la création de la fenêtre *TKINTER* ainsi que de la zone de dessin. 


<img width="700" alt="tk3" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/3036fbd9-3423-4f88-a61d-fd05a3e4cc85">

Et voici le code qui nous permet de gerer la zone de dessin et de la mettre à jour de manière automatique en effectuant un tour de boucle à chaque actualisation.

voici deux exemples de ce que donne la fenêtre*TKINTER* avec les variables utilisées lors de chacune des simulations.


Un cas avec une vaccination forte avec des paramètres élévés:

![Image Extreme](https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160223042/ae1f35ee-1d9e-46b1-9122-eb303fea1209)
![Gif_extreme](https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160223042/1eb39753-5a6c-4082-a212-e662b68a6d88)
en noir : les cases vides.

en blanc : les individus sains.

en rouge : les individus infectés.

en vert : les individus vaccinés.

on voit ici que dans le monde contenant le vaccin la propagation du virus est très limitée et serait surement totalement nulle si l'immunité post-infection était prise en compte.

Un cas où la vaccination sur la population est plus faible:

![Image Soft](https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160223042/9ea82310-2ac4-405f-907b-ec8c89e0909b)
![Gif_soft](https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160223042/33d8df13-1a06-442f-aecb-7daf4e360c49)
en noir : les cases vides.

en blanc : les individus sains.

en rouge : les individus infectés.

en vert : les individus vaccinés.


Ici nous pouvons observer que malgré la présence d'individus vaccinés le virus continue de circuler sans être beaucoup impacté.

## Les courbes :
Pour pouvoir visualiser l'impact des différentes variables individuelement nous avons décider de générer des courbes avec des variables fixe à certaine valeur et une variable unique,
qui change à chaque courbe.

Voici les paramètres utiliser:

<img width="528" alt="variables courbes" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/a15fbde6-6696-46d3-a3f8-643adbbf4e6a">

ainsi qu'un exemple du code utiliser pour les différentes courbes : 

<img width="742" alt="ex code courbe" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/886cab24-66da-4288-b307-641563d21463">


Pour la première courbe nous avons décidé de faire varier le nombre de personne qu'un individu infecté peut contaminer : 

<img width="447" alt="courbe propagation" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/854eb213-7b17-4c25-8f2e-f5f2f7e31de4">

de manière assez logique plus les personnes sont contagieuse plus le nombre d'infectés à la fin de la simulation est grand, une légère différence est présente entre le monde ayant accès au vaccin et celui qui n'y à pas accès mais malgré ça le nombre d'infectés reste très élevé avec l'augmentation de la contagiosité.



Pour la courbe suivante nous avons décider de jouer sur la capacitée des individus à résister à une transmission:

<img width="477" alt="courbe résistance" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/d70959d1-82c1-4ab8-8120-19ac407b2b23">


Sans surprise la baisse est proportionnelle au taux de résistance, la courbe du monde contenant le vaccin tend cependant légèrement plus vite vers 0. Ce facteur est donc très important pour prédire la 
viralitée d'un virus. Mais ce n'est pas la facteur sur le quel il est le plus simple d'influer. 



La troisième courbe fait varier la durée de l'infection dans le temps : 


<img width="444" alt="courbe duree infection" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/b82512d5-6ab2-43ee-85d5-641020139a43">

On peut observer que ce paramètre ne fait que légèrement varier les résultats si l'on fait abstraction de la variance dut  l'aléatoire de l'évolution des mondes qui a un grand impact en raison de leur taille .
De plus l'absence de l'immunité post-infection n'aide pas à avoir une représentation significative pour ce paramètre.



La suivante mets en avant la fluctuation de la durée d'efficacitée du vaccin :


<img width="455" alt="courbe duree efficacité" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/8e29ef50-4ec0-4de5-86eb-0de3e7148af8">

Effectivement la tendance de la courbe est à la baisse avec l'augmentation de la durée, cela s'explique par l'augmentation du nombre d'individu vacciné présent à la fin de la simulation ce qui réduit inévitablement le nombre d'individus infectés et infectable.



Pour la cinquième courbe nous avons décidé de jouer avec le taux d'efficacité du vaccin :


<img width="449" alt="courbe taux immun" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/5691e960-656d-43e7-9633-cbe9e0c8860d">



Nous avons poursuivi avec une analyse suivant le temps entre deux vague de vaccination :


<img width="443" alt="courbe freq vaccin" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/67afec60-57db-442b-b442-234ef0bc7a91">


Malgré la variance , il est très clair et très visible que plus il y a du temps entre les vagues de vaccinations plus le nombre d'infectés est élevé ce qui s'exlique par la réduction du nombre total de personne vacciner dans le monde au fur et à mesure du nombre de tour.



Pour finir une courbe mettant en avant la différence suivant le nombre de vaccin par vague de vaccination : 


<img width="455" alt="courbe vaccin partour" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/eaa83b5b-289f-497d-91aa-2885d5bdf14d">

Cette courbe est surement la plus explicite, effectivement malgré une variance possible dut à l'aléatoire le résultat reste très linéaire et une tendance très clair se dessine.

**Conclusion**: 
Les differentes variables ont une incidence plus ou moins visible sur le nombre d'infectés mais c'est l'accumulation de ces dernière que l'on obtient le meilleur resultat, de plus le monde est drastiquement simplifié par rapport à un cas réel ce qui explique certaines différence avec la réalité , l'absence de la prise en compte de l'immunité post-infection et la prise en compte de l'evolution du virus sont les deux plus gros facteurs non pris en compte dans notre réalisation, il serait donc très interessant de voir l'évolution des résultats avec l'ajout de ces derniers. Introduire une immunité dégressive serait aussi une piste très intéressante pour rendre notre simulation plus proche de la réalité mais demanderait plu de temps pour être implémenté et demanderait une optimsation plus poussé du code acutel pour éviter d'avoir un code final trop lourd lors de l'execution.

## Compte rendu

### Semaine 1

Aujourd'hui pour bien débuter nous avons fais quelques recherches afin d'essayer de récuperer certaines informations essentielles au bon déroulement du code, tel que le R0, le taux d'immunité et le temps d'infection.
De plus nous avons commencez le codage, en créeant des mondes 2D aléatoire(generate_spacial_world) avec des indivus sain représenté par des 0 et des None (dans les semaines à venir nous avons changé les None par des 0, 0 par des 1, et 1 par des 2 car nous aurons besoin de ces chnagement pour le TKinter) représentant par exemple des fronctière coupant les individus. Ce n'est pas tout ! En effet nous avons également codé Infection_world qui permet de piocher un individus au hasard et de lui infecter.

### Semaine 2

Cette semaine nous nous somme plus concentré sur le codage en codant plusieurs fonction. Tout d'abord la fonction "creation_parallèle" qui permet de creer un monde parallèle qui va être servit pour "desinfection", un fonction multifonctionnelle, car elle sert en réalité d'un compteur en se basant du monde parallèle d'un monde pour la durée d'infection, et en même temps de désinfecter quand la durée d'infection est atteint. Et en même temps, nous avons codé les fonction "voisins" utilisé dans "verif_voisin" qui permettent de de verifier si il y'a des individus infectable autour des individus infecté (ce code sert donc pour eviter des infections en boucle sur des individus déjà infecter ou encore sur des None qui ne sont pas des individus. 

### Semaine 3

De même, aujourd'hui nous nous sommes plus concentré sur le codage que sur la recherche, Par ailleurs plus nous avençons dans le codage, plus nous remarquons que les recherches n'était pas nécessaire puisque tous nos facteurs sont présenté par des variables. Nous avons implémenté en premier la fonction "tour" qui, comme sont nom indique faire un tour en infectant un individu utilisé avec verif_voisin et compèté avec désinfection. Comme notre projet était de se rapprocher de la réalité, nous avons également crée la fonction "déplacement" qui sert à changé de place entre 2 personne ce qui simule les déplacements telle que la migration. Et par la suite nous nous aidons de la fonction "tour" pour créer "tour_boucle" qui prend en plus le "nombre de tour" et la "fréquence de déplacement", en effet cette fonction permet de faire plusieurs tour correspondant à la variable "nombre de tour" complété par la "fréquence de déplament" faisant appel à la fonction déplacement.

### Semaine 4

Bonjour, la dernière fois nous avons terminé la fonction "tour_boucle" qui stimule la propagation du virus dans le premier monde, donc dans celui avec sans vaccin. Aujourd'hui nous attaquons donc le deuxième monde avec vaccin, comme on peu s'attendre, on a implémenté la fonction "vaccin" qui permet de vacciner un individu non infecté de manière aléatoire et ces individus seront indiqué par des 2 (plus tard devenus 3 pour TKinter). Cependant ces individus ne doivent pas se relacher, en effet être vacciné ne signifie pas 100% protégé du virus, nous avons donc créer la fonction "infection_vaccin" qui permet de se jouer sur la chance (une variable aléatoire de 0 à 1 comme dans la vrai vie) si la chance est plus fort que le "taux d'immunité" donné par le vaccin, alors l'individu sera infecté.
Ces 2 fonctions nous a pas pris énormémment de temps, donc nous avons profiter pour faire "devaccin" en se basant sur la fonction "désinfection" ce qui les rend assez similaire mais avec des entrées de variables différents et des fonctionnalités qui diffère un peu.

## Semaine 5

Cette semaine, compraré au précédante, nous avons eu quelque difficulté en plus. Tout d'abord nous avons commencé avec la fonction "tour_vaccin" et "tour_boucle_vaccin" en se basant sur les fonction "tour" et "tour_boucle", leurs utilités ne sont donc pas difficile à deviner. Le premier sert à faire un tour sur la base de "tour" mais avec les fonction : "devaccin", "vaccin" et "infection_vaccin" et le deuxième sert à faire plusieurs tour en fonction du variable nb_tour, des déplacement en fonction de la fréquence_deplacement, et enfin la vaccination en fonction de la fréquence_vaccin.
Et le plus difficile reste à comprendre la fonction TKinter qui permet de simuler nos fonction, de nos mondes créer. Pour cela nous avons seulement analysé la bibliothèque de tkinter.

## Semaine 6 

Après avoir pris le temps à analyser la bibliothèque TKinter, nous avons pu codé la fonction cycle_entier et la fonctier fenetre qui nous permet de montrer la simulation de nos mondes (l'évolution de nos mondes) en fonction de nos codes, cependant pour que la fonction fenetre marche bien nous avons fait quelque changement sur la façon d'appeller: "None" (deviens)-> "0" , "0" -> "1" , "1" -> "2" et "2" -> "3".
Et par la suite avec le peu de temps qui nous restait, nous avons redéfini les variables en utilisant la bibliothèque "numpy" (cf nom avec "var" au début) pour que les variables soient utilisables afin de tracer les courbes.

## Semaine 7

Sans surprise, comment peut on parler de science sans preuve donc les courbes, cette semaine nous sommes consacré à la création des courbes en nous appuyant sur les fonction précédemment fait ("tour_boucle" et "tour_boucle_vaccin" :
."Le nombre d'infecté en fonction de la fréquence de la propagation"
."Le nombre d'infecté en fonction du taux de ne pas se faire infecté"
."Le nombre d'infecté en fonction de la durée d'infection"
."Le nombre d'infecté en fonction la durée de vaccin"
."Le nombre d'infecté en fonction du taux d'immunitée"
."Le nombre d'infecté en fonction de la fréquance de vaccination"
."Le nombre d'infecté en fonction du nombre de vaccin par tour"








## Lien vers page de blog : <a href="blog.md"> C'est ici ! </a>
