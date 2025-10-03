## les etpes:

1-build l images dans dockerfiles:  

-- docker build -t [tag] .

2-init le docker swarm:

-- docker swarm init

3-lancer le stack:

-- docker stack deploy -c [fichier.yml] [nom_du_dossier]

4-allez dans navigateur:

-- http://localhost:[port]