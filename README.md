# <img src="https://github.com/Ubivius/ubivius/blob/feature/UBI-444-Create-github-base-doc/assets/ubivius_elephant.png" alt="Ubivius Icon" width="45" height="">Ubivius
This repo houses the entrypoint of Ubivius's documentation by providing links to every products and putting some context for them. Ubivius is a suite of products made to deploy and manage an online plateform for game development. The projects are split in the following families: microservices, infrastructure, telemetry, and game.
## Microservices
We have three parts linked to microservices: workflows-microservices, microservice-\* and shared-\*.
### Microservice's Workflow
This single repository is used to centralize and distribute CI/CD scripts to all microservices. This enables your team to modify it in one place and distribute it with one merge on dev and another one on master when it was successful.
- Here it is: [workflows-microservices](https://github.com/Ubivius/workflows-microservices).
### Microservice-\*
The services are developped in Golang and are mostly independent. There are two parts: core services and feature services. 
- There is also a template service to enable your team to develop and deploy your own microservices: [microservice-template](https://github.com/Ubivius/microservice-template).
#### Core Services
These services must be present in your cluster for basic functionnality of the platform.
- [microservice-authentication](https://github.com/Ubivius/microservice-authentication): A service that allows sign up and sign in of a player/administrator
- [microservice-dispatcher](https://github.com/Ubivius/microservice-dispatcher): A kubernetes controller that manages game servers' creation/destruction for players
- [microservice-user](https://github.com/Ubivius/microservice-user): A service that saves player/administrator related metadata
#### Feature Services
Theses services are feature-specific and your team can customize which ones to deploy based on your game's needs.
- [microservice-achievements](https://github.com/Ubivius/microservice-achievements):
- [microservice-character-data](https://github.com/Ubivius/microservice-character-data):
- [microservice-friendslist](https://github.com/Ubivius/microservice-friendslist):
- [microservice-matchmaking](https://github.com/Ubivius/microservice-matchmaking):
- [microservice-text-chat](https://github.com/Ubivius/microservice-text-chat):
- [~~microservice-leaderboards~~](https://github.com/Ubivius/ubivius#feature-services):(Not created for v1)
### Shared-\*
Those git repositories are for shared libraries that could be used in any of the microservices. 
- [shared-authentication](https://github.com/Ubivius/shared-authentication): An OIDC library validating JSON Web Token
- [shared-resource-manager](https://github.com/Ubivius/shared-resource-manager): A Go library to access Kubernetes cluster resources
## Infrastructure
Infrastructure are components developped by various external teams that are customized to support functions like routing, authentication management, databases and databases content viewers.
- [deploy-traefik]():
- [deploy-keycloak]():
- [deploy-elasticsearch]():
- [deploy-mongodb]():
- [~~deploy-kibana~~](https://github.com/Ubivius/ubivius#infrastructure):(Not created yet)
- [~~deploy-compass~~](https://github.com/Ubivius/ubivius#infrastructure):(Not created yet)
## Telemetry
Telemetry projects are also from external teams and were picked out form the Cloud Native Computing Foundation's([CNCF](https://landscape.cncf.io)) landscape page. They are the way administrators can monitor health and state from all deployed components in your Kubernetes cluster.
- [telemetry-grafana]():
- [telemetry-jaeger]():
- [telemetry-logstash]():
- [telemetry-prometheus]():
### Telemetry's Workflow
This single repository is used to centralize and distribute CI/CD scripts to all telemetry applications. This enables your team to modify it in one place and distribute it with one merge on dev and another one on master when it was successful.
- Here it is: [workflows-telemetry](https://github.com/Ubivius/workflows-telemetry).
## Game
Here is our game. Its purpose is to provide an example of the integration of our platform and give an easy way to customize DevOps scripts to create, build and deploy a game server and client package: [ubivius-game](https://github.com/Ubivius/ubivius-game).
