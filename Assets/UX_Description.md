Légende: 

~~Lorem~~ = v2


# Description Générale de l'application 

Solfego est une application d'apprentissage pour le solfége, il y a des leçons et des entrainement à disposition avec un systéme de récompense.

Les différents utilisateurs peuvent s'ajouter en amis.

Les utilisateurs ont la possibilité de mettre commentaires sur les leçons pour recevoir de l'aide su des principes incompris.

Comme toute applications avec des interactions écrite la modérations est importante dans ce cas les commentaires ne sont pas tout de suite publié mais en attente de confiration d'un admistrateur.

Si un utilisateurs est considérer comme nuisible il sera alors soit timeout (il pourra consulter les leçons mais ne pourra plus commenter) ou alors banni (ne peut plus utilisé le site).

Dans le cas d'un bannisement l'utilisateur pourra faire une demande de débanisement qui sera accepter ou non.

Il y a la possbilité d'avoir le rôle de prof ce rôle permet de creer des leçons grâce à un outils intégrer qui seront ensuite voté par d'autres profs jusq'à être publie


## Pour qui
Pour tout ceux qui veulent approfondir leurs connaissance en théorie musical

## Quel Problémes 
Beaucoup de musiciens non pas eu le priviliéges d'avoir accés à des cours de solfége, le but est d'offrir une solution accessible et gratuit

## Comment l'utiliser
En se connectant sur le site sans compte on peut consulter la premiere leçon et le premier entraiement puis ils doivent se connecter pour consulter le reste de l'application


# UX Description

## **-Client**


#### Arrivé

* Lors de mon arrivé sur le site si je suis  connecté j'ai ma derniére leçon consulté en haut et en visible j'ai une proposition d'entraînement lié à cette leçon, si je n'ai jamais consulté de leçon le même encadré est présent avec la premiére leçon disponible et à la place de l'entraînement la proposition de s'inscrire.

*  J'ai à disposition 4 pages 

    * Une d'entraînement 
    
    * Une de leçons

    * La home page décris au dessus accessible depuis le logo de l'application.

    * La page de profil

* La premiére leçon et le premier entrainement est diponible sans pouvoir se connecter, aprés la fin du premier exercices on nous propose de nous connecter avec un pop up .

#### Leçons

* Les leçon se débloque au fur et à mesure de leurs complétion (1->2->*) en terminer une pour la premiére fois fait gagner des piéces et de l'expériences.

* Elles sont composées de différentes diapositives avec un texte, des images (des sons ?) 

* On les parcours à l'aide des fléches du clavier, ou des fléches sur les diapositives

* On peu revenir en arriére

* On peut laisser un commentaire sur une leçon 

* On peut mettre un like ou un dislike sur un commentaire de leçon

* Les commentaires sont accessible depuis un bouton dans la leçon

* Une liste de commentaire par diapo

* Les commentaires sont publié une fois l'administrateur valide le commentaire 

* Les commentaire des profs sont automatiquement épingler 

* Les commentaires les plus liker sont le plus haut dans la liste 

#### Exercices

* Un entraînement est disponible seulement aprés avoir terminé la leçon liée


* Un entraînement est une série d'exercices sur la leçon liée en compléter une nous donne de l'expérience et des piéces la premiére fois la récompense est plus importante.


* Si je répond faux à une question une vie est retiré à mon compteur de vie. Et je peux répondre de nouveau.


* Un score est calculé à la fin avec certains paramétres pour le nombre d'xp et de piéces


#### Systéme de vie


* N vie maximum
* 1 vie par heures
* Visible sur les différentes pages 
* Lorsque l'on clique dessus un menu s'ouvre pour pouvoir soit en acheter un plein de vie avec des piéces soit en gagner 1 en regardant une pub 
* Si on arrive à 0 de vie en pleine leçon un menu s'ouvre pour soit faire le plein de vie soit **regarder une pub (*une fois par entraînement*)** soit quitter l'entraînement
* Si on essaye d'accéder à un entraînement ou à une leçon avec 0 de vie on nous en empêches et le menu de vie s'ouvre 

#### Systéme de piéces 

* On en gagne un certains nombre en étant actif sur l'application (compléter pour la premiére fois une leçon ou compléter un entrainement)

* On dépense N nombre de piéces pour refaire le plein de vie 

* Si on as pas de piéce on peut en acheter avec de l'argent réel

* ~~On peut aussi dépenser les piéces pour embellir son profil~~

#### Profil

* Une page de profil avec son avatar ses piéces et son expérience.

* ~~Une boutique où on peut acheter des cosmétiques~~

* On peut se connecter avec d'autres utilisateurs grâce à un code **unique**

* Notre encadré indique notre rôle avec un texte clair 

* On a un badge qui représente son niveau.

* Si l'utilisateur est banni alors toutes les pages redirige vers son profil avec marqué "Bannis" un boutton pour faire une demande de débannisement

* Si la demande à déjà été faite alors il est marqué "Veuillez attendre la réponse d'un administrateur"

#### Systéme d'éxpériences et de niveau 

* A chaque palier on gagne un niveau
* A chaque gain de niveau on gagne 2 vie et des piéces


#### Autres

 *  J'ai à disposition un bouton d'aide pour contacter un adminstrateur en cas de soucis rencontré


## Admin 

*   Lorsque je suis connecté et enregistrer en tant qu'admin j'ai à disposition dans mon profil un boutton pour switch en mode "admin"

*   En mode admin j'ai la possibilité de consulter les messages envoyer via le bouton d'aide 

*   Je peux y répondre 

*   Je peux regarder les leçons ayant assez de vote pour les publiée ou non.

*  Je peux regarder les commentaire en attente de validation

* Je peux acceder au différents profil de l'utilisateur avec des informations supplémentaire comme le nombre de commentaire refusé, ses activités

* Je peux bannir un utilisateur en donnant une raison

* Je peux accéder à une liste des réclamations de débanissement 

* Je peux accepter ou refuser un débannisment 

## Professeur 

*   Je peux créer une leçon et des exercices liée et en suite proposé de le publier. 

*   Je peux sauvegarder un brouillon de leçon ou exercices.

*   Je peux supprimer un brouillon de leçon ou exercices

*   Je peux edité une leçon ou exercice publiée 

*   Je peux voter pour ou contre une des leçon proposé, avec un avis obligatoire. 

*   Une fois ma leçon ayant obtenue un certains nombres de vote elle sera proposé aux administrateur afin de consulté l'intégralité de la forme 










## Résolutions des problémes 

* Framework : Symfony

    * Paradigme MVC Permettant une mise en place des différents utilisateurs rapide 
    * Moins d'habitude avec PHP donc bon entrainement 

* Pub : Video.js + videojs-ima (Google IMA SDK)

    * Docs : 
    - https://videojs.com/city
    - https://developers.google.com/interactive-media-ads?hl=fr
    * Projet Github :
    * https://github.com/googleads/videojs-ima

      

* Paiement : Stripe
    * Doc :
    * https://docs.stripe.com/payments/accept-a-payment?lang=php&platform=web





# Resume et partie 

* Gestion de compte
    * Creation de compte 
    * Authentification
    * Rôle
    * Autorisations


* Leçons
    * Consultations des leçons existante
    * Gestion de débloquage de leçon
    * Commentaires
    * Gestion des commentaires

* Outils pour création de leçon
    * Systéme de vote pour publié une leçon
    
* Exercices
    * Accéder aux exercices 
    * Répondre au questions

* Systéme de vie 
    * Perte ou gain de vie 
    * Possibilité d'acheter des vies

* Systéme de monnaie
    * Gain lors de différents complétions
    * Débloquage de certaines fonctionnalité 
    * Achat de monnaie 

* Pub

* Paiement 