
### Configuration initiale
```sh
git config --global user.name "Votre Nom"
git config --global user.email "votre@email.com"
```

### Initialisation d'un dépôt
```sh
git init
```

### Clonage d'un dépôt
```sh
git clone <URL_du_dépôt>
```

### Vérification du statut du dépôt
```sh
git status
```

### Ajout de fichiers à l'index
```sh
git add <fichier>
# Ajouter tous les fichiers modifiés
git add .
```

### Validation des modifications
```sh
git commit -m "Message de commit"
```

### Affichage de l'historique des commits
```sh
git log
```

### Envoi des modifications vers un dépôt distant
```sh
git push origin main
```

### Récupération des modifications depuis un dépôt distant
```sh
git pull origin main
```

### Création et changement de branche
```sh
git branch <nom_de_branche>
git checkout <nom_de_branche>
```

### Fusion de branches
```sh
git merge <nom_de_branche>
```

### Suppression d'une branche
```sh
git branch -d <nom_de_branche>
```

### Annulation des modifications
```sh
git checkout -- <fichier>  # Annuler les modifications locales
```

### Réinitialisation d'un commit
```sh
git reset --soft HEAD~1  # Garde les modifications en staging
git reset --hard HEAD~1  # Supprime complètement le dernier commit
