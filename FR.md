# Linux Desktop entry

Ce repo ne contient aucun code, il explique juste comment créer votre Raccourci-lanceur pour le client TeamSpeak 3.

N'hésitez pas à traduire ce document et à créer un Pull Request pour que nous l'ajoutions.

- [Original version](/README.md)

## Pré-requis

- Une image/logo qui sera affiché en guise d'icone, si vous n'en avez pas vous pouvez [le télécharger ici](https://www.teamspeak.com/assets/images/logos/teamspeak_small.png)
- Un environnement de bureau qui prend en charge les raccourcis-lanceur, comme Gnome, KDE, Unity
- Votre client TeamSpeak 3 installé et fonctionnel

## Ajouter TeamSpeak 3 à l'environnement

Ajouter le client Teamspeak 3 à votre environnement vous permet de le lancer simplement en utilisant la commande `teamspeak3-client` depuis un terminal.

```
$ sudo ln -s path/to/ts3client_runscript.sh /usr/local/bin/teamspeak3-client
$ sudo chmod +x /usr/local/bin/teamspeak3-client
```  

**Note** Il est possible de recharger l'environnement utilisateur sur les distributions basées sur Debian en utilisant la commande `source ~/.bashrc`.

## Créer votre raccourcis lanceur

Créez un fichier nommé `teamspeak3-client.desktop` dans `~/.local/share/applications`.

Editez le fichier fraîchement créé et ajoutez ce contenu :

```ini
[Desktop Entry]
Encoding=UTF-8
Version=1.0
Type=Application
Name=TeamSpeak 3
Icon=/chemin/absolu/vers/le/logo.png
Exec=teamspeak3-client
StartupNotify=true
```

Remplacez le chemin de `Icon` par celui de votre image.

C'est fini ! Maintenant vous devriez pouvoir ajouter le client TeamSpeak 3 à vos favoris et créer des raccourcis où vous voulez.
