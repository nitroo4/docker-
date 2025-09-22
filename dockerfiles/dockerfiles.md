## <h1>Dockerfiles</h1>

I/ dockerfiles permet de creer un images personnalise a partir d'une image de base.

exemple de dockerfile:

creer un fichier "Dockerfile" avec le contenu suivant:

 FROM ubuntu
 MAINTAINER mickael
 RUN apt-get update && apt-get install -y nano && apt-get install -y iputils-ping && apt-get install -y iproute2

1) ici l'image de base est ubuntu. 
2) on update les conteneurs.
3) on installe nano, iputils-ping pour les ping et iproute2 pour les ip.


## II/ Commande de base dockerfiles:

    1) FROM : permet de definir l'image de base.
    2) MAINTAINER : permet de definir l'auteur du dockerfile.
    3) RUN : permet d'executer une commande dans le conteneur.
    4) LABEL : permet d'ajouter des metadonnees a l'image.
    5) ADD : permet d'ajouter des fichiers ou des dossiers dans l'image.
    6) COPY : permet de copier des fichiers ou des dossiers dans l'image.
    7) WORKDIR : permet de definir le repertoire de travail.

    8) CMD : permet de definir la commande par defaut a executer lorsque le conteneur est lance.
    9) ENTRYPOINT : permet de definir la commande a executer lorsque le conteneur est lance.
    10) EXPOSE : permet de definir les ports exposes par le conteneur.
    11) ENV : permet de definir des variables d'environnement.
    12) VOLUME : permet de definir des volumes a monter dans le conteneur.      
    13) USER : permet de definir l'utilisateur qui executera les commandes dans le conteneur.
    14) ARG : permet de definir des arguments a passer lors de la construction de l'image.
    15) ONBUILD : permet de definir des instructions a executer lors de la construction d'une image fille.