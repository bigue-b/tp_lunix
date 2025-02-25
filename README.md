🚀 Projet Nginx & MySQL avec Vagrant

Description

Ce projet utilise Vagrant pour configurer un environnement de développement avec :

    Un serveur web Nginx
    Un serveur MySQL
    Une mini application front
Prérequis

    Vagrant
    VirtualBox

1. Initialisation et configuration de Vagrant

```bash
vagrant init
```
📝 Cela génère un fichier Vagrantfile de configuration.

![lunix](image/c1.png)

⚙ Configuration du Vagrantfile

Modifiez le fichier Vagrantfile pour définir la machine virtuelle souhaitée sur VSCode ou votre éditeur préféré.
Choisissez une box : Visitez Vagrant Cloud et sélectionnez bento/ubuntu-22.04.

![lunix](image/cap1.png)

✅Validation et Démarrage de la VM

Après avoir configuré le Vagrantfile, vous pouvez valider la configuration avec cette commande pour vérifier si la configuration est correcte.

1️⃣ Validez votre configuration

Cette commande permet de vérifier si la configuration est correcte :

```bash
vagrant validate
```
2️⃣ Démarrez la machine virtuelle

```bash
vagrant up
```
💡 Cela lance la VM.

![lunix](image/cap2.png)

![lunix](image/c2.png)

3️⃣ Accédez à la VM via SSH

```bash
vagrant ssh
```
![lunix](image/cap3.png)





