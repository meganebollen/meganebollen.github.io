Ce bookdown a pour but d'être un guide R pour les étudiants de statistique I.

## Bookdown

Il se base sur la structure du book mis par défault sur R Markdown et le package bookdown (https://github.com/rstudio/bookdown). 

Il est nécessaire d'installer le package bookdown pour utiliser cette extension dans R.

```{r}
# stable version on CRAN
install.packages("bookdown")
```

## Git
Il faut premièrement configurer Git sur votre ordinateur avant de pouvoir push sur le repo.

Lors de la première utilisation de Git, il faut ajouter son nom d'utilisateur ainsi que l'adresse mail à votre ordinateur à l'aide de l'invite de commandes avec les lignes de commande suivante:

```{bash}
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

Ensuite, il est nécessaire de vérifier si une clé privé et publique sont déjà présentes sur l'ordinateur:

```{bash}
cd ~/.ssh
ls
```

Si une clé est existante, une liste de fichier s'affiche. Le fichier `.pub` est la clé publique.
Dans le cas contraire, rien ne s'affiche. Il faudra donc créer une clé avec le code suivant:

```{bash}
ssh-keygen -o
```

Il sera demandé si vous voulez saver la clé (`.ssh/id_rsa`) et ensuite il vous sera demandé si vous désirez ajouter un mot de passe afin d'utiliser la clé.

Pour finir, il faudra envoyer la clé publique (`.pub`) au propriétaire du repository afin que vous receviez les accès pour push les modifications dans le repository.


### Conseil pour un bon usage de Git

1. Pull le repo en ligne avant de commencer à travailler.
1. Une fois les modifications réalisées, appuyez sur le bouton "Build Book" dans R
1. Sélectionnez les modifications que vous désirez mettre sur le github avec `stage`
1. Ajoutez un message clair puis vous pouvez `commit` les modifications
1. Pour mettre vos modifications sur github, réalisez un `push` de vos commits.
