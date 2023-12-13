# Spring-Boot/Angular full stack

## Description

Il s'agit d'une application Web e-commerce complète construite avec Spring Boot et Angular. C'est une simple application Web ecom qui permet aux utilisateurs de voir les produits et leurs commandes.
Le backend est réalisé par Spring Boot et le frontend est réalisé à par Angular.
Pour la base de données, j'ai utilisé la base de données h2 qui est une base de données en mémoire.

## Comment exécuter l'application

### Backend

Pour exécuter le backend, vous devez avoir une version de Java 8 ou plus installé sur votre ordinateur.

1. Clonez le répo
2. créez un dossier de configuration local et ajoutez un fichier appelé  `application.properties` et ajoutez-y les propriétés suivantes :
```properties
    spring.h2.console.enabled=true
    management.endpoints.web.exposure.include=*
```
3. Exécutez le service consul après l'avoir téléchargé depuis
https://developer.hashicorp.com/consul/install
utilisez la commande suivante pour exécuter consul :
```bash
    cd 'chemain d'installation de consul'
    ./consul.exe agent -server -bootstrap-expect=1 -data-dir="C:\Users\yahya\Desktop\consul\Data" -ui -bind='your ip address'
```
4. Accédez à http://localhost:8082/h2-console pour visualiser les microservices en cours d'exécution

### Frontend

#### Pour exécuter le frontend, vous devez avoir node.js et angulaire cli installés sur votre machine
1. Ouvrez le dossier ecom-web-app dans votre IDE et exécutez l'application frontend
2. Téléchargez node-modules en exécutant la commande suivante :
```bash
    npm install
```
3. exécutez l'application Fronend en exécutant la commande suivante :
```bash
    ng serve
```
4. testez l'application en allant sur http://localhost:4200

## Captures d'écrans :

### consul (Premier Lancement)

lors du premier lancement, Consul contiendra uniquement le service consul lui-même et le service de configuration, comme indiqué dans la capture d'écran suivante :

![1cosullunched](https://github.com/Yahyaa55/JEE_Activity_four/assets/100850367/3a900e5f-f71c-4dc3-b1e2-f37d09adbc76)

### Visualisant les propriétés par défaut du microservice COSTOMER-SERVICE

#### la capture d'écran suivante montre les propriétés par défaut du microservice COSTOMER-SERVICE  a travers GATEWAY-SERVICE:

![2 consulting customarserv default](https://github.com/Yahyaa55/JEE_Activity_four/assets/100850367/d9444eea-b81a-48da-8a56-28cec445d314)

### Visualisant les propriétés dev du microservice COSTOMER-SERVICE

#### la capture d'écran suivante montre les propriétés dev du microservice COSTOMER-SERVICE  a travers GATEWAY-SERVICE:

![3 consulting customarserv dev](https://github.com/Yahyaa55/JEE_Activity_four/assets/100850367/f3290783-4f55-41b7-8451-f27bb59b9720)

### Visualisant les propriétés prod du microservice COSTOMER-SERVICE

#### la capture d'écran suivante montre les propriétés prod du microservice COSTOMER-SERVICE  a travers GATEWAY-SERVICE:

![4 consulting customarserv prod](https://github.com/Yahyaa55/JEE_Activity_four/assets/100850367/97609428-a8df-4d93-b68c-44ca9a2b2741)

### consul (Deuxieme Lancement)

#### lors du deuxième lancement, Consul contiendra le microservice du COSTOMER-SERVICE, comme indiqué dans la capture d'écran suivante :

![5cosul ](https://github.com/Yahyaa55/JEE_Activity_four/assets/100850367/dc16c612-bd5c-4a0d-ac15-a6d69561ec44)

### consul (troisieme Lancement)

#### lors du troisieme lancement, Consul contiendra le microservice du GATEWAY-SERVICE, comme indiqué dans la capture d'écran suivante :

![7 cosul ](https://github.com/Yahyaa55/JEE_Activity_four/assets/100850367/d512833e-50ee-4b3f-b3f9-bbd885b1c046)

### Visualisant le microservice COSTOMER-SERVICE a travers GATEWAY-SERVICE:

#### la capture d'écran suivante montre la liste des clients dans le microservice du COSTOMER-SERVICE a travers GATEWAY-SERVICE :

![7consulting the service of cust via gatway ](https://github.com/Yahyaa55/JEE_Activity_four/assets/100850367/b4507402-01c7-4252-ad97-fc68f183a154)

### consul (quatrieme Lancement)

#### lors du quatrieme lancement, Consul contiendra le microservice du INVENTORY-SERVICE, comme indiqué dans la capture d'écran suivante :

![8 consul inventoryser](https://github.com/Yahyaa55/JEE_Activity_four/assets/100850367/3f4d55fd-3b92-450e-b57a-4d4f1e90675a)


### Visualisant la liste des produits dans INVENTORY-SERVICE a travers GATEWAY-SERVICE :


![10 consulting the service of inventoroies via gateway ](https://github.com/Yahyaa55/JEE_Activity_four/assets/100850367/2ae3313f-96d8-4165-bb25-bb52cb6eec11)

### Visualisant la liste des produits et des clients on utilisant une projection

#### la capture d'écran suivante montre la liste des produits et la liste des clients dans les microservices INVENTORY-SERVICE et CUSTOMER-SERVICE on utilisant une projection a travers GATEWAY-SERVICE :

![11 Projection](https://github.com/Yahyaa55/JEE_Activity_four/assets/100850367/d96b5a48-bc81-4c97-ac34-49b6ecf1086c)

### consultation de la liste des commandes dans le microservice ORDER-SERVICE a travers GATEWAY-SERVICE :

#### la capture d'écran suivante montre la liste des commandes dans le microservice ORDER-SERVICE a travers GATEWAY-SERVICE :

![12 order service orders](https://github.com/Yahyaa55/JEE_Activity_four/assets/100850367/5a4d1541-e805-44af-83c5-238516165844)

### consultation de la liste des articles de la commande d'identifiant 5 dans le microservice ORDER-SERVICE a travers GATEWAY-SERVICE :

#### la capture d'écran suivante montre la liste des articles de la commande d'identifiant 5 dans le microservice ORDER-SERVICE a travers GATEWAY-SERVICE :

![13 order service product Items ](https://github.com/Yahyaa55/JEE_Activity_four/assets/100850367/e385109e-febd-41eb-acd9-a64ad8ef06d6)

### consultation de la commande complète numero 1 dans le microservice ORDER-SERVICE a travers GATEWAY-SERVICE :

#### la capture d'écran suivante montre la commande complète numero 1 dans le microservice ORDER-SERVICE a travers GATEWAY-SERVICE :

![14 full order](https://github.com/Yahyaa55/JEE_Activity_four/assets/100850367/461de21c-590f-4ca4-8f8d-f905b04c7a42)

### consul (dernier Lancement)

#### la capture d'écran suivante montre la derniere etape du consul avec tous les microservices lancés :

![15 cosul ](https://github.com/Yahyaa55/JEE_Activity_four/assets/100850367/12d2ade2-0165-47e3-8292-7acece960453)
