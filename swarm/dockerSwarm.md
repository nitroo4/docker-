## I/ Docker swarm:  
# Intro:
c est un groupe de machines executant le moteur Docker et faisant partie du meme cluster.

- l'architecture est composer de:

-> composer: avec le fichier .yml et du docker CLI
-> Swarm: les machines worker. 
-> cluster: les machine qui executer les commandes appeler manager.

## II/ les commandes docker swarm:  
# Creer un cluster swarm  
1) initier le mode swarm:  
-- docker swarm init  

-- docker swarm  init --advertise-addr (adresse ip)

2) verifier l'etat du swarm:

-- docker info 

-- docker node ls

3) - 1) ajouter des noeuds au swarm(worker):  
-- docker swarm join --token (notre token de worker) (adresse ip):(port)

3) - 2) noued(manager):  
-- docker swarm join --token (token manager) (adresse ip):port

4) pour voir les details:  
-- docker node ls

5) pour deployer:  
-- docket stack deploy -c fichier.yml [nom_du_dossier_project]

6) arreter definitive ou supprimer un stack:  
-- docker stack rm [nom_du_dossier_project]

7) verifier stack:  
-- docker stack ls

8) verfier service d un stack:  
-- docker stack services [nom_du_dossier_project]

9) etat services (tres important pour verfier les replicas qui crash ou pas):  
-- docker service ps [nom_du_dossier_project]

10) mise a jour d un service:  
-- docker service update --force [nom_du_dossier_project] 

## pour faire le deployements :

1) creer le dossier avec Dockerfile car commande stack deploy ne prend pas encharge les build dans un fichier.yml donc on doit build nous meme notre images et l appele juste dans le fichier yml.

# etape 1:  

- build l images  
# etape 2:  

- docker init  
# etape 3:

- docket stack deploy -c fichier.yml [nom_du_dossier_project]