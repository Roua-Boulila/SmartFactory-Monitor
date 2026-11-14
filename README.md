# SmartFactory Monitor

Application web de surveillance d'une usine intelligente, basée sur une architecture microservices.

Elle permet de surveiller les machines, collecter leurs données, détecter les anomalies, gérer les alertes et organiser la maintenance.

## Équipe

| Membre | Microservice |
|---|---|
| Farah Amor | user-service |
| Kenza Hannafi | machine-service |
| Houyem Bensaid | event-service |
| Hazem Haddad | alert-service |
| Moujib Chaabani | maintenance-service |
| Roua Boulila | analytics-service |



## Microservices

| Service | Rôle | Base de données |
|---|---|---|
| user-service | Profils, équipes, rôles métier | H2 |
| machine-service | Gestion des machines | H2 |
| event-service | Collecte des mesures des capteurs | MySQL |
| alert-service | Détection des anomalies et alertes | H2 |
| maintenance-service | Interventions de maintenance | MySQL |
| analytics-service | Statistiques et tableaux de bord | MongoDB |

## Technologies

Java 21, Spring Boot, Spring Cloud (Gateway, Eureka, Config Server), Keycloak, Kafka, Angular, Swagger, Docker, Docker Compose, GitHub.

## Structure du dépôt

```
Backend/          les microservices
Frontend/         application Angular
Infrastructure/   gateway, eureka, config, keycloak, docker-compose
Documentation/    présentation, diagrammes, dossier technique
```


