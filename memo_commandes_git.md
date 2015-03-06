#Commande Git

###git init
Permet d’indiquer que le dossier dans lequel on se trouve  pwd pour savoir où on se trouve) devra être géré comme un repository git

###git status
Permet de connaitre l’état du dossier en cours (nouveau fichier, modifications, suppressions…)

###git add nom_du_fichier_ou_repertoire
Permet d’indiquer à git de gérer « nom_du_fichier_ou_repertoire » (en l’ajoutant à son « index)

###git commit -m « Ajout d’un nouveau fichier »
Commit des modifications réalisées
-m  : permet d’indiquer le message du commit
-a  : permet d’indiquer de réaliser le commit avec les fichiers déjà pris en comptes par git (lors des précédents commit)
-am : -a et -m en même temps

###git log
Visualisation de ce qui a été fait (les commit réalisées)

###git checkout plus_le_sha_code_d_un_commit OU nom_de_la_branche 
git checkout permet de vérifier un commit (via son code sa) ou de se « placer » une branche

###git clone adresse_du_dépot
clone d’un dépôt git (il faut ici indiquer l’adresse du dépôt)

###git push origin master
Envois d’un ou de plusieurs commit sur le « remote » indiqué (origin) et sur la branche indiquée (master)
« origin » et « master » sont des conventions  
« master » est la branche « principale » d’un dépot/remote
« origin » est l’endroit ou se trouve le remote //TODO essayé être plus précis ici

###git pull origin master
récupération du code modifié par d'autre personnes (on peut tout comme push, ajouter la branche qu'on récupère)

###git branch / git branch test et  git checkout test
visualisation de la branche en cours / création d’une branche « test » / switch vers la branche test

###permet d’envoyer le contenu de la branche indiquée (nom_de_la_branche) dans la branche en cours (pour savoir ou on est, on peut utiliser pwd)
git merge nom_de_la_branche

###git blame nom_fichier
Permet de savoir qu’elles ont été les actions sur un fichier (identifiée par le numéro_du_sha)


###git show numéro_du_sha
Visualisation des modifications effectuées lors d’un commit

###le fichier . gitignore 
Il permet d’indiquer à git de ne pas prendre en compte les fichiers qui seront indiqués (tel que les fichiers de configurations)
NE JAMAIS publier sur GITHUB OU AUTRE des fichiers de configurations ! !

###git stash / git stash pop
- Permet « d’enregistrer » le travail en cours pour revenir à l’état initial avant nos modifications (pour travailler sur des choses plus urgentes sans pour autant faire de « commit superflus »)
  Permet aussi lorsqu’on switch de branch de ne pas perdre notre travail
- Permet de retrouver le travail que l’on effectuait avant le stash (attention une fois git stash pop utilisé, la mémorisation du travail effectué est supprimée. Il faudra pensé à refaire un autre git stash si on a encore à changer de branch ou travailler sur autre chose