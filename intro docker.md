&nbsp;&nbsp;&nbsp;&nbsp;*****Petit introduction a docker****

&nbsp;&nbsp;#dans terminal:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--voir version docker:<br>
&nbsp;&nbsp;docker -v

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--telecharger un images depuis dockerhub: <br> 
&nbsp;&nbsp;docker pull nginx:latest

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--pour voir liste des images des images télécharger: <br>
&nbsp;&nbsp;docker images

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--supprimer un images: <br>
&nbsp;&nbsp;docker rmi [name image]

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--creation de conteneur: <br>
&nbsp;&nbsp;docker run --name [name conteneur] [name image and version] 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--demarrer un conteneur: <br>
&nbsp;&nbsp;docker start [name conteneur]

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--voir list de conteneur actif: <br>
&nbsp;&nbsp;docker ps (pour les conteneur inactif ajouter ""-a"")

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--arreter un conteneur:<br>
&nbsp;&nbsp;docker stop [name conteneur ou id]

&nbsp;&nbsp;#voir les options de commande qui peut etre utiliser :<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;docker 

&nbsp;&nbsp;&nbsp;#un exemple ouverture bash de conteneur: <br>
apres ceration de conteneur.<br>
&nbsp;&nbsp;-> docker start [name du conteneur ou id] <br>
&nbsp;&nbsp;-> docker docker exec -it [name du conteneur ou id] bash

