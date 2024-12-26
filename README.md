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
