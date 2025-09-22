## mapper des port 
introduction:  

il y a des contenaire qui partege des information via des port qu on peut utilise pour voir ou avoir ses informations..  

<h2>1) d'abord creer un contenair:</h2>

-- docker run --name testPort [images]

il devrait y avoir quelque chose comme 
->(start worker processes)  

<h2>2) commande pour mettre des ports</h2>  
*
docker run -it --name [name] -p 9000:80 [image] bash  

9000: port de notre machine.  
80: port du conteneur.  

<h2>3) dans navigateur:</h2>

faire : http://localhost:9000 

vous allez voir la pages de l'images.


##<h1>on va voir ce qu est un bind mount:</h1>

<p>
    Il s’agit de lié un fichier depuis la machine hôte vers docker (il plutôt monté dans le conteneur). Il doit exister avant le montage du fichier dans le conteneur.
</p>

on va faire un test:  

creer un dossier dans machine local: avec un fichier.html  
PUIS:  

- docker run -itd --name [name] --mount type=bind, source=[chemin_du_fichier_local],target=/usr/share/[image]/html -p [port_local]:[port_conteneur] [images_:_version]


## On va d abore test de ping 1 contenaire vers un autre 

1) creer 2 contenaire:

-- docker run -it --name [name1_et_2] [images]

# demarrer les contenaires  
-- docker start [name1_et_2]

# exec les contenaires:  
-- docker exec -it [name] bash

# --- apres tu peux interagir avec les contenaires et fait:  
-- apt update && apt install -y iputils-ping && apt install -y iproute2  

le premier pour pouvoir pinger.
le deuxieme pour pouvoir voir les adresses reseaux.

-- fais ping [adresses_contenaire_1_ou_2] 
