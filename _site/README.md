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
	- pour modifier le fichier apache2.conf, il est nécessaire d'installer un package avec la commande "sudo apt-get install joe". 
	- modifier le fichier "apache2.conf" et modifier la ligne " " avec la commande "joe apache2.conf " pour permettre d'accéder à son site depuis le navigateur.
	-

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

--> Installation de Git:
- tuto: http://michaelchelen.net/81fa/install-jekyll-2-ubuntu-14-04/
- commande installation: sudo apt-get install git

--> Créer une clé SSH publique :
- tuto : https://help.github.com/articles/generating-ssh-keys/
- commande :	ssh-keygen -t rsa -C "email@example.com"
		->	Enter file in which to save the key (/"your_home_patch"/.ssh/id_rsa) : "entrer le nom d'un dossier"
			"entrer un mot de passe"
			"confirmer mot de passe"
		->	The key fingerprint is : "id de la clé avec le nom de l'adresse mail rentrée"
		->	"ajouter sa clé à ssh-agent" commande -> eval "$(ssh-agent -s)"			Agent pid …..
		->	ssh-add ~/.ssh/id_rsa

--> Ajouter la clé publique SSH à son compte Github :
- cliquer sur settings -> "SSH Keys" dans le menu sidebar -> cliquer sur "Add SSH Key" -> c/c la clé obtenue dans le fichier que l'on a créé pour sa clé SSH à la précédente étape -> cliquer sur "Add Key"


