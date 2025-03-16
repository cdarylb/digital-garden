
### Affichage de base des logs
```sh
git log
```

### Affichage condensé et personnalisé
#### Voir un log plus compact avec une ligne par commit
```sh
git log --oneline
```

#### Affichage avec graphe des branches
```sh
git log --oneline --graph --decorate --all
```

#### Affichage personnalisé des commits
```sh
git log --pretty=format:"%h - %an, %ar : %s"
```
Explication des formats :
- `%h` : Hash court du commit
- `%an` : Auteur
- `%ar` : Date relative (ex: "2 hours ago")
- `%s` : Message du commit

#### Utilisation de thèmes colorés pour les logs
```sh
git log --color --pretty=format:"%C(auto)%h%Creset - %C(blue)%an%Creset, %C(green)%ar%Creset : %s"
```

### Filtrage des logs
#### Voir les commits d'un fichier spécifique
```sh
git log -- <fichier>
```

#### Filtrer par auteur
```sh
git log --author="Nom Auteur"
```

#### Rechercher un mot-clé dans les messages de commit
```sh
git log --grep="mot-clé"
```

#### Voir uniquement les commits modifiant un fichier spécifique
```sh
git log --name-only -- <fichier>
```

### Limiter le nombre de commits affichés
```sh
git log -n 10  # Afficher les 10 derniers commits
```

### Voir les différences dans chaque commit
```sh
git log -p
```

### Afficher les fichiers modifiés dans chaque commit
```sh
git log --stat
```

### Format graphique avancé
#### Voir un graphe détaillé avec les branches et leurs relations
```sh
git log --oneline --graph --decorate --all
```

#### Alias pratique pour un affichage lisible
alias pour une meilleure visu :
```sh
git config --global alias.lg "log --color --graph --pretty=format:'%C(yellow)%h%Creset -%C(auto)%d%Creset %s %C(blue)(%cr) %C(green)<%an>%Creset' --abbrev-commit"
```
Puis :
```sh
git lg
```

### Voir les commits entre deux branches
```sh
git log main..feature-branch
```

### Trouver quel commit a introduit un bug (bisect)
```sh
git bisect start
git bisect bad
git bisect good <commit_hash>
```