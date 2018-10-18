# Génération des clés publiques SSH


1. _Cela dit, de nombreux serveurs Git utilisent une authentification par clés publiques SSH. Pour fournir une clé publique, chaque utilisateur de votre système doit la générer s'il n'en a pas déjà. Le processus est similaire sur tous les systèmes d'exploitation. Premièrement, l'utilisateur doit vérifier qu'il n'en a pas déjà une. Par défaut, les clés SSH d'un utilisateur sont stockées dans le répertoire ~/.ssh du compte. Vous pouvez facilement vérifier si vous avez déjà une clé en listant le contenu de ce répertoire :_

``` 
$ cd ~/.ssh
$ ls
authorized_keys2  id_dsa       known_hosts
config            id_dsa.pub
```
2. _Recherchez une paire de fichiers appelés quelquechose et quelquechose.pub où le quelquechose en question est généralement id_dsa ou id_rsa. Le fichier en .pub est la clé publique tandis que l'autre est la clé privée. Si vous ne voyez pas ces fichiers (ou n'avez même pas de répertoire .ssh), vous pouvez les créer en lançant un programme appelé ssh-keygen fourni par le paquet SSH sur les systèmes Linux/Mac et MSysGit pour Windows :_

```
$ cat ~/.ssh/id_rsa.pub
ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAklOUpkDHrfHY17SbrmTIpNLTGK9Tjom/BWDSU
GPl+nafzlHDTYW7hdI4yZ5ew18JH4JW9jbhUFrviQzM7xlELEVf4h9lFX5QVkbPppSwg0cda3
Pbv7kOdJ/MTyBlWXFCR+HAo3FXRitBqxiX1nKhXpHAZsMciLq8V6RjsNAQwdsdMFvSlVK/7XA
t3FaoJoAsncM1Q9x5+3V0Ww68/eIFmb1zuUFljQJKprrX88XypNDvjYNby6vw/Pb0rwert/En
mZ+AW4OZPnTPI89ZPmVMLuayrD2cE86Z/il8b+gw3r3+1nKatmIkjn2so1d01QraTlMqVSsbx
NrRFi9wrf+M7Q== schacon@agadorlaptop.local
``
_Pour un tutoriel plus approfondi sur la création de clé SSH sur différents systèmes d'exploitation, référez-vous au guide GitHub sur les clés SSH à http://github.com/guides/providing-your-ssh-key._

SOURCE: [https://git-scm.com/book/fr/v1/Git-sur-le-serveur-Génération-des-clés-publiques-SSH](https://git-scm.com/book/fr/v1/Git-sur-le-serveur-Génération-des-clés-publiques-SSH)

