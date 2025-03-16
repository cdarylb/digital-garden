## Commandes avancées Git

### Modification de l'historique
#### Modifier le dernier commit
```sh
git commit --amend -m "Nouveau message de commit"
```
#### Modifier plusieurs commits précédents
```sh
git rebase -i HEAD~3  # Modifier les 3 derniers commits
```

### Travailler avec des branches distantes
#### Récupérer toutes les branches distantes
```sh
git fetch --all
```
#### Suivre une branche distante
```sh
git checkout -b ma_branche origin/ma_branche
```
#### Supprimer une branche distante
```sh
git push origin --delete ma_branche
```

### Stashing (mettre de côté des modifications)
#### Sauvegarder des modifications temporairement
```sh
git stash
```
#### Lister les stashes disponibles
```sh
git stash list
```
#### Restaurer le dernier stash
```sh
git stash pop
```
#### Restaurer un stash spécifique
```sh
git stash apply stash@{1}
```
#### Supprimer un stash spécifique
```sh
git stash drop stash@{1}
```
#### Supprimer tous les stashes
```sh
git stash clear
```

### Recherche et inspection
#### Trouver un commit par message
```sh
git log --grep="mot-clé"
```
#### Trouver un commit qui a modifié un fichier spécifique
```sh
git log -- <nom_fichier>
```
#### Voir les différences entre commits
```sh
git diff HEAD~1 HEAD
```
#### Voir les différences entre le fichier modifié et la dernière validation
```sh
git diff <fichier>
```

### Suppression et nettoyage
#### Supprimer un fichier du repository mais le garder localement
```sh
git rm --cached <fichier>
```
#### Supprimer un fichier complètement du repository
```sh
git rm <fichier>
```

### Revenir en arrière
#### Annuler un commit et garder les modifications
```sh
git reset --soft HEAD~1
```
#### Annuler un commit et supprimer les modifications
```sh
git reset --hard HEAD~1
```
#### Revenir à un commit spécifique
```sh
git reset --hard <commit_hash>
```

### Cherry-picking (récupérer un commit spécifique d'une branche)
```sh
git cherry-pick <commit_hash>
```

### Bisect (trouver l'origine d'un bug)
```sh
git bisect start
git bisect bad  # Marque la version actuelle comme contenant le bug
git bisect good <commit_hash>  # Marque une version correcte
git bisect run <script>  # Exécute un script pour tester chaque version
git bisect reset  # Terminer le bisect
