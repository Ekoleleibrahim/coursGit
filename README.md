# Cours Git et Github

# Etape1: travailler avec un dépot en local
Ceci est mon premier apprentissage de Git et Github. les commande comme: mkdir, touch, ls ou ls -la, git init, git status, git add --all ou git add . ou git add -A, git commit, git log, ainsi que travailler avec les branches: création, basculation, suppression, créer une branche d'urgence, fusionner les branches et gérer les conflits (git branch, git checkout, git checkout -b nom_branche_urgente, git merge, git branch -d nom_branche, git branch nom_branche, ...)
# Etape2: transférer un dépot locale vers un dépot distant
Lier un dépot local et distant, définir le dépot distant comme branche principale du projet en local. Les commandes: git remote add origin URL, git push --set-upstream origin master.
# Etapes3: Récevoir des mises à jour d'un dépot depuis Github
Lorsque nous travaillons sur un projet en équipe, il est indispensable d'etre toujours informé de toute les modifications et obtenir toujours des mises à jour des récents modification faite dans le dépot que vous suivez. les commandes comme: git fetch origin, git log origin/master, git diff origin/master et git pull origin, git branch -a, git branch -r
