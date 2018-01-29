# Rails ??? Oh Rails ! Where is that ?

Ma mission si je l'accepte (et a priori tel est le cas), c'est de t'expliquer ce qu'est Rails. Plutôt cool non ?

Bon commençons par le début :

## Quelle est la différence entre un site **statique** et un site **dynamique** ?

### D'abord, c'est quoi statique ?

Et bien comme nous l'indique le Larousse, c'est un adjectif qui nous vient du grec **statikos**, et pour reprendre la définition qui nous intéresse, *qui n'évolue pas, semble fixé de manière définitive (da viken comme disent les  bretons), par opposition à **dynamique**.*

Donc un site *statique* c'est un site qui n'est pas amené à évolué, d'où que tu viennes, qui que tu sois, c'est le même accueil et c'est le même contenu.

Normalement, tu en connais au moins un : http://motherfuckingwebsite.com/

La sainte trinité comme disait l'autre, du html, du css, et du JS.

### Et donc un site dynamique ???

Hum ? Un petit coup de Larousse ?
*Dynamique* : Ensemble de forces qui entraînent, provoquent un mouvement, une évolution à l'intérieur d'une structure en développement. T'y as compris ???

Plus sérieusement, et pour reprendre ce qui as été précédemment, en opposition à un site *statique*, un site **dynamique** c'est un site évoluant en fonction de son visiteur/utilisateur. Donc pas le même accueil pour tout le monde, contenu, ou encore utilisation.

Prenons un exemple, http://www.bzhecume.com/surflog/

Si tu surf, et qui plus est en Bretagne, bzhecume c'est un peu "légende". Pourquoi ? Parce que sur ce site, tu vas retrouver un forum de discussions autour du surf et tout ce qui y attrait, un surf check où tu retrouveras le report du jour pour checker à distance les conditions du jour de ton spot ou bien les poster, les commenter etc., des petites annonces et patatipatata.

**Ce qui est important de retenir ici**, c'est que sur site, tu peux consulter toutes les pages sans t'être préalablement enregistré comme *utilisateur*. Mais que si tu le fais, et que tu te *log*, tu pourras alors toi aussi participer aux discussions, poster les photos de tes sessions, commenter un report, ou encore y vendre ta vieille combar usagée qui pue la moule.
**Donc faire évoluer ce site.**

## Le *Model View Controller* Késako ?

Comme son nom l'indique, le MVC pour les intimes, c'est un motif d'architecture logicielle pour les interfaces graphique, et super cool pour les applications web !

### Toujours pas ?
Ok, bon regardons de plus près.

Le MVC est un motif composé de trois modules différents : **Model - View - Controller**

Et aucuns de ces trois là n'ont la même responsabilité.

..* La responsabilité du **Model** c'est de contenir les données à afficher;
..* Celle de **View** est de contenir la présentation de l'interface graphique (ce qui apparaît à l'écran);
..* Et enfin celle du **Controller** qui est de contenir la logique des actions effectuées par l'utilisateur (créer un article, le commenter, poster une vidéo, etc.)

### Et ça s'articule comment ??

Admettons que tu souhaite te connecter au site de THP (je dis bien admettons). Pour ça il faut que tu te log, donc tu le fais, et là comme par magie, tu te mets à avoir accès aux leçons, planning, corrections et tout pis tout.

Mais que s'est-il passé ?
Quand tu t'es loggé, **Controller** a traité ton action, et l'a indiqué au **Model**. Les données du **Model** s'en sont retrouvé modifiées, car ce sont les tiennes qui s'y trouvent désormais. Aussi, ce sont elles qui sont envoyées à l'écran (**View**).

## Les Routes

Les Routes, c'est ce qui va permettre à ton Controller de faire ce que tu lui dis de faire.

Imagine, tu as créer un blog et tu souhaite publié ton premier article. Heureusement pour toi, il y un joli bouton sur lequel cliquer pour pouvoir le faire. Quand tu cliques sur ce bouton, son URL va être interprété par une **Route**, et orienter l'ordre que tu viens de donner vers l'action du Controller correspondante (créer un article), tel que *show, create, destroy, edit, new, index, et update*.

## Les bases de données

Comme on a pu le lire un peu plus haut, la responsabilité du **Model** c'est de contenir des données. Toujours les mêmes ? Non ! Car le **Controller** peut être amené à les modifier en fonctions de tes volontés de tyran.

Mais alors où vont aller les données contenues dans le **Model**, et d'où vont venir celles qui vont êtres appelées. Et bien des bases de données malheureux !

Ces bases de données vont être organisées sous formes de tables, et en général toutes ces tables ont une clé commune (identifiant unique) pour pouvoir intéragir ensemble.

Exemple : tu as une table Users (id, firstname, lastname), et une autre Users_private_informations (id, size, age, weight).  Si tu veux savoir les données privées d'un utilisateur c'est grâce à l'id qui lui est attribué quelles seront retrouvées.

## GET/POST, What's the difference ?

Dans rails une *Route* dont on a déterminé les ressources (point de départ, point d'arrivée) entre des méthodes appellées verbes HTTP d'une part (en gros des requêtes qui déterminent les actions à réaliser sur une ressource donnée), et les URL d'autre part.

Par convention, chaque action et aussi liée à une opération CRUD spécifique (*Create, Read, Update, Delete*) appliquée à la base de donnée.

Pour en revenir à nos moutons que sont GET et PUSH, et bien ce sont tous deux des *verbes HTTP* donc des requêtes qui déterminent des actions à réaliser sur une ressource determinée (données de la base de de donnée).

**GET** permet d'aller chercher de la donnée dans la base de données
**POST** permet créer de la donnée dans la base de donnée.

## Migration

Le concept de **Migration** est là pour te permettre de *structurer et d'organiser ta base de donnée*. Mais aussi, et c'est important, *d'enregistrer tes actions* ou celles d'autres developers sur la base de données.

##Les relations entre les Models des BDD



## Les fonctions du CRUD
