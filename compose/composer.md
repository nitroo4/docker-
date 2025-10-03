## Docker compose

1.intro:

on utilise pour creer des text d images avec les functionalite utile qu on veut sur chaque images qu on va utiliser dedans. 

2. base d un docker compose:

    -services:
    -networks:
    -volumes:

3. creer un conteneur via compose:

- fichier.yml dedans  

services:  
  conteneur_one:   
    image: [name_images]   
    container_name: [name]  
    stdin_open: true /*garder alumer*/  
    tty: true  
    
    networks:
      - test_network_1


4. ajouter volume dans yml:

## mapper volume:
    volumes:  
      - ./[dossier_local]:/data_dans_le_conteneur


    mkdir [dossier_local]
    
## manager volume:

    volumes: 
      - test_volume:/test_volume_dans_dans_conteneur


volumes:
    test_volumes:

6. network: 

  conteneur_two: 
    image: [name_images]   
    container_name: [name]  
    stdin_open: true /*garder alumer*/  
    tty: true
    
    networks:
      - test_network_2

networks:
  test_networks_1
    driver:bridge

  test_networks_2
    driver:bridge


7. commande lancer compose: 

-- docker compose up -d

8. stop dossier avec compose.ymf 

-- docker compose stop 

9. supprimer: 

-- docker compose rm
