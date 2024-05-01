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
Pour pouvoir visualiser l'impact des différentes variables individuellement nous avons décidé de générer des courbes avec des variables fixées à certaines valeurs et une variable unique,
qui change à chaque courbe.

Voici les paramètres utilisés:

<img width="528" alt="variables courbes" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/a15fbde6-6696-46d3-a3f8-643adbbf4e6a">

ainsi qu'un exemple du code utilisé pour les différentes courbes : 

<img width="742" alt="ex code courbe" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/886cab24-66da-4288-b307-641563d21463">


Pour la première courbe nous avons décidé de faire varier le nombre de personnes qu'un individu infecté peut contaminer : 

<img width="447" alt="courbe propagation" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/854eb213-7b17-4c25-8f2e-f5f2f7e31de4">

de manière assez logique plus les personnes sont contagieuses, plus le nombre d'infectés à la fin de la simulation est grand. Une légère différence est présente entre le monde ayant accès au vaccin et celui qui n'y a pas accès mais malgré cela le nombre d'infectés reste très élevé avec l'augmentation de la contagiosité.



Pour la courbe suivante nous avons décidé de jouer sur la capacitée des individus à résister à une transmission:

<img width="477" alt="courbe résistance" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/d70959d1-82c1-4ab8-8120-19ac407b2b23">


Sans surprise la baisse est proportionnelle au taux de résistance. La courbe du monde contenant le vaccin tend cependant légèrement plus vite vers zéro. Ce facteur est donc très important pour prédire la 
viralitée d'un virus, mais ce n'est pas la facteur sur lequel il est le plus simple d'influer. 



La troisième courbe fait varier la durée de l'infection dans le temps : 


<img width="444" alt="courbe duree infection" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/b82512d5-6ab2-43ee-85d5-641020139a43">

On peut observer que ce paramètre ne fait que légèrement varier les résultats si l'on fait abstraction de la variance due à l'aléatoire de l'évolution des mondes qui a un grand impact en raison de leur taille .
De plus l'absence de l'immunité post-infection n'aide pas à avoir une représentation significative pour ce paramètre.



La suivante met en avant la fluctuation de la durée d'efficacité du vaccin :


<img width="455" alt="courbe duree efficacité" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/8e29ef50-4ec0-4de5-86eb-0de3e7148af8">

Effectivement la tendance de la courbe est à la baisse avec l'augmentation de la durée. Cela s'explique par l'augmentation du nombre d'individus vaccinés présents à la fin de la simulation ce qui réduit inévitablement le nombre d'individus infectés et infectables.



Pour la cinquième courbe nous avons décidé de jouer avec le taux d'efficacité du vaccin :


<img width="449" alt="courbe taux immun" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/5691e960-656d-43e7-9633-cbe9e0c8860d">

Il est possible de faire un lien assez évident entre le taux d'immunité du vaccin et la réduction du nombre d'individus infectés à la fin des simulations, malgré quelques inconsistances dues encore une fois au côté aléatoire et la taille réduite de notre représentation ce qui accentue l'impact de l'aléatoire.



Nous avons poursuivi avec une analyse suivant le temps entre deux vagues de vaccination :


<img width="443" alt="courbe freq vaccin" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/67afec60-57db-442b-b442-234ef0bc7a91">


Malgré la variance , il est très clair et très visible que plus il y a du temps entre les vagues de vaccinations plus le nombre d'infectés est élevé ce qui s'exlique par la réduction du nombre total de personnes vaccinées dans le monde au fur et à mesure du nombre de tour.



Pour finir une courbe mettant en avant la différence suivant le nombre de vaccin par vague de vaccination : 


<img width="455" alt="courbe vaccin partour" src="https://github.com/are-dynamic-2024-g3/Sars-cov-2/assets/160217069/eaa83b5b-289f-497d-91aa-2885d5bdf14d">

Cette courbe est surement la plus explicite. Effectivement, malgré une variance possible dut à l'aléatoire, le résultat reste très linéaire et une tendance très claire se dessine.

**Conclusion**: 
Les differentes variables ont une incidence plus ou moins visible sur le nombre d'infectés, mais c'est grâce à l'accumulation de ces dernières que l'on obtient le meilleur resultat. De plus, le monde est drastiquement simplifié par rapport à un cas réel ce qui explique certaines différences avec la réalité. La prise en compte de l'immunité post-infection et de l'evolution du virus sont les deux plus gros facteurs non implémentés dans notre réalisation. Il serait donc très interessant de voir l'évolution des résultats avec l'ajout de ces derniers. Introduire une immunité dégressive serait aussi une piste très pertinante pour rendre notre simulation plus proche de la réalité mais demanderait plus de temps pour être implémenté et demanderait une optimsation plus poussée du code acutel pour éviter d'avoir un code final trop lourd lors de l'execution.

## Compte rendu

### Semaine 1

Aujourd'hui, pour bien débuter, nous avons fais quelques recherches afin d'essayer de récuperer certaines informations essentielles au bon déroulement du code, tel que le R0, le taux d'immunité et le temps d'infection.
De plus nous avons commencé le codage, en créeant des mondes 2D aléatoires (generate_spacial_world) avec des indivus sains représentées par des 0 et des None (dans les semaines à venir nous avons changé les None par des 0, 0 par des 1, et 1 par des 2 car nous aurons besoin de ces changements pour le TKinter) représentant par exemple des frontières coupant les individus. Ce n'est pas tout ! En effet nous avons également codé Infection_world qui permet de piocher un individu au hasard et de l'infecter.

### Semaine 2

Cette semaine nous nous sommes plus concentré sur le codage de plusieurs fonction. Tout d'abord la fonction "creation_parallèle" qui permet de créer un monde parallèle qui va servir pour "desinfection", un fonction multifonctionnelle, car elle sert en réalité aussi de compteur en se basant sur le monde parallèle d'un monde pour la durée d'infection, et en même temps de désinfecter quand la durée d'infection est atteinte. De plus, nous avons codé la fonction "voisins" utilisée dans "verif_voisin" qui permet de verifier si il y'a des individus infectables autour des individus infectés (ce code sert donc pour éviter des infections en boucle sur des individus déjà infectés ou encore sur des None qui ne sont pas des individus).

### Semaine 3

Aujourd'hui nous nous sommes restés concentré sur le codage. Par ailleurs, plus nous avançons dans le codage, plus nous remarquons que les recherches n'étaient pas nécessaires puisque tous nos facteurs sont représentés par des variables. Nous avons implémenté en premier la fonction "tour" qui, comme son nom l'indique fait un tour en infectant un individu,en utilisant "verif_voisin" et "désinfection". Comme notre projet était de se rapprocher de la réalité, nous avons également crée la fonction "déplacement" qui sert à changer de place entre 2 personnes, ce qui simule les déplacements telle que la migration. Par la suit,  nous nous aidons de la fonction "tour" pour créer "tour_boucle" qui prend en plus le "nombre de tour" et la "fréquence de déplacement". En effet cette fonction permet de faire plusieurs tours correspondant à la variable "nombre de tour" complété par la "fréquence de déplacement" faisant appel à la fonction déplacement.

### Semaine 4

Bonjour, la dernière fois nous avons terminé la fonction "tour_boucle" qui simule la propagation du virus dans le premier monde, donc dans celui sans vaccin. Aujourd'hui nous attaquons donc le deuxième monde avec vaccin. Nous avons 
 implémenté la fonction "vaccin" qui permet de vacciner un individu non infecté de manière aléatoire, ces individus seront indiqués par des 2 (plus tard devenus 3 pour TKinter). Cependant, ces individus ne doivent pas se relacher, en effet être vacciné ne signifie pas 100% protégé du virus. Nous avons donc crée la fonction "infection_vaccin" qui permet de jouer sur l'aléatoire (une variable aléatoire de 0 à 1 ). Si la variable aléatoire est plus elevée que le "taux d'immunité" donné par le vaccin, alors l'individu sera infecté.
Ces 2 fonctions ne nous ont pas pris énormémment de temps, donc nous en avons profité pour faire "devaccin" en se basant sur la fonction "désinfection", ce qui les rend assez similaire mais avec des entrées de variables différentes et des fonctionnalités qui diffèrent légèrement.

## Semaine 5

Cette semaine, comparé aux précédentes, nous avons eu quelques difficultés en plus. Tout d'abord nous avons commencé avec la fonction "tour_vaccin" et "tour_boucle_vaccin" en se basant sur les fonction "tour" et "tour_boucle", leurs utilités ne sont donc pas difficile à deviner. Le premier sert à faire un tour sur la base de "tour" mais avec les fonctions : "devaccin", "vaccin" et "infection_vaccin" et le deuxième sert à faire plusieurs tours en fonction de la variable : "nb_tour", des déplacements en fonction de la "fréquence_deplacement", et enfin la vaccination en fonction de la "fréquence_vaccin".
Le plus difficile reste à comprendre la bibliothèque TKinter qui permet de simuler nos fonctions, pour avoir un affichage graphique de l'évolution de nos mondes. Pour cela nous avons commencé à étudier la bibliothèque Tkinter.

## Semaine 6 

Après avoir pris le temps d'analyser la bibliothèque TKinter, nous avons pu coder la fonction cycle_entier et la fonctier fenetre qui nous permet de montrer la simulation de nos mondes (l'évolution de nos mondes) en fonction du temps. Cependant, pour que la fonction fenêtre fonctionne comme prévu nous avons fait quelques changements sur la façon d'appeller nos individus: "None" (deviens)-> "0" , "0" -> "1" , "1" -> "2" et "2" -> "3".
Par la suite, avec le peu de temps qui nous restait, nous avons redéfini les variables en utilisant la bibliothèque "numpy" (cf nom avec "var" au début) pour que les variables soient utilisables afin de tracer les courbes.

## Semaine 7

Il est primordial d'analyser ses résultats lorsque l'on souhaite tirer des conclusions d'une étude. Cette semaine nous nous sommes donc logiquement consacrés à la création des courbes en nous appuyant sur les fonctions précédemment faites "tour_boucle" et "tour_boucle_vaccin" :
."Le nombre d'infectés en fonction de la fréquence de la propagation"
."Le nombre d'infectés en fonction du taux de ne pas se faire infecté"
."Le nombre d'infectés en fonction de la durée d'infection"
."Le nombre d'infectés en fonction la durée de vaccin"
."Le nombre d'infectés en fonction du taux d'immunitée"
."Le nombre d'infectés en fonction de la fréquance de vaccination"
."Le nombre d'infectés en fonction du nombre de vaccin par tour"





