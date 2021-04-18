# <img src="https://avatars.githubusercontent.com/u/64909001" alt="Ubivius Icon" width="76" height=""> Ubivius
This repo houses the home of Ubivius by providing links to every products and putting some context for them. Ubivius is a suite of products to deploy and manage an online plateform for game development. The projects are split in the following families: microservices, infrastructure, telemetry, and game.
## Microservices
We have two parts linked to microservices: microservice-\* and shared-\*.
### Microservice-\*
The services are developped in Golang and are mostly independent. There is two parts: core services and feature services. 
- There is also a template service to enable your team to devlop and deploy your own microservices: [microservice-template](https://github.com/Ubivius/microservice-template).
#### Core Services
These services must be present in your cluster for basic functionnality of the platform.
- [microservice-authentication](https://github.com/Ubivius/microservice-authentication): A service that allow sign up and sign in of a player/administrator
- [microservice-dispatcher](https://github.com/Ubivius/microservice-dispatcher): A kubernetes controller that manages game server's creation/destruction for players
- [microservice-user](https://github.com/Ubivius/microservice-user): A service that save player/administrator related metadata
#### Feature Services
Theses services are feature-specific and your team can customise which ones to deploy based on your game's needs.
- [microservice-achievements](https://github.com/Ubivius/microservice-achievements):
- [microservice-character-data](https://github.com/Ubivius/microservice-character-data):
- [microservice-friendslist](https://github.com/Ubivius/microservice-friendslist):
- [microservice-matchmaking](https://github.com/Ubivius/microservice-matchmaking):
- [microservice-text-chat](https://github.com/Ubivius/microservice-text-chat):
- [~~microservice-leaderboards~~]():(Not created for v1)
### Shared-\*
Those git repositories are for shared libraries that could be used in any of the microservices. 
- [shared-authentication](https://github.com/Ubivius/shared-authentication): An OIDC library validing JSON Web Token
- [shared-ressource-manager](https://github.com/Ubivius/shared-resource-manager): A Go library to access kubernetes cluster ressources
## Infrastructure
Infrastructure are components developped by various external teams that are customized to support functions like routing, authentication management, databases and databases content viewers.
- [deploy-traefik]():
- [deploy-keycloak]():
- [deploy-elasticsearch]():
- [deploy-mongodb]():
- [~~deploy-kibana~~]():(Not created yet)
- [~~deploy-compass~~]():(Not created yet)
## Telemetry
Telemetry projects are also from external teams and were pick out of the Cloud Native Computing Foundation's([CNCF](https://landscape.cncf.io)) landscape page. They are the way administrators can monitor health and state from all deployed components in your Kubernetes cluster.
- [telemetry-grafana]():
- [telemetry-jaeger]():
- [telemetry-logstash]():
- [telemetry-prometheus]():
