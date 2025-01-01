# Cours Git et Github

# Etape1: travailler avec un dépot en local
Ceci est mon premier apprentissage de Git et Github. les commande comme: mkdir, touch, ls ou ls -la, git init, git status, git add --all ou git add . ou git add -A, git commit, git log, ainsi que travailler avec les branches: création, basculation, suppression, créer une branche d'urgence, fusionner les branches et gérer les conflits (git branch, git checkout, git checkout -b nom_branche_urgente, git merge, git branch -d nom_branche, git branch nom_branche, ...)
# Etape2: transférer un dépot locale vers un dépot distant
Lier un dépot local et distant, définir le dépot distant comme branche principale du projet en local. Les commandes: git remote add origin URL, git push --set-upstream origin master.
# Etapes3: Récevoir des mises à jour d'un dépot depuis Github
Lorsque nous travaillons sur un projet en équipe, il est indispensable d'etre toujours informé de toute les modifications et obtenir toujours des mises à jour des récents modification faite dans le dépot que vous suivez. les commandes comme: git fetch origin, git log origin/master, git diff origin/master et git pull origin, git branch -a, git branch -r
# Etape4: Vérification des branches en locale et distante
git branch -a (voir toute les branches locales et distantes), git branch -r (voir uniquement les branches distantes)
# Etape5: Faire un Pull Request pour un projet  (demande d'extraction)
Un Pull Request c'est le fait de demander à un admin d'un projet l'autorisation de fusionner votre code à son projet comme contribution. Github ne permet pas de modifier le code d'un tiers si ce n'est que par l'autorisation du sien.
# Etepe6: Github Flow
Les étapes de la réalisation d'un projet en équipe. Nous avons appris 5 étapes lors du flux de travail avec Github:
- La création des branches,
- Appliquer les modifications du code et faire des commits (validation des modification),
- Créer un Pull Request (demande d'extraction du code),
- Révision du code: Est un étape très importante lorsqu'on collabore sur un projet, c'est là que les développeurs vont discutées afin de savoir quel modification doit etre appliquer ou non dans un projet.
- Déployer le code: Ceci est un test du code. Avant de fusionner des modifications à la branche principale, il est très nécessaire de passer par cette étape afin de voir qu'est ce qui va et qu'est ce qui ne va pas, réperer des erreurs. Pour cela, plusieurs hébergeurs sont utilisés comme *Github Pages* et *Bitbucket Cloud*.
- Fusion du code: Vous ne devez pas arrivé à cet étape que si vous etes rassuré des modifications apportées dans le projet car ceci consiste à fusionner les modifications avec la branche principale. Si vous n'etes pas encore rassuré des modifications, il faut continuer d'apporter des modifications, correction des bugs avant de faire la fusion.
# Etape7: Github Fork
Cette étape consiste à avoir une copie d'un projet que vous voulez y contribuer ou vous voulez lancer votre projet à partir d'un projet quelconque. Un *Fork* n'est tout simplement que la copie d'un projet.
# Etape8: Cloner un dépot distant
utilisation de la commande git clone Url afin d'avoir une copie d'un projet en locale afin de travailler dessus. Utiliser les commandes comme git remote -v, git remote rename origin upstream.
# Etape9: Ignorer des fichiers avec Git
Pour ce faire utiliser un fichier *.gitignore* et mettez à l'intérieur toute les dossiers ou fichiers que vous voulez que Git ne les suivent pas. Par exemple: des fichiers de log (.log), des fichiers temporaires, des fichiers cachés, dossiers personnels, etc ...
N.B: Seul votre fichier *.gitignore* sera suivi par Git.
Si vous voulez ignoré des fichiers sans les afficher sur *.gitignore*, placez-les dans ce fichier dans cet emplacement *.git/info/exclude.
# Etape 10: Le Protocole SSH avec Git et Github
Le SSH est un protocole réseau shell sécurisé qui permet la gestion d'un réseau, le transfert des fichiers à distance et l'accès à un système distant; Il permet d'établir un réseau sécurisé, authentifié et chiffré. Il est utile de l'utiliser lorsque vous utilisez des réseaux non sécurisées.
Lors de la génération d'une paire de clés SSH vous aurez une *clé publique* et une *clé privé*.
-Une clé publique : est celle que vous partagez avec la partie distante.
-Une clé privé: est celle que vous gardez vous meme dans un lieu sur.
N.B: Une clé publique dérive de la clé privé et non vice versa.

exemple: ssh-keygen -t rsa -b 4096 -C "votre email" : permettra de générer une paire de clés.

# Remarque : Vous serez appélé à :
- Déterminer l'emplacement pour votre clé
- Saisir une phrase de passe. Ceci vous permet d'ajouter une couche de sécurité pour la clé car à chaque fois que vous en aurez besoin, vous devez saisir cette pharse de passe.

utilisez la commande *ssh-add /Users/emplacement* afin d'ajouter la pire de clés SSH à l'agent SSH.

Tester la connexion avec Github: en utilisant la commande *ssh -T git@github.com*. Si vous voyez votre nom s'afficher, bravo! la connexion a été établie.

Changer un remote d'origine de HTTPS en SSH ou vice versa avec la commande *git remote set-url origin URL_SSH/URL_HTTPS*

# Etape11: Git Revert
*Revert* est une commande Git qui vous permet d'écraser ce que vous avez fait comme commit modification en locale mais en gardant l'historique des modifications. Pour ce faire:
- Recherchez le commit à écraser (git log)
- Ecrasez-le

*git reset HEAD*: Ceci vous permet d'écraser le commit précédent (le dernier commit que vous avez fait). On peut ajout *l'option --no-edit* afin d'ignorer le message du commit et de laisser le dernier message par défaut.

* Si vous voulez écraser les modifications d'un commit spécifique, prenez le *commit hash (Une suite de caractère d'un commit)* et tapez la commande *git revert commithash* ensuite vous puvez ignoré le message du commit.  

# Etape12: Git Reset 
*Reset* est une commande qui vous permet de revenir au commit précédent lorsqu'il est important et cela supprimera toutes les modifications qui vient après le commit sur lequel vous etes revenu.

* N.B: Il est dangereux de modifier l'historique de modification d'un dépot. Il est generalement acceptable d'effectuer ce type de modification dans votre propre dépot en local.
Evitez de le faire dans le *remote dépot* en particulier d'autres personnes travaillent dessus.
Meme si les commits n'apparaissent plus dans le log, ils sont pas supprimé par Git.

# Etape 13 & Fin: Git Amend
Avec la commande *git commit --amend "message du commit"* vous pouvez modifier le message d'un commit. Cette modification se fera à partir du *staging, le dernier commit et créera un nouveau commit*. Cette commit créer remplacera entièrement le dernier commit.

* N.B: IL n'est pas conseillé de cette action. Mais toute fois si cela est nécessaire, vous pouvez le faire.

# FIN