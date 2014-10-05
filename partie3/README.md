# Exercie partie 3

## Consigne
L'objectif est d'expliquer 3 concepts de git pour un développeur web qui ne l'utilise pas (encore).
* Qu'est-ce qu'un commit;
* À quoi sert la commande git log;
* Qu'est-ce qu'une branche.


## Contenu de l'exercice

### Introduction
Il ne s'agit pas ici de revenir sur ce qu'est git ou pourquoi l'utiliser, mais j'aimerais ajouter ce petit complément sous forme de fichier README.md, fichier important dans un "repository" car c'est celui qui va donner la première impression du contenu d'un projet géré sur Github.

La documentation est souvent le maillon manquant entre les développeurs et les utilisateurs, et ce fichier contribue à créer ce lien, en indiquant le contenu d'un projet et en renvoyant vers les principales informations et documentations accessibles aux utilsateurs comme à d'autres développeurs.

Quelque peu frustré par l'accès aux vidéos, qui avec ma version d'ubuntu et de flash fonctionnent bien sur Vimeo mais pas sur OpenClassrooms (pratique...), je privilégie pour cette exercice la forme texte la plus simple, le contenu de l'exercice étant ici rédigé avec nano et gedit sous la forme de fichiers README.md

L'export PDF sera fait en fin de rédaction sous LibreOffice Text, par copier-coller des parties suivantes depuis le rendu sur Github https://github.com/Facyla/mooc-openclassrooms-github/blob/master/partie3/README.md


### Qu'est-ce qu'un commit ?
Git est un outil de suivi de versions, qui permet de "suivre" les modifications apportées aux fichiers indexés dans un projet. 

Pour expliquer ce qu'est un commit, reprenons la petite séquence suivante qui permet de créer un nouveau commit :

1. Lorsqu'on suit un projet avec "git", par exemple ici la réponse à un exercice, les modifications apportées aux fichiers sont listées dans le projet, et peuvent être affichées par la commande qui affiche l'état actuel du répertoire de travail du projet par rapport à l'index de "git" :
 git status
Cela signifie à ce stade que ces modifications existent bien dans l'état actuel du projet (si on l'affiche sur un serveur local, les modifications faites sont bien visibles), mais qu'elles n'ont pas encore été "validées" pour le prochain "commit".

2. Ces modifications doivent alors être "validées", c'est-à-dire qu'il convient d'indiquer lesquelles doivent être inclues dans ce prochain "commit", ce que l'on fait avec la commande suivante qui ajoute tous les fichiers déjà suivis à l'index (mais n'ajoutera pas les fichiers que l'on vient de créer) :
 git add .
Le ou les fichiers modifiés (et déjà indexés) sont alors "prêts à être commités", c'est-à-dire *prêts à être inclus dans le prochain commit*. Une variante de cette commande permet d'ajouter de nouveaux fichiers à l'index, ou de les supprimer.

3. Le "commit" lui-même est créé par la commande suivante, qui va créer un nouveau commit, et ajouter un commentaire pour décrire la raison et/ou le contenu des modifications :
 git commit -m "Rédaction de l'exercice 1"


 **Un commit est un état précis des fichiers du projet indexés avec git**. Cet état est identifié par une chaine de caractères réputée unique (un hash).

Du point de vue du développeur qui utilise "git", l'évolution d'un projet est ainsi composé d'une succession de "commits", commentés, qui correspondent à autant de modifications des fichiers du projet, commentées par leur auteur.


Par comparaison avec l'état précédent du projet, un commit peut être considéré comme la matérialisation d'une série de modifications que l'on souhaite enregistrer dans le projet : d'un point de vue très "pratique", un commit peut être vu comme une étape de plus dans l'avancement d'un projet.

Il peut aussi bien consister en la modification d'un caractère, que l'ajout d'une librairie complète au projet.




### À quoi sert la commande git log ?
**La commande "git log" permet d'afficher la liste des derniers commits**, c'est-à-dire l'historique des dernières modifications. 

Cette liste précise l'auteur, la date et le commentaire associé à chacun des commits, et dispose de diverses options qui permettent d'affiner les résultats sur une période ou un répertoire précis, afin de "voir ce qui s'est passé récemment" dans un répertoire précis.

C'est donc une commande informative, qui ne modifie rien... elle est tout à fait comparable à un "tail" sur un fichier de log apache.



### Qu'est-ce qu'une branche ?

Une branche ou "fork" est une dérivation à partir du "tronc commun" d'un projet, avec lequel elle peut ensuite être fusionnée.

C'est une manière de cloisonner certains développements, comme par exemple le développement d'une nouvelle fonctionnalité ou d'un patch, mais aussi de maintenir et faire évoluer en parallèle plusieurs versions d'un même logiciel.

**Une branche constitue un espace de travail isolé dans lequel il est possible d'apporter diverses évolutions sans perturber le développement de la partie principale du code.**


Les branches peuvent servir aussi bien seul qu'en collaboration, en permettant de structurer et d'organiser le travail sur différentes parties d'un projet, ou à plusieurs niveaux de maturité de ce projet. Une forme d'organisation simple peut ainsi consister à travailler dans une  ou plusieurs branches de "dev" (par. ex. "dev_marc", "dev_utf8" ou "dev_v1.0.3"), puis à utiliser une branche "preprod" pour les tests, et enfin la "master" pour les versions prêtes à déployer.

Une branche peut être ensuite tout simplement abandonnée, ou fusionnée avec une autre branche. Dans ce cas, il peut être nécessaire de gérer des conflits de fusion, lorsque certains fichiers ont évolué différemment dans les deux branches.



