# voici comment ignorer certains fichier (ex:github)MacOs

Si le .DS_Store apparait lors d'un ``` git status ```:
Il est possible d'ignorer ce .DS_Store lors d'un prochain commit.
Il suffira d'utiliser ces commandes en terminal:

```
$ git config --global core.excludesfile ~/.gitignore
$ echo *.DS_Store >> ~/.gitignore

``` 
SOURCE: https://www.jeffgeerling.com/blogs/jeff-geerling/stop-letting-dsstore-slow-you
