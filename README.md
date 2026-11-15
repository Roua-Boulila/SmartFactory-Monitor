# SmartFactory Monitor

Application web de surveillance d'une usine intelligente, basée sur une architecture microservices.

Elle permet de surveiller les machines, collecter leurs données, détecter les anomalies, gérer les alertes, organiser la maintenance et suivre le stock des pièces de rechange.

## Équipe

| Membre | Microservice | Base de données |
|---|---|---|
| Farah Amor | user-service | H2 |
| Kenza Hannafi | machine-service | H2 |
| Houyem Bensaid | event-service | MySQL |
| Hazem Haddad | alert-service | H2 |
| Moujib Chaabani | maintenance-service | MySQL |
| Roua Boulila | spare-parts-service | MySQL |
| Toute l'équipe | analytics-service (microservice commun) | MongoDB |


## Microservices

| Service | Rôle |
|---|---|
| user-service | Profils, équipes, rôles métier |
| machine-service | Gestion des machines et de leur état |
| event-service | Collecte des mesures des capteurs |
| alert-service | Détection des anomalies et gestion des alertes |
| maintenance-service | Planification et suivi des interventions |
| spare-parts-service | Stock des pièces de rechange : ajout, entrées et sorties, réservation pour les interventions, détection des ruptures et des stocks faibles |
| analytics-service | Statistiques et tableaux de bord (service commun) |

## Communication entre services

- **Synchrone (OpenFeign)** : maintenance-service appelle spare-parts-service pour vérifier et réserver une pièce, et machine-service pour vérifier une machine.
- **Asynchrone (Kafka)** : événements `telemetry.received`, `alert.created`, `intervention.closed`, `stock.low`.

## Technologies

Java 21, Spring Boot, Spring Cloud (Gateway, Eureka, Config Server), OpenFeign, Keycloak, Kafka, Angular, Swagger, Docker, Docker Compose, GitHub.

## Structure du dépôt

```
Backend/          les microservices
Frontend/         application Angular
Infrastructure/   gateway, eureka, config, keycloak, docker-compose
Documentation/    présentation, diagrammes, dossier technique
```

## Lancement

À compléter plus tard :

```
cd Infrastructure
docker compose up --build
```
