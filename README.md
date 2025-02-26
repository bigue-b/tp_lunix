🚀 Projet Nginx & MySQL avec Vagrant

#   Description

Ce projet utilise Vagrant pour configurer un environnement de développement avec :

    Un serveur web Nginx
    Un serveur MySQL
    Une mini application front
#   Prérequis

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
![lunix](image/c3.png)

2️⃣ Démarrez la machine virtuelle

```bash
vagrant up
```
💡 Cela lance la VM.

![lunix](image/c2.png)

3️⃣ Accédez à la VM via SSH

```bash
vagrant ssh
```
![lunix](image/cap3.png)

4. Installer les packages:

Mets à jour les paquets de la VM :

```bash
sudo apt update && sudo apt upgrade -y
```
![lunix](image/c8.png)

5. Installer NGINX

Maintenant installez Nginx sur Ubuntu:

```bash
sudo apt install nginx -y
```
![lunix](image/c9.png)

5. ✅ Vérification de l'installation

Vérifier que Nginx est installé et actif:

```bash
systemctl service nginx start
systemctl service nginx status

```
![lunix](image/l2.png)

Donc : Si Nginx est actif, tu verras un message indiquant "active (running)

![lunix](image/cap6.png)

6. Déploiement de l'application

Crer un dossier mini-app et y placer votre index.html vers le chemin /var/www/html/

```bash
sudo mkdir -p /var/www/html/mini-app
nano /var/www/html/mini-app/index.html
sudo ln -s /etc/nginx/sites-available/mini-app /etc/nginx/sites-enabled
```

Ensuite on ajoute le site dans les site-enabled

```bash
sudo ln -s /etc/nginx/sites-available/mini-app /etc/nginx/sites-enabled

```
![lunix](image/l3.png)

Prenez l'adresse ip de votre app

📌 Adresse IP de l'application : 192.168.0.10

👉 Ouvre ton navigateur et entre l’URL suivante : http://192.168.0.10

![lunix](image/cap7.png)

6. Installation de MySQL Server

```bash
sudo apt install mysql-server -y
```
![lunix](image/m1.png)

Se connecter à MySQL :

```bash
sudo mysql -u root
```
![lunix](image/m2.png)
