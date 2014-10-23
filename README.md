eloker.github.io
================

Procédure pour la configuration de son environnement virtuel (à faire dans l'ordre):

--> Installer la virtual box en premier.
- juste à télécharger VirtualBox
- Commencer par créer un répertoire "sites" dans la racine du compte (user).   
- /home/user/sites … et c'est ici que dois se trouver notre page GitHub :)

--> Installer et configurer un serveur Apache.
- tuto: https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu
- commande installation: sudo apt-get install apache2
- configuration du serveur apache:
	- tuto: http://www.linux-france.org/prj/edu/archinet/systeme/ch16s02.html
	- pour modifier le fichier apache2.conf, il est nécessaire d'installer un package avec la commande "sudo apt-get install gedit". 
	- modifier le fichier "apache2.conf" dans /etc/apache2/ et modifier la ligne "Directory /var/www/html" par "Directory /home/xubuntu/sites" avec la commande "gedit apache2.conf " pour permettre d'accéder à son site depuis le navigateur.
	- modifier le fichier 000-default.conf dans /etc/apache2/sites-available et modifier la ligne "DocumentRoot /var/www/html" par "DocumentRoot /home/xubuntu/sites"

--> Installation de "Mysql":
- tuto: https://ariejan.net/2007/12/12/how-to-install-mysql-on-ubuntudebian/
- commande installation: sudo apt-get install mysql

--> Installation de Ruby:
- tuto: https://www.ruby-lang.org/en/installation/
- commande installation: sudo apt-get install ruby

--> Installation de Jekyll:
- tuto: http://jekyllrb.com/
- tuto: http://www.garron.me/en/bits/install-jekyll-on-ubuntu.html
- commande installation: sudo apt-get install Jekyll
- Installer ruby-dev : sudo apt-get install ruby-dev
- Si la version 2 de Jekyll n'est pas installée, taper : install Jekyll 2 on Ubuntu dans un moteur de recherche

--> Installation de Git:
- tuto: http://michaelchelen.net/81fa/install-jekyll-2-ubuntu-14-04/
- commande installation: sudo apt-get install git

--> Créer une clé SSH publique :
- tuto : https://help.github.com/articles/generating-ssh-keys/ rubrique "Linux"
- commande :
- ssh-keygen -t rsa -C "your_email@example.com" dans le dossier /home/xubuntu/
- eval "$(ssh-agent -s)"
- ssh-add ~/.ssh/id_rsa
- sudo apt-get install xclip
- xclip -sel clip < ~/.ssh/id_rsa.pub (Copie la clé dans le presse papier)

- Ajouter la clé SSH à son compte Github :
	- Aller sur la page : https://github.com/settings/ssh
	- Cliquer sur "Add"
	- Donner le titre de votre choix et dans "key" copier le code du presse papier

- git add . -A
- git commit -m "comment"
- git push origin master
- git pull
