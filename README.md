Pour "nettoyer" le projet, j'ai indenté la majorité des classes présentes et les ais divisés dans trois packages : - echec - main - model

Plusieurs changements dans la classe Exécuteur où la méthode main manquait le static et prenait un mauvais paramètre (Character[] > String[]). Changement également par la bonne variable 'g' (représentant l'instantiation d'un nouveau Jeu) pour appliquer sa méthode lancer().

Dans la Classe Position : Changement de la visibilité de la méthode inBounds() et clone() en public.

Dans la Classe Roi : Changement de la visibilité des attributs en private et la méthode de getRoiCouleur() en public. Ajout du "public" dans String update(). Génération des getter et setter.

Classe Joueur : Création des getter/setter pour la variable tab. Inversement dans la méthode updateTab de la couleurEnnemie qui n'était pas relié correctement et affecté l'affichage des pièces sur l'échiquier.

Classe Game : Ajout d'un choix de sélection de nom pour les deux joueurs. Dans la méthode update() changement des appels d'attributs en leur getter puisqu'elles sont dorénavant en private.

Classe Echiquier : Dans la méthode afficherEchiquier(), remplacement des termes anglais dans le switch par ceux en français pour permettre l'affichage des pièces.

Classe Reine : Ajout de l'héritage avec "extends Piece". Génération de son constructeur, de la méthode toString(), et des différerentes boucles contenus dans la méthode getMouvementPossible() pour s'adapter aux règles de la Reine.

Suppression de l'implémentation de l'interface Mouvements dans les classes filles puisqu'elle est présente dans celle de la classe mère (Pièce).

(Diagramme des classes en capture d'écran dans le root du dossier).
