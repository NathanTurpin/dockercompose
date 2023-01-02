J'ai generé 4 services : 
  - Apache : serveur web sur le port 80. 
    -> Avec son volume, pour le cas d'un serveur Apache, un volume peut être utilisé pour partager les fichiers du répertoire htdocs.
    -> il se lance avec le fichier /web/Dockerfile qui se base sur une image httpd. Dedans je copie une fichier de conf dans le serveur apache /usr/local/apache2/conf/httpd.conf
  - DB : serveur base de donnée
    -> se base sur une image mysql 
    -> avec des variables d'environement pour definir les mdp ect
    -> volumes pour garder la bdd telquel sans la delete
  - PHP : PHP
    -> se base sur une image php 7.4
  - PHPMYADMIN : pour voir la base de donnée sur une interface

  et je declare enfin les volumes utilisés.