# Linux Desktop entry

This repository does not contains code, it just explain how to create your desktop entry for the TeamSpeak 3 Client.

Feel free to translate this document and make a pull request to add it.

- [Version française](/FR.md)

## Required stuff

- An image to use for your entry, if you have not the client logo you can [download it here](https://www.teamspeak.com/assets/images/logos/teamspeak_small.png)
- A desktop environment like Gnome, KDE, Unity
- Your current TeamSpeak 3 Client path

## Add TeamSpeak 3 to the binaries

Adding the TeamSpeak 3 Client to your binaries allow you to start it quickly from terminal by typing `teamspeak3-client`.

```
$ sudo ln -s path/to/ts3client_runscript.sh /usr/local/bin/teamspeak3-client
$ sudo chmod +x /usr/local/bin/teamspeak3-client
```  

**Note** On Debian base distributions you can reload your environment using `source ~/.bashrc`, this will add `teamspeak3-client` to it.

## Create your entry file

Create a file named `teamspeak3-client.desktop` in `~/.local/share/applications`.

Edit the file and put this content:

```ini
[Desktop Entry]
Encoding=UTF-8
Version=1.0
Type=Application
Name=TeamSpeak 3
Icon=/path/to/the/logo.png
Exec=teamspeak3-client
StartupNotify=true
```

Update the Icon path depending on your TeamSpeak 3 installation.

It's done! Now you should be able to add the client to your bookmarks on your desktop/docked menu.
